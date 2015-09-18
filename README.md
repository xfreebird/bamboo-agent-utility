# bamboo-agent-utility
A [Bamboo](https://www.atlassian.com/software/bamboo) utility for installing or removing an agent on OS X

## How to install ?

```shell
brew tap xfreebird/utils
brew install bamboo-agent-utility
```

## Usage

* Install a Bamboo agent:

```shell
export DOWNLOAD_URL='https://bamboo.server.com/agentServer/agentInstaller/atlassian-bamboo-agent-installer-5.7.2.jar'
bamboo-agent-utility install ~/bamboo
```

* Uninstall a Bamboo agent:

```shell
bamboo-agent-utility uninstall ~/bamboo
```

## What it can do ?

* Install the Bamboo agent
* If your Bamboo CI server is hosted on internal server with self signed SSL certificate, it will import the certificate in a local keychain and point the agent to use it.
* It will make the agent use the environment settings from ```~/.profile```
* Uninstall the Bamboo agent

## Gotchas 

* The agent will start only when the user is logged in (e.g. enable autologin)
* The agent will run in user's UI session (e.g. you can run iOS UI and unit tests)

## Logs

All logs are written to ```/tmp/<bamboo-dirname>-agent.log``` and ```/tmp/<bamboo-dirname>-agent_err.log```.

# License

```
The MIT License (MIT)

Copyright (c) 2014 Nicolae Ghimbovschi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```