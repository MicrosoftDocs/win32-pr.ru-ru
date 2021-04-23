---
title: Событие Фолдерсканстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Фолдерсканстатечанже возникает при изменении состояния операции наблюдения за папками.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Событие Фолдерсканстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694450"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a7a7c-104">Событие Фолдерсканстатечанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="a7a7c-104">FolderScanStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a7a7c-105">Событие Фолдерсканстатечанже возникает при изменении состояния операции наблюдения за папками.</span><span class="sxs-lookup"><span data-stu-id="a7a7c-105">The FolderScanStateChange event occurs when a folder monitoring operation changes state.</span></span>

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a><span data-ttu-id="a7a7c-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="a7a7c-106">Event Data</span></span>

<span data-ttu-id="a7a7c-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ фолдерсканстатечанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="a7a7c-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEventHandler**.</span></span> <span data-ttu-id="a7a7c-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ фолдерсканстатечанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="a7a7c-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a7a7c-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="a7a7c-109">Property</span></span> | <span data-ttu-id="a7a7c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a7a7c-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a7c-111">вмпфсс</span><span class="sxs-lookup"><span data-stu-id="a7a7c-111">wmpfss</span></span>   | <span data-ttu-id="a7a7c-112">Значение перечисления Вмплиб. Вмпфолдерсканстатесе, указывающее новое состояние.</span><span class="sxs-lookup"><span data-stu-id="a7a7c-112">WMPLib.WMPFolderScanStateThe enumeration value that indicates the new state.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a7a7c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a7a7c-113">Requirements</span></span>



| <span data-ttu-id="a7a7c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a7a7c-114">Requirement</span></span> | <span data-ttu-id="a7a7c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a7a7c-115">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a7c-116">Версия</span><span class="sxs-lookup"><span data-stu-id="a7a7c-116">Version</span></span><br/>   | <span data-ttu-id="a7a7c-117">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="a7a7c-117">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="a7a7c-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a7a7c-118">Namespace</span></span><br/> | <span data-ttu-id="a7a7c-119">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="a7a7c-119">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a7a7c-120">Сборка</span><span class="sxs-lookup"><span data-stu-id="a7a7c-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a7a7c-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a7a7c-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7a7c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7a7c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7a7c-123">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a7a7c-123">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a7a7c-124">**вмпфолдерсканстате**</span><span class="sxs-lookup"><span data-stu-id="a7a7c-124">**WMPFolderScanState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





