---
title: АБСТРАКТный элемент
description: АБСТРАКТный элемент содержит текст, описывающий связанный элемент ASX, BANNER или ENTRY.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- АБСТРАКТный элемент Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698854"
---
# <a name="abstract-element"></a><span data-ttu-id="76e05-104">АБСТРАКТный элемент</span><span class="sxs-lookup"><span data-stu-id="76e05-104">ABSTRACT Element</span></span>

<span data-ttu-id="76e05-105">**Абстрактный** элемент содержит текст, описывающий связанный элемент **ASX**, **Banner** или **entry** .</span><span class="sxs-lookup"><span data-stu-id="76e05-105">The **ABSTRACT** element contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a><span data-ttu-id="76e05-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="76e05-106">Attributes</span></span>

<span data-ttu-id="76e05-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="76e05-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="76e05-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="76e05-108">Parent/Child Elements</span></span>



| <span data-ttu-id="76e05-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="76e05-109">Hierarchy</span></span> | <span data-ttu-id="76e05-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="76e05-110">Elements</span></span>                       |
|-----------|--------------------------------|
| <span data-ttu-id="76e05-111">Parent</span><span class="sxs-lookup"><span data-stu-id="76e05-111">Parent</span></span>    | <span data-ttu-id="76e05-112">**ASX**, **запись**, **баннер**</span><span class="sxs-lookup"><span data-stu-id="76e05-112">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="76e05-113">Дочерний</span><span class="sxs-lookup"><span data-stu-id="76e05-113">Child</span></span>     | <span data-ttu-id="76e05-114">None</span><span class="sxs-lookup"><span data-stu-id="76e05-114">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="76e05-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="76e05-115">Remarks</span></span>

<span data-ttu-id="76e05-116">Если этот элемент встречается в элементе **ASX** , то текст отображается как подсказка при наведении курсора мыши на заголовок показать.</span><span class="sxs-lookup"><span data-stu-id="76e05-116">If this element appears within an **ASX** element, the text displays as a ToolTip when the mouse hovers over the show title.</span></span>

<span data-ttu-id="76e05-117">Если этот элемент встречается в элементе **entry** , текст отображается в виде подсказки при наведении указателя мыши на заголовок клипа.</span><span class="sxs-lookup"><span data-stu-id="76e05-117">If this element appears within an **ENTRY** element, the text displays as a ToolTip when the mouse hovers over the clip title.</span></span>

<span data-ttu-id="76e05-118">Если этот элемент встречается в элементе **баннера** , текст отображается в виде подсказки для изображения баннера.</span><span class="sxs-lookup"><span data-stu-id="76e05-118">If this element appears within a **BANNER** element, the text displays as a ToolTip for the banner graphic.</span></span>

<span data-ttu-id="76e05-119">Используйте только один **абстрактный** элемент для области.</span><span class="sxs-lookup"><span data-stu-id="76e05-119">Use only one **ABSTRACT** element per scope.</span></span> <span data-ttu-id="76e05-120">При обработке файла метафайла используется только первый **абстрактный** элемент в области другого элемента.</span><span class="sxs-lookup"><span data-stu-id="76e05-120">Only the first **ABSTRACT** element within the scope of another element is used when a metafile file is processed.</span></span> <span data-ttu-id="76e05-121">Все последующие **абстрактные** элементы в этой области игнорируются.</span><span class="sxs-lookup"><span data-stu-id="76e05-121">Any subsequent **ABSTRACT** elements in that scope are ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="76e05-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="76e05-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="76e05-123">Требования</span><span class="sxs-lookup"><span data-stu-id="76e05-123">Requirements</span></span>



| <span data-ttu-id="76e05-124">Требование</span><span class="sxs-lookup"><span data-stu-id="76e05-124">Requirement</span></span> | <span data-ttu-id="76e05-125">Значение</span><span class="sxs-lookup"><span data-stu-id="76e05-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="76e05-126">Версия</span><span class="sxs-lookup"><span data-stu-id="76e05-126">Version</span></span><br/> | <span data-ttu-id="76e05-127">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="76e05-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76e05-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76e05-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76e05-129">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="76e05-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="76e05-130">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="76e05-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





