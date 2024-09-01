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

### Standardmethoden

Diese Methoden sind Teil der ERC-20 Schnittstelle oder sind allgemein in Ethereum Smart Contracts verwendet.

#### ERC-20 Standardmethoden:
- `totalSupply()`: Gibt die gesamte Menge an Token im Umlauf zurück.
- `balanceOf(address account)`: Gibt den Kontostand eines bestimmten Kontos zurück.
- `transfer(address recipient, uint256 amount)`: Überträgt eine bestimmte Menge an Token an einen Empfänger.
- `allowance(address owner, address spender)`: Gibt die erlaubte Menge an Token zurück, die ein Spender vom Besitzer ausgeben darf.
- `approve(address spender, uint256 amount)`: Genehmigt einen Spender, eine bestimmte Menge an Token vom Besitzer auszugeben.
- `transferFrom(address sender, address recipient, uint256 amount)`: Überträgt eine bestimmte Menge an Token von einem Sender an einen Empfänger, vorausgesetzt, der Sender hat genug erlaubte Token.

#### ERC-20 Events:
- `Transfer(address indexed from, address indexed to, uint256 value)`: Wird ausgelöst, wenn Token übertragen werden.
- `Approval(address indexed owner, address indexed spender, uint256 value)`: Wird ausgelöst, wenn die Genehmigung für die Übertragung von Token erteilt wird.






















<br><br>
<br><br>
-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
<br><br>
<br><br>




# ABI - Application Binary Interface
- **Auf Blockchain Explorer wie z.b. Etherscan kann man den Contract und den jeweiligen ABI zu einem Token sehen. Diesen ABI kann man verwendetn um mit web3.js einen Contract zu erstellen**

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

# Ethereum Smart Contract ABI Methodennamen

## Überblick

Die Methodennamen in einem Ethereum-Smart-Contract-ABI (Application Binary Interface) sind nicht standardisiert oder universell identisch. Die Namen und Signaturen von Methoden in einem ABI werden beim Erstellen des Smart Contracts vom Entwickler definiert und können von Contract zu Contract unterschiedlich sein.

### Wichtige Punkte

1. **Entwicklerspezifisch**
   - Die Namen der Methoden sind vollständig vom Entwickler des Smart Contracts definiert. Daher können verschiedene Contracts, selbst wenn sie ähnliche Funktionalitäten bieten, unterschiedliche Namen verwenden.

2. **Kollisionsgefahr**
   - Bei Contracts von verschiedenen Entwicklern oder für unterschiedliche Zwecke kann es zu Namensüberschneidungen kommen. Beispielsweise könnte ein Contract `getTaxThreshold()` und ein anderer `taxSwapThreshold()` verwenden, obwohl beide ähnliche Funktionalitäten bieten.

3. **Standardisierte Methoden**
   - Einige Methoden sind in bekannten Standards wie ERC-20 oder ERC-721 definiert und haben standardisierte Namen, z.B. `transfer`, `approve`, `balanceOf` bei ERC-20 Tokens. Diese Namen sind in den jeweiligen Standards festgelegt und daher konsistent.

4. **Benutzerdefinierte Methoden**
   - Für spezifische Funktionen oder Implementierungen können die Methodennamen benutzerdefiniert sein. Ein Contract könnte Methoden wie `_taxSwapThreshold` oder `_maxTxAmount` verwenden, die speziell für diesen Contract entwickelt wurden und nicht notwendigerweise in anderen Contracts zu finden sind.

### Beispiel

Hier ist ein Überblick über häufige und benutzerdefinierte Methodennamen:

- **Standardisierte Namen (z.B. ERC-20):**
  - `transfer`
  - `approve`
  - `balanceOf`
  - `allowance`

- **Benutzerdefinierte Namen:**
  - `_taxSwapThreshold`
  - `isFree_AnyERC20Tokens`
  - `caLimiter`
  - `addToBlackList`

## Verwendung von Web3.js mit ABI

Um Methoden eines Smart Contracts aufzurufen, müssen Sie das ABI des spezifischen Contracts verwenden, mit dem Sie arbeiten möchten. Hier ist ein Beispiel, wie Sie dies in TypeScript tun können:

```typescript
import Web3 from 'web3';

class ContractInteraction {
  private web3: Web3;
  private contract: any;

  constructor(provider: string, contractAddress: string, abi: any[]) {
    this.web3 = new Web3(provider);
    this.contract = new this.web3.eth.Contract(abi, contractAddress);
  }

  async callMethod(methodName: string, ...args: any[]): Promise<any> {
    if (!this.contract.methods[methodName]) {
      throw new Error(`Method ${methodName} does not exist in the contract ABI.`);
    }
    return this.contract.methods[methodName](...args).call();
  }
}

// Usage
const provider = 'https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID';
const contractAddress = '0x08c4bb1def099bca4c6b84ebb4e7d0f4eac2f3c9';
const abi = [ /* Ihr ABI hier */ ];

const contract = new ContractInteraction(provider, contractAddress, abi);

contract.callMethod('_taxSwapThreshold')
  .then(console.log)
  .catch(console.error);
```


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
_________________________________________________________
_________________________________________________________
<br><br>
<br><br>

# Uniswap
- Uniswap is a decentralized exchange protocol built on Ethereum. To be more precise, it is an automated liquidity protocol. There is no order book or any centralized party required to make trades. Uniswap allows users to trade without intermediaries, with a high degree of decentralization and censorship-resistance.

- Traders can exchange Ethereum tokens (ERC20) on Uniswap without having to trust anyone with their funds. Meanwhile, anyone can lend their crypto to special reserves called liquidity pools. In exchange for providing money to these pools, they earn fees.

- **There are different versions v2, v3, v4 and each version ist not tradeable with the other version**








<br><br>
<br><br>
<br><br>
<br><br>


## v2
- https://docs.uniswap.org/contracts/v2/overview

<br><br>
<br><br>

### Contract

<br><br>
<br><br>

#### Factory
- https://docs.uniswap.org/contracts/v2/reference/smart-contracts/factory

<br><br>
<br><br>

##### Events

<br><br>
<br><br>

###### PairCreated (https://docs.uniswap.org/contracts/v2/reference/smart-contracts/factory#paircreated)
- Emitted each time a pair is created via createPair.
- token0 is guaranteed to be strictly less than token1 by sort order.
- The final uint log value will be 1 for the first pair created, 2 for the second, etc. (see allPairs/getPair).
```javascript
import { Web3 } from 'web3'

const providerUrl = 'https://mainnet.infura.io/v3/xxxxxxxxxxxxxxxxxxx4'
const web3 = new Web3(providerUrl)

const UNISWAP_FACTORY_ADDRESS = "0x5C69bEe701ef814a2B6a3EDD4B1652CB9cc5aA6f";

const FACTORY_ABI = [
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "token0",
        "type": "address"
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "token1",
        "type": "address"
      },
      {
        "indexed": false,
        "internalType": "address",
        "name": "pair",
        "type": "address"
      }
    ],
    "name": "PairCreated",
    "type": "event"
  }
];

// Create a contract instance
const uniswapFactory = new web3.eth.Contract(FACTORY_ABI, UNISWAP_FACTORY_ADDRESS);

// Subscribe to PairCreated events
const myEvent = await uniswapFactory.events.PairCreated({
    fromBlock:  'latest'
})

console.log('Subscribed to PairCreated events')

myEvent.on('data', (event) => {
  console.log(`New pair created! Token0: ${event.returnValues.token0}, Token1: ${event.returnValues.token1}, Pair Address: ${event.returnValues.pair}`);
})

myEvent.on('error', (error) => {
  console.error(error);
})
```









<br><br>
<br><br>
<br><br>
<br><br>


## v3
- https://docs.uniswap.org/contracts/v3/overview

<br><br>
<br><br>

### Wichtige Contracts für Uniswap V3

| Contract Name                        | Funktion                                                                                          |
|--------------------------------------|---------------------------------------------------------------------------------------------------|
| **UniswapV3Factory**                 | Erstellt und verwaltet Pools (nicht direkt für Trading).                                           |
| **SwapRouter / SwapRouter02**        | Führt die eigentlichen Swaps durch (Tokens kaufen/verkaufen).                                      |
| **Quoter / QuoterV2**                | Gibt Preisinformationen für Swaps (Preisschätzung vor einem echten Handel).                        |
| **Multicall / Multicall2**           | Führt mehrere Calls in einer einzigen Transaktion aus (Gas sparen, komplexe Interaktionen).        |
| **NonfungiblePositionManager**       | Verwalten von Liquiditätspositionen als NFTs in V3 (für Bereitstellung/Entfernung von Liquidität). |
| **TickLens**                         | Ruft Tick-Informationen ab, die für Gebühren und Liquiditätsbereich relevant sind.                |
| **V3Migrator**                       | Ermöglicht die Migration von Positionen von Uniswap V2 zu V3.                                      |
| **UniversalRouter**                  | Bietet erweiterten Routing-Support für komplexere Swap-Logiken.                                   |
| **Permit2**                          | Erlaubt Transaktionen mit erweiterter Genehmigungslogik (Gas-Einsparungen und Benutzerfreundlichkeit).|

## Muss alles über Uniswap laufen?

- **Nein**, du musst nicht ausschließlich Uniswap verwenden. Andere DEXs oder Aggregatoren können bessere Liquidität oder Gebühren bieten.
- Berücksichtige spezialisierte DEXs auf Layer 2 Netzwerken wie Arbitrum, Optimism oder zkSync.

## Wichtige Punkte bei der Integration von ETH Layer 2 Tokens

1. **Layer 2 Integration**:
   - Uniswap unterstützt mehrere Layer 2 Netzwerke, aber stelle sicher, dass dein Code und deine Infrastruktur kompatibel sind.

2. **Routing und Aggregation**:
   - Nutze DEX-Aggregatoren (z.B. 1inch, Matcha), um immer den besten Preis für Swaps zu erhalten, auch wenn sie nicht über Uniswap laufen.

3. **Token-Verfügbarkeit und Liquidität**:
   - Prüfe, ob deine Zieltokens auf dem gewählten Layer 2 Netzwerk verfügbar sind und ausreichend Liquidität haben.

## Zusammenfassung

- Für Swaps nutze primär den **SwapRouter** und für Preisanfragen den **Quoter** Contract.
- Stelle sicher, dass alle Contracts auf dem richtigen Layer 2 Netzwerk konfiguriert sind.
- Überlege den Einsatz von Aggregatoren oder anderen DEXs für optimale Handelsbedingungen.






<br><br>
<br><br>


### Deployments
- - https://docs.uniswap.org/contracts/v3/reference/deployments
- https://docs.uniswap.org/contracts/v3/reference/deployments/ethereum-deployments




<br><br>
<br><br>

### Contract

<br><br>
<br><br>

#### Factory
- https://docs.uniswap.org/contracts/v3/reference/core/interfaces/IUniswapV3Factory

<br><br>
<br><br>

##### Events
- https://docs.uniswap.org/contracts/v3/reference/core/interfaces/IUniswapV3Factory#events

<br><br>
<br><br>

###### PoolCreated
- https://docs.uniswap.org/contracts/v3/reference/core/interfaces/IUniswapV3Factory#poolcreated
```javascript

// Uniswap V3 Factory Contract Adresse und ABI
const uniswapV3FactoryAddress = '0x1F98431c8aD98523631AE4a59f267346ea31F984';
const uniswapV3FactoryABI = [
    {
        "anonymous": false,
        "inputs": [
            {
                "indexed": true,
                "internalType": "address",
                "name": "token0",
                "type": "address"
            },
            {
                "indexed": true,
                "internalType": "address",
                "name": "token1",
                "type": "address"
            },
            {
                "indexed": true,
                "internalType": "uint24",
                "name": "fee",
                "type": "uint24"
            },
            {
                "indexed": false,
                "internalType": "address",
                "name": "pool",
                "type": "address"
            }
        ],
        "name": "PoolCreated",
        "type": "event"
    }
];

// Erstelle eine Contract-Instanz
const uniswapV3FactoryContract = new web3.eth.Contract(uniswapV3FactoryABI, uniswapV3FactoryAddress);

// Lausche auf das `PoolCreated` Event
uniswapV3FactoryContract.events.PoolCreated({
    fromBlock: 'latest'
}, (error, event) => {
    if (error) {
        console.error('Fehler beim Abfangen des Events:', error);
    } else {
        console.log('Neuer Pool erstellt:');
        console.log('Token0:', event.returnValues.token0);
        console.log('Token1:', event.returnValues.token1);
        console.log('Fee:', event.returnValues.fee);
        console.log('Pool-Adresse:', event.returnValues.pool);
    }
});
```











<br><br>
<br><br>
<br><br>
<br><br>



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
