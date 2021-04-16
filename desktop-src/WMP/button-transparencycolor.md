---
title: КНОПКА. Транспаренциколор
description: Атрибут Транспаренциколор указывает или получает цвет, который будет прозрачным в изображениях кнопки.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- КНОПКА. Транспаренциколор Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699124"
---
# <a name="buttontransparencycolor"></a><span data-ttu-id="84823-104">КНОПКА. Транспаренциколор</span><span class="sxs-lookup"><span data-stu-id="84823-104">BUTTON.transparencyColor</span></span>

<span data-ttu-id="84823-105">Атрибут **транспаренциколор** указывает или получает цвет, который будет прозрачным в изображениях **кнопки** .</span><span class="sxs-lookup"><span data-stu-id="84823-105">The **transparencyColor** attribute specifies or retrieves the color that will be transparent in the **BUTTON** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="84823-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="84823-106">Possible Values</span></span>

<span data-ttu-id="84823-107">Этот атрибут является **строкой** для чтения и записи и не имеет значения по умолчанию, содержащего одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="84823-107">This attribute is a read/write **String** with no default containing one of the following values.</span></span>



| <span data-ttu-id="84823-108">Значение</span><span class="sxs-lookup"><span data-stu-id="84823-108">Value</span></span>                                    | <span data-ttu-id="84823-109">Описание</span><span class="sxs-lookup"><span data-stu-id="84823-109">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84823-110">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="84823-110">Auto</span></span>                                     | <span data-ttu-id="84823-111">Цвет пикселя в положении 0, 0 в изображении превращается в прозрачный цвет.</span><span class="sxs-lookup"><span data-stu-id="84823-111">The color of the pixel at location 0,0 in the image becomes the transparent color.</span></span>                        |
| <span data-ttu-id="84823-112">Любое значение формата цвета Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="84823-112">Any Internet Explorer color format value</span></span> | <span data-ttu-id="84823-113">Значение формата цвета Internet Explorer превращается в прозрачный цвет (например, "Red" или " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="84823-113">An Internet Explorer color format value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="84823-114">Нет</span><span class="sxs-lookup"><span data-stu-id="84823-114">None</span></span>                                     | <span data-ttu-id="84823-115">Прозрачность отсутствует.</span><span class="sxs-lookup"><span data-stu-id="84823-115">No transparency.</span></span>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="84823-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84823-116">Remarks</span></span>

<span data-ttu-id="84823-117">Прозрачный цвет в изображении позволяет отображать все, что находится за изображением, с помощью прозрачных областей.</span><span class="sxs-lookup"><span data-stu-id="84823-117">A transparent color in an image allows whatever is behind the image to show through the transparent areas.</span></span> <span data-ttu-id="84823-118">**Кнопка** по-прежнему будет принимать щелчки в прозрачной области.</span><span class="sxs-lookup"><span data-stu-id="84823-118">The **BUTTON** will still receive clicks on the transparent region.</span></span>

<span data-ttu-id="84823-119">Прозрачный цвет может быть любым значением цвета Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="84823-119">The transparent color can be any Internet Explorer color value.</span></span> <span data-ttu-id="84823-120">Если для атрибута **транспаренциколор** задано значение Auto, то используется цвет пикселя в положении 0, 0 в изображении.</span><span class="sxs-lookup"><span data-stu-id="84823-120">If the value of the **transparencyColor** attribute is set to "Auto", the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="84823-121">Если указанный цвет не является одним из допустимых цветов IE, сохраняется предыдущее значение.</span><span class="sxs-lookup"><span data-stu-id="84823-121">If the color specified is not one of the valid IE colors, the previous value is maintained.</span></span>

<span data-ttu-id="84823-122">Так как Жпгс являются утерянными и поэтому подвержены непредвиденному изменению цвета, они не рекомендуются при использовании **транспаренциколор** .</span><span class="sxs-lookup"><span data-stu-id="84823-122">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="84823-123">Требования</span><span class="sxs-lookup"><span data-stu-id="84823-123">Requirements</span></span>



| <span data-ttu-id="84823-124">Требование</span><span class="sxs-lookup"><span data-stu-id="84823-124">Requirement</span></span> | <span data-ttu-id="84823-125">Значение</span><span class="sxs-lookup"><span data-stu-id="84823-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="84823-126">Версия</span><span class="sxs-lookup"><span data-stu-id="84823-126">Version</span></span><br/> | <span data-ttu-id="84823-127">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="84823-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84823-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84823-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84823-129">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="84823-129">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="84823-130">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="84823-130">**BUTTON.image**</span></span>](button-image.md)
</dt> <dt>

[<span data-ttu-id="84823-131">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="84823-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





