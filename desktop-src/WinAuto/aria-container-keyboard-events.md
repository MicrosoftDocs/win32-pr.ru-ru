---
title: Ошибка специальных возможностей клавиатуры для роли контейнера ARIA
description: Ошибка специальных возможностей клавиатуры для роли контейнера ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- ариаконтаинеркэйбоардакцессибилитеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330944"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a><span data-ttu-id="0884f-104">Ошибка специальных возможностей клавиатуры для роли контейнера ARIA</span><span class="sxs-lookup"><span data-stu-id="0884f-104">ARIA Container Role Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="0884f-105">Текст</span><span class="sxs-lookup"><span data-stu-id="0884f-105">Text</span></span>

<span data-ttu-id="0884f-106">— Это контейнер с активной функцией-потомком и настраиваемой функциональностью мыши, но без соответствующей функциональности клавиатуры: обработчики событий JavaScript для функции **OnKeyDown** или **OnKeyDown**.</span><span class="sxs-lookup"><span data-stu-id="0884f-106">Element is a container with active descendant and custom mouse functionality but without the corresponding keyboard functionality: JavaScript event handlers for **OnKeyDown** or **OnKeyPress**.</span></span>

## <a name="type"></a><span data-ttu-id="0884f-107">Тип</span><span class="sxs-lookup"><span data-stu-id="0884f-107">Type</span></span>

<span data-ttu-id="0884f-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="0884f-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="0884f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0884f-109">Description</span></span>

<span data-ttu-id="0884f-110">Эта ошибка применяется к элементам, имеющим атрибут **ARIA-активедесцендант** .</span><span class="sxs-lookup"><span data-stu-id="0884f-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span> <span data-ttu-id="0884f-111">Эти элементы имеют один или несколько обработчиков событий мыши (**MouseMove**, **MouseDown** или **MouseUp**), но в них отсутствуют эквивалентные обработчики событий клавиатуры (**KeyDown**, **KeyUp** или **KeyPress**).</span><span class="sxs-lookup"><span data-stu-id="0884f-111">These elements have one or more mouse event handlers (**mousemove**, **mousedown** or **mouseup**), but are missing the equivalent keyboard event handlers (**keydown**, **keyup** or **keypress**).</span></span> <span data-ttu-id="0884f-112">Обработчики событий клавиатуры необходимы для того, чтобы пользователь мог вызвать функциональность элемента с помощью клавиатуры, а также убедиться, что элемент поддерживает атрибут **ARIA-активедесцендант** .</span><span class="sxs-lookup"><span data-stu-id="0884f-112">The keyboard event handlers are needed to ensure that the user can invoke the element's functionality by using the keyboard, and to ensure that the element maintains the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="0884f-113">Чтобы устранить эту ошибку, реализуйте один из обработчиков событий клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="0884f-113">To fix this error, implement one of the keyboard event handlers.</span></span>

## <a name="example"></a><span data-ttu-id="0884f-114">Пример</span><span class="sxs-lookup"><span data-stu-id="0884f-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0884f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0884f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0884f-116">Роль контейнера ARIA (без активной дочерней области) ошибка доступа к клавиатуре</span><span class="sxs-lookup"><span data-stu-id="0884f-116">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




