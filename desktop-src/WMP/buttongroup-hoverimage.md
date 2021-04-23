---
title: BUTTONGROUP. Ховеримаже
description: Атрибут Ховеримаже указывает или получает имя изображения, представляющего состояние наведения указателя кнопки в BUTTONGROUP. Состояние наведения наведением возникает, когда кнопка находится в состоянии "вверх", и пользователь наводит на нее указатель мыши.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Ховеримаже
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694406"
---
# <a name="buttongrouphoverimage"></a><span data-ttu-id="5cf54-105">BUTTONGROUP. Ховеримаже</span><span class="sxs-lookup"><span data-stu-id="5cf54-105">BUTTONGROUP.hoverImage</span></span>

<span data-ttu-id="5cf54-106">Атрибут **ховеримаже** указывает или получает имя изображения, представляющего состояние наведения указателя кнопки в **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="5cf54-106">The **hoverImage** attribute specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="5cf54-107">Состояние наведения наведением возникает, когда кнопка находится в состоянии "вверх", и пользователь наводит на нее указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="5cf54-107">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="5cf54-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="5cf54-108">Possible Values</span></span>

<span data-ttu-id="5cf54-109">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5cf54-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf54-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cf54-110">Remarks</span></span>

<span data-ttu-id="5cf54-111">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="5cf54-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="5cf54-112">Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .</span><span class="sxs-lookup"><span data-stu-id="5cf54-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="5cf54-113">Изображение по умолчанию — это образ, указанный в атрибуте **Image** , или его значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5cf54-113">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="5cf54-114">Если изображение с наведением больше, чем определенная область, изображение для наведения будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="5cf54-114">If the hover image is larger than the defined region, the hover image will be cropped.</span></span>

<span data-ttu-id="5cf54-115">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="5cf54-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="5cf54-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="5cf54-116">Examples</span></span>

<span data-ttu-id="5cf54-117">См. *буттонелемент*. атрибут [маппингколор](buttonelement-mappingcolor.md) для примера, иллюстрирующий использование этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="5cf54-117">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf54-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5cf54-118">Requirements</span></span>



| <span data-ttu-id="5cf54-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5cf54-119">Requirement</span></span> | <span data-ttu-id="5cf54-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5cf54-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5cf54-121">Версия</span><span class="sxs-lookup"><span data-stu-id="5cf54-121">Version</span></span><br/> | <span data-ttu-id="5cf54-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="5cf54-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cf54-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cf54-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf54-124">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="5cf54-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="5cf54-125">**BUTTONGROUP. Хуешифт**</span><span class="sxs-lookup"><span data-stu-id="5cf54-125">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="5cf54-126">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="5cf54-126">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="5cf54-127">**BUTTONGROUP. насыщенность**</span><span class="sxs-lookup"><span data-stu-id="5cf54-127">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





