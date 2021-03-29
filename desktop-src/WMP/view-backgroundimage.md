---
title: Просмотр. backgroundImage
description: Атрибут backgroundImage указывает или получает фоновое изображение представления или подпредставления.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- Просмотр. backgroundImage проигрывателя Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648054"
---
# <a name="viewbackgroundimage"></a><span data-ttu-id="4849e-104">Просмотр. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="4849e-104">VIEW.backgroundImage</span></span>

<span data-ttu-id="4849e-105">Атрибут **backgroundImage** указывает или получает фоновое изображение **представления** или **подпредставления**.</span><span class="sxs-lookup"><span data-stu-id="4849e-105">The **backgroundImage** attribute specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="4849e-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="4849e-106">Possible Values</span></span>

<span data-ttu-id="4849e-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4849e-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4849e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4849e-108">Remarks</span></span>

<span data-ttu-id="4849e-109">Поддерживаются форматы BMP, JPG, GIF и PNG.</span><span class="sxs-lookup"><span data-stu-id="4849e-109">The supported formats are BMP, JPG, GIF, and PNG.</span></span> <span data-ttu-id="4849e-110">Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **баккграундимажехуешифт** и **баккграундимажесатуратион** .</span><span class="sxs-lookup"><span data-stu-id="4849e-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **backgroundImageHueShift** and **backgroundImageSaturation** attributes.</span></span>

<span data-ttu-id="4849e-111">Если в пакете загрузки Windows Media задан атрибут **backgroundImage** для элемента **View** , необходимо также указать атрибут **backgroundColor** для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="4849e-111">In a Windows Media Download package, if you specify the **backgroundImage** attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4849e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4849e-112">Requirements</span></span>



| <span data-ttu-id="4849e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4849e-113">Requirement</span></span> | <span data-ttu-id="4849e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4849e-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4849e-115">Версия</span><span class="sxs-lookup"><span data-stu-id="4849e-115">Version</span></span><br/> | <span data-ttu-id="4849e-116">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="4849e-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4849e-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4849e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4849e-118">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="4849e-118">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="4849e-119">**VIEW. Баккграундимажехуешифт**</span><span class="sxs-lookup"><span data-stu-id="4849e-119">**VIEW.backgroundImageHueShift**</span></span>](view-backgroundimagehueshift.md)
</dt> <dt>

[<span data-ttu-id="4849e-120">**VIEW. Баккграундимажесатуратион**</span><span class="sxs-lookup"><span data-stu-id="4849e-120">**VIEW.backgroundImageSaturation**</span></span>](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





