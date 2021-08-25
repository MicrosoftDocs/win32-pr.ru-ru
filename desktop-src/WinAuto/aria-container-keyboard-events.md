---
title: Ошибка специальных возможностей клавиатуры для роли контейнера ARIA
description: Ошибка специальных возможностей клавиатуры для роли контейнера ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- ариаконтаинеркэйбоардакцессибилитеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591098ba6e38836f1f39d13e72495bc1d7a3d5f9fe088873661e3dd3a7e65d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122404"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>Ошибка специальных возможностей клавиатуры для роли контейнера ARIA

## <a name="text"></a>Текст

— Это контейнер с активной функцией-потомком и настраиваемой функциональностью мыши, но без соответствующей функциональности клавиатуры: обработчики событий JavaScript для функции **OnKeyDown** или **OnKeyDown**.

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Эта ошибка применяется к элементам, имеющим атрибут **ARIA-активедесцендант** . Эти элементы имеют один или несколько обработчиков событий мыши (**MouseMove**, **MouseDown** или **MouseUp**), но в них отсутствуют эквивалентные обработчики событий клавиатуры (**KeyDown**, **KeyUp** или **KeyPress**). Обработчики событий клавиатуры необходимы для того, чтобы пользователь мог вызвать функциональность элемента с помощью клавиатуры, а также убедиться, что элемент поддерживает атрибут **ARIA-активедесцендант** .

Чтобы устранить эту ошибку, реализуйте один из обработчиков событий клавиатуры.

## <a name="example"></a>Пример


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Роль контейнера ARIA (без активной дочерней области) ошибка доступа к клавиатуре](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




