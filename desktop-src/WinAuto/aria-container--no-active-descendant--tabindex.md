---
title: Роль контейнера ARIA (без активных потомков), ошибка TabIndex
description: Роль контейнера ARIA (без активных потомков), ошибка TabIndex
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- ариаконтаинервисаутактиведесценданттабиндексеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253307"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Роль контейнера ARIA (без активных потомков), ошибка TabIndex

## <a name="text"></a>Текст

Элемент является контейнером с фокусом без определенного активного потомка, но ни один дочерний элемент не имеет значения **TabIndex** больше или равен 0.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, которые имеют роль контейнера, не имеют атрибута **ARIA-активедесцендант** и не отключаются. Эти элементы реализуют навигацию с помощью клавиатуры между дочерними элементами с использованием концепции, известной как "параллельный *индекс*". В этой концепции атрибуты **TabIndex** дочерних элементов поддерживаются динамически, гарантируя, что в любой момент только один дочерний элемент находится в последовательности табуляции.

Чтобы устранить эту ошибку, задайте для атрибута **TabIndex** одного из дочерних элементов значение, равное или больше 0.

## <a name="example"></a>Пример


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Ошибка TabIndex контейнера ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




