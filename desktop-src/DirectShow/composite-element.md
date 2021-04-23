---
description: Составной элемент определяет композицию, объект-контейнер для дорожек и другие вложенные композиции.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: составной элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908842"
---
# <a name="composite-element"></a><span data-ttu-id="d7b2a-103">составной элемент</span><span class="sxs-lookup"><span data-stu-id="d7b2a-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="d7b2a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="d7b2a-104">\[Deprecated.</span></span> <span data-ttu-id="d7b2a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7b2a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d7b2a-106">`composite`Элемент определяет композицию, объект контейнера для дорожек и другие вложенные композиции.</span><span class="sxs-lookup"><span data-stu-id="d7b2a-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="d7b2a-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d7b2a-107">Attributes</span></span>

<span data-ttu-id="d7b2a-108">[**Блокировка**](lock-attribute.md), [**Отключение звука**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="d7b2a-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="d7b2a-109">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="d7b2a-109">Parent/Child Information</span></span>



| <span data-ttu-id="d7b2a-110">Метка</span><span class="sxs-lookup"><span data-stu-id="d7b2a-110">Label</span></span> | <span data-ttu-id="d7b2a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b2a-111">Value</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b2a-112">Parent</span><span class="sxs-lookup"><span data-stu-id="d7b2a-112">Parent</span></span>   | <span data-ttu-id="d7b2a-113">`composite`, [ **Группа**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="d7b2a-113">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="d7b2a-114">Дети</span><span class="sxs-lookup"><span data-stu-id="d7b2a-114">Children</span></span> | <span data-ttu-id="d7b2a-115">`composite`, [**воздействие**](effect-element.md), [**Трассировка**](track-element.md), [**Переход**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="d7b2a-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d7b2a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7b2a-116">Remarks</span></span>

<span data-ttu-id="d7b2a-117">В пределах `composite` элемента приоритет вложенных слоев определяется неявно в порядке, в котором они отображаются внутри элемента.</span><span class="sxs-lookup"><span data-stu-id="d7b2a-117">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="d7b2a-118">Первый уровень имеет приоритет 0, а последующие уровни увеличивают значения приоритета.</span><span class="sxs-lookup"><span data-stu-id="d7b2a-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="d7b2a-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="d7b2a-119">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="d7b2a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d7b2a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b2a-121">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="d7b2a-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



