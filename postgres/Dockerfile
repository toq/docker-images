FROM postgres:18-alpine
RUN apk add --no-cache bash zstd
CMD ["postgres","-c","fsync=off","-c","synchronous_commit=off","-c","full_page_writes=off","-c","autovacuum=off"]
