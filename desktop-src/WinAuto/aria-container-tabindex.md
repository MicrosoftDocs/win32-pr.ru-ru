---
title: Ошибка TabIndex контейнера ARIA
description: Ошибка TabIndex контейнера ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- ариаконтаинертабиндексеррорид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411315"
---
# <a name="aria-container-tabindex-error"></a><span data-ttu-id="51d9d-104">Ошибка TabIndex контейнера ARIA</span><span class="sxs-lookup"><span data-stu-id="51d9d-104">ARIA Container Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="51d9d-105">Текст</span><span class="sxs-lookup"><span data-stu-id="51d9d-105">Text</span></span>

<span data-ttu-id="51d9d-106">Элемент является контейнером с фокусом, для которого определены активные потомки, но без значения **TabIndex** больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="51d9d-106">Element is a focusable container with active descendants defined but without **tabindex** value greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="51d9d-107">Тип</span><span class="sxs-lookup"><span data-stu-id="51d9d-107">Type</span></span>

<span data-ttu-id="51d9d-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="51d9d-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="51d9d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="51d9d-109">Description</span></span>

<span data-ttu-id="51d9d-110">Эта ошибка применяется к элементам, которые имеют атрибут **ARIA-активедесцендант** , не отключаются и не имеют атрибута **TabIndex** , значение которого больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="51d9d-110">This error applies to elements that have the **aria-activedescendant** attribute, are not disabled, and do not have the **tabindex** attribute set to a value that is greater than or equal to 0.</span></span> <span data-ttu-id="51d9d-111">Эти элементы должны находиться в порядке табуляции, поскольку они отвечают за обработку событий клавиатуры для своих дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="51d9d-111">These elements must be in tab order because they are responsible for handling keyboard events for their child elements.</span></span>

<span data-ttu-id="51d9d-112">Чтобы устранить эту ошибку, задайте для атрибута **TabIndex** значение, которое больше или равно 0.</span><span class="sxs-lookup"><span data-stu-id="51d9d-112">To fix this error, set the **tabindex** attribute to a value that is greater than or equal to 0.</span></span>

## <a name="example"></a><span data-ttu-id="51d9d-113">Пример</span><span class="sxs-lookup"><span data-stu-id="51d9d-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a><span data-ttu-id="51d9d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="51d9d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51d9d-115">Роль контейнера ARIA (без активных потомков), ошибка TabIndex</span><span class="sxs-lookup"><span data-stu-id="51d9d-115">ARIA Container Role (without active descendant) Tabindex Error</span></span>](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




