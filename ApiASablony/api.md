### API (Application Programming Interface)

API je definice rozhraní aplikace. Popisuje jaká rozhraní jsou dostupná — tedy
**na co se váš program či skript může ptát a jakou dostane odpověď**. 

Příkladem může být zdroj informací o počasí, např.:

- můžete se zeptat na předpověď **počasí**
  - na **určitém místě** (popsáno zeměpisnými souřadnicemi ve formátu dle [RFC 5870](https://tools.ietf.org/html/rfc5870)) 
  - a v **určitém čase** (popsáno řetězcem vytvořeným na základě [RFC 3339](https://tools.ietf.org/html/rfc3339)) 
- a dostanete odpověď coby **číslo s jedním desetinným místem**, které
vyjadřuje teplotu stupních Celsia.


> Díky popisu API přesně víte, co je potřeba a co dostanete.

Při práci s API propojujete jednotlivé služby mezi sebou — podobně jako
minule, když jsme se dívali na automatizační služby. Tentokrát však dochází ke
skutečné integraci: cizí data dostanete přímo do své aplikace (nebo naopak,
svá data poskytnete ostatním). Namísto obdélníků, které obsahují cizí weby,
jsou získaná data využitelná kdekoli si zamanete.

Dalším příkladem je třeba kalendář — zeptáte se na plán konkrétního dne
(zadáte např. datum ve formátu "YYYY-MM-DD") a kalendář vrátí seznam vašich
schůzek ve formátu [ICAL](https://en.wikipedia.org/wiki/ICalendar). 
