---
description: Линейный элемент определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего элемент param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: линейный элемент (Камерауиконтрол. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910092"
---
# <a name="linear-element"></a><span data-ttu-id="e45b0-103">линейный элемент</span><span class="sxs-lookup"><span data-stu-id="e45b0-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="e45b0-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e45b0-104">\[Deprecated.</span></span> <span data-ttu-id="e45b0-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e45b0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e45b0-106">Линейный элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего элемент **param** .</span><span class="sxs-lookup"><span data-stu-id="e45b0-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="e45b0-107">`linear`Элемент заставляет параметр выполнить плавный переход из предыдущего значения к новому значению.</span><span class="sxs-lookup"><span data-stu-id="e45b0-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="e45b0-108">Для мгновенного перехода к новому значению используйте элемент [**at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e45b0-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="e45b0-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e45b0-109">Attributes</span></span>

<span data-ttu-id="e45b0-110">[**время**](time-attribute.md), [ **значение**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="e45b0-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="e45b0-111">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="e45b0-111">Parent/Child Information</span></span>



| <span data-ttu-id="e45b0-112">Метка</span><span class="sxs-lookup"><span data-stu-id="e45b0-112">Label</span></span> | <span data-ttu-id="e45b0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e45b0-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="e45b0-114">Parent</span><span class="sxs-lookup"><span data-stu-id="e45b0-114">Parent</span></span>   | [<span data-ttu-id="e45b0-115">**param**</span><span class="sxs-lookup"><span data-stu-id="e45b0-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="e45b0-116">Дети</span><span class="sxs-lookup"><span data-stu-id="e45b0-116">Children</span></span> | <span data-ttu-id="e45b0-117">None</span><span class="sxs-lookup"><span data-stu-id="e45b0-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="e45b0-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="e45b0-118">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="e45b0-119">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="e45b0-119">Requirements</span></span>



| <span data-ttu-id="e45b0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e45b0-120">Requirement</span></span> | <span data-ttu-id="e45b0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e45b0-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e45b0-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e45b0-122">Header</span></span><br/> | <dl> <span data-ttu-id="e45b0-123"><dt>Камерауиконтрол. h</dt></span><span class="sxs-lookup"><span data-stu-id="e45b0-123"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e45b0-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e45b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e45b0-125">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="e45b0-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




