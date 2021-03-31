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
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a><span data-ttu-id="abca0-104">Роль контейнера ARIA (без активных потомков), ошибка TabIndex</span><span class="sxs-lookup"><span data-stu-id="abca0-104">ARIA Container Role (without active descendant) Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="abca0-105">Текст</span><span class="sxs-lookup"><span data-stu-id="abca0-105">Text</span></span>

<span data-ttu-id="abca0-106">Элемент является контейнером с фокусом без определенного активного потомка, но ни один дочерний элемент не имеет значения **TabIndex** больше или равен 0.</span><span class="sxs-lookup"><span data-stu-id="abca0-106">Element is a focusable container without active descendant defined, but no child element has **tabindex** greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="abca0-107">Тип</span><span class="sxs-lookup"><span data-stu-id="abca0-107">Type</span></span>

<span data-ttu-id="abca0-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="abca0-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="abca0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="abca0-109">Description</span></span>

<span data-ttu-id="abca0-110">Эта ошибка применяется к элементам, которые имеют роль контейнера, не имеют атрибута **ARIA-активедесцендант** и не отключаются.</span><span class="sxs-lookup"><span data-stu-id="abca0-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="abca0-111">Эти элементы реализуют навигацию с помощью клавиатуры между дочерними элементами с использованием концепции, известной как "параллельный *индекс*".</span><span class="sxs-lookup"><span data-stu-id="abca0-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="abca0-112">В этой концепции атрибуты **TabIndex** дочерних элементов поддерживаются динамически, гарантируя, что в любой момент только один дочерний элемент находится в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="abca0-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="abca0-113">Чтобы устранить эту ошибку, задайте для атрибута **TabIndex** одного из дочерних элементов значение, равное или больше 0.</span><span class="sxs-lookup"><span data-stu-id="abca0-113">To fix this error, set the **tabindex** attribute of one of the child elements to a value equal to or greater than 0.</span></span>

## <a name="example"></a><span data-ttu-id="abca0-114">Пример</span><span class="sxs-lookup"><span data-stu-id="abca0-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="abca0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="abca0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abca0-116">Ошибка TabIndex контейнера ARIA</span><span class="sxs-lookup"><span data-stu-id="abca0-116">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
</dt> </dl>

 

 




