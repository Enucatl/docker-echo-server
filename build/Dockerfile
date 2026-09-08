FROM python:3.12-slim

COPY echo-server.py /echo-server.py

CMD ["python", "-u","/echo-server.py"]

EXPOSE 4001/udp
EXPOSE 5001/tcp

HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
  CMD python -c "import socket; s=socket.create_connection(('127.0.0.1', 5001), 2); s.close()"
