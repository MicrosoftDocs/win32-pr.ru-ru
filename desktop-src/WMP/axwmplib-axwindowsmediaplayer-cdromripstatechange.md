---
title: Событие Кдромрипстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Кдромрипстатечанже возникает при изменении состояния операции копирования компакт-диска.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Событие Кдромрипстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694383"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="bbf6d-104">Событие Кдромрипстатечанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="bbf6d-104">CdromRipStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="bbf6d-105">Событие Кдромрипстатечанже возникает при изменении состояния операции копирования компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-105">The CdromRipStateChange event occurs when a CD ripping operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a><span data-ttu-id="bbf6d-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="bbf6d-106">Event Data</span></span>

<span data-ttu-id="bbf6d-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромрипстатечанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEventHandler**.</span></span> <span data-ttu-id="bbf6d-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромрипстатечанжеевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="bbf6d-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="bbf6d-109">Property</span></span>  | <span data-ttu-id="bbf6d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bbf6d-110">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf6d-111">пкдромрип</span><span class="sxs-lookup"><span data-stu-id="bbf6d-111">pCdromRip</span></span> | <span data-ttu-id="bbf6d-112">Интерфейс Вмплиб. Ивмпкдромрипсе, представляющий операцию копирования, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/> |
| <span data-ttu-id="bbf6d-113">вмпрс</span><span class="sxs-lookup"><span data-stu-id="bbf6d-113">wmprs</span></span>     | <span data-ttu-id="bbf6d-114">Значение перечисления Вмплиб. Вмприпстатесе, указывающее новое состояние.</span><span class="sxs-lookup"><span data-stu-id="bbf6d-114">WMPLib.WMPRipStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="bbf6d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bbf6d-115">Requirements</span></span>



| <span data-ttu-id="bbf6d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bbf6d-116">Requirement</span></span> | <span data-ttu-id="bbf6d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bbf6d-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf6d-118">Версия</span><span class="sxs-lookup"><span data-stu-id="bbf6d-118">Version</span></span><br/>   | <span data-ttu-id="bbf6d-119">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="bbf6d-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="bbf6d-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bbf6d-120">Namespace</span></span><br/> | <span data-ttu-id="bbf6d-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="bbf6d-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="bbf6d-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="bbf6d-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bbf6d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bbf6d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf6d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbf6d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf6d-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bbf6d-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bbf6d-126">**Интерфейс Ивмпкдромрип (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bbf6d-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bbf6d-127">**вмприпстате**</span><span class="sxs-lookup"><span data-stu-id="bbf6d-127">**WMPRipState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





