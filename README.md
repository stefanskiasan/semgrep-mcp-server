# Semgrep Server

[![smithery badge](https://smithery.ai/badge/@stefanskiasan/semgrep-mcp-server)](https://smithery.ai/server/@stefanskiasan/semgrep-mcp-server)

Ein Model Context Protocol (MCP) Server für die Integration von Semgrep in die Entwicklungsumgebung. Dieser Server ermöglicht die Durchführung von statischen Code-Analysen und die Verwaltung von Semgrep-Regeln direkt über das MCP-Protokoll.

## Installation

### Installing via Smithery

To install Semgrep Server for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@stefanskiasan/semgrep-mcp-server):

```bash
npx -y @smithery/cli install @stefanskiasan/semgrep-mcp-server --client claude
```

### Manual Installation
```bash
# Repository klonen
git clone [repository-url]
cd semgrep-server

# Abhängigkeiten installieren
npm install

# Server bauen
npm run build
```

## Verwendung

Der Server kann auf folgende Weise gestartet werden:

```bash
# Produktionsmodus
npm start

# Entwicklungsmodus
npm run dev
```

## Verfügbare Tools

Der Server stellt folgende MCP-Tools zur Verfügung:

- `scan_directory`: Führt einen Semgrep-Scan in einem Verzeichnis aus
- `list_rules`: Listet verfügbare Semgrep-Regeln auf
- `analyze_results`: Analysiert die Scan-Ergebnisse
- `create_rule`: Erstellt eine neue Semgrep-Regel
- `filter_results`: Filtert Scan-Ergebnisse nach verschiedenen Kriterien
- `export_results`: Exportiert Scan-Ergebnisse in verschiedene Formate
- `compare_results`: Vergleicht zwei Scan-Ergebnisse

## Entwicklung

Das Projekt ist in TypeScript geschrieben und verwendet das MCP SDK für die Server-Implementierung. 

### Projektstruktur

```
semgrep-server/
├── src/           # Quellcode
├── build/         # Kompilierte JavaScript-Dateien
├── test.js        # Testdateien
└── test-rule.yaml # Beispiel Semgrep-Regel
```

### Abhängigkeiten

- Node.js & npm
- TypeScript
- MCP SDK
- Axios für HTTP-Anfragen

## Lizenz

Dieses Projekt steht unter der ISC-Lizenz. Weitere Details finden Sie in der [LICENSE](LICENSE) Datei.
