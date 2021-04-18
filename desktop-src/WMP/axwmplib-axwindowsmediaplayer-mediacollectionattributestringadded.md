---
title: Событие Медиаколлектионаттрибутестрингаддед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионаттрибутестрингаддед возникает при добавлении значения атрибута в библиотеку. | Событие Медиаколлектионаттрибутестрингаддед объекта Аксвиндовсмедиаплайер
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Событие Медиаколлектионаттрибутестрингаддед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694594"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="38fe1-105">Событие Медиаколлектионаттрибутестрингаддед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="38fe1-105">MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="38fe1-106">Событие Медиаколлектионаттрибутестрингаддед возникает при добавлении значения атрибута в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="38fe1-106">The MediaCollectionAttributeStringAdded event occurs when an attribute value is added to the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a><span data-ttu-id="38fe1-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="38fe1-107">Event Data</span></span>

<span data-ttu-id="38fe1-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингаддедевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEventHandler**.</span></span> <span data-ttu-id="38fe1-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингаддедевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="38fe1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="38fe1-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="38fe1-110">Property</span></span>           | <span data-ttu-id="38fe1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="38fe1-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38fe1-112">**бстраттрибнаме**</span><span class="sxs-lookup"><span data-stu-id="38fe1-112">**bstrAttribName**</span></span> | <span data-ttu-id="38fe1-113">System. СтрингспеЦифиес имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="38fe1-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="38fe1-114">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="38fe1-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="38fe1-115">бстраттрибвал</span><span class="sxs-lookup"><span data-stu-id="38fe1-115">bstrAttribVal</span></span>      | <span data-ttu-id="38fe1-116">System. СтрингспеЦифиес значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="38fe1-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="38fe1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38fe1-117">Remarks</span></span>

<span data-ttu-id="38fe1-118">При добавлении элемента мультимедиа в библиотеку его метаданные добавляются в коллекцию носителей, и это событие срабатывает для каждого добавленного атрибута.</span><span class="sxs-lookup"><span data-stu-id="38fe1-118">When a media item is added to the library, its metadata is added to the media collection and this event is fired for each attribute added.</span></span>

## <a name="requirements"></a><span data-ttu-id="38fe1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="38fe1-119">Requirements</span></span>



| <span data-ttu-id="38fe1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="38fe1-120">Requirement</span></span> | <span data-ttu-id="38fe1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="38fe1-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38fe1-122">Версия</span><span class="sxs-lookup"><span data-stu-id="38fe1-122">Version</span></span><br/>   | <span data-ttu-id="38fe1-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="38fe1-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="38fe1-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38fe1-124">Namespace</span></span><br/> | <span data-ttu-id="38fe1-125">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="38fe1-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="38fe1-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="38fe1-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="38fe1-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="38fe1-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38fe1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38fe1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38fe1-129">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="38fe1-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="38fe1-130">**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="38fe1-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="38fe1-131">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="38fe1-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





