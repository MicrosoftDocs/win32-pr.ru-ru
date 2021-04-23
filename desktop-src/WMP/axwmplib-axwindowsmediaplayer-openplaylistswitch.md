---
title: Событие Опенплайлистсвитч объекта Аксвиндовсмедиаплайер
description: Событие Опенплайлистсвитч возникает, когда начинается воспроизведение заголовка на DVD-диске. | Событие Опенплайлистсвитч объекта Аксвиндовсмедиаплайер
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Событие Опенплайлистсвитч в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694729"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6071d-105">Событие Опенплайлистсвитч объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="6071d-105">OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6071d-106">Событие Опенплайлистсвитч возникает, когда начинается воспроизведение заголовка на DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="6071d-106">The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.</span></span>

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a><span data-ttu-id="6071d-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="6071d-107">Event Data</span></span>

<span data-ttu-id="6071d-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ опенплайлистсвитчевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="6071d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEventHandler**.</span></span> <span data-ttu-id="6071d-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ опенплайлистсвитчевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="6071d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="6071d-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="6071d-110">Property</span></span>  | <span data-ttu-id="6071d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6071d-111">Description</span></span>                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6071d-112">**питем**</span><span class="sxs-lookup"><span data-stu-id="6071d-112">**pItem**</span></span> | <span data-ttu-id="6071d-113">System. Обжектобжект, представляющий заголовок.</span><span class="sxs-lookup"><span data-stu-id="6071d-113">System.ObjectObject representing the title.</span></span> <span data-ttu-id="6071d-114">Это можно привести к интерфейсу Ивмпплайлист для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="6071d-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6071d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6071d-115">Requirements</span></span>



| <span data-ttu-id="6071d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6071d-116">Requirement</span></span> | <span data-ttu-id="6071d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6071d-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6071d-118">Версия</span><span class="sxs-lookup"><span data-stu-id="6071d-118">Version</span></span><br/>   | <span data-ttu-id="6071d-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6071d-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6071d-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6071d-120">Namespace</span></span><br/> | <span data-ttu-id="6071d-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="6071d-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6071d-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="6071d-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6071d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6071d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6071d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6071d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6071d-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6071d-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6071d-126">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6071d-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





