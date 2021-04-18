---
title: Событие Медиаколлектионаттрибутестрингчанжед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионаттрибутестрингчанжед возникает при изменении значения атрибута в библиотеке. | Событие Медиаколлектионаттрибутестрингчанжед объекта Аксвиндовсмедиаплайер
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Событие Медиаколлектионаттрибутестрингчанжед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699017"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ce7fd-105">Событие Медиаколлектионаттрибутестрингчанжед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="ce7fd-105">MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ce7fd-106">Событие Медиаколлектионаттрибутестрингчанжед возникает при изменении значения атрибута в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="ce7fd-106">The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a><span data-ttu-id="ce7fd-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="ce7fd-107">Event Data</span></span>

<span data-ttu-id="ce7fd-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингчанжедевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="ce7fd-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEventHandler**.</span></span> <span data-ttu-id="ce7fd-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионаттрибутестрингчанжедевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="ce7fd-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="ce7fd-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="ce7fd-110">Property</span></span>         | <span data-ttu-id="ce7fd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ce7fd-111">Description</span></span>                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7fd-112">бстраттрибнаме</span><span class="sxs-lookup"><span data-stu-id="ce7fd-112">bstrAttribName</span></span>   | <span data-ttu-id="ce7fd-113">System. СтрингспеЦифиес имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="ce7fd-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="ce7fd-114">Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ce7fd-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="ce7fd-115">бстролдаттрибвал</span><span class="sxs-lookup"><span data-stu-id="ce7fd-115">bstrOldAttribVal</span></span> | <span data-ttu-id="ce7fd-116">System. СтрингспеЦифиес старое значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="ce7fd-116">System.StringSpecifies the old value of the attribute.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="ce7fd-117">бстрневаттрибвал</span><span class="sxs-lookup"><span data-stu-id="ce7fd-117">bstrNewAttribVal</span></span> | <span data-ttu-id="ce7fd-118">System. СтрингспеЦифиес новое значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="ce7fd-118">System.StringSpecifies the new value of the attribute.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="ce7fd-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce7fd-119">Remarks</span></span>

<span data-ttu-id="ce7fd-120">Когда пользователь изменяет метаданные библиотеки, коллекция носителей обновляется, и это событие срабатывает для каждого измененного атрибута.</span><span class="sxs-lookup"><span data-stu-id="ce7fd-120">When a user modifies library metadata, the media collection is updated and this event fires for each attribute changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7fd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ce7fd-121">Requirements</span></span>



| <span data-ttu-id="ce7fd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ce7fd-122">Requirement</span></span> | <span data-ttu-id="ce7fd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ce7fd-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7fd-124">Версия</span><span class="sxs-lookup"><span data-stu-id="ce7fd-124">Version</span></span><br/>   | <span data-ttu-id="ce7fd-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ce7fd-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ce7fd-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ce7fd-126">Namespace</span></span><br/> | <span data-ttu-id="ce7fd-127">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="ce7fd-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ce7fd-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="ce7fd-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ce7fd-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ce7fd-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce7fd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce7fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce7fd-131">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ce7fd-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce7fd-132">**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ce7fd-132">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce7fd-133">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ce7fd-133">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





