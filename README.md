# Basic yii2 docker container configuration

## Development

Including basic dependencies, extensions and Xdebug which uses `9005` port.

Start by cloning this repo and copy or move all the files to your yii2 project folder.

All you will need to do is start up the container:

```
docker-compose up -d
```

### OSX Quirks

To use xdebug is OSX with docker container is a little bit tricky. I've spent a couple of days to try all the solutions and found the one below work for me. Big thanks to [ralphschindler](https://gist.github.com/ralphschindler).

To read more details please open the link:
https://gist.github.com/ralphschindler/535dc5916ccbd06f53c1b0ee5a868c93

For people don't want to read text, please just run the command below.


```
sudo curl -o /Library/LaunchDaemons/com.ralphschindler.docker_10254_alias.plist https://gist.githubusercontent.com/ralphschindler/535dc5916ccbd06f53c1b0ee5a868c93/raw/com.ralphschindler.docker_10254_alias.plist

```

After reboot you will have the alias set up.

Or, you just want to try it out without rebooting or adding a startup script:
```
ifconfig lo0 alias 10.254.254.254
```