FROM mcr.microsoft.com/java/jdk:8-zulu-alpine AS compiler
COPY /source /usr/src/uygulama
WORKDIR /usr/src/uygulama
RUN javac uygulama.java
CMD ["java" , "uygulama"]

FROM mcr.microsoft.com/java/jre:8-zulu-alpine AS runtime
WORKDIR /uygulama
COPY --from=compiler /usr/src/uygulama .
CMD ["java" , "uygulama"]
