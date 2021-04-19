FROM telegraf:latest

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 379CE192D401AB61 && \
    echo "deb https://ookla.bintray.com/debian generic main" | tee /etc/apt/sources.list.d/speedtest.list && \
    apt-get update && \
    apt-get install -y --no-install-recommends speedtest && \
    rm -rf /var/lib/apt/lists/* && \
    timeout 1 speedtest --accept-license || true
