# TurboChain — Mobile App Mocks
## Pago de Turbosina con Tokens en Blockchain

Plataforma de pago automático para abastecimiento de turbosina (Jet A-1) en pista. Las pipas cargan combustible a las aeronaves y los tokens se debitan automáticamente de la wallet del operador al completar la descarga.

---

## 📁 Archivos incluidos

| Archivo | Módulo | Descripción |
|---|---|---|
| `01_splash.html` | Splash / Onboarding | Pantalla de bienvenida, propuesta de valor, CTA |
| `02_register.html` | Registro | Alta de operador: nombre, correo, código IATA, password |
| `03_login.html` | Login | Autenticación con correo/password, biometría y wallet |
| `04_wallet_setup.html` | Configuración Wallet | Conectar MetaMask, WalletConnect, Coinbase o crear wallet |
| `05_home.html` | Home / Dashboard | Balance USDC/TURBO, cargas activas, TX on-chain |
| `06_new_order.html` | Nueva Carga | Selección aeronave, litros, posición en pista, token de pago |
| `07_payment.html` | Confirmar Pago | Detalle TX, smart contract, firma de autorización |
| `07b_tx_processing.html` | TX Confirmada | Confirmación on-chain, hash, PolygonScan, estado de descarga |
| `08_wallet.html` | Mis Tokens | Saldo USDC/TURBO/MATIC, QR, swap, historial on-chain |
| `09_orders.html` | Mis Cargas | Gauge de descarga en tiempo real, historial de cargas |
| `shared.css` | Design System | Variables CSS, componentes, tipografía |

---

## 🔗 Flujo de la app

```
Avión aterriza → Operador abre app → Selecciona aeronave y litros
→ Elige token (USDC/TURBO) → Firma autorización en blockchain
→ Pipa recibe autorización → Inicia descarga de turbosina
→ Litros se miden en tiempo real → Al completar: tokens debitados automáticamente
→ TX queda registrada en Polygon → Trazabilidad inmutable
```

## 🎨 Design Tokens

- **Red blockchain:** Polygon (MATIC) — bajas comisiones
- **Tokens de pago:** USDC, TURBO (token nativo), ETH
- **Fuentes:** Inter (UI), JetBrains Mono (addresses/hashes)
- **Paleta:** Verde Pemex (#00843D), Verde oscuro (#006341), Sky (#0C7BB3), Fuel (#B8860B)

## 🔗 Flujos navegables

```
01_splash → 02_register → 04_wallet_setup → 05_home
01_splash → 03_login → 05_home
05_home → 06_new_order → 07_payment → 07b_tx_processing → 05_home
05_home → 08_wallet
05_home → 09_orders
```
