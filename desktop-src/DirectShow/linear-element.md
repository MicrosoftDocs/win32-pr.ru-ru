---
description: Линейный элемент определяет значение элемента Param в определенное время относительно начала перехода или действия, содержащего элемент param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: линейный элемент (Камерауиконтрол. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674889"
---
# <a name="linear-element"></a><span data-ttu-id="4378b-103">линейный элемент</span><span class="sxs-lookup"><span data-stu-id="4378b-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="4378b-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4378b-104">\[Deprecated.</span></span> <span data-ttu-id="4378b-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4378b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4378b-106">Линейный элемент определяет значение элемента [**param**](param-element.md) в определенное время относительно начала перехода или действия, содержащего элемент **param** .</span><span class="sxs-lookup"><span data-stu-id="4378b-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="4378b-107">`linear`Элемент заставляет параметр выполнить плавный переход из предыдущего значения к новому значению.</span><span class="sxs-lookup"><span data-stu-id="4378b-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="4378b-108">Для мгновенного перехода к новому значению используйте элемент [**at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4378b-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="4378b-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4378b-109">Attributes</span></span>

<span data-ttu-id="4378b-110">[**время**](time-attribute.md), [ **значение**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="4378b-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="4378b-111">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="4378b-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="4378b-112">Parent</span><span class="sxs-lookup"><span data-stu-id="4378b-112">Parent</span></span>   | [<span data-ttu-id="4378b-113">**байт**</span><span class="sxs-lookup"><span data-stu-id="4378b-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="4378b-114">Дети</span><span class="sxs-lookup"><span data-stu-id="4378b-114">Children</span></span> | <span data-ttu-id="4378b-115">None</span><span class="sxs-lookup"><span data-stu-id="4378b-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="4378b-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="4378b-116">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="4378b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4378b-117">Requirements</span></span>



| <span data-ttu-id="4378b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4378b-118">Requirement</span></span> | <span data-ttu-id="4378b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4378b-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4378b-120">Header</span><span class="sxs-lookup"><span data-stu-id="4378b-120">Header</span></span><br/> | <dl> <span data-ttu-id="4378b-121"><dt>Камерауиконтрол. h</dt></span><span class="sxs-lookup"><span data-stu-id="4378b-121"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4378b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4378b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4378b-123">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="4378b-123">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




