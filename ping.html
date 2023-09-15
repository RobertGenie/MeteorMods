# scope: hikka_only
# meta developer: @MeteorMods

import datetime
import logging
import time

from telethon.tl.types import Message

from .. import loader, main, utils

logger = logging.getLogger(__name__)


class MyPing(loader.Module):
    """Check your userbot ping."""

    strings = {
        "name": "MyPing",
        "uptime": "⏰ Uptime",
        "com": "{} <code>{}</code> <b>ms</b>\n{}",
    }

    def __init__(self):
        self.config = loader.ModuleConfig(
            loader.ConfigValue(
                "return",
                "no",
                doc=lambda: "The module supports  {time}, {uptime}",
            ),
            loader.ConfigValue(
                "ping",
                "🚀 Ping:"
            ),
            loader.ConfigValue(
                "timezone",
                "0",
            ),
        )

    def _render_ping(self):
        offset = datetime.timedelta(hours=self.config["timezone"])
        tz = datetime.timezone(offset)
        time2 = datetime.datetime.now(tz)
        time = time2.strftime("%H:%M:%S")
        uptime = utils.formatted_uptime()
        return (
            self.config["return"].format(
                time=time,
                uptime=uptime,
            )
            if self.config["return"] != "no"
            else (f'{self.strings("uptime")}: <b>{uptime}</b>')
        )

    @loader.unrestricted
    async def pcmd(self, message):
        """- Check your userbot ping"""
        ping = self.config["ping"]
        start = time.perf_counter_ns()
        message = await utils.answer(message, "<code>☄</code>")
        try:
            await utils.answer(
                message,
                self.strings("com").format(
                    ping,
                    round((time.perf_counter_ns() - start) / 10**6, 3),
                    self._render_ping(),
                ),
            )
        except TypeError:
            await utils.answer(
                message,
                "✖ Invalid number! Fix it: '.config' > 'MyPing' > '⏰ Uptime' - timezone, please update it!",
            )
