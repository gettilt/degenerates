<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(f"# {config['name'].title()}")
]]]-->
# Degen
<!--//[[[end]]]-->

## Mission

Tilt's mission is to map every theme to a basket of stocks for anyone to invest in. Mappings are AI generated and expert curated.
Expert improvements are accepted if they provide a better representation of a given theme.

## Theme Prompt
<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(config['prompt'])
]]]-->
Mobile apps allow investing, ownership, lotteries, betting, and casinos 24 hours a day for anyone. Degenerates are spending money on gambling. Companies involved in investing, trading, speculation, crypto, sports betting and gambling win.
<!--[[[end]]]-->

## Theme Stocks

<!--[[[cog
import cog
import csv
import json

with open('context.json') as file:
  contexts = json.load(file)

def _get_context_str_for_ticker(ticker):
  try:
    context = contexts[ticker]
    context_str = context['chat_gpt'] or context['claude'] or ""
  except KeyError:
    context_str = ""

  return context_str

cog.outl("| Ticker  | Context | Source |")
cog.outl("| ------- | ---- | ---- |")

with open('theme.csv') as file:
  reader = csv.reader(file)
  next(reader) # skip the header
  for row in reader:
    context_str = _get_context_str_for_ticker(row[0])
    cog.outl(f"| {row[0]} | {context_str} | {row[1]} |")
]]]-->
| Ticker  | Context | Source |
| ------- | ---- | ---- |
| CRSR | Corsair Gaming provides gaming peripherals and streaming equipment, indirectly benefiting from the increased interest in online gaming and gambling. | chat_gpt |
| CZR | Caesars Entertainment is a major player in the casino and online gambling industry, benefiting directly from the rise in mobile gambling. | chat_gpt,google,claude |
| DKNG | DraftKings is a leading player in the online sports betting and fantasy sports market, directly benefiting from increased gambling activities. | chat_gpt,twitter,google,claude |
| GOOGL | Alphabet benefits indirectly through its Google Play Store, which hosts a variety of gambling and betting apps, generating revenue from app sales and ads. | chat_gpt,claude |
| LVS | Las Vegas Sands is a major casino operator with a growing online presence, benefiting from the trend towards mobile gambling. | chat_gpt,google |
| MA | Mastercard benefits indirectly from the trend as higher gambling activities increase transaction volumes on its network. | chat_gpt |
| MGM | MGM Resorts International has a strong presence in both physical casinos and online sports betting, positioning it well to gain from increased gambling. | chat_gpt,google,claude |
| MSFT | Microsoft, through its Xbox platform and cloud services, indirectly benefits from the increased engagement in online gaming and gambling. | chat_gpt |
| PENN | Penn National Gaming operates casinos and racetracks, and has a significant online presence through its Barstool Sportsbook, making it a direct beneficiary of the trend. | chat_gpt,twitter,google,claude |
| RSI | Rush Street Interactive operates online casinos and sports betting platforms, directly benefiting from the rise in mobile gambling. | chat_gpt,twitter,google,claude |
| SQ | Square, through its Cash App, facilitates transactions for gambling and betting, indirectly benefiting from the trend. | chat_gpt,google |
| V | Visa benefits indirectly as increased gambling activities lead to higher transaction volumes on its payment network. | chat_gpt |
| WYNN | Wynn Resorts operates high-end casinos and has expanded into online sports betting, making it a direct beneficiary of increased gambling activities. | chat_gpt,google |
| ABNB |  | twitter |
| FLUT |  | twitter,google |
| GENI | Genius Sports provides data and technology services to sports leagues and betting operators, playing a crucial role in the sports betting ecosystem. | twitter,claude |
| BALY | Bally's Corporation, a regional casino operator, has been acquiring online gaming assets to establish a significant presence in the iGaming and sports betting markets. | google,claude |
| BYD |  | google |
| HOOD |  | google |
| IGT | International Game Technology is another leading supplier of gaming machines and lottery systems, with a growing presence in the online gambling market. | google,claude |
| CHDN | Churchill Downs, known for its iconic Kentucky Derby racetrack, has been investing in online horse betting and gaming platforms. | claude |
| TKO |  | experts |
| MANU |  | experts |
| FWONK |  | experts |
| LYV |  | experts |
<!--[[[end]]]-->

## License

<p>
This project is licensed under <a href="./LICENSE">AGPLv3</a>.
</p>


## Contributors

Thank you for your improvements! We appreciate all the contributions from the community.

<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  repo = config['github_repo'].lower()
  cog.outl(f'<a href="https://github.com/gettilt/{repo}/graphs/contributors">')
  cog.outl(f'  <img src="https://contrib.rocks/image?repo=gettilt/{repo}" />')
  cog.outl('</a>')
]]]-->
<a href="https://github.com/gettilt/degen/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gettilt/degen" />
</a>
<!--[[[end]]]-->

## Join Our Community

<a href="https://discord.gg/4vYMhRpaMY" target="_blank">
<img src="https://discord.com/api/guilds/1179775688421683220/widget.png?style=banner3" alt="">
</a>
