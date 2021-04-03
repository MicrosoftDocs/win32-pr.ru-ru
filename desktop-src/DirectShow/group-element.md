---
description: Элемент Group определяет группу, объект верхнего уровня на временной шкале.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Элемент Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990255"
---
# <a name="group-element"></a><span data-ttu-id="7e577-103">Group, элемент</span><span class="sxs-lookup"><span data-stu-id="7e577-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="7e577-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7e577-104">\[Deprecated.</span></span> <span data-ttu-id="7e577-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7e577-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7e577-106">Элемент **Group** определяет группу, объект верхнего уровня на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="7e577-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="7e577-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7e577-107">Attributes</span></span>

<span data-ttu-id="7e577-108">[**битдепс**](bitdepth-attribute.md), [**буферизация**](buffering-attribute.md), [**Частота кадров**](framerate-attribute.md), [**Высота**](height-attribute.md), [**Блокировка**](lock-attribute.md), [**Отключение звука**](mute-attribute.md), [**имя**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**самплинграте**](samplingrate-attribute.md), [**тип**](type-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md), [**Ширина**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="7e577-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="7e577-109">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="7e577-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e577-110">Parent</span><span class="sxs-lookup"><span data-stu-id="7e577-110">Parent</span></span>   | [<span data-ttu-id="7e577-111">**графика**</span><span class="sxs-lookup"><span data-stu-id="7e577-111">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="7e577-112">Дети</span><span class="sxs-lookup"><span data-stu-id="7e577-112">Children</span></span> | <span data-ttu-id="7e577-113">[**составной**](composite-element.md), [**результат**](effect-element.md), [**трекинг**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="7e577-113">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7e577-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e577-114">Remarks</span></span>

<span data-ttu-id="7e577-115">В пределах `group` элемента приоритет вложенных слоев определяется неявно в порядке их расположения в элементе.</span><span class="sxs-lookup"><span data-stu-id="7e577-115">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="7e577-116">Первый уровень имеет приоритет 0, а последующие уровни увеличивают значения приоритета.</span><span class="sxs-lookup"><span data-stu-id="7e577-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="7e577-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e577-117">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="7e577-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e577-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e577-119">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="7e577-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



