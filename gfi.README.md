## How to create a new build?
- 1) Modify the code
- 2) Run the following commands
```
yarn install
yarn build
```
- 3) New build will be available under dist folder


## How to try the new build?
- 1) In your grafana docker image copy the dist to the `grafana-opensearch-datasource` plugin directory <br>
`COPY <PATH-TO-DIST-FOLDER>/dist/ /var/lib/grafana/plugins/grafana-opensearch-datasource`
- 2) Allow loading unsigned plugin for this plugin via setting the following env<br>
`ENV GF_PLUGINS_ALLOW_LOADING_UNSIGNED_PLUGINS grafana-opensearch-datasource`
