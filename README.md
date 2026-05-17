# Curso iAmasters OS

Curso completo sobre o sistema operativo agêntico **iAmasters OS** — formato INEMA.CLUB, em português.

## Estrutura

- **Landing** (`index.html`)
- **Trilha 1 — Fundamentos** (Emerald · 3 módulos · ~2h30)
- **Trilha 2 — Skills Curadas** (Blue · 3 módulos · ~3h)
- **Trilha 3 — Operação** (Purple · 3 módulos · ~2h30)

Total: **9 módulos · 54 tópicos · ~8h**

## Publicar com GitHub Pages

### 1. Criar repo no teu GitHub

```bash
cd /home/nmaldaner/projetos/curso-iamasters-os
git init
git add .
git commit -m "feat: initial course content"
gh repo create curso-iamasters-os --public --source=. --push
```

### 2. Ativar GitHub Pages

```bash
gh repo edit --enable-pages
```

Ou via web:
1. Vai a `https://github.com/<teu-user>/curso-iamasters-os/settings/pages`
2. **Source**: GitHub Actions
3. O workflow `.github/workflows/deploy.yml` já está configurado.

### 3. Aceder ao site

Após o primeiro push o site está em:
```
https://<teu-user>.github.io/curso-iamasters-os/
```

O deploy demora ~1-2 min. Estado em `Actions` no GitHub.

## Atualizar conteúdo

Qualquer push para `main` re-deploya automaticamente.

```bash
# Editar conteúdo
git add .
git commit -m "docs: update module 1.2"
git push
# ↓ Workflow corre automaticamente
# ↓ Site atualizado em ~90s
```

## Desenvolvimento local

Não precisa de build. Abre `index.html` no browser:

```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Ou servidor simples
python3 -m http.server 8000
# → http://localhost:8000
```

## Formato

Seguindo padrão **INEMA.CLUB**:
- Tailwind CDN, sem build
- Dark/light mode toggle
- 3 secções por tópico (O que é / Por que aprender / Conceitos-chave)
- Navegação rápida em cada trilha
- Modal + página completa por módulo

## Repo do sistema

Versão PT-PT do iAmasters OS (a que este curso ensina): [inematds/iamasters-os](https://github.com/inematds/iamasters-os).

Curso por [INEMA.CLUB](https://inema.club).

Licença: MIT.
