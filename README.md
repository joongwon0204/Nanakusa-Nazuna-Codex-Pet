# Nanakusa Nazuna Codex Pet

`Nanakusa Nazuna` is an unofficial animated pet for the Codex desktop app, inspired by Nazuna Nanakusa from *Call of the Night*.

## Animations

<table>
  <tr>
    <td align="center"><strong>Idle</strong><br><img src="previews/idle.gif" alt="Idle animation" width="160"></td>
    <td align="center"><strong>Run right</strong><br><img src="previews/running-right.gif" alt="Run-right animation" width="160"></td>
    <td align="center"><strong>Run left</strong><br><img src="previews/running-left.gif" alt="Run-left animation" width="160"></td>
  </tr>
  <tr>
    <td align="center"><strong>Waving</strong><br><img src="previews/waving.gif" alt="Waving animation" width="160"></td>
    <td align="center"><strong>Jumping</strong><br><img src="previews/jumping.gif" alt="Jumping animation" width="160"></td>
    <td align="center"><strong>Failed</strong><br><img src="previews/failed.gif" alt="Failed animation" width="160"></td>
  </tr>
  <tr>
    <td align="center"><strong>Waiting</strong><br><img src="previews/waiting.gif" alt="Waiting animation" width="160"></td>
    <td align="center"><strong>Running / working</strong><br><img src="previews/running.gif" alt="Working animation" width="160"></td>
    <td align="center"><strong>Review</strong><br><img src="previews/review.gif" alt="Review animation" width="160"></td>
  </tr>
</table>

## Installation

### macOS or Linux

Run the following commands in Terminal:

```bash
git clone https://github.com/joongwon0204/Nanakusa-Nazuna-Codex-Pet.git
cd Nanakusa-Nazuna-Codex-Pet

PET_DIR="${CODEX_HOME:-$HOME/.codex}/pets/nazuna-byte"
mkdir -p "$PET_DIR"
cp pet.json spritesheet.webp "$PET_DIR/"
```

### Windows PowerShell

Run the following commands in PowerShell:

```powershell
git clone https://github.com/joongwon0204/Nanakusa-Nazuna-Codex-Pet.git
Set-Location Nanakusa-Nazuna-Codex-Pet

$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $env:USERPROFILE ".codex" }
$petDir = Join-Path $codexHome "pets\nazuna-byte"
New-Item -ItemType Directory -Force -Path $petDir | Out-Null
Copy-Item .\pet.json, .\spritesheet.webp -Destination $petDir -Force
```

The installed directory should contain exactly these two required files:

```text
.codex/
└── pets/
    └── nazuna-byte/
        ├── pet.json
        └── spritesheet.webp
```

`README.md`, `SHA256SUMS`, and the `previews` directory are not required by Codex.

## Usage

1. Restart the Codex desktop app after installation.
2. Open the pet selector and choose **Nanakusa Nazuna**.
3. If the previous name or artwork is still cached, select another pet once and then select **Nanakusa Nazuna** again.

## Updating

Pull the latest repository version, then repeat the copy step for your operating system:

```bash
git pull
PET_DIR="${CODEX_HOME:-$HOME/.codex}/pets/nazuna-byte"
cp pet.json spritesheet.webp "$PET_DIR/"
```

On Windows PowerShell:

```powershell
git pull
$codexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $env:USERPROFILE ".codex" }
$petDir = Join-Path $codexHome "pets\nazuna-byte"
Copy-Item .\pet.json, .\spritesheet.webp -Destination $petDir -Force
```

Restart Codex after updating so it reloads the package.

## Package details

- Pet ID: `nazuna-byte`
- Display name: `Nanakusa Nazuna`
- Sprite contract: Codex v2 (`spriteVersionNumber: 2`)
- Atlas: `1536×2288` WebP, `8×11` cells
- SHA-256: `eef0d4710746c6665bf2525dc37a9e9196dff16592cd86fe54fc6dbfee81ac83`

To verify the downloaded spritesheet:

```bash
shasum -a 256 -c SHA256SUMS
```

## Notice

This is unofficial fan-made artwork for personal use. The original character and related rights belong to their respective rights holders. This project is not affiliated with or endorsed by them.
