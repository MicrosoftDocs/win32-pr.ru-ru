---
title: Элемент COPYRIGHT (Мсфидс. h)
description: Элемент COPYRIGHT определяет текстовую строку, указывающую сведения об авторских правах для элемента ASX или ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Проигрыватель Windows Media, элемент об АВТОРских правах
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698788"
---
# <a name="copyright-element"></a><span data-ttu-id="71e11-104">Элемент COPYRIGHT</span><span class="sxs-lookup"><span data-stu-id="71e11-104">COPYRIGHT Element</span></span>

<span data-ttu-id="71e11-105">Элемент **Copyright** определяет текстовую строку, указывающую сведения об авторских правах для элемента **ASX** или **entry** .</span><span class="sxs-lookup"><span data-stu-id="71e11-105">The **COPYRIGHT** element defines a text string specifying the copyright information for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a><span data-ttu-id="71e11-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="71e11-106">Attributes</span></span>

<span data-ttu-id="71e11-107">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="71e11-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="71e11-108">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="71e11-108">Parent/Child Elements</span></span>



| <span data-ttu-id="71e11-109">Иерархия</span><span class="sxs-lookup"><span data-stu-id="71e11-109">Hierarchy</span></span>       | <span data-ttu-id="71e11-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="71e11-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="71e11-111">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="71e11-111">Parent elements</span></span> | <span data-ttu-id="71e11-112">**ASX**, **запись**</span><span class="sxs-lookup"><span data-stu-id="71e11-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="71e11-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="71e11-113">Child elements</span></span>  | <span data-ttu-id="71e11-114">Нет</span><span class="sxs-lookup"><span data-stu-id="71e11-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="71e11-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="71e11-115">Remarks</span></span>

<span data-ttu-id="71e11-116">Этот элемент определяет текстовую строку, указывающую сведения об авторских правах для элемента **ASX** или **entry** .</span><span class="sxs-lookup"><span data-stu-id="71e11-116">This element defines a text string that specifies the copyright information for an **ASX** or **ENTRY** element.</span></span>

<span data-ttu-id="71e11-117">Когда этот элемент появляется в элементе **ASX** , строка авторского права отображается только как **Показать** информацию.</span><span class="sxs-lookup"><span data-stu-id="71e11-117">When this element appears within an **ASX** element, the copyright string is displayed only as **Show** information.</span></span> <span data-ttu-id="71e11-118">Когда этот элемент появляется в элементе **entry** , он отображается как сведения об обрезке.</span><span class="sxs-lookup"><span data-stu-id="71e11-118">When this element appears within an **ENTRY** element, the text is displayed as clip information.</span></span> <span data-ttu-id="71e11-119">Каждый родительский элемент **ASX** и **entry** должен содержать не более одного дочернего элемента **Copyright** .</span><span class="sxs-lookup"><span data-stu-id="71e11-119">Each parent **ASX** and **ENTRY** element should contain at most one child **COPYRIGHT** element.</span></span> <span data-ttu-id="71e11-120">Несколько элементов **авторского права** после первого будут пропущены и не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="71e11-120">Multiple **COPYRIGHT** elements after the first will be ignored and will not be displayed.</span></span>

<span data-ttu-id="71e11-121">Символы для авторского права и символов регистрации товарного знака (или) могут отображаться неправильно, если метафайл не кодируется с помощью схемы кодировки UTF-8.</span><span class="sxs-lookup"><span data-stu-id="71e11-121">The characters for copyright and trademark registration symbols (   or   ) may not display properly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="71e11-122">В этом случае для правильного вывода любого из этих символов для всех пользователей можно использовать эквиваленты ASCII (c) и (R).</span><span class="sxs-lookup"><span data-stu-id="71e11-122">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (R) instead.</span></span>

<span data-ttu-id="71e11-123">Если метафайл кодируется с помощью UTF-8, то авторские знаки и символы товарных знаков будут отображаться правильно.</span><span class="sxs-lookup"><span data-stu-id="71e11-123">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="71e11-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="71e11-124">Examples</span></span>


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a><span data-ttu-id="71e11-125">Требования</span><span class="sxs-lookup"><span data-stu-id="71e11-125">Requirements</span></span>



| <span data-ttu-id="71e11-126">Требование</span><span class="sxs-lookup"><span data-stu-id="71e11-126">Requirement</span></span> | <span data-ttu-id="71e11-127">Значение</span><span class="sxs-lookup"><span data-stu-id="71e11-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71e11-128">Версия</span><span class="sxs-lookup"><span data-stu-id="71e11-128">Version</span></span><br/> | <span data-ttu-id="71e11-129">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="71e11-129">Windows Media Player version 7.0 or later</span></span><br/>                                 |
| <span data-ttu-id="71e11-130">Header</span><span class="sxs-lookup"><span data-stu-id="71e11-130">Header</span></span><br/>  | <dl> <span data-ttu-id="71e11-131"><dt>Мсфидс. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e11-131"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e11-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71e11-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e11-133">**Добавление символов авторского права в метафайлы**</span><span class="sxs-lookup"><span data-stu-id="71e11-133">**Adding Copyright Characters to Metafiles**</span></span>](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[<span data-ttu-id="71e11-134">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="71e11-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="71e11-135">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="71e11-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





