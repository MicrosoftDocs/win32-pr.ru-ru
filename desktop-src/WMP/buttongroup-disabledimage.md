---
title: BUTTONGROUP. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает имя изображения, представляющего отключенное состояние кнопок в BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Дисабледимаже
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694589"
---
# <a name="buttongroupdisabledimage"></a><span data-ttu-id="2d4b4-104">BUTTONGROUP. Дисабледимаже</span><span class="sxs-lookup"><span data-stu-id="2d4b4-104">BUTTONGROUP.disabledImage</span></span>

<span data-ttu-id="2d4b4-105">Атрибут **дисабледимаже** указывает или получает имя изображения, представляющего отключенное состояние кнопок в **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="2d4b4-105">The **disabledImage** attribute specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="2d4b4-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="2d4b4-106">Possible Values</span></span>

<span data-ttu-id="2d4b4-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2d4b4-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d4b4-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d4b4-108">Remarks</span></span>

<span data-ttu-id="2d4b4-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="2d4b4-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="2d4b4-110">Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .</span><span class="sxs-lookup"><span data-stu-id="2d4b4-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="2d4b4-111">Если атрибуту **disabled** элемента **буттонелемент** присвоено значение true, то отображается соответствующий регион **дисабледимаже** для **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="2d4b4-111">When the **disabled** attribute of a **BUTTONELEMENT** element is set to true, the corresponding region of the **disabledImage** for the **BUTTONGROUP** is displayed.</span></span> <span data-ttu-id="2d4b4-112">Если отключенный образ больше, чем заданный регион, отключенный образ будет обрезан.</span><span class="sxs-lookup"><span data-stu-id="2d4b4-112">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="2d4b4-113">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="2d4b4-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d4b4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2d4b4-114">Requirements</span></span>



| <span data-ttu-id="2d4b4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2d4b4-115">Requirement</span></span> | <span data-ttu-id="2d4b4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2d4b4-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2d4b4-117">Версия</span><span class="sxs-lookup"><span data-stu-id="2d4b4-117">Version</span></span><br/> | <span data-ttu-id="2d4b4-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="2d4b4-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d4b4-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d4b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d4b4-120">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="2d4b4-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="2d4b4-121">**BUTTONGROUP. Хуешифт**</span><span class="sxs-lookup"><span data-stu-id="2d4b4-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="2d4b4-122">**BUTTONGROUP. насыщенность**</span><span class="sxs-lookup"><span data-stu-id="2d4b4-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





