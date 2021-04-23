---
title: КНОПКА. Ховеримаже
description: Атрибут Ховеримаже указывает или получает изображение, отображаемое, когда кнопка находится в состоянии "вверх", и пользователь наводит указатель мыши на него.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- КНОПКА. Ховеримаже Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694664"
---
# <a name="buttonhoverimage"></a><span data-ttu-id="da856-104">КНОПКА. Ховеримаже</span><span class="sxs-lookup"><span data-stu-id="da856-104">BUTTON.hoverImage</span></span>

<span data-ttu-id="da856-105">Атрибут **ховеримаже** указывает или получает изображение, отображаемое, когда **кнопка** находится в состоянии "вверх", и пользователь наводит указатель мыши на него.</span><span class="sxs-lookup"><span data-stu-id="da856-105">The **hoverImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the up state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="da856-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="da856-106">Possible Values</span></span>

<span data-ttu-id="da856-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="da856-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="da856-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da856-108">Remarks</span></span>

<span data-ttu-id="da856-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="da856-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="da856-110">Изображение по умолчанию — это образ, указанный в атрибуте **Image** , или его значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da856-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="da856-111">Если изображение с наведением больше, чем заданная область во внешнем атрибуте, изображение для наведения будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="da856-111">If the hover image is larger than the defined region in the ambient attribute, the hover image will be cropped.</span></span>

<span data-ttu-id="da856-112">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="da856-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="da856-113">Требования</span><span class="sxs-lookup"><span data-stu-id="da856-113">Requirements</span></span>



| <span data-ttu-id="da856-114">Требование</span><span class="sxs-lookup"><span data-stu-id="da856-114">Requirement</span></span> | <span data-ttu-id="da856-115">Значение</span><span class="sxs-lookup"><span data-stu-id="da856-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="da856-116">Версия</span><span class="sxs-lookup"><span data-stu-id="da856-116">Version</span></span><br/> | <span data-ttu-id="da856-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="da856-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da856-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da856-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da856-119">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="da856-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="da856-120">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="da856-120">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





