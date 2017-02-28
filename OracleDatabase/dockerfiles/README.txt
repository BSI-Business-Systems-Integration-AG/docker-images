For 12.1.0.2:
- Before building this image, adjust the INSTALL_FILE_BASE_URL in the corresponding Dockerfile
- When running the built image, don't forget to add a volume mapping for /opt/oracle/oradata if you want to keep your data!
    Example:
    docker run --name oracle -p 1521:1521 -p 5500:5500 -e ORACLE_SID=MYSID -v /opt/oracle/oradata:/opt/oracle/oradata oracle-nopdb-novolume:12.1.0.2-se2
