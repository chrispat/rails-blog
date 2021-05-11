# [Choice] Ruby version: 2, 2.7, 2.6, 2.5
ARG VARIANT=2.7
FROM mcr.microsoft.com/vscode/devcontainers/ruby:${VARIANT}

# Install Rails
RUN gem install rails webdrivers 

ARG NODE_VERSION="lts/*"
RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && nvm install ${NODE_VERSION} 2>&1"

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment this line to install additional gems.
# RUN gem install <your-gem-names-here>

# [Optional] Uncomment this line to install global node packages.
# RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && npm install -g <your-package-here>" 2>&1

# Install the railway cli
RUN curl -sSL https://raw.githubusercontent.com/railwayapp/cli/master/install.sh | sudo sh

# Install bicep tooling
RUN curl -Lo bicep https://github.com/Azure/bicep/releases/latest/download/bicep-linux-x64 \
    && chmod +x ./bicep \
    && sudo mv ./bicep /usr/local/bin/bicep

# Install Azure cli
RUN curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash

# Install digital ocean cli
RUN curl -sSLo doctl.tar.gz https://github.com/digitalocean/doctl/releases/download/v1.57.0/doctl-1.57.0-linux-amd64.tar.gz  \
    && tar xf doctl.tar.gz \
    && sudo mv doctl /usr/local/bin

# Install Heroku CLI
RUN curl https://cli-assets.heroku.com/install.sh | sudo sh


# Install GH cli
RUN export DEBIAN_FRONTEND=noninteractive \
    && sudo apt-get update \
    && sudo apt -y install --no-install-recommends software-properties-common \
    && sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0 \ 
    && sudo apt-add-repository https://cli.github.com/packages \
    && sudo apt-get update \
    && sudo apt-get -y install --no-install-recommends gh 

# Install phantomjs
RUN apt-get update \
      && apt-get install -y --no-install-recommends \
          ca-certificates \
          bzip2 \
          libfontconfig \
      && apt-get clean \
      && rm -rf /var/lib/apt/lists/*
  
RUN   mkdir /tmp/phantomjs \
      && curl -L https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2 \
              | tar -xj --strip-components=1 -C /tmp/phantomjs \
      && cd /tmp/phantomjs \
      && mv bin/phantomjs /usr/local/bin 