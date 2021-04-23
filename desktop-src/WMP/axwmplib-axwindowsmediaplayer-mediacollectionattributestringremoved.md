---
title: Событие Медиаколлектионаттрибутестрингремовед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионаттрибутестрингремовед возникает при удалении значения атрибута из библиотеки. | Событие Медиаколлектионаттрибутестрингремовед объекта Аксвиндовсмедиаплайер
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Событие Медиаколлектионаттрибутестрингремовед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694538"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="95226-105">Событие Медиаколлектионаттрибутестрингремовед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="95226-105">MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="95226-106">Событие Медиаколлектионаттрибутестрингремовед возникает при удалении значения атрибута из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="95226-106">The MediaCollectionAttributeStringRemoved event occurs when an attribute value is removed from the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a><span data-ttu-id="95226-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="95226-107">Event Data</span></span>

<span data-ttu-id="95226-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингремоведевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="95226-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEventHandler**.</span></span> <span data-ttu-id="95226-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингремоведевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="95226-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="95226-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="95226-110">Property</span></span>           | <span data-ttu-id="95226-111">Описание</span><span class="sxs-lookup"><span data-stu-id="95226-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95226-112">**бстраттрибнаме**</span><span class="sxs-lookup"><span data-stu-id="95226-112">**bstrAttribName**</span></span> | <span data-ttu-id="95226-113">System. СтрингспеЦифиес имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="95226-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="95226-114">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="95226-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="95226-115">бстраттрибвал</span><span class="sxs-lookup"><span data-stu-id="95226-115">bstrAttribVal</span></span>      | <span data-ttu-id="95226-116">System. СтрингспеЦифиес значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="95226-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="95226-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95226-117">Remarks</span></span>

<span data-ttu-id="95226-118">При удалении элемента мультимедиа из библиотеки его метаданные удаляются из **медиаколлектион** , и это событие срабатывает для каждого удаляемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="95226-118">When a media item is removed from the library, its metadata is removed from the **MediaCollection** and this event is fired for each attribute removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="95226-119">Требования</span><span class="sxs-lookup"><span data-stu-id="95226-119">Requirements</span></span>



| <span data-ttu-id="95226-120">Требование</span><span class="sxs-lookup"><span data-stu-id="95226-120">Requirement</span></span> | <span data-ttu-id="95226-121">Значение</span><span class="sxs-lookup"><span data-stu-id="95226-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95226-122">Версия</span><span class="sxs-lookup"><span data-stu-id="95226-122">Version</span></span><br/>   | <span data-ttu-id="95226-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="95226-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="95226-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95226-124">Namespace</span></span><br/> | <span data-ttu-id="95226-125">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="95226-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="95226-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="95226-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="95226-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="95226-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95226-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95226-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95226-129">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="95226-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95226-130">**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="95226-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="95226-131">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="95226-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





