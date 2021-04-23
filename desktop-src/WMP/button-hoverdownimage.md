---
title: КНОПКА. Ховердовнимаже
description: Атрибут Ховердовнимаже указывает или получает изображение, отображаемое, когда кнопка находится в состоянии Down, и пользователь наводит указатель мыши на него.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- КНОПКА. Ховердовнимаже Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694666"
---
# <a name="buttonhoverdownimage"></a><span data-ttu-id="7bcde-104">КНОПКА. Ховердовнимаже</span><span class="sxs-lookup"><span data-stu-id="7bcde-104">BUTTON.hoverDownImage</span></span>

<span data-ttu-id="7bcde-105">Атрибут **ховердовнимаже** указывает или получает изображение, отображаемое, когда **кнопка** находится в состоянии Down, и пользователь наводит указатель мыши на него.</span><span class="sxs-lookup"><span data-stu-id="7bcde-105">The **hoverDownImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the down state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="7bcde-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="7bcde-106">Possible Values</span></span>

<span data-ttu-id="7bcde-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="7bcde-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bcde-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bcde-108">Remarks</span></span>

<span data-ttu-id="7bcde-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="7bcde-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="7bcde-110">Изображение по умолчанию — это образ, указанный в атрибуте **довнимаже** , или его значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bcde-110">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="7bcde-111">Если изображение наведения указателя больше, чем заданная область во внешнем атрибуте, то изображение с наведением будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="7bcde-111">If the hover-down image is larger than the defined region in the ambient attribute, the hover-down image will be cropped.</span></span>

<span data-ttu-id="7bcde-112">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="7bcde-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bcde-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7bcde-113">Requirements</span></span>



| <span data-ttu-id="7bcde-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7bcde-114">Requirement</span></span> | <span data-ttu-id="7bcde-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7bcde-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7bcde-116">Версия</span><span class="sxs-lookup"><span data-stu-id="7bcde-116">Version</span></span><br/> | <span data-ttu-id="7bcde-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="7bcde-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7bcde-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bcde-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bcde-119">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="7bcde-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="7bcde-120">**КНОПКА. Довнимаже**</span><span class="sxs-lookup"><span data-stu-id="7bcde-120">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





