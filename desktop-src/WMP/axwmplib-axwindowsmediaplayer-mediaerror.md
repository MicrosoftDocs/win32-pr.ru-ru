---
title: Событие Медиаеррор объекта Аксвиндовсмедиаплайер
description: Событие Медиаеррор возникает, когда объект мультимедиа имеет условие ошибки.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Событие Медиаеррор в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699009"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="31914-104">Событие Медиаеррор объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="31914-104">MediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="31914-105">Событие Медиаеррор возникает, когда объект мультимедиа имеет условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="31914-105">The MediaError event occurs when a media object has an error condition.</span></span>

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a><span data-ttu-id="31914-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="31914-106">Event Data</span></span>

<span data-ttu-id="31914-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаерроревенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="31914-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEventHandler**.</span></span> <span data-ttu-id="31914-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаерроревент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="31914-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="31914-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="31914-109">Property</span></span>     | <span data-ttu-id="31914-110">Описание</span><span class="sxs-lookup"><span data-stu-id="31914-110">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31914-111">пмедиаобжект</span><span class="sxs-lookup"><span data-stu-id="31914-111">pMediaObject</span></span> | <span data-ttu-id="31914-112">System. Обжектобжект с условием ошибки.</span><span class="sxs-lookup"><span data-stu-id="31914-112">System.ObjectObject that has an error condition.</span></span> <span data-ttu-id="31914-113">Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="31914-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="31914-114">Требования</span><span class="sxs-lookup"><span data-stu-id="31914-114">Requirements</span></span>



| <span data-ttu-id="31914-115">Требование</span><span class="sxs-lookup"><span data-stu-id="31914-115">Requirement</span></span> | <span data-ttu-id="31914-116">Значение</span><span class="sxs-lookup"><span data-stu-id="31914-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31914-117">Версия</span><span class="sxs-lookup"><span data-stu-id="31914-117">Version</span></span><br/>   | <span data-ttu-id="31914-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="31914-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="31914-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="31914-119">Namespace</span></span><br/> | <span data-ttu-id="31914-120">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="31914-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="31914-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="31914-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="31914-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="31914-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31914-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31914-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31914-124">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="31914-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="31914-125">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="31914-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





