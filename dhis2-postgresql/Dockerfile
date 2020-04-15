#Build from
FROM mdillon/postgis:9.5-alpine

LABEL "Author"="Mamadou Ben TRAORE - ben@savics.org"
LABEL description="DHIS2 2.28 database for the RHIES project"
ADD dhis2-db.sql /tmp/data/dhis2-db.sql
ADD init-dhis2-db.sh /docker-entrypoint-initdb.d/
ADD create-target-db.sh /docker-entrypoint-initdb.d/



EXPOSE 5432
