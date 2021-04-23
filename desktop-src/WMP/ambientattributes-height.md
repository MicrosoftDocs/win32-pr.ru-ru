---
title: Амбиентаттрибутес. Height
description: Атрибут height указывает или получает высоту элемента управления.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Height
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698926"
---
# <a name="ambientattributesheight"></a><span data-ttu-id="50c06-104">Амбиентаттрибутес. Height</span><span class="sxs-lookup"><span data-stu-id="50c06-104">AmbientAttributes.height</span></span>

<span data-ttu-id="50c06-105">Атрибут **Height** указывает или получает высоту элемента управления.</span><span class="sxs-lookup"><span data-stu-id="50c06-105">The **height** attribute specifies or retrieves the height of the control.</span></span>

``` syntax
        elementID.height
```

## <a name="possible-values"></a><span data-ttu-id="50c06-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="50c06-106">Possible Values</span></span>

<span data-ttu-id="50c06-107">Этот атрибут является **числом** для чтения и записи (**длинное**), представляющим высоту элемента управления в пикселях.</span><span class="sxs-lookup"><span data-stu-id="50c06-107">This attribute is a read/write **Number** (**long**) representing the height of the control in pixels.</span></span> <span data-ttu-id="50c06-108">Значение по умолчанию равно нулю или высоте изображения, указанного в атрибуте **Image** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="50c06-108">The default value is zero or the height of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="50c06-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50c06-109">Remarks</span></span>

<span data-ttu-id="50c06-110">Если указанная высота меньше высоты предоставленного изображения, то изображение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="50c06-110">If the height specified is smaller than the height of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="50c06-111">Если высота превышает высоту изображения, то область щелчка выйдет за пределы границы изображения.</span><span class="sxs-lookup"><span data-stu-id="50c06-111">If the height is larger than the height of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="50c06-112">Независимо от того, какое значение присвоено этому атрибуту, изображение не может увеличиваться за пределами родительского **представления** или вложенного **представления**.</span><span class="sxs-lookup"><span data-stu-id="50c06-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c06-113">Требования</span><span class="sxs-lookup"><span data-stu-id="50c06-113">Requirements</span></span>



| <span data-ttu-id="50c06-114">Требование</span><span class="sxs-lookup"><span data-stu-id="50c06-114">Requirement</span></span> | <span data-ttu-id="50c06-115">Значение</span><span class="sxs-lookup"><span data-stu-id="50c06-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="50c06-116">Версия</span><span class="sxs-lookup"><span data-stu-id="50c06-116">Version</span></span><br/> | <span data-ttu-id="50c06-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="50c06-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50c06-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50c06-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c06-119">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="50c06-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





