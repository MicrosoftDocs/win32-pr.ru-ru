---
title: Событие Кдромрипмедиаеррор объекта Аксвиндовсмедиаплайер
description: Событие Кдромрипмедиаеррор возникает при возникновении ошибки при копировании отдельной дорожки с компакт-диска.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Событие Кдромрипмедиаеррор в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694385"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e3ef8-104">Событие Кдромрипмедиаеррор объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="e3ef8-104">CdromRipMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e3ef8-105">Событие Кдромрипмедиаеррор возникает при возникновении ошибки при копировании отдельной дорожки с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-105">The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.</span></span>

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a><span data-ttu-id="e3ef8-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="e3ef8-106">Event Data</span></span>

<span data-ttu-id="e3ef8-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромрипмедиаерроревенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEventHandler**.</span></span> <span data-ttu-id="e3ef8-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромрипмедиаерроревент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="e3ef8-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="e3ef8-109">Property</span></span>  | <span data-ttu-id="e3ef8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e3ef8-110">Description</span></span>                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ef8-111">пкдромрип</span><span class="sxs-lookup"><span data-stu-id="e3ef8-111">pCdromRip</span></span> | <span data-ttu-id="e3ef8-112">Интерфейс Вмплиб. Ивмпкдромрипсе, представляющий операцию копирования, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/>                |
| <span data-ttu-id="e3ef8-113">пмедиа</span><span class="sxs-lookup"><span data-stu-id="e3ef8-113">pMedia</span></span>    | <span data-ttu-id="e3ef8-114">Элемент мультимедиа System. Обжектсе, вызвавший ошибку.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="e3ef8-115">Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="e3ef8-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e3ef8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e3ef8-116">Requirements</span></span>



| <span data-ttu-id="e3ef8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e3ef8-117">Requirement</span></span> | <span data-ttu-id="e3ef8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e3ef8-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ef8-119">Версия</span><span class="sxs-lookup"><span data-stu-id="e3ef8-119">Version</span></span><br/>   | <span data-ttu-id="e3ef8-120">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="e3ef8-120">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="e3ef8-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3ef8-121">Namespace</span></span><br/> | <span data-ttu-id="e3ef8-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="e3ef8-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e3ef8-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="e3ef8-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e3ef8-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e3ef8-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ef8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3ef8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ef8-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3ef8-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3ef8-127">**Интерфейс Ивмпкдромрип (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3ef8-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3ef8-128">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3ef8-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





