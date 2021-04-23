---
title: Событие Disconnect объекта Аксвиндовсмедиаплайер
description: Событие Disconnect зарезервировано для будущего использования.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Событие отключения проигрывателя Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694677"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f0b66-104">Событие Disconnect объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="f0b66-104">Disconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f0b66-105">Событие Disconnect зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="f0b66-105">The Disconnect event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a><span data-ttu-id="f0b66-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="f0b66-106">Event Data</span></span>

<span data-ttu-id="f0b66-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ дисконнектевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="f0b66-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEventHandler**.</span></span> <span data-ttu-id="f0b66-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ дисконнектевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="f0b66-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="f0b66-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="f0b66-109">Property</span></span> | <span data-ttu-id="f0b66-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f0b66-110">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="f0b66-111">result</span><span class="sxs-lookup"><span data-stu-id="f0b66-111">result</span></span>   | <span data-ttu-id="f0b66-112">**System. Int32** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f0b66-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0b66-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0b66-113">Remarks</span></span>

<span data-ttu-id="f0b66-114">Это событие зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="f0b66-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b66-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f0b66-115">Requirements</span></span>



| <span data-ttu-id="f0b66-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f0b66-116">Requirement</span></span> | <span data-ttu-id="f0b66-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f0b66-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b66-118">Версия</span><span class="sxs-lookup"><span data-stu-id="f0b66-118">Version</span></span><br/>   | <span data-ttu-id="f0b66-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f0b66-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f0b66-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0b66-120">Namespace</span></span><br/> | <span data-ttu-id="f0b66-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="f0b66-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f0b66-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="f0b66-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f0b66-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f0b66-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0b66-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0b66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b66-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f0b66-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





