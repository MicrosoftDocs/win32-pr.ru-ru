---
description: Элемент at определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего параметр.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Элемент at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909832"
---
# <a name="at-element"></a><span data-ttu-id="c632d-103">Элемент at</span><span class="sxs-lookup"><span data-stu-id="c632d-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="c632d-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c632d-104">\[Deprecated.</span></span> <span data-ttu-id="c632d-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c632d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c632d-106">`at`Элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего параметр.</span><span class="sxs-lookup"><span data-stu-id="c632d-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="c632d-107">`at`Элемент приводит к резкому переходу параметра к новому значению в заданный момент времени.</span><span class="sxs-lookup"><span data-stu-id="c632d-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="c632d-108">Для плавного продвижения нового значения используйте [**линейный**](linear-element.md) элемент.</span><span class="sxs-lookup"><span data-stu-id="c632d-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="c632d-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c632d-109">Attributes</span></span>

<span data-ttu-id="c632d-110">[**время**](time-attribute.md), [ **значение**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="c632d-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="c632d-111">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="c632d-111">Parent/Child Information</span></span>



| <span data-ttu-id="c632d-112">Метка</span><span class="sxs-lookup"><span data-stu-id="c632d-112">Label</span></span> | <span data-ttu-id="c632d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c632d-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="c632d-114">Parent</span><span class="sxs-lookup"><span data-stu-id="c632d-114">Parent</span></span>   | [<span data-ttu-id="c632d-115">**param**</span><span class="sxs-lookup"><span data-stu-id="c632d-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="c632d-116">Дети</span><span class="sxs-lookup"><span data-stu-id="c632d-116">Children</span></span> | <span data-ttu-id="c632d-117">None</span><span class="sxs-lookup"><span data-stu-id="c632d-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="c632d-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="c632d-118">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="c632d-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c632d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c632d-120">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="c632d-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



