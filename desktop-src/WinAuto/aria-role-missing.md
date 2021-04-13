---
title: Ошибка роли ARIA для элементов с обработчиками событий
description: Ошибка роли ARIA для элементов с обработчиками событий
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- ариаконтаинерролиррормессаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104414013"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a><span data-ttu-id="198ec-104">Ошибка роли ARIA для элементов с обработчиками событий</span><span class="sxs-lookup"><span data-stu-id="198ec-104">ARIA Role Error for elements with event handlers</span></span>

## <a name="text"></a><span data-ttu-id="198ec-105">Текст</span><span class="sxs-lookup"><span data-stu-id="198ec-105">Text</span></span>

<span data-ttu-id="198ec-106">Элемент имеет обработчик событий, но допустимая роль ожидать-ARIA не определена.</span><span class="sxs-lookup"><span data-stu-id="198ec-106">Element has an event handler but valid WAI-ARIA role is not defined.</span></span>

## <a name="type"></a><span data-ttu-id="198ec-107">Тип</span><span class="sxs-lookup"><span data-stu-id="198ec-107">Type</span></span>

<span data-ttu-id="198ec-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="198ec-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="198ec-109">Описание</span><span class="sxs-lookup"><span data-stu-id="198ec-109">Description</span></span>

<span data-ttu-id="198ec-110">Эта ошибка относится к элементам, у которых нет неявной роли веб-приложений с широкими возможностями доступа к Интернету (ожидать-ARIA).</span><span class="sxs-lookup"><span data-stu-id="198ec-110">This error applies to elements that do not have an implicit Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role.</span></span>

<span data-ttu-id="198ec-111">Эта ошибка означает, что элемент имеет обработчик событий мыши или клавиатуры (щелчок, кнопка " **вниз\*\*\*\*", "** **MouseUp**", " **Перемещение**", " **указатель мыши** **", "** **KeyUp**", " **вниз**" или " **Нажатие клавиши**"), но не имеет атрибута [**роли**](https://developer.mozilla.org/docs/Web/HTML/Reference) и не является одним из тегов HTML с неявной ролью ожидать-Aria ( **например,** **кнопка**, **img**, **input**, **SELECT** и т</span><span class="sxs-lookup"><span data-stu-id="198ec-111">This error indicates that an element has a mouse or keyboard event handler (**click**, **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown**, or **keypress**), but doesn’t have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set, and is not one of the HTML tags that has an implicit WAI-ARIA role (for example, **a**, **button**, **img**, **input**, **select** and so on).</span></span>

<span data-ttu-id="198ec-112">Задание атрибута [**роли**](https://developer.mozilla.org/docs/Web/HTML/Reference) для интерактивных элементов, не имеющих неявной роли (например, тега **div** ), необходимо для предоставления шаблонов поведения элемента средствам чтения с экрана и другим вспомогательным технологиям.</span><span class="sxs-lookup"><span data-stu-id="198ec-112">Setting the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute for interactive elements that have no implicit role (such as a **div** tag) is necessary to expose the element's behavior patterns to screen readers and other assistive technologies.</span></span>

<span data-ttu-id="198ec-113">Чтобы устранить эту ошибку, присвойте атрибуту [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) допустимую роль ожидать-ARIA, которая лучше подходит для шаблонов поведения этого элемента и необходимых атрибутов.</span><span class="sxs-lookup"><span data-stu-id="198ec-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role that best fits this element's behavior patterns and required attributes.</span></span> <span data-ttu-id="198ec-114">Например, если тег **div** выступает в качестве кнопки, задайте для атрибута role значение "Button".</span><span class="sxs-lookup"><span data-stu-id="198ec-114">For example, if a **div** tag functions as a button, set the role attribute to "button".</span></span>

## <a name="example"></a><span data-ttu-id="198ec-115">Пример</span><span class="sxs-lookup"><span data-stu-id="198ec-115">Example</span></span>


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




