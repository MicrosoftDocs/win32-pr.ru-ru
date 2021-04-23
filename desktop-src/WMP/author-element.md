---
title: AUTHOR, элемент
description: Элемент AUTHOR содержит имя автора метафайла Windows Media или клипа мультимедиа.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Проигрыватель Windows Media, элемент AUTHOR
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694638"
---
# <a name="author-element"></a><span data-ttu-id="bd5e2-104">AUTHOR, элемент</span><span class="sxs-lookup"><span data-stu-id="bd5e2-104">AUTHOR Element</span></span>

<span data-ttu-id="bd5e2-105">Элемент **Author** содержит имя автора метафайла Windows Media или клипа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bd5e2-105">The **AUTHOR** element contains the name of the author of a Windows Media metafile or media clip.</span></span>

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a><span data-ttu-id="bd5e2-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bd5e2-106">Attributes</span></span>

<span data-ttu-id="bd5e2-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="bd5e2-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="bd5e2-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bd5e2-108">Parent/Child Elements</span></span>



| <span data-ttu-id="bd5e2-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="bd5e2-109">Hierarchy</span></span>       | <span data-ttu-id="bd5e2-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="bd5e2-110">Element</span></span>            |
|-----------------|--------------------|
| <span data-ttu-id="bd5e2-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bd5e2-111">Parent elements</span></span> | <span data-ttu-id="bd5e2-112">**ASX**, **запись**</span><span class="sxs-lookup"><span data-stu-id="bd5e2-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="bd5e2-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bd5e2-113">Child elements</span></span>  | <span data-ttu-id="bd5e2-114">Нет</span><span class="sxs-lookup"><span data-stu-id="bd5e2-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="bd5e2-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="bd5e2-115">Remarks</span></span>

<span data-ttu-id="bd5e2-116">Этот элемент содержит текстовую строку, представляющую имя автора метафайла Windows Media или клипа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bd5e2-116">This element contains a text string representing the name of the author of a Windows Media metafile or media clip.</span></span> <span data-ttu-id="bd5e2-117">Элемент **Author** можно использовать внутри элемента **ASX** и в элементах **entry** .</span><span class="sxs-lookup"><span data-stu-id="bd5e2-117">You can use the **AUTHOR** element within the **ASX** element and within **ENTRY** elements.</span></span>

<span data-ttu-id="bd5e2-118">Если этот элемент отображается в элементе **ASX** , то текст отображается как **Показать** информацию.</span><span class="sxs-lookup"><span data-stu-id="bd5e2-118">If this element appears in the **ASX** element, the text is displayed as **Show** information.</span></span>

<span data-ttu-id="bd5e2-119">Если этот элемент встречается в элементе **entry** , то текст отображается как Автор клипа.</span><span class="sxs-lookup"><span data-stu-id="bd5e2-119">If this element appears in an **ENTRY** element, the text is displayed as the clip author.</span></span>

<span data-ttu-id="bd5e2-120">Каждый родительский элемент **ASX** и **entry** должен содержать не более одного дочернего элемента **Author** .</span><span class="sxs-lookup"><span data-stu-id="bd5e2-120">Each parent **ASX** and **ENTRY** element should contain at most one child **AUTHOR** element.</span></span> <span data-ttu-id="bd5e2-121">Несколько элементов **Author** после первого будут пропущены и не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="bd5e2-121">Multiple **AUTHOR** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="bd5e2-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="bd5e2-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="bd5e2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="bd5e2-123">Requirements</span></span>



| <span data-ttu-id="bd5e2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="bd5e2-124">Requirement</span></span> | <span data-ttu-id="bd5e2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="bd5e2-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="bd5e2-126">Версия</span><span class="sxs-lookup"><span data-stu-id="bd5e2-126">Version</span></span><br/> | <span data-ttu-id="bd5e2-127">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="bd5e2-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd5e2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd5e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5e2-129">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bd5e2-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="bd5e2-130">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bd5e2-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





