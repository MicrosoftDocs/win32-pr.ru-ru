---
title: ПОЛЗУНок. Бордерсизе
description: Атрибут Бордерсизе указывает или получает ширину границы в пикселях.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- ПОЛЗУНок. Бордерсизе Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657618"
---
# <a name="sliderbordersize"></a><span data-ttu-id="d4de5-104">ПОЛЗУНок. Бордерсизе</span><span class="sxs-lookup"><span data-stu-id="d4de5-104">SLIDER.borderSize</span></span>

<span data-ttu-id="d4de5-105">Атрибут **бордерсизе** указывает или получает ширину границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d4de5-105">The **borderSize** attribute specifies or retrieves the border width in pixels.</span></span>

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a><span data-ttu-id="d4de5-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d4de5-106">Possible Values</span></span>

<span data-ttu-id="d4de5-107">Этот атрибут является **числом** для чтения и записи (**длинное целое**), представляющим ширину границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d4de5-107">This attribute is a read/write **Number** (**long**) representing the border width in pixels.</span></span> <span data-ttu-id="d4de5-108">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d4de5-108">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4de5-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4de5-109">Remarks</span></span>

<span data-ttu-id="d4de5-110">Этот атрибут определяет смещение от начала и конца элемента управления "ползунок", находящегося слева и справа, если для атрибута **Direction** задано значение "горизонтально", а сверху и снизу — "вертикальный".</span><span class="sxs-lookup"><span data-stu-id="d4de5-110">This attribute defines an offset from the beginning and end of the slider control that is, from the left and right if the **direction** attribute is set to "horizontal", and from the top and bottom if it is set to "vertical".</span></span> <span data-ttu-id="d4de5-111">Эти положения смещения определяют минимальное и максимальное положение ползунка, за исключением того, что цвет переднего плана или изображения не будут применены.</span><span class="sxs-lookup"><span data-stu-id="d4de5-111">These offset positions dictate the minimum and maximum positions of the slider thumb, beyond which the foreground color or image will not be applied.</span></span>

<span data-ttu-id="d4de5-112">Если фоновое изображение используется с атрибутом **мозаичного заполнения** , установленным в значение true, то смещение применяется к изображению, заменяя объем изображения (слева и справа или сверху и снизу), который будет использоваться для начальной и конечной границ элемента управления "ползунок", с центральной частью изображения, мозаичной в пределах оставшейся части.</span><span class="sxs-lookup"><span data-stu-id="d4de5-112">If a background image is used with the **tiled** attribute set to true, the offset is applied to the image, dictating the amount of the image (either from the left and right or from the top and bottom) to be used for the beginning and end borders of the slider control, with the central portion of the image being tiled throughout the remainder.</span></span> <span data-ttu-id="d4de5-113">Таким образом, можно использовать небольшое фоновое изображение, чтобы охватить полную длину элемента управления "ползунок" большего размера.</span><span class="sxs-lookup"><span data-stu-id="d4de5-113">In this way, a small background image can be used to cover the full length of a larger slider control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4de5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d4de5-114">Requirements</span></span>



| <span data-ttu-id="d4de5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d4de5-115">Requirement</span></span> | <span data-ttu-id="d4de5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d4de5-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d4de5-117">Версия</span><span class="sxs-lookup"><span data-stu-id="d4de5-117">Version</span></span><br/> | <span data-ttu-id="d4de5-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="d4de5-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4de5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4de5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4de5-120">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="d4de5-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="d4de5-121">**ПОЛЗУНок. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="d4de5-121">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="d4de5-122">**ПОЛЗУНок. Фореграундимаже**</span><span class="sxs-lookup"><span data-stu-id="d4de5-122">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="d4de5-123">**ПОЛЗУНок. Сумбимаже**</span><span class="sxs-lookup"><span data-stu-id="d4de5-123">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="d4de5-124">**ПОЛЗУНок. мозаичный**</span><span class="sxs-lookup"><span data-stu-id="d4de5-124">**SLIDER.tiled**</span></span>](slider-tiled.md)
</dt> </dl>

 

 





