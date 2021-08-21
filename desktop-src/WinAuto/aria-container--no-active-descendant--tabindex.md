---
title: Роль контейнера ARIA (без активных потомков), ошибка TabIndex
description: Роль контейнера ARIA (без активных потомков), ошибка TabIndex
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- ариаконтаинервисаутактиведесценданттабиндексеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6eb2198b5ad28cf8a2dd1c625342fef399eefbe3f93ed5e09f4796e06d16338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994344"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Роль контейнера ARIA (без активных потомков), ошибка TabIndex

## <a name="text"></a>Текст

Элемент является контейнером с фокусом без определенного активного потомка, но ни один дочерний элемент не имеет значения **TabIndex** больше или равен 0.

## <a name="type"></a>Тип

Error

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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ошибка TabIndex контейнера ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




