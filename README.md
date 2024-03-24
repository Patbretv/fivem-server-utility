# Fivem Server Utility

## Description
This npm package allows you to interact with a FiveM server by retrieving server information, player details, sending commands via RCON, and more.

## Installation
To install the package, run the following command:
```
npm install fivem-server-utility
```

## Usage
```javascript
const FivemServer = require('fivem-server-utility');

// Initialize the FivemServer object with IP, port, and RCON password
const server = new FivemServer('server_ip', 'server_port', 'rcon_password');

// Example usage
server.getPlayers()
    .then(players => console.log('Players:', players))
    .catch(error => console.error('Error:', error));

server.getPlayerCount()
    .then(count => console.log('Player Count:', count))
    .catch(error => console.error('Error:', error));

server.getserverdata('resources').then(resources) {
  console.log(resources)
}

// and so on...
```

## Functions
- `getPlayers()`: Retrieves information about all players on the server.
- `getPlayerCount()`: Retrieves the total number of players currently connected to the server.
- `getserverdata(key: string)`: Retrieves specific server data based on the provided key (e.g., 'resources').
- `getservervariable(key: string)`: Retrieves specific server variables based on the provided key.
- `getServerResources()`: Retrieves information about server resources.
- `sendCommand(command: string)`: Sends a command to the server via RCON.
- `getplayerbyid(id: int)`: Retrieves player information by player ID.
- `getplayerbyidentifier(identifier: string)`: Retrieves player information by player identifier.

## Contributing
Contributions are welcome! Please fork the repository, make your changes, and submit a pull request.

## Issues
If you encounter any issues or have suggestions for improvement, please [open an issue](https://github.com/yourusername/fivem-server-info/issues).

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
