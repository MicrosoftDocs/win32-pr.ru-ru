---
title: Амбиентаттрибутес. Алфабленд
description: Атрибут Алфабленд указывает или получает значение для альфа-смешения любого представления, подпредставления или мини-приложения пользовательского интерфейса.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Алфабленд
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698932"
---
# <a name="ambientattributesalphablend"></a><span data-ttu-id="d16ea-104">Амбиентаттрибутес. Алфабленд</span><span class="sxs-lookup"><span data-stu-id="d16ea-104">AmbientAttributes.alphaBlend</span></span>

<span data-ttu-id="d16ea-105">Атрибут **алфабленд** указывает или получает значение для альфа-смешения любого **представления**, **подпредставления** или мини-приложения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d16ea-105">The **alphaBlend** attribute specifies or retrieves a value for alpha blending any **VIEW**, **SUBVIEW**, or UI widget.</span></span>

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a><span data-ttu-id="d16ea-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d16ea-106">Possible Values</span></span>

<span data-ttu-id="d16ea-107">Этот атрибут является **числом** для чтения и записи (**длинное**) со значением в диапазоне от 0 (без непрозрачности) до 255 (полная непрозрачность) и значением по умолчанию 255.</span><span class="sxs-lookup"><span data-stu-id="d16ea-107">This attribute is a read/write **Number** (**long**) with a value ranging from 0 (no opacity) to 255 (full opacity) and a default value of 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="d16ea-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d16ea-108">Remarks</span></span>

<span data-ttu-id="d16ea-109">Этот атрибут позволяет элементу отображаться полупрозрачным, в зависимости от объема непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="d16ea-109">This attribute allows an element to appear semitransparent, depending on the amount of opacity set.</span></span> <span data-ttu-id="d16ea-110">Чем меньше непрозрачность, тем более прозрачным будет элемент.</span><span class="sxs-lookup"><span data-stu-id="d16ea-110">The less opacity, the more transparent the element will appear.</span></span> <span data-ttu-id="d16ea-111">Каждый элемент обложки может иметь отдельное значение прозрачности, за исключением элементов Button в элементе управления **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="d16ea-111">Each element in the skin can have a separate opacity value except for button elements in a **BUTTONGROUP** control.</span></span> <span data-ttu-id="d16ea-112">Если **алфабленд** задан в **представлении**, будет задано непрозрачность всей обложки.</span><span class="sxs-lookup"><span data-stu-id="d16ea-112">When **alphaBlend** is set in **VIEW**, the opacity of the entire skin will be set.</span></span> <span data-ttu-id="d16ea-113">Альфа-смешение не будет работать для оконных элементов управления, включая **списки воспроизведения**, **эффекты**, **списки**, **всплывающие подсказки**, **EDITBOX** и **видео** (если **окно без окон** имеет значение false).</span><span class="sxs-lookup"><span data-stu-id="d16ea-113">Alpha blend will not work for windowed controls, including **PLAYLIST**, **EFFECTS**, **LISTBOX**, **POPUP**, **EDITBOX**, and **VIDEO** (if **windowless** is set to false).</span></span> <span data-ttu-id="d16ea-114">Если для **представления** задано значение **алфабленд** , вся Обложка становится прозрачной.</span><span class="sxs-lookup"><span data-stu-id="d16ea-114">When **alphaBlend** is set on **VIEW**, the whole skin becomes transparent.</span></span> <span data-ttu-id="d16ea-115">Атрибуты **транспаренциколор** , используемые несколькими элементами, не поддерживаются в **алфабленд**.</span><span class="sxs-lookup"><span data-stu-id="d16ea-115">The **transparencyColor** attributes used by several elements are not supported with **alphaBlend**.</span></span>

<span data-ttu-id="d16ea-116">При использовании **алфабленд** с **текстовым** элементом, для которого не указан **backgroundColor** , будет использоваться цвет фона черного цвета.</span><span class="sxs-lookup"><span data-stu-id="d16ea-116">When you use **alphaBlend** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="d16ea-117">Если цвет переднего плана также является черным (значением по умолчанию для *текста*).**foregroundColor**), текст может стать нечитаемым.</span><span class="sxs-lookup"><span data-stu-id="d16ea-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="d16ea-118">Чтобы избежать этого, всегда указывайте атрибут **backgroundColor** или задайте для **foregroundColor** цвет, отличный от черного.</span><span class="sxs-lookup"><span data-stu-id="d16ea-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="d16ea-119">Этот атрибут не поддерживается в Windows 98.</span><span class="sxs-lookup"><span data-stu-id="d16ea-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d16ea-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d16ea-120">Requirements</span></span>



| <span data-ttu-id="d16ea-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d16ea-121">Requirement</span></span> | <span data-ttu-id="d16ea-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d16ea-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d16ea-123">Версия</span><span class="sxs-lookup"><span data-stu-id="d16ea-123">Version</span></span><br/> | <span data-ttu-id="d16ea-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d16ea-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d16ea-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d16ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16ea-126">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="d16ea-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="d16ea-127">**Амбиентаттрибутес. Алфаблендто**</span><span class="sxs-lookup"><span data-stu-id="d16ea-127">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="d16ea-128">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="d16ea-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="d16ea-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="d16ea-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="d16ea-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="d16ea-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





