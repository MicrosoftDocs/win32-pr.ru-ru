---
title: Событие Кдромбурнстатечанже объекта Аксвиндовсмедиаплайер
description: Событие Кдромбурнстатечанже возникает при изменении состояния операции записи компакт-диска.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Событие Кдромбурнстатечанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694389"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="24039-104">Событие Кдромбурнстатечанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="24039-104">CdromBurnStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="24039-105">Событие Кдромбурнстатечанже возникает при изменении состояния операции записи компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="24039-105">The CdromBurnStateChange event occurs when a CD burning operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a><span data-ttu-id="24039-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="24039-106">Event Data</span></span>

<span data-ttu-id="24039-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнстатечанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="24039-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEventHandler**.</span></span> <span data-ttu-id="24039-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнстатечанжеевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="24039-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="24039-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="24039-109">Property</span></span>   | <span data-ttu-id="24039-110">Описание</span><span class="sxs-lookup"><span data-stu-id="24039-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24039-111">пкдромбурн</span><span class="sxs-lookup"><span data-stu-id="24039-111">pCdromBurn</span></span> | <span data-ttu-id="24039-112">Интерфейс Вмплиб. Ивмпкдромбурнсе, представляющий операцию записи, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="24039-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |
| <span data-ttu-id="24039-113">вмпбс</span><span class="sxs-lookup"><span data-stu-id="24039-113">wmpbs</span></span>      | <span data-ttu-id="24039-114">Значение перечисления Вмплиб. Вмпбурнстатесе, указывающее новое состояние.</span><span class="sxs-lookup"><span data-stu-id="24039-114">WMPLib.WMPBurnStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="24039-115">Требования</span><span class="sxs-lookup"><span data-stu-id="24039-115">Requirements</span></span>



| <span data-ttu-id="24039-116">Требование</span><span class="sxs-lookup"><span data-stu-id="24039-116">Requirement</span></span> | <span data-ttu-id="24039-117">Значение</span><span class="sxs-lookup"><span data-stu-id="24039-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24039-118">Версия</span><span class="sxs-lookup"><span data-stu-id="24039-118">Version</span></span><br/>   | <span data-ttu-id="24039-119">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="24039-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="24039-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="24039-120">Namespace</span></span><br/> | <span data-ttu-id="24039-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="24039-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="24039-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="24039-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="24039-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="24039-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24039-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24039-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24039-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="24039-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="24039-126">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="24039-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="24039-127">**вмпбурнстате**</span><span class="sxs-lookup"><span data-stu-id="24039-127">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





