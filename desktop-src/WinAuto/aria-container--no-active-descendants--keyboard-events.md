---
title: Роль контейнера ARIA (без активной дочерней области) ошибка доступа к клавиатуре
description: Роль контейнера ARIA (без активной дочерней области) ошибка доступа к клавиатуре
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- ариаконтаинервисаутактиведесценданткэйбоардакцессиблитид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888355"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Роль контейнера ARIA (без активной дочерней области) ошибка доступа к клавиатуре

## <a name="text"></a>Текст

Элемент является контейнером с фокусом без определения активного потомка **и без** / обработчиков событий **OnKeyDown** / **онкэйуп** (ни для контейнера, ни для одного из дочерних элементов).

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, которые имеют роль контейнера, не имеют атрибута **ARIA-активедесцендант** и не отключаются. Эти элементы реализуют навигацию с помощью клавиатуры между дочерними элементами с использованием концепции, известной как "параллельный *индекс*". В этой концепции атрибуты **TabIndex** дочерних элементов поддерживаются динамически, гарантируя, что в любой момент только один дочерний элемент находится в последовательности табуляции.

Эта ошибка означает, что элемент контейнера, не имеющий атрибута **ARIA-активедесцендант** и не отключенный, недоступен для пользователей с клавиатуры. Проблема существует, потому что контейнер не имеет необходимых обработчиков событий клавиатуры (**KeyDown**, **KeyUp** или **KeyPress**) и ни один из дочерних элементов контейнера не имеет.

Чтобы устранить эту ошибку, определите обработчик событий **KeyDown**, **KeyUp** или **KeyPress** для контейнера или одного из его дочерних элементов.

## <a name="example"></a>Пример


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Ошибка специальных возможностей клавиатуры для роли контейнера ARIA](aria-container-keyboard-events.md)
</dt> </dl>

 

 




