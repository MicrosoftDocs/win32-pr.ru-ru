---
title: BUTTONGROUP. Довнимаже
description: Атрибут Довнимаже указывает или получает имя изображения, представляющего состояние down BUTTONGROUP.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Довнимаже
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694957"
---
# <a name="buttongroupdownimage"></a><span data-ttu-id="30621-104">BUTTONGROUP. Довнимаже</span><span class="sxs-lookup"><span data-stu-id="30621-104">BUTTONGROUP.downImage</span></span>

<span data-ttu-id="30621-105">Атрибут **довнимаже** указывает или получает имя изображения, представляющего состояние down **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="30621-105">The **downImage** attribute specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="30621-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="30621-106">Possible Values</span></span>

<span data-ttu-id="30621-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="30621-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="30621-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30621-108">Remarks</span></span>

<span data-ttu-id="30621-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="30621-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="30621-110">Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .</span><span class="sxs-lookup"><span data-stu-id="30621-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="30621-111">Изображение по умолчанию — это образ, указанный в атрибуте **Image** .</span><span class="sxs-lookup"><span data-stu-id="30621-111">The default image is the one specified in the **image** attribute.</span></span>

<span data-ttu-id="30621-112">Если изображение вниз больше, чем определенная область, то изображение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="30621-112">If the down image is larger than the defined region, the down image will be cropped.</span></span>

<span data-ttu-id="30621-113">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="30621-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="30621-114">Требования</span><span class="sxs-lookup"><span data-stu-id="30621-114">Requirements</span></span>



| <span data-ttu-id="30621-115">Требование</span><span class="sxs-lookup"><span data-stu-id="30621-115">Requirement</span></span> | <span data-ttu-id="30621-116">Значение</span><span class="sxs-lookup"><span data-stu-id="30621-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="30621-117">Версия</span><span class="sxs-lookup"><span data-stu-id="30621-117">Version</span></span><br/> | <span data-ttu-id="30621-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="30621-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30621-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30621-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30621-120">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="30621-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="30621-121">**BUTTONGROUP. Хуешифт**</span><span class="sxs-lookup"><span data-stu-id="30621-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="30621-122">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="30621-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="30621-123">**BUTTONGROUP. насыщенность**</span><span class="sxs-lookup"><span data-stu-id="30621-123">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





