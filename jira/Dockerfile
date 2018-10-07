FROM cptactionhank/atlassian-jira:7.3.6

ENV JIRA_HOME     /var/atlassian/jira
ENV JIRA_INSTALL  /opt/atlassian/jira
ENV JIRA_WEB      ${JIRA_INSTALL}/atlassian-jira/WEB-INF
ENV JIRA_WEB_LIB  ${JIRA_WEB}/lib
ENV JIRA_VERSION  7.3.6

ENV X_PROXY_NAME   dev.slyak.com
ENV X_PROXY_PORT   80
ENV X_PATH         /jira

#use mysql
COPY mysql-connector-java-5.1.39.jar ${JIRA_WEB_LIB}/

#jira crack
COPY atlassian-extras-3.2.jar ${JIRA_WEB_LIB}/

RUN  chmod -R 700 "${JIRA_WEB}/atlassian-bundled-plugins" \
    && rm "${JIRA_WEB}/atlassian-bundled-plugins/atlassian-universal-plugin-manager-plugin-2.21.jar"
COPY atlassian-universal-plugin-manager-plugin-2.22.jar ${JIRA_WEB}/atlassian-bundled-plugins/