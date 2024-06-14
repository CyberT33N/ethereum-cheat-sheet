# Ethereum Cheat Sheet



# Wiki






## Uniswap

### Pair

#### Informationen zu Uniswap Paaren
Ein "Pair" (Paar) in Bezug auf Uniswap und ähnliche dezentrale Börsen (DEX) bezieht sich auf ein Handelspaar, das aus genau zwei verschiedenen Token besteht. Hier sind einige wichtige Details und Funktionen eines Paares:

- **Token0 und Token1**: Ein Paar besteht aus genau zwei Token, die als `token0` und `token1` bezeichnet werden. Diese Token können ERC-20-Token sein, die auf der Ethereum-Blockchain basieren.

- **Liquiditätspool**: Ein Paar auf Uniswap bildet einen Liquiditätspool, in dem Benutzer ihre Token einzahlen können, um Liquidität bereitzustellen. Dies ermöglicht es anderen Benutzern, diese Token zu handeln.

- **Preisbildung**: Der Preis eines Tokens in einem Paar wird durch das Verhältnis der in diesem Pool vorhandenen Token bestimmt. Beispielsweise wird der Preis von `token0` in `token1` durch das Verhältnis von `token0` zu `token1` im Pool bestimmt und umgekehrt.

- **Automatische Market Maker (AMM)**: Uniswap verwendet ein AMM-Modell, bei dem Preise automatisch basierend auf Angebot und Nachfrage angepasst werden. Dies unterscheidet sich von traditionellen Börsen, die ein Orderbuch verwenden.

- **Swapping (Austausch)**: Benutzer können Token in einem Paar mithilfe der Uniswap-Schnittstelle austauschen. Der Preis ändert sich dabei dynamisch basierend auf dem Token-Bestand im Pool.

- **Pair-Adresse**: Jedes Paar hat eine eindeutige Ethereum-Adresse, über die es auf der Blockchain identifiziert und verwaltet wird. Diese Adresse wird verwendet, um auf das Paar zuzugreifen und darauf zuzugreifen, beispielsweise um Liquidität hinzuzufügen oder zu entfernen.

- **Paar-Ereignisse**: Ereignisse wie `PairCreated` werden ausgelöst, wenn ein neues Paar erstellt wird. Diese Ereignisse können über die Blockchain überwacht werden, um über neue Paare und deren Details informiert zu werden.

Insgesamt sind Paare die grundlegenden Bausteine für den Handel auf dezentralen Börsen wie Uniswap. Sie ermöglichen es Benutzern, nahtlos Token zu handeln und Liquidität bereitzustellen, was eine wichtige Rolle im Ökosystem der dezentralen Finanzen (DeFi) spielt.














<br><br>
<br><br>
-- -- -- -- -- -- -- -- -- -- -- -- 
<br><br>
<br><br>


# Smart Contracts

## Überblick

Smart Contracts sind selbstausführende Verträge, bei denen die Bedingungen der Vereinbarung direkt in Code geschrieben sind. Sie laufen auf Blockchains und ermöglichen es, vertrauenswürdige Transaktionen und Vereinbarungen ohne eine zentrale Autorität durchzuführen.

## Ethereum

### Überblick
Ethereum ist die führende Plattform für die Erstellung und Bereitstellung von Smart Contracts. Es verwendet die Ethereum Virtual Machine (EVM), um den Code auszuführen.

### Eigenschaften
- **Programmiersprachen:** Primär Solidity, aber auch Vyper und andere.
- **EVM:** Führt Smart Contracts auf der Blockchain aus.
- **Gas:** Transaktionen erfordern Gas, eine Gebühr, die in Ether (ETH) bezahlt wird.

### Schlüsselfunktionen
- **ERC20:** Standard für fungible Token.
- **ERC721:** Standard für nicht-fungible Token (NFTs).
- **Dezentralisierte Anwendungen (DApps):** Anwendungen, die auf Smart Contracts basieren.

### Beispiel
```solidity
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint256 public data;

    function set(uint256 _data) public {
        data = _data;
    }

    function get() public view returns (uint256) {
        return data;
    }
}
```




















<br><br>
<br><br>
-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
<br><br>
<br><br>


# Token-Standard

<br><br>

## ERC20
- https://github.com/ethereum/ercs/blob/master/ERCS/erc-20.md








<br><br>
<br><br>
-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
<br><br>
<br><br>




# ABI - Application Binary Interface

## Definition

ABI steht für "Application Binary Interface" (Anwendungs-Binär-Schnittstelle). Es handelt sich um eine Schnittstellenspezifikation auf binärer Ebene zwischen zwei Programmmodulen, oft zwischen einem Betriebssystem und einem Computerprogramm oder zwischen verschiedenen Programmkomponenten.

## Hauptmerkmale

- Definiert, wie Funktionen aufgerufen werden
- Legt fest, wie Daten in Datenstrukturen organisiert werden
- Bestimmt die binäre Schnittstelle zwischen kompilierten Objektdateien oder Programmbibliotheken

## Bedeutung

- Ermöglicht die Interoperabilität zwischen verschiedenen Softwarekomponenten
- Wichtig für die Kompatibilität zwischen verschiedenen Versionen einer Softwarebibliothek
- Erlaubt die Verwendung von Binärdateien auf verschiedenen Systemen mit demselben ABI

## Unterschied zur API

- API (Application Programming Interface) definiert die Schnittstelle auf Quellcode-Ebene
- ABI definiert die Schnittstelle auf binärer Ebene
- Eine stabile ABI ermöglicht die Verwendung von Binärdateien ohne Neukompilierung

## Beispiele für ABIs

- System V ABI für Unix-ähnliche Systeme
- Microsoft Windows ABI
- ARM EABI für eingebettete ARM-Systeme

## Herausforderungen

- Änderungen am ABI können zu Inkompatibilitäten führen
- Verschiedene Compiler können unterschiedliche ABIs für die gleiche Architektur erzeugen
- Plattformübergreifende Entwicklung erfordert oft die Berücksichtigung mehrerer ABIs

## Fazit

Das Verständnis und die korrekte Implementierung von ABIs sind entscheidend für die Entwicklung von interoperabler und langlebiger Software, insbesondere in heterogenen Systemumgebungen.



<br><br>
<br><br>




















<br><br>
<br><br>
-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
<br><br>
<br><br>



# Dezentrale Börsen (DEX) und Automated Market Maker (AMM) Protokolle

## Uniswap

 Überblick
Uniswap ist ein dezentrales Austauschprotokoll (DEX) auf der Ethereum-Blockchain. Es ermöglicht den Tausch von ERC20-Token direkt zwischen Nutzern mittels automatischer Marktliquidität (AMM).

### Eigenschaften
- **Automatisches Market Making:** Verwendet ein Constant Product Market Making Modell.
- **ERC20-Token Unterstützung:** Unterstützt den Tausch einer Vielzahl von ERC20-Token.
- **Uniswap V2 und V3:** Bietet verschiedene Versionen mit unterschiedlichen Funktionen und Optimierungen.

### Schlüsselfunktionen
- **Liquidity Pools:** Nutzer können Liquidität bereitstellen und verdienen Handelsgebühren.
- **Swap-Funktionalität:** Ermöglicht den sofortigen Tausch von Token ohne Orderbuch.

### Website
[Uniswap](https://uniswap.org/)

---

## SushiSwap

### Überblick
SushiSwap ist ein Fork von Uniswap, der zusätzliche Funktionen und Governance-Aspekte integriert hat.

### Eigenschaften
- **Erweiterte Funktionen:** Bietet Funktionen wie Yield Farming und Staking.
- **SUSHI Token:** Eigenes Governance-Token für Nutzer des Protokolls.
- **SushiSwap AMM:** Verbesserte Version des AMM-Modells von Uniswap.

### Schlüsselfunktionen
- **MasterChef:** Belohnungsprogramm für Yield Farming.
- **Onsen:** Temporäre Incentives für bestimmte Liquiditätspools.

### Website
[SushiSwap](https://sushi.com/)

---

## Weitere AMM-Protokolle

### Curve Finance
- Spezialisiert auf Stablecoin-Tausch mit geringen Slippage-Raten.
- Besondere Anpassungen für Stablecoin-Paare.

### Balancer
- Ermöglicht das Erstellen von benutzerdefinierten Pools mit unterschiedlichen Gewichtungen.
- Unterstützt auch Stablecoin-Paare und andere Token.

### Bancor
- Verwendet ein einzigartiges System der permanenten Liquidität, um den Handel zu erleichtern.
- Ermöglicht direktes Tauschen von Token ohne gegen eine andere Partei zu handeln.

---

Diese Protokolle sind grundlegende Bausteine der dezentralen Finanzwelt (DeFi) und bieten eine alternative Möglichkeit zum traditionellen Börsenhandel durch ihre dezentrale und automatisierte Natur.













<br><br>
<br><br>
-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
<br><br>
<br><br>


# Gas
-  Ist eine Einheit, die für die Messung der Rechenarbeit verwendet wird, die zur Durchführung von Transaktionen oder zur Ausführung von Smart Contracts auf der Ethereum-Plattform erforderlich ist.

<br><br>

## GasUsed
- Bezieht sich auf die Menge an Gas, die für eine einzelne Transaktion verwendet wurde.

<br><br>

 cumulativeGasUsed
- Ist die Summe des Gases, das von allen Transaktionen in einem Block verbraucht wurde, bis einschließlich der aktuellen Transaktion. Es ist also ein kumulativer Wert.



















<br><br>
<br><br>
-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
<br><br>
<br><br>


## Accounts

Ein **Ethereum Account** ist eine Entität, die Transaktionen auf der Ethereum-Blockchain senden und empfangen kann. Es gibt zwei Arten von Accounts:

1. **Extern verwaltete Konten (EOA)**: Diese Konten werden von Benutzern kontrolliert und erfordern einen privaten Schlüssel, um Transaktionen zu signieren.
2. **Contract-Konten**: Diese werden durch Smart Contracts verwaltet und können keine Transaktionen initiieren; sie reagieren nur auf Transaktionen, die von EOAs gesendet werden.

Jeder Account hat eine eindeutige Adresse, die aus 40 hexadezimalen Zeichen besteht (z. B. `0x32Be343B94f860124dC4fEe278FDCBD38C102D88`).





<br><br>
<br><br>

## Private Keys

Ein **Private Key** ist ein geheimes, kryptografisches Passwort, das die vollständige Kontrolle über einen Ethereum-Account gewährt. Der Private Key besteht aus 64 hexadezimalen Zeichen und sieht etwa so aus:
- 4c0883a69102937d6234145d0d4d2a8010118f04064f1a6d6b4fb15f573f794b

Dieser Schlüssel ist essenziell für das Signieren von Transaktionen und das Ausgeben von Geldern. **Verlust des Private Keys bedeutet den Verlust des Zugangs zu den damit verbundenen Geldern**.

### Private Key exportieren

#### Metamask
Three dots -> Accounts details -> Show private key




<br><br>
<br><br>

## Passphrase

Eine **Passphrase** ist eine zusätzliche Sicherheitsschicht, die verwendet wird, um den Private Key zu verschlüsseln. Sie wird oft in Form eines Mnemonischen Phrasensets (auch Seed Phrase genannt) dargestellt, das aus 12, 18 oder 24 Wörtern besteht:

































<br><br>
<br><br>
_____________________________________________
_____________________________________________
<br><br>
<br><br>

# Clients

<br><br>
<br><br>

## Third Party
- https://dashboard.alchemy.com/

<br><br>
<br><br>

## Own Nodes
- https://geth.ethereum.org/docs/getting-started/hardware-requirements
- parity

<br><br>
<br><br>

### Geth

<br><br>

#### Install

<br><br>

#### Docker
```shell
docker pull ethereum/client-go
docker run -it -p 30303:30303 ethereum/client-go
```














<br><br>
<br><br>
<br><br>
<br><br>

# Uniswap
- Uniswap is a decentralized exchange protocol built on Ethereum. To be more precise, it is an automated liquidity protocol. There is no order book or any centralized party required to make trades. Uniswap allows users to trade without intermediaries, with a high degree of decentralization and censorship-resistance.

Traders can exchange Ethereum tokens (ERC20) on Uniswap without having to trust anyone with their funds. Meanwhile, anyone can lend their crypto to special reserves called liquidity pools. In exchange for providing money to these pools, they earn fees.

## SDK
- https://ethereum.stackexchange.com/questions/152662/how-to-find-out-right-away-when-a-new-uniswap-pool-is-created-with-liquidity

### The Uniswap V3 SDK
- https://docs.uniswap.org/sdk/v3/overview
```shell
npm i --save @uniswap/v3-sdk
npm i --save @uniswap/sdk-core
```






## API
- https://docs.uniswap.org/contracts/v2/reference/API/queries
- - https://docs.uniswap.org/api/subgraph/guides/examples












<br><br>
<br><br>


## bitquery
- https://docs.bitquery.io/docs/examples/dextrades/latest-trading-pairs-api

<br><br>
<br><br>

#### Find new pairs
- https://docs.uniswap.org/contracts/v2/reference/API/queries
