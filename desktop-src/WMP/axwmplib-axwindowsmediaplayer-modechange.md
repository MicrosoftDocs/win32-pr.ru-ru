---
title: Событие Модечанже объекта Аксвиндовсмедиаплайер
description: Событие Модечанже возникает при изменении режима проигрывателя Windows Media. | Событие Модечанже объекта Аксвиндовсмедиаплайер
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Событие Модечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698769"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="aa2a7-105">Событие Модечанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="aa2a7-105">ModeChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="aa2a7-106">Событие Модечанже возникает при изменении режима проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-106">The ModeChange event occurs when a mode of Windows Media Player is changed.</span></span>

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a><span data-ttu-id="aa2a7-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="aa2a7-107">Event Data</span></span>

<span data-ttu-id="aa2a7-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ модечанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEventHandler**.</span></span> <span data-ttu-id="aa2a7-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ модечанжеевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="aa2a7-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="aa2a7-110">Property</span></span> | <span data-ttu-id="aa2a7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="aa2a7-111">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2a7-112">моденаме</span><span class="sxs-lookup"><span data-stu-id="aa2a7-112">modeName</span></span> | <span data-ttu-id="aa2a7-113">System. Стрингиндикатес режим, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-113">System.StringIndicates the mode that was changed.</span></span> <span data-ttu-id="aa2a7-114">Возможные значения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-114">For possible values, see Remarks.</span></span><br/> |
| <span data-ttu-id="aa2a7-115">newValue</span><span class="sxs-lookup"><span data-stu-id="aa2a7-115">newValue</span></span> | <span data-ttu-id="aa2a7-116">System. Булеаниндикатес новое состояние указанного режима.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-116">System.BooleanIndicates the new state of the specified mode.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="aa2a7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa2a7-117">Remarks</span></span>

<span data-ttu-id="aa2a7-118">В следующей таблице приведены возможные значения для свойства Моденаме.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-118">The following table shows the possible values for the modeName property.</span></span>



| <span data-ttu-id="aa2a7-119">Строка</span><span class="sxs-lookup"><span data-stu-id="aa2a7-119">String</span></span>  | <span data-ttu-id="aa2a7-120">Описание</span><span class="sxs-lookup"><span data-stu-id="aa2a7-120">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="aa2a7-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="aa2a7-121">shuffle</span></span> | <span data-ttu-id="aa2a7-122">Дорожки воспроизводятся в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-122">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="aa2a7-123">loop</span><span class="sxs-lookup"><span data-stu-id="aa2a7-123">loop</span></span>    | <span data-ttu-id="aa2a7-124">Все последовательности дорожек воспроизводятся постоянно.</span><span class="sxs-lookup"><span data-stu-id="aa2a7-124">The entire sequence of tracks is played repeatedly.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="aa2a7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="aa2a7-125">Requirements</span></span>



| <span data-ttu-id="aa2a7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="aa2a7-126">Requirement</span></span> | <span data-ttu-id="aa2a7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="aa2a7-127">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2a7-128">Версия</span><span class="sxs-lookup"><span data-stu-id="aa2a7-128">Version</span></span><br/>   | <span data-ttu-id="aa2a7-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="aa2a7-129">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="aa2a7-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aa2a7-130">Namespace</span></span><br/> | <span data-ttu-id="aa2a7-131">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="aa2a7-131">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="aa2a7-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="aa2a7-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="aa2a7-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="aa2a7-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa2a7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa2a7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa2a7-135">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="aa2a7-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aa2a7-136">**Ивмпсеттингс. мода (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="aa2a7-136">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aa2a7-137">**Ивмпсеттингс. setMode (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="aa2a7-137">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





