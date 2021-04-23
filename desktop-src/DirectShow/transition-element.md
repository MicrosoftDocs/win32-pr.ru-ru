---
description: Элемент TRANSITION определяет объект перехода. Переход — это преобразование с двумя входными данными, которое приводит к переходу из одного потока (например, составного или отслеживающего) в другой.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Элемент TRANSITION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910042"
---
# <a name="transition-element"></a><span data-ttu-id="0a223-104">Элемент TRANSITION</span><span class="sxs-lookup"><span data-stu-id="0a223-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="0a223-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0a223-105">\[Deprecated.</span></span> <span data-ttu-id="0a223-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a223-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a223-107">`transition`Элемент определяет объект перехода.</span><span class="sxs-lookup"><span data-stu-id="0a223-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="0a223-108">Переход — это преобразование с двумя входными данными, которое приводит к переходу из одного потока (например, составного или отслеживающего) в другой.</span><span class="sxs-lookup"><span data-stu-id="0a223-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="0a223-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0a223-109">Attributes</span></span>

<span data-ttu-id="0a223-110">[**CLSID**](clsid-attribute.md), [**кутпоинт**](cutpoint-attribute.md), [**кутсонли**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**выкл**](mute-attribute.md)., [**Start**](start-attribute.md), [**останавливаться**](stop-attribute.md), [**свапинпутс**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="0a223-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="0a223-111">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="0a223-111">Parent/Child Information</span></span>



| <span data-ttu-id="0a223-112">Метка</span><span class="sxs-lookup"><span data-stu-id="0a223-112">Label</span></span> | <span data-ttu-id="0a223-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0a223-113">Value</span></span> |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="0a223-114">Parent</span><span class="sxs-lookup"><span data-stu-id="0a223-114">Parent</span></span>   | <span data-ttu-id="0a223-115">[**составной**](composite-element.md), [ **Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="0a223-115">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="0a223-116">Дети</span><span class="sxs-lookup"><span data-stu-id="0a223-116">Children</span></span> | [<span data-ttu-id="0a223-117">**param**</span><span class="sxs-lookup"><span data-stu-id="0a223-117">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="0a223-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a223-118">Remarks</span></span>

<span data-ttu-id="0a223-119">Атрибут **CLSID** задает подобъект, который создает переход.</span><span class="sxs-lookup"><span data-stu-id="0a223-119">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="0a223-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="0a223-120">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="0a223-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0a223-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a223-122">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="0a223-122">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



