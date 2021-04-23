---
title: TEXT. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона для элемента управления "текст".
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- Проигрыватель Windows Media TEXT. backgroundColor
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717826"
---
# <a name="textbackgroundcolor"></a><span data-ttu-id="55556-104">TEXT. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="55556-104">TEXT.backgroundColor</span></span>

<span data-ttu-id="55556-105">Атрибут **backgroundColor** указывает или получает цвет фона для элемента управления "текст".</span><span class="sxs-lookup"><span data-stu-id="55556-105">The **backgroundColor** attribute specifies or retrieves the background color for the Text control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="55556-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="55556-106">Possible Values</span></span>

<span data-ttu-id="55556-107">Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer, или значение None.</span><span class="sxs-lookup"><span data-stu-id="55556-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="55556-108">Он имеет значение по умолчанию «нет», что означает, что фон прозрачен.</span><span class="sxs-lookup"><span data-stu-id="55556-108">It has a default value of "none", which means the background is transparent.</span></span>

## <a name="remarks"></a><span data-ttu-id="55556-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55556-109">Remarks</span></span>

<span data-ttu-id="55556-110">Цвет фона задается для высоты и ширины элемента управления.</span><span class="sxs-lookup"><span data-stu-id="55556-110">The background color is set for the height and width of the control.</span></span> <span data-ttu-id="55556-111">Если высота и ширина не заданы, то цвет фона устанавливается равным высоте и ширине текста.</span><span class="sxs-lookup"><span data-stu-id="55556-111">If height and width are not set, the background color is set to the height and width of the text.</span></span>

<span data-ttu-id="55556-112">При использовании **алфабленд** или **алфаблендто** с **текстовым** элементом, в котором не указан **backgroundColor** , будет использоваться цвет фона черного цвета.</span><span class="sxs-lookup"><span data-stu-id="55556-112">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="55556-113">Если цвет переднего плана также является черным (значением по умолчанию для атрибута **foregroundColor** ), текст может стать нечитаемым.</span><span class="sxs-lookup"><span data-stu-id="55556-113">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="55556-114">Чтобы избежать этого, всегда указывайте атрибут **backgroundColor** или задайте для **foregroundColor** цвет, отличный от черного.</span><span class="sxs-lookup"><span data-stu-id="55556-114">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

<span data-ttu-id="55556-115">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="55556-115">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="55556-116">Требования</span><span class="sxs-lookup"><span data-stu-id="55556-116">Requirements</span></span>



| <span data-ttu-id="55556-117">Требование</span><span class="sxs-lookup"><span data-stu-id="55556-117">Requirement</span></span> | <span data-ttu-id="55556-118">Значение</span><span class="sxs-lookup"><span data-stu-id="55556-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="55556-119">Версия</span><span class="sxs-lookup"><span data-stu-id="55556-119">Version</span></span><br/> | <span data-ttu-id="55556-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="55556-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55556-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55556-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55556-122">**Амбиентаттрибутес. Алфабленд**</span><span class="sxs-lookup"><span data-stu-id="55556-122">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="55556-123">**Амбиентаттрибутес. Алфаблендто**</span><span class="sxs-lookup"><span data-stu-id="55556-123">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="55556-124">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="55556-124">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="55556-125">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="55556-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="55556-126">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="55556-126">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





