---
title: BUTTON. мозаичное заполнение
description: Атрибут мозаичного заполнения указывает или получает значение, указывающее, будет ли изображение кнопки мозаичным.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BUTTON. мозаичный проигрыватель Windows Media
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699218"
---
# <a name="buttontiled"></a><span data-ttu-id="b9374-104">BUTTON. мозаичное заполнение</span><span class="sxs-lookup"><span data-stu-id="b9374-104">BUTTON.tiled</span></span>

<span data-ttu-id="b9374-105">Атрибут **мозаичного заполнения** указывает или получает значение, указывающее, будет ли изображение **кнопки** мозаичным.</span><span class="sxs-lookup"><span data-stu-id="b9374-105">The **tiled** attribute specifies or retrieves a value indicating whether the **BUTTON** image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="b9374-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b9374-106">Possible Values</span></span>

<span data-ttu-id="b9374-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b9374-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b9374-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b9374-108">Value</span></span> | <span data-ttu-id="b9374-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b9374-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="b9374-110">true</span><span class="sxs-lookup"><span data-stu-id="b9374-110">true</span></span>  | <span data-ttu-id="b9374-111">Изображение будет мозаичным.</span><span class="sxs-lookup"><span data-stu-id="b9374-111">Image will be tiled.</span></span>              |
| <span data-ttu-id="b9374-112">false</span><span class="sxs-lookup"><span data-stu-id="b9374-112">false</span></span> | <span data-ttu-id="b9374-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9374-113">Default.</span></span> <span data-ttu-id="b9374-114">Изображение не будет мозаичным.</span><span class="sxs-lookup"><span data-stu-id="b9374-114">Image will not be tiled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b9374-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9374-115">Remarks</span></span>

<span data-ttu-id="b9374-116">Если изображение меньше фактической области элемента управления, мозаичное изображение будет повторяться до тех пор, пока не заполнит весь регион.</span><span class="sxs-lookup"><span data-stu-id="b9374-116">If the image is smaller than the actual region of the control, then tiling the image will repeat it until it fills the entire region.</span></span> <span data-ttu-id="b9374-117">Если образ не указан или не может быть получен, для **мозаичного заполнения** будет установлено значение false.</span><span class="sxs-lookup"><span data-stu-id="b9374-117">If an image is not specified or cannot be retrieved, **tiled** will be set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9374-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b9374-118">Requirements</span></span>



| <span data-ttu-id="b9374-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b9374-119">Requirement</span></span> | <span data-ttu-id="b9374-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b9374-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b9374-121">Версия</span><span class="sxs-lookup"><span data-stu-id="b9374-121">Version</span></span><br/> | <span data-ttu-id="b9374-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b9374-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9374-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9374-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9374-124">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="b9374-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="b9374-125">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="b9374-125">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





