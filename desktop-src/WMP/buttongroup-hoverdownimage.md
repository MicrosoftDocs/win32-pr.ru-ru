---
title: BUTTONGROUP. Ховердовнимаже
description: Атрибут Ховердовнимаже указывает или получает имя изображения, представляющего состояние наведения указателя кнопки в BUTTONGROUP. Состояние наведения указателя мыши возникает, когда кнопка находится в состоянии Down, и пользователь наводит на нее указатель мышью.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Ховердовнимаже
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694407"
---
# <a name="buttongrouphoverdownimage"></a><span data-ttu-id="b7bf4-105">BUTTONGROUP. Ховердовнимаже</span><span class="sxs-lookup"><span data-stu-id="b7bf4-105">BUTTONGROUP.hoverDownImage</span></span>

<span data-ttu-id="b7bf4-106">Атрибут **ховердовнимаже** указывает или получает имя изображения, представляющего состояние наведения указателя кнопки в **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="b7bf4-106">The **hoverDownImage** attribute specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="b7bf4-107">Состояние наведения указателя мыши возникает, когда кнопка находится в состоянии Down, и пользователь наводит на нее указатель мышью.</span><span class="sxs-lookup"><span data-stu-id="b7bf4-107">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="b7bf4-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b7bf4-108">Possible Values</span></span>

<span data-ttu-id="b7bf4-109">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b7bf4-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7bf4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7bf4-110">Remarks</span></span>

<span data-ttu-id="b7bf4-111">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="b7bf4-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="b7bf4-112">Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .</span><span class="sxs-lookup"><span data-stu-id="b7bf4-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="b7bf4-113">Изображение по умолчанию — это образ, указанный в атрибуте **довнимаже** , или его значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7bf4-113">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="b7bf4-114">Если изображение наведения мыши больше, чем определенная область, изображение с наведением будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="b7bf4-114">If the hover-down image is larger than the defined region, the hover-down image will be cropped.</span></span>

<span data-ttu-id="b7bf4-115">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="b7bf4-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7bf4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b7bf4-116">Requirements</span></span>



| <span data-ttu-id="b7bf4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b7bf4-117">Requirement</span></span> | <span data-ttu-id="b7bf4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b7bf4-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b7bf4-119">Версия</span><span class="sxs-lookup"><span data-stu-id="b7bf4-119">Version</span></span><br/> | <span data-ttu-id="b7bf4-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b7bf4-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7bf4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7bf4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bf4-122">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="b7bf4-122">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="b7bf4-123">**BUTTONGROUP. Довнимаже**</span><span class="sxs-lookup"><span data-stu-id="b7bf4-123">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="b7bf4-124">**BUTTONGROUP. Хуешифт**</span><span class="sxs-lookup"><span data-stu-id="b7bf4-124">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="b7bf4-125">**BUTTONGROUP. насыщенность**</span><span class="sxs-lookup"><span data-stu-id="b7bf4-125">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





