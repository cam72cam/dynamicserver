# dynamicserver
A system to dynamically launch DigitalOcean droplets as Minecraft servers if people are trying to connect, and creates a snapshot and destroys the droplet when there's nobody on the server to save running costs. A "launch on demand" model similar to [toffer/minecloud](https://github.com/toffer/minecloud), except instead of using a web browser, everything can be interacted with through the Minecraft multiplayer server list.

You can see the status of the server on the server list, and connect to it if it's not running to start it. It has an intelligent reverse proxy which automatically routes connections based on hostnames, essentially VirtualHosts for Minecraft allowing you to run and manage multiple severs routed through a single server/IP address. The reverse proxy can provide helpful error messages if issues occur, and is able to detect issues on its own and put up an "unavailability" warning for users trying to connect.

No web browser is required as it is controlled by people trying to connect, and configuration is done through .json files, so no database required either. Configuration is live reloaded and is automatically applied when they are changed, which allows for zero downtime modifications, even people who are already connected and playing on the server won't disconnect.

Need help? Have any questions or queries? Think this can become something bigger (An alternative to BungeeCord)? Feel free to email me at me@chuie.io with anything.
