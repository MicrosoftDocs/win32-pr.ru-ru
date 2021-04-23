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
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a><span data-ttu-id="aa036-104">Роль контейнера ARIA (без активной дочерней области) ошибка доступа к клавиатуре</span><span class="sxs-lookup"><span data-stu-id="aa036-104">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="aa036-105">Текст</span><span class="sxs-lookup"><span data-stu-id="aa036-105">Text</span></span>

<span data-ttu-id="aa036-106">Элемент является контейнером с фокусом без определения активного потомка **и без** / обработчиков событий **OnKeyDown** / **онкэйуп** (ни для контейнера, ни для одного из дочерних элементов).</span><span class="sxs-lookup"><span data-stu-id="aa036-106">Element is a focusable container without active descendant defined and without **OnKeyDown**/**OnKeyPress**/**OnKeyUp** event handlers (neither on container nor on one of child elements).</span></span>

## <a name="type"></a><span data-ttu-id="aa036-107">Тип</span><span class="sxs-lookup"><span data-stu-id="aa036-107">Type</span></span>

<span data-ttu-id="aa036-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="aa036-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="aa036-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aa036-109">Description</span></span>

<span data-ttu-id="aa036-110">Эта ошибка применяется к элементам, которые имеют роль контейнера, не имеют атрибута **ARIA-активедесцендант** и не отключаются.</span><span class="sxs-lookup"><span data-stu-id="aa036-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="aa036-111">Эти элементы реализуют навигацию с помощью клавиатуры между дочерними элементами с использованием концепции, известной как "параллельный *индекс*".</span><span class="sxs-lookup"><span data-stu-id="aa036-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="aa036-112">В этой концепции атрибуты **TabIndex** дочерних элементов поддерживаются динамически, гарантируя, что в любой момент только один дочерний элемент находится в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="aa036-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="aa036-113">Эта ошибка означает, что элемент контейнера, не имеющий атрибута **ARIA-активедесцендант** и не отключенный, недоступен для пользователей с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="aa036-113">This error indicates that a container element that does not have the **aria-activedescendant** attribute, and that is not disabled, is not accessible to keyboard users.</span></span> <span data-ttu-id="aa036-114">Проблема существует, потому что контейнер не имеет необходимых обработчиков событий клавиатуры (**KeyDown**, **KeyUp** или **KeyPress**) и ни один из дочерних элементов контейнера не имеет.</span><span class="sxs-lookup"><span data-stu-id="aa036-114">The problem exists because the container does not have the needed keyboard event handlers (**keydown**, **keyup**, or **keypress**), and neither do any of the container's child elements.</span></span>

<span data-ttu-id="aa036-115">Чтобы устранить эту ошибку, определите обработчик событий **KeyDown**, **KeyUp** или **KeyPress** для контейнера или одного из его дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="aa036-115">To fix this error, define a **keydown**, **keyup**, or **keypress** event handler for the container or one of its child elements.</span></span>

## <a name="example"></a><span data-ttu-id="aa036-116">Пример</span><span class="sxs-lookup"><span data-stu-id="aa036-116">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aa036-117">См. также</span><span class="sxs-lookup"><span data-stu-id="aa036-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa036-118">Ошибка специальных возможностей клавиатуры для роли контейнера ARIA</span><span class="sxs-lookup"><span data-stu-id="aa036-118">ARIA Container Role Keyboard Accessibility Error</span></span>](aria-container-keyboard-events.md)
</dt> </dl>

 

 




