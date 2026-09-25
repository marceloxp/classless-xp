# classless-xp

Temas CSS drop-in para HTML semântico. Sem classes no conteúdo.

O `index.html` é o kitchen sink compartilhado. O picker troca o `<link>` (`?theme=xp-001`).

## Uso

```html
<link rel="stylesheet" href="./xp-001/style.css">
```

## Contrato

O tema estiliza tags e aninhamento. Se o visual pede classe ou `style` inline, o padrão quebrou.

| Markup | Resultado |
|---|---|
| `small` imediatamente antes de `h1`/`h2`/`h3` | Eyebrow |
| `nav ul` | Menu horizontal |
| `section` com `article` filhos diretos | Grid de cartões; os outros filhos ocupam a linha inteira |
| `section` sem `article` | Bloco normal |
| `aside` | Nota / callout |
| `table`, `form`, `figure`, `details`, `pre`, … | Elementos padrão do tema |

Ênfase via tags (`strong`, `mark`, `em`, `ins`, `del`). Nada de pintar célula por coluna.

## Temas

Cada pasta `xp-NNN/style.css` é um experimento. Para publicar um novo:

1. Criar `xp-NNN/style.css` honrando o contrato (e o sink).
2. Registrar `{ id, label }` em `THEMES` no `index.html`.
