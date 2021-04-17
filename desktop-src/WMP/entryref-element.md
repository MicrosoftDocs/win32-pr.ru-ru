---
title: ЕНТРИРЕФ, элемент
description: Элемент ЕНТРИРЕФ указывает на элементы записи во внешнем метафайле.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Проигрыватель Windows Media, элемент ЕНТРИРЕФ
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694625"
---
# <a name="entryref-element"></a><span data-ttu-id="b71f3-104">ЕНТРИРЕФ, элемент</span><span class="sxs-lookup"><span data-stu-id="b71f3-104">ENTRYREF Element</span></span>

<span data-ttu-id="b71f3-105">Элемент **ентриреф** указывает на элементы **записи** во внешнем метафайле.</span><span class="sxs-lookup"><span data-stu-id="b71f3-105">The **ENTRYREF** element points to the **ENTRY** elements in an external metafile.</span></span>

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="b71f3-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b71f3-106">Attributes</span></span>

<span data-ttu-id="b71f3-107">**Href** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b71f3-107">**HREF** (required)</span></span>

<span data-ttu-id="b71f3-108">URL-адрес метафайла, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="b71f3-108">URL to a referenced metafile.</span></span>

<span data-ttu-id="b71f3-109">**клиентбинд**</span><span class="sxs-lookup"><span data-stu-id="b71f3-109">**CLIENTBIND**</span></span>

<span data-ttu-id="b71f3-110">Этот атрибут больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b71f3-110">This attribute is no longer supported.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b71f3-111">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b71f3-111">Parent/Child Elements</span></span>



| <span data-ttu-id="b71f3-112">Иерархия</span><span class="sxs-lookup"><span data-stu-id="b71f3-112">Hierarchy</span></span>       | <span data-ttu-id="b71f3-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="b71f3-113">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="b71f3-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b71f3-114">Parent elements</span></span> | <span data-ttu-id="b71f3-115">**ASX**, **событие**, **Повтор**</span><span class="sxs-lookup"><span data-stu-id="b71f3-115">**ASX**, **EVENT**, **REPEAT**</span></span> |
| <span data-ttu-id="b71f3-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b71f3-116">Child elements</span></span>  | <span data-ttu-id="b71f3-117">Нет</span><span class="sxs-lookup"><span data-stu-id="b71f3-117">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="b71f3-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="b71f3-118">Remarks</span></span>

<span data-ttu-id="b71f3-119">Этот элемент указывает на содержимое внешнего метафайла.</span><span class="sxs-lookup"><span data-stu-id="b71f3-119">This element points to the contents of an external metafile.</span></span> <span data-ttu-id="b71f3-120">Проигрыватель Windows Media обрабатывает элементы **записи** метафайла, на который указывает ссылка, как если бы они были добавлены в основной метафайл в позиции элемента **ентриреф** .</span><span class="sxs-lookup"><span data-stu-id="b71f3-120">Windows Media Player processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="b71f3-121">Однако он пропускает все элементы **записи** в метафайле, на который указывает ссылка, для которого атрибут **СКИПИФРЕФ** имеет значение Да.</span><span class="sxs-lookup"><span data-stu-id="b71f3-121">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="b71f3-122">Проигрыватель Windows Media 7,0, 7,1 и проигрыватель Windows Media для Windows XP игнорируют все элементы **ентриреф** в метафайле, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="b71f3-122">Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="b71f3-123">Поэтому при использовании этих версий проигрывателя метафайлы могут быть вложены только на один уровень глубже.</span><span class="sxs-lookup"><span data-stu-id="b71f3-123">Thus, metafiles can only be nested one level deep when using these versions of the Player.</span></span> <span data-ttu-id="b71f3-124">Проигрыватель Windows Media также игнорирует элемент **ASX** в файле, на который указывает ссылка, вместе с его атрибутами.</span><span class="sxs-lookup"><span data-stu-id="b71f3-124">Windows Media Player also ignores the **ASX** element in the referenced file along with its attributes.</span></span> <span data-ttu-id="b71f3-125">Проигрыватель Windows Media 9 Series или более поздней версии поддерживает вложение метафайлов размером до пяти уровней.</span><span class="sxs-lookup"><span data-stu-id="b71f3-125">Windows Media Player 9 Series or later supports nesting metafiles up to five levels deep.</span></span>

<span data-ttu-id="b71f3-126">URL-адрес, указанный в атрибуте **href** , станет базовым URL-адресом для всех относительных URL-адресов во внешнем метафайле.</span><span class="sxs-lookup"><span data-stu-id="b71f3-126">The URL specified in the **HREF** attribute becomes the base URL for any relative URLs in the external metafile.</span></span> <span data-ttu-id="b71f3-127">Этот URL-адрес используется, когда воспроизводится запись из внешнего метафайла и пользователь добавляет его в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b71f3-127">This URL is used when an entry from the external metafile is playing and the user adds it to the library.</span></span>

## <a name="examples"></a><span data-ttu-id="b71f3-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="b71f3-128">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="b71f3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b71f3-129">Requirements</span></span>



| <span data-ttu-id="b71f3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b71f3-130">Requirement</span></span> | <span data-ttu-id="b71f3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b71f3-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b71f3-132">Версия</span><span class="sxs-lookup"><span data-stu-id="b71f3-132">Version</span></span><br/> | <span data-ttu-id="b71f3-133">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b71f3-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b71f3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b71f3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b71f3-135">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b71f3-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b71f3-136">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b71f3-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





