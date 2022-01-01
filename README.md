$ npm install discord.js@12.5.3
{
    "token": "OTI2NzY5MDgxMTg3NzA4OTg4.YdAe9w.ddJ-dAL-SkUT6Mo702x9HPjtgQY"
}
const Discord = require('discord.js');
const { token } = require('./token.json');
const client = new Discord.Client();

// 連上線時的事件
client.on('ready', () => {
    console.log(`Logged in as ${client.user.tag}!`);
});

// 當 Bot 接收到訊息時的事件
client.on('message', msg => {
    // 如果訊息的內容是 'ping'
    if (msg.content === 'ping') {
        // 則 Bot 回應 'Pong'
        msg.reply('pong');
    }
});

client.login(token);
