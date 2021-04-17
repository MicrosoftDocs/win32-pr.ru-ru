---
title: ПРЕВИЕВДУРАТИОН, элемент
description: Элемент ПРЕВИЕВДУРАТИОН определяет продолжительность воспроизведения клипа в режиме предварительного просмотра.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Проигрыватель Windows Media, элемент ПРЕВИЕВДУРАТИОН
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704189"
---
# <a name="previewduration-element"></a><span data-ttu-id="176c6-104">ПРЕВИЕВДУРАТИОН, элемент</span><span class="sxs-lookup"><span data-stu-id="176c6-104">PREVIEWDURATION Element</span></span>

<span data-ttu-id="176c6-105">Элемент **превиевдуратион** определяет продолжительность воспроизведения клипа в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="176c6-105">The **PREVIEWDURATION** element defines the length of time a clip plays in preview mode.</span></span>

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="176c6-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="176c6-106">Attributes</span></span>

<span data-ttu-id="176c6-107">**Значение** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="176c6-107">**VALUE** (required)</span></span>

<span data-ttu-id="176c6-108">Продолжительность времени (в часах, минутах, секундах и сотых долях секунды), воспроизводимой клипом в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="176c6-108">Length of time (in hours, minutes, seconds, and hundredths of a second) that the clip plays in preview mode.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="176c6-109">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="176c6-109">Parent/Child Elements</span></span>



| <span data-ttu-id="176c6-110">Иерархия</span><span class="sxs-lookup"><span data-stu-id="176c6-110">Hierarchy</span></span>       | <span data-ttu-id="176c6-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="176c6-111">Elements</span></span>                    |
|-----------------|-----------------------------|
| <span data-ttu-id="176c6-112">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="176c6-112">Parent elements</span></span> | <span data-ttu-id="176c6-113">**ASX**, **запись**, **ссылка**</span><span class="sxs-lookup"><span data-stu-id="176c6-113">**ASX**, **ENTRY**, **REF**</span></span> |
| <span data-ttu-id="176c6-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="176c6-114">Child elements</span></span>  | <span data-ttu-id="176c6-115">Нет</span><span class="sxs-lookup"><span data-stu-id="176c6-115">None</span></span>                        |



 

## <a name="remarks"></a><span data-ttu-id="176c6-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="176c6-116">Remarks</span></span>

<span data-ttu-id="176c6-117">Этот элемент определяет продолжительность времени воспроизведения клипа в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="176c6-117">This element defines the length of time that a clip plays in preview mode.</span></span> <span data-ttu-id="176c6-118">Если этот элемент встречается в элементе **entry** или **ref** , он применяется к картинке, определенной этим элементом.</span><span class="sxs-lookup"><span data-stu-id="176c6-118">If this element appears within an **ENTRY** element or a **REF** element, it applies to the clip defined by that element.</span></span> <span data-ttu-id="176c6-119">Если он присутствует в области элемента **ASX** , он применяется к каждому клипу в метафайле.</span><span class="sxs-lookup"><span data-stu-id="176c6-119">If it appears within the scope of an **ASX** element, it applies to every clip in the metafile.</span></span> <span data-ttu-id="176c6-120">Элемент **превиевдуратион** в **ссылочном** элементе имеет приоритет **над элементом записи, и** либо имеет приоритет над элементами **превиевдуратион** в элементе **ASX** .</span><span class="sxs-lookup"><span data-stu-id="176c6-120">A **PREVIEWDURATION** element in a **REF** element takes precedence over one in an ENTRY **element**, and either takes precedence over a **PREVIEWDURATION** element in an **ASX** element.</span></span> <span data-ttu-id="176c6-121">Если для клипа не определен ни один элемент **превиевдуратион** , время просмотра по умолчанию составляет 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="176c6-121">If no **PREVIEWDURATION** element is defined for a clip, the default preview time is 10 seconds.</span></span>

<span data-ttu-id="176c6-122">Если для клипа имеется элемент **StartTime** или **Стартмаркер** , проигрыватель Windows Media визуализирует клип, начиная с точки, определенной одним из этих элементов. в противном случае он визуализируется с начала клипа.</span><span class="sxs-lookup"><span data-stu-id="176c6-122">If there is a **STARTTIME** or **STARTMARKER** element for the clip, Windows Media Player renders the clip starting at the point defined by one of these elements; otherwise it renders from the beginning of the clip.</span></span> <span data-ttu-id="176c6-123">Если этот клип короче времени, определенного элементом **превиевдуратион** , он останавливается.</span><span class="sxs-lookup"><span data-stu-id="176c6-123">The clip stops normally if it is shorter than the time defined by the **PREVIEWDURATION** element.</span></span>

<span data-ttu-id="176c6-124">Элемент **DURATION** переопределяет элемент **превиевдуратион** .</span><span class="sxs-lookup"><span data-stu-id="176c6-124">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="176c6-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="176c6-125">Examples</span></span>


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="176c6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="176c6-126">Requirements</span></span>



| <span data-ttu-id="176c6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="176c6-127">Requirement</span></span> | <span data-ttu-id="176c6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="176c6-128">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="176c6-129">Версия</span><span class="sxs-lookup"><span data-stu-id="176c6-129">Version</span></span><br/> | <span data-ttu-id="176c6-130">Проигрыватель Windows Media версии 70 или более поздней</span><span class="sxs-lookup"><span data-stu-id="176c6-130">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="176c6-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="176c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="176c6-132">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="176c6-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="176c6-133">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="176c6-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





