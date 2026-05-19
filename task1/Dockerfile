FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip

# Fix externally managed environment issue
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask with pip3
RUN pip3 install flask

WORKDIR /app

COPY api.py /app/api.py

EXPOSE 5252

CMD ["python3", "api.py"]
