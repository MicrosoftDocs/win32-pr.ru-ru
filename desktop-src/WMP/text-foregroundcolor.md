---
title: TEXT. foregroundColor
description: Атрибут foregroundColor указывает или получает цвет текста для элемента управления "текст".
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Проигрыватель Windows Media TEXT. foregroundColor
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694696"
---
# <a name="textforegroundcolor"></a><span data-ttu-id="26004-104">TEXT. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="26004-104">TEXT.foregroundColor</span></span>

<span data-ttu-id="26004-105">Атрибут **foregroundColor** указывает или получает цвет текста для элемента управления "текст".</span><span class="sxs-lookup"><span data-stu-id="26004-105">The **foregroundColor** attribute specifies or retrieves the text color for the Text control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="26004-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="26004-106">Possible Values</span></span>

<span data-ttu-id="26004-107">Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="26004-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="26004-108">Значение по умолчанию — "Black".</span><span class="sxs-lookup"><span data-stu-id="26004-108">The default value is "black".</span></span>

<span data-ttu-id="26004-109">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="26004-109">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

<span data-ttu-id="26004-110">При использовании **алфабленд** или **алфаблендто** с **текстовым** элементом, в котором не указан **backgroundColor** , будет использоваться цвет фона черного цвета.</span><span class="sxs-lookup"><span data-stu-id="26004-110">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="26004-111">Если цвет переднего плана также является черным (значением по умолчанию для атрибута **foregroundColor** ), текст может стать нечитаемым.</span><span class="sxs-lookup"><span data-stu-id="26004-111">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="26004-112">Чтобы избежать этого, всегда указывайте атрибут **backgroundColor** или задайте для **foregroundColor** цвет, отличный от черного.</span><span class="sxs-lookup"><span data-stu-id="26004-112">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

## <a name="requirements"></a><span data-ttu-id="26004-113">Требования</span><span class="sxs-lookup"><span data-stu-id="26004-113">Requirements</span></span>



| <span data-ttu-id="26004-114">Требование</span><span class="sxs-lookup"><span data-stu-id="26004-114">Requirement</span></span> | <span data-ttu-id="26004-115">Значение</span><span class="sxs-lookup"><span data-stu-id="26004-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="26004-116">Версия</span><span class="sxs-lookup"><span data-stu-id="26004-116">Version</span></span><br/> | <span data-ttu-id="26004-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="26004-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26004-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26004-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26004-119">**Амбиентаттрибутес. Алфабленд**</span><span class="sxs-lookup"><span data-stu-id="26004-119">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="26004-120">**Амбиентаттрибутес. Алфаблендто**</span><span class="sxs-lookup"><span data-stu-id="26004-120">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="26004-121">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="26004-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="26004-122">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="26004-122">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="26004-123">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="26004-123">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> </dl>

 

 





