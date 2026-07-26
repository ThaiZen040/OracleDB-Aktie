# Oracle-Aktienanalyse

Dieses Projekt analysiert die Oracle-Aktie (`ORCL`) für den Zeitraum von 2020
bis 2024. Das Jupyter-Notebook lädt Kurs- und Dividendendaten über Yahoo
Finance, berechnet Rendite- und Risikokennzahlen und erstellt verschiedene
Diagramme.

## Projekt starten

### 1. Voraussetzungen

Für die Ausführung werden benötigt:

- Python 3
- eine Internetverbindung für den Abruf der Börsendaten
- Git (optional, zum Klonen des Repositorys)

### 2. Repository herunterladen

Das Repository kann mit Git geklont werden:

```bash
git clone https://github.com/ThaiZen040/OracleDB-Aktie.git
cd OracleDB-Aktie
```

Alternativ kann das Projekt auf GitHub als ZIP-Datei heruntergeladen und
anschließend entpackt werden.

### 3. Virtuelle Umgebung erstellen

Es wird empfohlen, die benötigten Pakete in einer virtuellen Python-Umgebung
zu installieren.

macOS und Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows PowerShell:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 4. Abhängigkeiten installieren

macOS und Linux:

```bash
python3 -m pip install --upgrade pip
python3 -m pip install jupyter numpy pandas yfinance matplotlib
```

Windows:

```powershell
py -m pip install --upgrade pip
py -m pip install jupyter numpy pandas yfinance matplotlib
```

### 5. Notebook öffnen

macOS und Linux:

```bash
jupyter notebook oracledb.ipynb
```

Windows:

```powershell
jupyter notebook oracledb.ipynb
```

Daraufhin öffnet sich Jupyter im Browser. Dort im Menü
**Kernel → Restart & Run All** auswählen, um die gesamte Analyse auszuführen.

Alternativ lässt sich das Notebook mit JupyterLab starten:

```bash
jupyter lab oracledb.ipynb
```

Das Notebook kann auch direkt in einer Entwicklungsumgebung mit
Jupyter-Unterstützung, beispielsweise Visual Studio Code oder PyCharm,
geöffnet und ausgeführt werden.

## Verwendete Bibliotheken

| Bibliothek | Verwendung |
|---|---|
| `numpy` | Mathematische Berechnungen |
| `pandas` | Verarbeitung und Auswertung der Kursdaten |
| `yfinance` | Abruf der Kurs- und Dividendendaten |
| `matplotlib` | Erstellung der Diagramme |
| `jupyter` | Ausführung des Notebooks |

## Inhalt des Projekts

```text
OracleDB-Aktie/
├── oracledb.ipynb   # Vollständige Aktienanalyse
└── README.md        # Installation und Startanleitung
```

Das Notebook untersucht unter anderem:

- den Kursverlauf mit gleitenden Durchschnitten,
- tägliche, jährliche und kumulative Renditen,
- Volatilität und maximalen Drawdown,
- die Sharpe Ratio,
- die Verteilung der täglichen Renditen sowie
- Dividenden und Dividendenrenditen.

Beim Ausführen werden die aktuellen historischen Daten von Yahoo Finance
abgerufen. Die berechneten Werte können sich daher von den bereits im Notebook
gespeicherten Ausgaben unterscheiden.

## Konfiguration anpassen

Die wichtigsten Einstellungen befinden sich am Anfang von `oracledb.ipynb` in
der Klasse `Config`:

```python
TICKER = "ORCL"
START = "2020-01-01"
END = "2024-12-31"
RISK_FREE_RATE = 0.04
TRADING_DAYS = 252
```

Über diese Werte können beispielsweise ein anderes Unternehmen, ein anderer
Analysezeitraum oder ein anderer risikofreier Zinssatz gewählt werden.

## Hinweise

- Zum Laden der Börsendaten muss während der Ausführung eine
  Internetverbindung bestehen.
- Die erzeugten Diagramme werden im Projektordner als PNG-Dateien gespeichert.
- Die Analyse dient ausschließlich Lehr- und Demonstrationszwecken und stellt
  keine Anlageberatung dar.
