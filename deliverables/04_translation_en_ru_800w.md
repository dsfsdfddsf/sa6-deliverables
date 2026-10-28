# EN→RU translation template (~800 words)

Ready deliverable type for any "EN->RU 800-word translation" gig (Dework content gigs, Kwork/FL text orders, or a Zcash-RU localization line).
Source: ZecHub wiki, "Zcash Shielded Assets" (public, fetched 2026-10-28: https://github.com/ZecHub/zechub/blob/main/site/Zcash_Tech/Zcash_Shielded_Assets.md) — first ~800 words.
Usage: for a real gig, swap the embedded EN source for the client's text (keep the same format: EN source -> RU translation -> glossary/notes).

---

## English source (~800 words)

# Zcash Shielded Assets

## TL;DR

Zcash Shielded Assets (ZSA) are a proposed protocol extension that would let assets **other than ZEC** — stablecoins, governance tokens, or any custom asset — live inside Zcash's shielded pool, with the sender, the recipient, and the amount kept private.

- **What it is:** ERC-20-style custom assets, but shielded by default.
- **Who is building it:** QEDIT, under a grant from the Zcash Foundation, in collaboration with the Electric Coin Company.
- **How it is specified:** ZIP 226 (transfer and burn) together with ZIP 227 (issuance).
- **Status:** not live on mainnet and not part of Network Upgrade 7 (NU7). ZIP 259, which lists everything NU7 deploys, does not include ZIP 226 or ZIP 227, and no ZSA activation date has been set.
- **Fees:** always paid in ZEC, regardless of the asset being moved.

## Core Explanation

Zcash Shielded Assets (ZSA) are a proposed improvement to the Zcash protocol that would enable the creation, transfer, and burn of custom assets on the Zcash chain. If you are familiar with the ERC-20 token standard on the Ethereum blockchain, ZSAs are to Zcash as ERC-20 tokens are to Ethereum.

Zcash Shielded Assets would enable the creation of custom tokens on the Zcash blockchain, thereby allowing tokens other than ZEC to benefit from the anonymity and privacy of shielded transactions on the Zcash blockchain.

A major potential use of ZSAs would be to issue stablecoins on the Zcash protocol. Stablecoins are cryptocurrencies that peg their value to a fiat currency, such as the US Dollar or Euro. Currently, some of the most widely circulated stablecoins are ERC-20 tokens such as USDC and Dai.

Another potential use of ZSAs would be for the issuing of governance tokens. For example, ZecHub (the publisher of this wiki) is a Decentralized Autonomous Organization (DAO) and could create and issue to its members a ZSA for voting on proposals and governance decisions.

ZSAs are being developed by QEDIT, under a major grant from the Zcash Foundation in collaboration with the Electric Coin Company. As this project is still being actively developed, updates are posted on the project thread of the Zcash forum. The ZSA grant application by QEDIT is available from the Zcash Foundation grants website.

## Visual / Analogy — The sealed envelope

Picture a Zcash shielded transaction as a plain, sealed envelope dropped into a public mailbox. Anyone can see that an envelope was posted. Nobody can see who sent it, who collects it, or what is inside — and every envelope looks identical to every other one.

Today, an envelope on the Zcash network can only carry one thing: ZEC. ZSA does not change the envelope. It changes what is allowed inside it. After ZSA, the same sealed envelope could carry a stablecoin, a DAO governance token, or a company loyalty point — and from the outside it would still look exactly like every other envelope on the network.

One detail is worth holding on to: the postage is always paid in ZEC, no matter what is inside the envelope.

### What an outside observer can see

| An observer can see... | ERC-20 on Ethereum | ZSA on Zcash |
| --- | --- | --- |
| Who sent it | Public | Shielded |
| Who received it | Public | Shielded |
| How much was moved | Public | Shielded |
| Individual balances | Public | Shielded |
| Total supply of the asset | Public | Public — deliberately |
| Currency the fee is paid in | ETH | ZEC |

### Why the supply row is not a bug

The bottom two rows of the table are where ZSA gets interesting. ZIP 227 deliberately keeps issuance transparent, so that the circulating supply of every asset can be tracked on-chain. Individual holdings and individual payments stay private; the total number of tokens in existence does not.

For a stablecoin issuer, that combination is the point rather than a compromise. Reserves can be audited against a publicly verifiable supply, while the people actually using the token keep their balances and payments to themselves.

### One asset, one identity

Every asset gets a unique Asset Identifier, derived from the issuer's issuance key together with a text description of the asset. Two different issuers cannot produce the same identifier, and minting or changing an asset requires cryptographic authorization from its issuer. In envelope terms: anyone can post an envelope, but only the mint that owns a given asset can print more of it.

---

## Russian translation (ru-RU)

# Щитовые активы Zcash (Zcash Shielded Assets)

## Кратко

Zcash Shielded Assets (ZSA) — предлагаемое расширение протокола, которое позволит активам **кроме ZEC** — стейблкоинам, токенам управления или любому кастомному активу — находиться внутри щитового пула Zcash при сохранении конфиденциальности отправителя, получателя и суммы.

- **Суть:** кастомные активы в стиле ERC-20, но щитовые по умолчанию.
- **Кто разрабатывает:** QEDIT по гранту Фонда Zcash во взаимодействии с Electric Coin Company.
- **Спецификация:** ZIP 226 (перевод и сжигание) вместе с ZIP 227 (эмиссия).
- **Статус:** не запущено в mainnet и не входит в Network Upgrade 7 (NU7). ZIP 259, перечисляющий всё, что устанавливает NU7, не включает ZIP 226 и ZIP 227; дата активации ZSA не назначена.
- **Комиссии:** всегда оплачиваются ZEC, независимо от перемещаемого актива.

## Основное объяснение

Zcash Shielded Assets (ZSA) — предлагаемое улучшение протокола Zcash, позволяющее создавать, перемещать и сжигать кастомные активы на цепи Zcash. Если вам знаком стандарт токенов ERC-20 в блокчейне Ethereum, то ZSA для Zcash — то же самое, что токены ERC-20 для Ethereum.

Zcash Shielded Assets позволят создавать кастомные токены в блокчейне Zcash, тем самым дав токенам, отличным от ZEC, доступ к анонимности и приватности щитовых транзакций.

Одно из ключевых применений ZSA — выпуск стейблкоинов в протоколе Zcash. Стейблкоины — криптовалюта с привязкой стоимости к фиатной валюте, например к доллару США или евро. Сегодня часть наиболее распространённых стейблкоинов — токены ERC-20, такие как USDC и Dai.

Другое применение ZSA — выпуск токенов управления (governance tokens). Например, ZecHub (издатель этой вики) — децентрализованная автономная организация (DAO), которая могла бы создать и выпустить своим членам ZSA для голосования по предложениям и решениям об управлении.

ZSA разрабатывают в QEDIT по крупному гранту Фонда Zcash во взаимодействии с Electric Coin Company. Проект активно развивается; обновления публикуются на теме проекта в форуме Zcash. Заявка на грант ZSA от QEDIT доступна на сайте грантов Фонда Zcash.

## Визуализация / Аналогия — Письмо в конверте

Представьте щитовую транзакцию Zcash как обычный запечатанный конверт, брошенный в общественный почтовый ящик. Все видят, что конверт был отправлен. Никто не видит, кто отправил, кто получит и что внутри, — при этом все конверты выглядят одинаково.

Сегодня конверт в сети Zcash может содержать только одну вещь: ZEC. ZSA не меняет конверт — оно меняет **то, что в него можно положить**. После ZSA тот же запечатанный конверт может нести стейблкоин, токен управления DAO или балл программы лояльности компании — и со стороны он по-прежнему выглядит как любой другой конверт в сети.

Важная деталь: «почтовый сбор» всегда оплачивается ZEC, независимо от содержимого конверта.

### Что видит внешний наблюдатель

| Наблюдатель видит... | ERC-20 в Ethereum | ZSA в Zcash |
| --- | --- | --- |
| Кто отправил | Публично | Щитово |
| Кто получил | Публично | Щитово |
| Сумма перевода | Публично | Щитово |
| Индивидуальные балансы | Публично | Щитово |
| Общий объём эмиссии актива | Публично | Публично — намеренно |
| Валюта, в которой платится комиссия | ETH | ZEC |

### Почему строка об эмиссии — это не баг

Именно последние две строки таблицы делают ZSA интересными. ZIP 227 намеренно оставляет эмиссию прозрачной, чтобы обращение каждого актива можно было отслеживать он-чейн. Индивидуальные владения и платежи остаются приватными; общее количество выпущенных токенов — нет.

Для издателя стейблкоина такое сочетание — не компромисс, а суть: резервы можно аудитировать по публично проверяемому объёму эмиссии, пока реальные пользователи токена держат свои балансы и платежи при себе.

### Один актив — одна идентичность

Каждый актив получает уникальный Asset Identifier (идентификатор актива), вычисляемый из ключа эмиссии издателя вместе с текстовым описанием актива. Два разных издателя не смогут получить одинаковый идентификатор, а чеканка или изменение актива требуют криптографической авторизации его издателя. В терминах конверта: конверт может отправить любой, но печатать конкретный актив может только «монетный двор», которым этот актив принадлежит.

## Glossary and notes (for the client)
- Terms kept in original where standard: ZSA, DAO, ZIP, ERC-20, mainnet, NU7, USDC, Dai, ZEC, ETH, Asset Identifier, shielded -> «щитовой(ая)».
- Style: ru-RU, technical but accessible (wiki register); «shielded pool» -> «щитовый пул», «issuance» -> «эмиссия», «burn» -> «сжигание».
- Length: EN source ~800 words; RU translation ~760-820 words (translation-equivalent, no padding).
