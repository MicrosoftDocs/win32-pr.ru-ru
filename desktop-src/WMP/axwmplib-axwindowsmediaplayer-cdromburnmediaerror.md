---
title: Событие Кдромбурнмедиаеррор объекта Аксвиндовсмедиаплайер
description: Событие Кдромбурнмедиаеррор возникает при возникновении ошибки при записи отдельного элемента мультимедиа на компакт-диск.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Событие Кдромбурнмедиаеррор в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694388"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8a243-104">Событие Кдромбурнмедиаеррор объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="8a243-104">CdromBurnMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8a243-105">Событие Кдромбурнмедиаеррор возникает при возникновении ошибки при записи отдельного элемента мультимедиа на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="8a243-105">The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.</span></span>

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a><span data-ttu-id="8a243-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="8a243-106">Event Data</span></span>

<span data-ttu-id="8a243-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнмедиаерроревенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="8a243-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEventHandler**.</span></span> <span data-ttu-id="8a243-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнмедиаерроревент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="8a243-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="8a243-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="8a243-109">Property</span></span>   | <span data-ttu-id="8a243-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8a243-110">Description</span></span>                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a243-111">пкдромбурн</span><span class="sxs-lookup"><span data-stu-id="8a243-111">pCdromBurn</span></span> | <span data-ttu-id="8a243-112">Интерфейс Вмплиб. Ивмпкдромбурнсе, представляющий операцию записи, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="8a243-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/>               |
| <span data-ttu-id="8a243-113">пмедиа</span><span class="sxs-lookup"><span data-stu-id="8a243-113">pMedia</span></span>     | <span data-ttu-id="8a243-114">Элемент мультимедиа System. Обжектсе, вызвавший ошибку.</span><span class="sxs-lookup"><span data-stu-id="8a243-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="8a243-115">Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="8a243-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a243-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a243-116">Remarks</span></span>

<span data-ttu-id="8a243-117">Для захвата общих ошибок обрабатывайте Аксвмплиб. \_ \_Событие вмпокксевентс кдромбурнеррор.</span><span class="sxs-lookup"><span data-stu-id="8a243-117">To capture generic errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a243-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8a243-118">Requirements</span></span>



| <span data-ttu-id="8a243-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8a243-119">Requirement</span></span> | <span data-ttu-id="8a243-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8a243-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a243-121">Версия</span><span class="sxs-lookup"><span data-stu-id="8a243-121">Version</span></span><br/>   | <span data-ttu-id="8a243-122">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="8a243-122">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="8a243-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a243-123">Namespace</span></span><br/> | <span data-ttu-id="8a243-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="8a243-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8a243-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="8a243-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a243-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8a243-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a243-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a243-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a243-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8a243-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a243-129">**Событие Аксвиндовсмедиаплайер. Кдромбурнеррор (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8a243-129">**AxWindowsMediaPlayer.CdromBurnError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[<span data-ttu-id="8a243-130">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8a243-130">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a243-131">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8a243-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





