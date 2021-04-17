---
title: BUTTONGROUP. Транспаренциколор
description: Атрибут Транспаренциколор указывает или получает прозрачный цвет изображений BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Транспаренциколор
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694852"
---
# <a name="buttongrouptransparencycolor"></a><span data-ttu-id="54b35-104">BUTTONGROUP. Транспаренциколор</span><span class="sxs-lookup"><span data-stu-id="54b35-104">BUTTONGROUP.transparencyColor</span></span>

<span data-ttu-id="54b35-105">Атрибут **транспаренциколор** указывает или получает прозрачный цвет изображений **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="54b35-105">The **transparencyColor** attribute specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="54b35-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="54b35-106">Possible Values</span></span>

<span data-ttu-id="54b35-107">Этот атрибут является **строкой** для чтения и записи и не имеет значения по умолчанию, содержащей одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="54b35-107">This attribute is a read/write **String** with no default, containing one of the following values.</span></span>



| <span data-ttu-id="54b35-108">Значение</span><span class="sxs-lookup"><span data-stu-id="54b35-108">Value</span></span>                                       | <span data-ttu-id="54b35-109">Описание</span><span class="sxs-lookup"><span data-stu-id="54b35-109">Description</span></span>                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54b35-110">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="54b35-110">Auto</span></span>                                        | <span data-ttu-id="54b35-111">Пиксель в положении 0, 0 в изображении превращается в прозрачный цвет.</span><span class="sxs-lookup"><span data-stu-id="54b35-111">The pixel at location 0,0 in the image becomes the transparent color.</span></span>                              |
| <span data-ttu-id="54b35-112">любое значение цвета Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="54b35-112">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="54b35-113">Значение цвета Internet Explorer превращается в прозрачный цвет (например, "Red" или " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="54b35-113">An Internet Explorer color value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="54b35-114">Нет</span><span class="sxs-lookup"><span data-stu-id="54b35-114">None</span></span>                                        | <span data-ttu-id="54b35-115">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54b35-115">Default.</span></span> <span data-ttu-id="54b35-116">Прозрачность отсутствует.</span><span class="sxs-lookup"><span data-stu-id="54b35-116">No transparency.</span></span>                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="54b35-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54b35-117">Remarks</span></span>

<span data-ttu-id="54b35-118">Прозрачный цвет в изображении позволяет отображать все, что находится за изображением, с помощью областей прозрачности.</span><span class="sxs-lookup"><span data-stu-id="54b35-118">A transparent color in an image will allow whatever is behind the image to show through the areas of transparency.</span></span> <span data-ttu-id="54b35-119">Прозрачная область может быть нажата, если не обрезаться тегом **клиппингимаже** .</span><span class="sxs-lookup"><span data-stu-id="54b35-119">The transparent region is clickable unless clipped by the **clippingImage** tag.</span></span>

<span data-ttu-id="54b35-120">Цвет может быть любым значением цвета Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="54b35-120">The color can be any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="54b35-121">Если значение равно Auto, то используется цвет пикселя в положении 0, 0 в изображении.</span><span class="sxs-lookup"><span data-stu-id="54b35-121">If the value is Auto, then the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="54b35-122">Если указанный цвет не является одним из допустимых цветов Internet Explorer, то возвращается предупреждение, а предыдущее значение сохраняется.</span><span class="sxs-lookup"><span data-stu-id="54b35-122">If the color specified is not one of the valid Internet Explorer colors, a warning is returned and the previous value is maintained.</span></span>

<span data-ttu-id="54b35-123">Так как Жпгс являются утерянными и поэтому подвержены непредвиденному изменению цвета, они не рекомендуются при использовании **транспаренциколор** .</span><span class="sxs-lookup"><span data-stu-id="54b35-123">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b35-124">Требования</span><span class="sxs-lookup"><span data-stu-id="54b35-124">Requirements</span></span>



| <span data-ttu-id="54b35-125">Требование</span><span class="sxs-lookup"><span data-stu-id="54b35-125">Requirement</span></span> | <span data-ttu-id="54b35-126">Значение</span><span class="sxs-lookup"><span data-stu-id="54b35-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="54b35-127">Версия</span><span class="sxs-lookup"><span data-stu-id="54b35-127">Version</span></span><br/> | <span data-ttu-id="54b35-128">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="54b35-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54b35-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54b35-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b35-130">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="54b35-130">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="54b35-131">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="54b35-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





