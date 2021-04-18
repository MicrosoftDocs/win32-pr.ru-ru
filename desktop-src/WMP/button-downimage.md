---
title: КНОПКА. Довнимаже
description: Атрибут Довнимаже указывает или получает изображение, представляющее состояние кнопки "вниз".
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- КНОПКА. Довнимаже Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694520"
---
# <a name="buttondownimage"></a><span data-ttu-id="b11df-104">КНОПКА. Довнимаже</span><span class="sxs-lookup"><span data-stu-id="b11df-104">BUTTON.downImage</span></span>

<span data-ttu-id="b11df-105">Атрибут **довнимаже** указывает или получает изображение, представляющее состояние **кнопки "вниз"**.</span><span class="sxs-lookup"><span data-stu-id="b11df-105">The **downImage** attribute specifies or retrieves the image representing the down state of the **BUTTON**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="b11df-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b11df-106">Possible Values</span></span>

<span data-ttu-id="b11df-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="b11df-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="b11df-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b11df-108">Remarks</span></span>

<span data-ttu-id="b11df-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="b11df-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="b11df-110">Изображение по умолчанию — это образ, указанный в атрибуте **Image** , или его значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b11df-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="b11df-111">Если изображение вниз больше, чем заданная область во внешнем атрибуте, то изображение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="b11df-111">If the down image is larger than the defined region in the ambient attribute, the down image will be cropped.</span></span>

<span data-ttu-id="b11df-112">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="b11df-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b11df-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b11df-113">Requirements</span></span>



| <span data-ttu-id="b11df-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b11df-114">Requirement</span></span> | <span data-ttu-id="b11df-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b11df-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b11df-116">Версия</span><span class="sxs-lookup"><span data-stu-id="b11df-116">Version</span></span><br/> | <span data-ttu-id="b11df-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b11df-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b11df-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b11df-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b11df-119">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="b11df-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="b11df-120">**КНОПКА. вниз**</span><span class="sxs-lookup"><span data-stu-id="b11df-120">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="b11df-121">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="b11df-121">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





