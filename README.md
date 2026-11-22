# 📁 Photos Player para Windows Explorer

Transforme **qualquer pasta de fotos** em um álbum navegável com **2 imagens por tela**, direto pelo botão direito do mouse.

> Gratuito · portátil · sem instalar Python, PHP ou runtime · sem precisar de administrador

---

## ✨ O que ele faz

- Adiciona a opção **Abrir no Photos Player** no menu de contexto do Windows Explorer
- Gera um `Album.html` dentro da própria pasta, com as fotos dessa pasta
- Abre o álbum automaticamente no navegador
- Mostra o **nome da pasta** na faixa amarela
- Navegação: `←` / `→`, `Home` / `End`, clique nos lados da tela e botões
- Contador `1-2 / N`, barra de progresso e cartão **FIM** com crédito
- Ordenação natural: `1, 2, 3 ... 10, 11`
- Funciona com PNG, JPG, JPEG, WEBP, GIF e BMP

---

## 🚀 Instalação em 10 segundos

### Opção 1 — um arquivo só (recomendada)

1. Baixe **`Instalar_PhotosPlayer.bat`**
2. Dê duplo clique
3. Responda **S** para reiniciar o Explorer

Pronto. Não precisa de administrador nem de internet.

### Quer testar antes? (recomendado)

Baixe o **`PhotosPlayer-Demo-10-Fotos.zip`** (0,7 MB): são 10 fotos públicas + o `Album-Unico.bat`. Extraia, dê duplo clique no `.bat` e veja o álbum abrir **sem instalar nada**.

### Opção 2 — pacote com os arquivos separados

1. Baixe **`PhotosPlayer-Pacote.zip`**
2. Extraia em qualquer pasta
3. Execute **`Instalar_Menu.bat`**

Os arquivos ficam em `%LOCALAPPDATA%\PhotosPlayer`. Para remover, execute **`Desinstalar_Menu.bat`**.

---

## 🖱️ Como usar

1. Abra o Windows Explorer
2. Clique com o botão direito em uma pasta com fotos
3. Escolha **Mais opções → Abrir no Photos Player**

> **Windows 11:** a opção fica em **Mostrar mais opções** no fim do menu (ou `Shift+F10`). Se ainda não aparecer, habilite-a nas configurações do menu de contexto do sistema ou rode `Reiniciar_Explorer.bat`.

Se você adicionar/remover fotos ou renomear a pasta, rode o menu novamente para atualizar o álbum.

---

## 🧠 Como funciona

O instalador registra um verbo no `HKCU\Software\Classes\Directory\shell` (por usuário, sem admin). Ao clicar, um pequeno script PowerShell:

1. lê o nome da pasta;
2. lista as imagens em ordem natural;
3. preenche um modelo HTML (`var NOME`, `var FOTOS`);
4. grava `Album.html` na pasta e abre no navegador.

As fotos **não são enviadas para lugar nenhum** — tudo acontece localmente.

---

## 📦 Arquivos

| Arquivo | Função |
|---|---|
| `Instalar_PhotosPlayer.bat` | Instalador portátil (contém tudo embutido) |
| `PhotosPlayer-Pacote.zip` | Arquivos separados |
| `PhotosPlayer-Demo-10-Fotos.zip` | Demonstração com 10 fotos públicas (teste sem instalar) |
| `Abrir_Photos_Player.cmd` | Executado pelo menu do Explorer |
| `gerar_album.ps1` | Gerador do álbum |
| `Instalar_Menu.bat` / `.ps1` | Registro do menu |
| `Desinstalar_Menu.bat` | Remoção do menu |
| `Reiniciar_Explorer.bat` | Atualiza o Explorer |

---

## 🔒 Privacidade

Nenhum dado é coletado. O álbum é gerado apenas com os arquivos da pasta escolhida e roda localmente no navegador.

---

## 📄 Licença

Distribuído sob a licença MIT. Veja `LICENSE`.

---

## 🙌 Créditos

```
Produzido por:
OpenCode V: 2.3.2 e Pepeh
```

---

## ⭐ Gostou?

Deixe uma estrela no repositório e compartilhe com quem trabalha com muitas fotos no Windows!

> Sugestões no Leave a Reply -> Comment *  do  blog:
> https://pepeh.com.br/index.php/2026/11/21/photos-player-sua-pasta-de-fotos-vira-um-album-profissional-em-2-cliques/
