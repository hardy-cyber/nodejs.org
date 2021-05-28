const Discord = require ('discord.js')
const { MessageEmbed } = require('discord.js')
module.exports = {
info: {
    name: "server",
        usage: "",
        description: "اطلاعات سرور  ",
        aliases: [],
},
run: async(client, message, args) => {
const embed = new Discord.MessageEmbed()
        .setColor('RANDOM')
        .setTitle("Server Info")
        .setImage(message.guild.iconURL)
        .setDescription(`${message.guild}'اسم سرور`)
        .addField("✨Owner", `صاحب سرور:  ${message.guild.owner}`)
        .addField("👮‍♂️Member Count", `تعداد ممبر: ${message.guild.memberCount} members`)
        .addField("😂Emoji Count", `تعداد ایموجی: ${message.guild.emojis.cache.size} emoji Hast`)
        .addField("🔐Roles Count", `تعداد رول: ${message.guild.roles.cache.size} role Dard`)
        message.channel.send(embed)
    }
};
