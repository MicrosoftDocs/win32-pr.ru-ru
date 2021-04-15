---
title: Элемент REPEAT
description: Элемент REPEAT определяет, сколько раз проигрыватель Windows Media повторяет один или несколько элементов ENTRY или ЕНТРИРЕФ.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- ПОВТОРЯЮЩИйся элемент проигрыватель Windows Media
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648963"
---
# <a name="repeat-element"></a><span data-ttu-id="b8db4-104">Элемент REPEAT</span><span class="sxs-lookup"><span data-stu-id="b8db4-104">REPEAT Element</span></span>

<span data-ttu-id="b8db4-105">Элемент **Repeat** определяет, сколько раз проигрыватель Windows Media повторяет один или несколько элементов **entry** или **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="b8db4-105">The **REPEAT** element defines the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a><span data-ttu-id="b8db4-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b8db4-106">Attributes</span></span>

<span data-ttu-id="b8db4-107">**COUNT**</span><span class="sxs-lookup"><span data-stu-id="b8db4-107">**COUNT**</span></span>

<span data-ttu-id="b8db4-108">Целое число, представляющее количество повторов в проигрывателе Windows Media элементов **entry** и **ентриреф** в области действия этого элемента.</span><span class="sxs-lookup"><span data-stu-id="b8db4-108">Integer representing the number of times Windows Media Player repeats the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b8db4-109">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b8db4-109">Parent/Child Elements</span></span>



| <span data-ttu-id="b8db4-110">Иерархия</span><span class="sxs-lookup"><span data-stu-id="b8db4-110">Hierarchy</span></span>       | <span data-ttu-id="b8db4-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="b8db4-111">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="b8db4-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b8db4-112">Parent elements</span></span> | <span data-ttu-id="b8db4-113">**ASX**</span><span class="sxs-lookup"><span data-stu-id="b8db4-113">**ASX**</span></span>                 |
| <span data-ttu-id="b8db4-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b8db4-114">Child elements</span></span>  | <span data-ttu-id="b8db4-115">**запись**, **ентриреф**</span><span class="sxs-lookup"><span data-stu-id="b8db4-115">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b8db4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8db4-116">Remarks</span></span>

<span data-ttu-id="b8db4-117">Этот элемент определяет число повторов в проигрывателе Windows Media Player или цикл по элементам, которые задаются элементами **entry** и **ентриреф** в области действия этого элемента.</span><span class="sxs-lookup"><span data-stu-id="b8db4-117">This element defines the number of times Windows Media Player repeats, or loops through, the clips defined by the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span> <span data-ttu-id="b8db4-118">Допустим только первый элемент **Repeat** в метафайле; последующие элементы **Repeat** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b8db4-118">Only the first **REPEAT** element in a metafile is valid; subsequent **REPEAT** elements are ignored.</span></span>

<span data-ttu-id="b8db4-119">Если атрибут **Count** не определен, содержимое связанных элементов **entry** и **ентриреф** повторяется бесконечное число раз.</span><span class="sxs-lookup"><span data-stu-id="b8db4-119">If no **COUNT** attribute is defined, the content in the associated **ENTRY** and **ENTRYREF** elements repeats an infinite number of times.</span></span> <span data-ttu-id="b8db4-120">Нулевое значение приводит к тому, что проигрыватель Windows Media игнорирует элемент **Repeat** и воспроизводит содержимое один раз.</span><span class="sxs-lookup"><span data-stu-id="b8db4-120">A value of zero causes Windows Media Player to ignore the **REPEAT** element and play the content once.</span></span>

## <a name="examples"></a><span data-ttu-id="b8db4-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="b8db4-121">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="b8db4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b8db4-122">Requirements</span></span>



| <span data-ttu-id="b8db4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b8db4-123">Requirement</span></span> | <span data-ttu-id="b8db4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b8db4-124">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b8db4-125">Версия</span><span class="sxs-lookup"><span data-stu-id="b8db4-125">Version</span></span><br/> | <span data-ttu-id="b8db4-126">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b8db4-126">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8db4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8db4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8db4-128">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b8db4-128">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b8db4-129">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b8db4-129">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





