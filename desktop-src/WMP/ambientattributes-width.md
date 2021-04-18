---
title: Амбиентаттрибутес. Width
description: Атрибут Width указывает или получает ширину элемента управления.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Width
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694678"
---
# <a name="ambientattributeswidth"></a><span data-ttu-id="20e4d-104">Амбиентаттрибутес. Width</span><span class="sxs-lookup"><span data-stu-id="20e4d-104">AmbientAttributes.width</span></span>

<span data-ttu-id="20e4d-105">Атрибут **Width** указывает или получает ширину элемента управления.</span><span class="sxs-lookup"><span data-stu-id="20e4d-105">The **width** attribute specifies or retrieves the width of the control.</span></span>

``` syntax
        elementID.width
```

## <a name="possible-values"></a><span data-ttu-id="20e4d-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="20e4d-106">Possible Values</span></span>

<span data-ttu-id="20e4d-107">Этот атрибут представляет собой 16-разрядное **целое число** для чтения и записи (от 0 до 32 767), представляющее ширину элемента управления в пикселях.</span><span class="sxs-lookup"><span data-stu-id="20e4d-107">This attribute is a read/write 16-bit **Integer** (0 to 32,767) representing the width of the control in pixels.</span></span> <span data-ttu-id="20e4d-108">Значение по умолчанию равно нулю или ширине изображения, указанного в атрибуте **Image** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="20e4d-108">The default value is zero or the width of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="20e4d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20e4d-109">Remarks</span></span>

<span data-ttu-id="20e4d-110">Если заданная ширина является более узким, чем ширина предоставленного изображения, то изображение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="20e4d-110">If the width specified is narrower than the width of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="20e4d-111">Если ширина превышает ширину изображения, то область щелчка будет выходить за границы изображения.</span><span class="sxs-lookup"><span data-stu-id="20e4d-111">If the width is wider than the width of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="20e4d-112">Независимо от того, какое значение присвоено этому атрибуту, изображение не может увеличиваться за пределами родительского **представления** или вложенного **представления**.</span><span class="sxs-lookup"><span data-stu-id="20e4d-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="20e4d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="20e4d-113">Requirements</span></span>



| <span data-ttu-id="20e4d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="20e4d-114">Requirement</span></span> | <span data-ttu-id="20e4d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="20e4d-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="20e4d-116">Версия</span><span class="sxs-lookup"><span data-stu-id="20e4d-116">Version</span></span><br/> | <span data-ttu-id="20e4d-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="20e4d-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20e4d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20e4d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e4d-119">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="20e4d-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





