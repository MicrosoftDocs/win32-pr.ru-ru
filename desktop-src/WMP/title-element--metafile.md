---
title: Элемент TITLE (метафайл)
description: Элемент TITLE определяет текстовую строку, указывающую заголовок для элемента ASX или ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Элемент TITLE (метафайл) проигрыватель Windows Media
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708434"
---
# <a name="title-element-metafile"></a><span data-ttu-id="ef2e6-104">Элемент TITLE (метафайл)</span><span class="sxs-lookup"><span data-stu-id="ef2e6-104">TITLE Element (metafile)</span></span>

<span data-ttu-id="ef2e6-105">Элемент **Title** определяет текстовую строку, указывающую заголовок для элемента **ASX** или **entry** .</span><span class="sxs-lookup"><span data-stu-id="ef2e6-105">The **TITLE** element defines a text string specifying the title for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a><span data-ttu-id="ef2e6-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ef2e6-106">Attributes</span></span>

<span data-ttu-id="ef2e6-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ef2e6-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ef2e6-108">Parent/Child Elements</span></span>



| <span data-ttu-id="ef2e6-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="ef2e6-109">Hierarchy</span></span>       | <span data-ttu-id="ef2e6-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="ef2e6-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="ef2e6-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ef2e6-111">Parent elements</span></span> | <span data-ttu-id="ef2e6-112">**ASX**, **запись**</span><span class="sxs-lookup"><span data-stu-id="ef2e6-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="ef2e6-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ef2e6-113">Child elements</span></span>  | <span data-ttu-id="ef2e6-114">Нет</span><span class="sxs-lookup"><span data-stu-id="ef2e6-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="ef2e6-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="ef2e6-115">Remarks</span></span>

<span data-ttu-id="ef2e6-116">Этот элемент определяет текстовую строку, указывающую заголовок элемента **ASX** или **entry** .</span><span class="sxs-lookup"><span data-stu-id="ef2e6-116">This element defines a text string that specifies the title of an **ASX** or **ENTRY** element.</span></span> <span data-ttu-id="ef2e6-117">Заголовок отображается на панели отображения и в диалоговом окне **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="ef2e6-117">The title is displayed in the display panel and **Properties** dialog box.</span></span>

<span data-ttu-id="ef2e6-118">Когда этот элемент появляется внутри элемента **ASX** , он отображается как **Показать** информацию.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-118">When this element appears within an **ASX** element, the text is displayed as **Show** information.</span></span> <span data-ttu-id="ef2e6-119">Когда этот элемент появляется в элементе **entry** , он отображается как сведения об **обрезке** .</span><span class="sxs-lookup"><span data-stu-id="ef2e6-119">When this element appears within an **ENTRY** element, the text is displayed as **Clip** information.</span></span>

<span data-ttu-id="ef2e6-120">Если элемент **мореинфо** также используется со связанным (родительским) элементом, это текст заголовка, который пользователь щелкает для доступа к URL-адресу, определенному в элементе **мореинфо** .</span><span class="sxs-lookup"><span data-stu-id="ef2e6-120">If a **MOREINFO** element is also used with the associated (parent) element, it is the title text that the user clicks to access the URL defined in the **MOREINFO** element.</span></span>

<span data-ttu-id="ef2e6-121">Каждый родительский элемент **ASX** и **entry** должен содержать не более одного дочернего элемента **Title** .</span><span class="sxs-lookup"><span data-stu-id="ef2e6-121">Each parent **ASX** and **ENTRY** element should contain at most one child **TITLE** element.</span></span> <span data-ttu-id="ef2e6-122">Несколько элементов **Title** после первого будут пропущены и не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="ef2e6-122">Multiple **TITLE** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="ef2e6-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="ef2e6-123">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="ef2e6-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ef2e6-124">Requirements</span></span>



| <span data-ttu-id="ef2e6-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ef2e6-125">Requirement</span></span> | <span data-ttu-id="ef2e6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ef2e6-126">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="ef2e6-127">Версия</span><span class="sxs-lookup"><span data-stu-id="ef2e6-127">Version</span></span><br/> | <span data-ttu-id="ef2e6-128">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ef2e6-128">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef2e6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef2e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2e6-130">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ef2e6-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ef2e6-131">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ef2e6-131">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





