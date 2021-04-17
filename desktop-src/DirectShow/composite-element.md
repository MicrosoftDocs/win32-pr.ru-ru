---
description: Составной элемент определяет композицию, объект-контейнер для дорожек и другие вложенные композиции.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: составной элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672983"
---
# <a name="composite-element"></a><span data-ttu-id="45ec7-103">составной элемент</span><span class="sxs-lookup"><span data-stu-id="45ec7-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="45ec7-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="45ec7-104">\[Deprecated.</span></span> <span data-ttu-id="45ec7-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="45ec7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="45ec7-106">`composite`Элемент определяет композицию, объект контейнера для дорожек и другие вложенные композиции.</span><span class="sxs-lookup"><span data-stu-id="45ec7-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="45ec7-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="45ec7-107">Attributes</span></span>

<span data-ttu-id="45ec7-108">[**Блокировка**](lock-attribute.md), [**Отключение звука**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="45ec7-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="45ec7-109">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="45ec7-109">Parent/Child Information</span></span>



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ec7-110">Parent</span><span class="sxs-lookup"><span data-stu-id="45ec7-110">Parent</span></span>   | <span data-ttu-id="45ec7-111">`composite`, [ **Группа**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="45ec7-111">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="45ec7-112">Дети</span><span class="sxs-lookup"><span data-stu-id="45ec7-112">Children</span></span> | <span data-ttu-id="45ec7-113">`composite`, [**воздействие**](effect-element.md), [**Трассировка**](track-element.md), [**Переход**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="45ec7-113">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="45ec7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45ec7-114">Remarks</span></span>

<span data-ttu-id="45ec7-115">В пределах `composite` элемента приоритет вложенных слоев определяется неявно в порядке, в котором они отображаются внутри элемента.</span><span class="sxs-lookup"><span data-stu-id="45ec7-115">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="45ec7-116">Первый уровень имеет приоритет 0, а последующие уровни увеличивают значения приоритета.</span><span class="sxs-lookup"><span data-stu-id="45ec7-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="45ec7-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="45ec7-117">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="45ec7-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45ec7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ec7-119">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="45ec7-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



