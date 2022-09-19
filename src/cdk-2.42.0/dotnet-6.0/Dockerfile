FROM  amazon/aws-cli:2.7.33

RUN rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
RUN yum install -y dotnet-sdk-6.0 tar gzip && yum clean all

RUN touch ~/.bashrc && chmod +x ~/.bashrc

RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash \
    && . ~/.nvm/nvm.sh \
    && nvm install 16.17 \
    && nvm use node \
    && npm install -g cdk@2.42.0

#ENTRYPOINT ["/bin/bash"]