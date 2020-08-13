#
# docker build -t ehsmeng/smalltest_native:latest .
# docker save ehsmeng/smalltest_native > smalltest_native.tar
#
# docker cleanup: 
# docker image prune --all
#
# docker run ehsmeng/smalltest_native:latest 
FROM scratch

WORKDIR /

COPY ./a.exe /

CMD ["/a.exe"]

#ENTRYPOINT ["/"]


# native-image -static --no-fallback -cp smalltest-0.0.1-SNAPSHOT.jar -H:Class=io.manycore.Main io.manycore.Main -H:Name=a.exe -H:+ReportExceptionStackTraces -H:EnableURLProtocols=http,https -H:-UseServiceLoaderFeature
