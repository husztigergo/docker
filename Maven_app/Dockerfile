FROM maven:3-jdk-11 as builder

WORKDIR /build
COPY pom.xml /build

RUN mvn -B dependency:resolve dependency:resolve-plugins

COPY src /build/src

RUN mvn package
ENTRYPOINT ["java","-cp","app:app/lib/*","hello.Application"]