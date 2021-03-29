---
description: Элемент at определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего параметр.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Элемент at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806598"
---
# <a name="at-element"></a><span data-ttu-id="32283-103">Элемент at</span><span class="sxs-lookup"><span data-stu-id="32283-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="32283-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="32283-104">\[Deprecated.</span></span> <span data-ttu-id="32283-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="32283-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="32283-106">`at`Элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего параметр.</span><span class="sxs-lookup"><span data-stu-id="32283-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="32283-107">`at`Элемент приводит к резкому переходу параметра к новому значению в заданный момент времени.</span><span class="sxs-lookup"><span data-stu-id="32283-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="32283-108">Для плавного продвижения нового значения используйте [**линейный**](linear-element.md) элемент.</span><span class="sxs-lookup"><span data-stu-id="32283-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="32283-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="32283-109">Attributes</span></span>

<span data-ttu-id="32283-110">[**время**](time-attribute.md), [ **значение**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="32283-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="32283-111">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="32283-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="32283-112">Parent</span><span class="sxs-lookup"><span data-stu-id="32283-112">Parent</span></span>   | [<span data-ttu-id="32283-113">**байт**</span><span class="sxs-lookup"><span data-stu-id="32283-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="32283-114">Дети</span><span class="sxs-lookup"><span data-stu-id="32283-114">Children</span></span> | <span data-ttu-id="32283-115">None</span><span class="sxs-lookup"><span data-stu-id="32283-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="32283-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="32283-116">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="32283-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32283-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32283-118">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="32283-118">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



