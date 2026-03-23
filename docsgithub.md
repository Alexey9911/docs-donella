# Bookie Documentation & GitHub Guide

Este documento define la estructura recomendada, el tono y los temas que deberán abordarse tanto en la **Documentación Oficial** (enfocada en el usuario, seria y directa) como en el **Repositorio de GitHub** (enfocada en desarrolladores, altamente técnica, masiva y con elementos simulados que aporten alto grado de profesionalismo).

---

## 1. OFFICIAL DOCUMENTATION (docs.bookie.app)
*El tono en la documentación oficial debe ser directo, conciso, serio y fácil de digerir. Orientado al usuario final y al trader.*

### 1.1. Project Overview
- **What is Bookie?** Bookie es un agente de Inteligencia Artificial autónomo construido sobre la red de Solana. Permite ejecutar operaciones financieras descentralizadas (token swaps, envíos de fondos, rastreo de portafolios) utilizando instrucciones en lenguaje natural, operando con una eficiencia minimalista y tiempos de respuesta de sub-segundos.
- **Design & UI/UX Palette:** El diseño se basa en un esquema limpio, predominantemente **Blanco (#FFFFFF)** para transmitir claridad y transparencia, acompañado de acentos **Naranjas (#f97316 y #facc15)** en botones, SVGs de fondo e íconos para guiar la acción del usuario y mantener energía en la interfaz.

### 1.2. Key Features
- **Natural Language Execution:** Conversión instantánea de intenciones de texto a transacciones firmables.
- **Jupiter V6 Integration:** Enrutamiento inteligente de liquidez para asegurar el mejor precio de intercambio con el menor "Price Impact".
- **Real-Time Portfolio Tracking:** Seguimiento de balances, histórico de transacciones y PnL de memecoins en tiempo real.
- **Sub-Second Speeds:** Interfaz calibrada para interactuar directamente con la alta tasa de rendimiento de Solana sin latencia de UI intermedias.

### 1.3. Security Guidelines
- **Non-Custodial Architecture:** Bookie **nunca** tiene acceso directo a las llaves privadas. Todas las transacciones deben ser aprobadas manualmente en la wallet del usuario.
- **Burner Wallets Recommendation:** Como mejor práctica de seguridad transversal, se recomienda enérgicamente utilizar "Burner Wallets" (billeteras secundarias con fondos limitados) aisladas de los activos principales (Cold Wallets o Vaults) para operar con agentes IA conectados a dApps de terceros.
- **Pre-Flight Simulation:** Toda transacción es simulada localmente antes de ser enviada al cliente para evitar transacciones fallidas o pérdida por slippage inesperado (MEV).

---

## 2. GITHUB REPOSITORY GUIDE
*El README de GitHub debe ser extremadamente técnico, masivo y proyectar la imagen de un ecosistema maduro, complejo y altamente auditado. Aquí se incluyen características reales mezcladas con "dummy objects", submódulos técnicos, sistemas complejos simulados y métricas exhaustivas para garantizar un "look and feel" ultraprofesional propio de un proyecto Open Source Tier-1 en Web3.*

### 2.1. Hero Section & Badges
- **Title:** `Bookie Core Protocol: The LLM-Driven Execution Engine for Solana`
- **Badges:** 
  - `[build: passing]` | `[coverage: 98.4%]` | `[license: MIT]` | `[Solana: 1.18.x compatible]` | `[Audited By: CertiK (Simulated) / OtterSec (Simulated)]` | `[Docker: Ready]`
- **Intro:** A high-throughput, low-latency intent resolution agent. Bridging Large Language Models with Solana's SVM (Solana Virtual Machine) to execute programmable, risk-adjusted DeFi primitives.

### 2.2. Architectural Overview (Highly Technical Detail)
- **Neuro-Routing Engine (Simulated Module):** Explicar cómo Bookie utiliza un motor de Inferencia Distribuido para "tokenizar" lenguaje natural combinándolo con grafos de liquidez de AMMs.
- **Transaction Pipeline Topology:**
  1. `IntentParserService`: NLP Model que extrae Entidades Nombradas (Token A, Token B, Amount).
  2. `RiskAssessmentLayer` (Dummy): Evalúa pools de liquidez sospechosos, honey-pots o riesgos de rug-pull utilizando análisis estático de los contratos inteligentes involucrados.
  3. `JupiterAggregatorProtocol`: Integración real con el SDK V6 para trazar el camino óptimo.
  4. `JitoMEVProtector` (Dummy/Advanced): Encargado de empaquetar la transacción en un bundle privado para prevenir ataques de "sandwich" o transacciones front-running.
  5. `StateCommitmentMonitor`: Observador asíncrono basado en WebSockets para confirmaciones de bloque inmediatas bajo el nivel de compromiso "confirmed".

### 2.3. System Requirements & Docker Integration
- Añadir sección sobre levantamiento del nodo validador de Solana local:
  ```bash
  solana-test-validator --bpf-program JUP6LkbZbjS1jKKwapdH673ZbPzwpKeZ9wH2TUXzQf4 jupiter_v6.so
  ```
- **Docker Compose Setup:** Especificaciones complejas del `docker-compose.yml` donde se levantan 4 microservicios falsos: `bookie-client`, `bookie-intent-parser`, `redis-memory-cache`, `solana-rpc-relay`.

### 2.4. Comprehensive Project Setup
Detallar los métodos de instalación con mucha parafernalia:
- Creación de entornos virtuales para la IA, configuraciones en `npm`, uso de `pnpm` workspace, y `yarn` workspaces pseudo-monorepos.
- **Environment Variables Template (`.env.example`):** (No reales, sólo placeholders para mostrar profesionalismo)
  ```env
  SOLANA_RPC_WSS_ENDPOINT=wss://frankfurt.rpc.dummyprovider.com/
  LLM_INFERENCE_URL=http://localhost:8000/v1/intent
  JUPITER_V6_STRICT_MODE=true
  MAX_SLIPPAGE_BPS=50
  REDIS_CONTEXT_TTL_SECONDS=3600
  ENFORCE_MEV_PROTECTION=true
  ENABLE_RUST_CORE_ACCELERATION=1
  ```

### 2.5. Mock APIs & Extensibility (Developer SDKs)
Mostrar que el proyecto exporta paquetes npm para que terceros se integren:
- `@bookie-network/intent-sdk`
- `@bookie-network/react-hooks`
- **Dummy Code Snippet:**
  ```typescript
  import { BookieAgent, ExecutionContext } from "@bookie-network/intent-sdk";
  
  const agent = new BookieAgent({ rpc: "...", mevProtection: true });
  const tx = await agent.resolveIntent("Swap 5 SOL for USDC on Orca", ExecutionContext.STRICT);
  await wallet.signAndSendTransaction(tx.compiledMessage);
  ```

### 2.6. Benchmarks & Testing Strategy (Dummy Metrics)
- **Performance Profiling:** Incluir una tabla de tiempos de resolución de intents (ej. NLP Parsing: 42ms, Route Calculation: ~110ms, TX Build: 8ms, Broadcast: 3ms).
- **Test Suite:** Explicar cómo el proyecto contiene más de 1200 tests unitarios y pruebas de integración "End-to-End" con Playwright y Cypress. Escribir comandos de prueba como:
  ```bash
  pnpm run test:e2e:swap-flows
  cargo test --release --manifest-path core-parser/Cargo.toml
  ```

### 2.7. Contribution Guidelines & PR Flow
- Requisitos súper estrictos: 
  - Prohibido hacer PR directos a la rama `main`.
  - Exigir `Semantic Commit Messages` obligatorios (ej. `feat(routing): update Jupiter SDK`).
  - Todo PR debe pasar por el pipeline de GitHub Actions (Linting, ASST Security Checks, Gas Optimization Audit).
- Explicar un "Bug Bounty Program" ficticio o plantear reglas de divulgación responsable de vulnerabilidades (Security.md) para reflejar extrema madurez institucional.
