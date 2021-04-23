---
title: BUTTONGROUP. Image
description: Атрибут Image указывает или получает имя изображения, представляющего кнопки BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Image
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699053"
---
# <a name="buttongroupimage"></a><span data-ttu-id="30042-104">BUTTONGROUP. Image</span><span class="sxs-lookup"><span data-stu-id="30042-104">BUTTONGROUP.image</span></span>

<span data-ttu-id="30042-105">Атрибут **Image** указывает или получает имя изображения, представляющего кнопки **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="30042-105">The **image** attribute specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="30042-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="30042-106">Possible Values</span></span>

<span data-ttu-id="30042-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="30042-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="30042-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30042-108">Remarks</span></span>

<span data-ttu-id="30042-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="30042-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="30042-110">Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .</span><span class="sxs-lookup"><span data-stu-id="30042-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="30042-111">Если изображение элемента управления больше, чем определенная область, изображение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="30042-111">If the image of the control is larger than the defined region, the image will be cropped.</span></span>

<span data-ttu-id="30042-112">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="30042-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="30042-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30042-113">Requirements</span></span>



| <span data-ttu-id="30042-114">Требование</span><span class="sxs-lookup"><span data-stu-id="30042-114">Requirement</span></span> | <span data-ttu-id="30042-115">Значение</span><span class="sxs-lookup"><span data-stu-id="30042-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="30042-116">Версия</span><span class="sxs-lookup"><span data-stu-id="30042-116">Version</span></span><br/> | <span data-ttu-id="30042-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="30042-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30042-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30042-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30042-119">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="30042-119">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="30042-120">**BUTTONGROUP. Хуешифт**</span><span class="sxs-lookup"><span data-stu-id="30042-120">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="30042-121">**BUTTONGROUP. насыщенность**</span><span class="sxs-lookup"><span data-stu-id="30042-121">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





