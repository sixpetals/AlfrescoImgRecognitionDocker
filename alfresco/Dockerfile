FROM alfresco/alfresco-content-repository-community:6.1.2-ga

RUN echo "aws.accessKey=hoge" >> /usr/local/tomcat/shared/classes/alfresco-global.properties && \
    echo "aws.secretKey=fuga" >> /usr/local/tomcat/shared/classes/alfresco-global.properties && \
    echo "aws.maxNumberOfLabels=5" >> /usr/local/tomcat/shared/classes/alfresco-global.properties && \
    echo "aws.confidentLevel=90.0F" >> /usr/local/tomcat/shared/classes/alfresco-global.properties && \
    echo "bluemix.version=2018-03-19" >> /usr/local/tomcat/shared/classes/alfresco-global.properties && \
    echo "bluemix.apikey=cT0mZAGP4DHiT7ez9M2tDw3ASE2egl_5IdZV1222-h3W" >> /usr/local/tomcat/shared/classes/alfresco-global.properties && \
    echo "bluemix.confidentLevel=0.55" >> /usr/local/tomcat/shared/classes/alfresco-global.properties

COPY imgRecognition-platform-jar-1.2-20190116.amp /usr/local/tomcat/amps/

RUN java -jar /usr/local/tomcat/alfresco-mmt/alfresco-mmt*.jar install \
              /usr/local/tomcat/amps/imgRecognition-platform-jar-1.2-20190116.amp \
              /usr/local/tomcat/webapps/alfresco -nobackup -force