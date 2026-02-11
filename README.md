# a fast raid bot built with seyfert. bot can spam 6 messages up to per button press.

## features

- **flood command**: send multiple messages to flood a channel
- **raid command**: start a server raid with customizable messages
- **custom raid**: use saved message presets for raids
- **file spamming**: upload and spam files in channels
- **preset management**: save and manage custom message presets
- **thug raid**: raid with thug porn
- **say command**: send messages through the bot

## installation

### prerequisites

- node.js v18 or higher
- bun runtime (or you can use NPM, although i recommend bun.)
- a discord bot token

### setup

1. clone the repository:
   ```bash
   git clone https://github.com/fuhnut/raid-bot
   cd 767-v3
   ```

2. install dependencies:
   ```bash
   bun install
   ```

3. configure the bot:
   - edit `bot.yaml` with your bot token and client id
   - or set environment variables: `discord_token` and `discord_client_id`

4. build the project:
   ```bash
   bun/npm run build
   ```

5. deploy commands:
   ```bash
   bun/npm run deploy
   ```

6. start the bot:
   ```bash
   bun/npm run start
   ```

## configuration

create a `bot.yaml` file in the root directory:

```yaml
token: "your-discord-bot-token"
client_id: "your-bot-client-id"
```

or use environment variables:
- `discord_token=your-token`
- `discord_client_id=your-client-id`

## commands

### raid commands

- `/raid` - start a basic server raid
- `/custom-r4id` - raid using a saved message preset
- `/flood <message>` - flood the channel with a custom message
- `/thug` - spam thug porn
- `/say <message>` - send a message through the bot
- `/filespam` - upload and spam files
- `/presetmessage` - manage message presets (add/edit/remove)
### linting

```bash
bun/npm run lint
bun/npm run lint:fix
```

### project structure

- `src/commands/` - slash command handlers
- `src/components/` - button/modal component handlers
- `src/db.ts` - database operations (nedb)
- `src/config.ts` - configuration management
- `src/types.ts` - typescript type definitions
- `data/` - database files

the bot uses nedb for data storage:
- `user_presets.db` - user message presets
- `stored_files.db` - temporary file storage
- `thug_selections.db` - thug mode data
- `flood.db` - flood message storage

## contributing

1. fork the repository
2. create a feature branch
3. make your changes
4. test thoroughly
5. submit a pull request

## license

this project is licensed under the mit license.

---

built with [seyfert](https://seyfert.dev) - a modern discord api framework.
