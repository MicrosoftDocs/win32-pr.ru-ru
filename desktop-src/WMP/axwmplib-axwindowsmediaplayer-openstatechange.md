---
title: Событие Опенстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Опенстатечанже возникает при изменении значения свойства Опенстате. | Событие Опенстатечанже объекта Аксвиндовсмедиаплайер
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Событие Опенстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694523"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="553d5-105">Событие Опенстатечанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="553d5-105">OpenStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="553d5-106">Событие Опенстатечанже возникает при изменении значения свойства **опенстате** .</span><span class="sxs-lookup"><span data-stu-id="553d5-106">The OpenStateChange event occurs when the **openState** property changes value.</span></span>

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a><span data-ttu-id="553d5-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="553d5-107">Event Data</span></span>

<span data-ttu-id="553d5-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ опенстатечанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="553d5-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEventHandler**.</span></span> <span data-ttu-id="553d5-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ опенстатечанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="553d5-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="553d5-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="553d5-110">Property</span></span> | <span data-ttu-id="553d5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="553d5-111">Description</span></span>                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553d5-112">NewState</span><span class="sxs-lookup"><span data-stu-id="553d5-112">NewState</span></span> | <span data-ttu-id="553d5-113">System. Int32Specifies новое состояние открытия.</span><span class="sxs-lookup"><span data-stu-id="553d5-113">System.Int32Specifies the new open state.</span></span> <span data-ttu-id="553d5-114">Таблицу значений см. в разделе [опенстате](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="553d5-114">For a table of values, see [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="553d5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="553d5-115">Remarks</span></span>

<span data-ttu-id="553d5-116">Проигрыватель Windows Media может пройти несколько открытых состояний при попытке открыть сетевой файл, например найти сервер, подключиться к серверу и, наконец, открыть файл.</span><span class="sxs-lookup"><span data-stu-id="553d5-116">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="553d5-117">Это событие будет срабатывать каждый раз при изменении состояния открытия.</span><span class="sxs-lookup"><span data-stu-id="553d5-117">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="553d5-118">Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="553d5-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="553d5-119">Кроме того, не все состояния должны происходить во время последовательности событий.</span><span class="sxs-lookup"><span data-stu-id="553d5-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="553d5-120">Не следует писать код, зависящий от порядка состояний.</span><span class="sxs-lookup"><span data-stu-id="553d5-120">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="553d5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="553d5-121">Requirements</span></span>



| <span data-ttu-id="553d5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="553d5-122">Requirement</span></span> | <span data-ttu-id="553d5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="553d5-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553d5-124">Версия</span><span class="sxs-lookup"><span data-stu-id="553d5-124">Version</span></span><br/>   | <span data-ttu-id="553d5-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="553d5-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="553d5-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="553d5-126">Namespace</span></span><br/> | <span data-ttu-id="553d5-127">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="553d5-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="553d5-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="553d5-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="553d5-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="553d5-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="553d5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="553d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553d5-131">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="553d5-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="553d5-132">**Аксвиндовсмедиаплайер. Опенстате (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="553d5-132">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





