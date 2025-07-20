# 🪙 Proyecto de Tokens ERC20 en Solidity

¡Bienvenido! Este repositorio contiene **dos contratos inteligentes ERC20** escritos en **Solidity**, listos para desplegar en Ethereum (testnets como Sepolia o Goerli).

---

## 🚀 Contrato 1:
[Mi token ERC20 en eth Escan](https://sepolia.etherscan.io/address/0x30be507d86743ab23bc34dbd06d9177d546c50bd)

### 📝 Descripción
Token ERC20 básico:
- **Nombre:** Mi Token
- **Símbolo:** MIT
- **Suministro inicial:** 1000 tokens (18 decimales)
- **Propietario inicial:** El creador recibe todos los tokens

### ⚙️ Características
- ✅ Implementa el estándar ERC20
- 🔐 Suministro fijo inicial
- 👤 El dueño inicial recibe todos los tokens

### 🧩 Código clave

```solidity
constructor() ERC20("Mi Token", "MIT") {
    _mint(msg.sender, 1000 * 10 ** decimals());
}
```
> 💡 Se crean 1000 tokens (con 18 decimales) al desplegar.

---

## 🛠️ Cómo desplegar

1. Abre [Remix IDE](https://remix.ethereum.org/)
2. Crea un archivo llamado `MiToken.sol` y pega el código del contrato.
3. Compila con Solidity **0.8.x**
4. Despliega desde la pestaña **Deploy & Run Transactions**
5. Asegúrate de tener MetaMask conectada a una testnet

---

## 💬 Cómo interactuar

- `totalSupply()`: Ver el suministro total del token
- `balanceOf(address)`: Ver saldo de tokens de una dirección
- `transfer(to, amount)`: Enviar tokens a otra cuenta

---

## 🪙 Contrato 2:
[MiToken ERC721](https://sepolia.etherscan.io/address/0xd07be9993713d419f90ec8036809199a2754331c)

### 📝 Descripción
Token ERC20 personalizable:
- **Nombre, símbolo y suministro inicial** definidos al desplegar

### ⚙️ Características
- ✅ ERC20 estándar
- 🛠️ Personalización completa al desplegar
- 📦 Todos los tokens asignados al creador

### 🧩 Código clave

```solidity
constructor(string memory name, string memory symbol, uint256 initialSupply)
    ERC20(name, symbol)
{
    _mint(msg.sender, initialSupply * 10 ** decimals());
}
```
> 🧠 Puedes pasar el nombre, símbolo y cantidad de tokens desde Remix o scripts de despliegue.

---

## 🛠️ Cómo desplegar `MiToken2`

1. Abre Remix y crea `MiToken2.sol`
2. Compila el contrato
3. En "Deploy", introduce:
   - `name`: Ej. "Crypto Sol"
   - `symbol`: Ej. "CSOL"
   - `initialSupply`: Ej. 10000
4. Haz clic en **Deploy**

---

## 💬 Cómo interactuar

Igual que el contrato anterior, pero los valores dependen de lo que pusiste al desplegar.

---

## ✅ Requisitos

- [MetaMask](https://metamask.io/) instalada
- [Remix IDE](https://remix.ethereum.org/)
- Conexión a testnet (Sepolia o Goerli)
- ETH de prueba para gas ([Faucet Sepolia](https://sepoliafaucet.com/))

---

## 📦 Librerías usadas

Ambos contratos usan [OpenZeppelin](https://docs.openzeppelin.com/contracts/):

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```
> Si usas Hardhat o Truffle, asegúrate de instalar OpenZeppelin.

---

## 📚 Recursos útiles

- [Documentación ERC20 - OpenZeppelin](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20)
  
© 2025 JhamilCali
