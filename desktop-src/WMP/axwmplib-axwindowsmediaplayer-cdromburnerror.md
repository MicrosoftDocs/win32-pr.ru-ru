---
title: Событие Кдромбурнеррор объекта Аксвиндовсмедиаплайер
description: Событие Кдромбурнеррор возникает при возникновении общей ошибки во время операции записи компакт-дисков.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Событие Кдромбурнеррор в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694390"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="41b98-104">Событие Кдромбурнеррор объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="41b98-104">CdromBurnError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="41b98-105">Событие Кдромбурнеррор возникает при возникновении общей ошибки во время операции записи компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="41b98-105">The CdromBurnError event occurs when a generic error happens during a CD burning operation.</span></span>

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a><span data-ttu-id="41b98-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="41b98-106">Event Data</span></span>

<span data-ttu-id="41b98-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнерроревенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="41b98-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEventHandler**.</span></span> <span data-ttu-id="41b98-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдромбурнерроревент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="41b98-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="41b98-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="41b98-109">Property</span></span>   | <span data-ttu-id="41b98-110">Описание</span><span class="sxs-lookup"><span data-stu-id="41b98-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b98-111">хреррор</span><span class="sxs-lookup"><span data-stu-id="41b98-111">hrError</span></span>    | <span data-ttu-id="41b98-112">**System. Int32** Ошибка, вызвавшая событие.</span><span class="sxs-lookup"><span data-stu-id="41b98-112">**System.Int32** The error that raised the event.</span></span><br/>                                               |
| <span data-ttu-id="41b98-113">пкдромбурн</span><span class="sxs-lookup"><span data-stu-id="41b98-113">pCdromBurn</span></span> | <span data-ttu-id="41b98-114">Интерфейс Вмплиб. Ивмпкдромбурнсе, представляющий операцию записи, вызвавшую ошибку.</span><span class="sxs-lookup"><span data-stu-id="41b98-114">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41b98-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41b98-115">Remarks</span></span>

<span data-ttu-id="41b98-116">Для записи ошибок, связанных с носителями, необходимо выполнить обработку Аксвмплиб. \_ \_Событие вмпокксевентс кдромбурнмедиаеррор.</span><span class="sxs-lookup"><span data-stu-id="41b98-116">To capture media specific errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b98-117">Требования</span><span class="sxs-lookup"><span data-stu-id="41b98-117">Requirements</span></span>



| <span data-ttu-id="41b98-118">Требование</span><span class="sxs-lookup"><span data-stu-id="41b98-118">Requirement</span></span> | <span data-ttu-id="41b98-119">Значение</span><span class="sxs-lookup"><span data-stu-id="41b98-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b98-120">Версия</span><span class="sxs-lookup"><span data-stu-id="41b98-120">Version</span></span><br/>   | <span data-ttu-id="41b98-121">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="41b98-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="41b98-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="41b98-122">Namespace</span></span><br/> | <span data-ttu-id="41b98-123">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="41b98-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="41b98-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="41b98-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="41b98-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="41b98-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b98-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41b98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b98-127">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="41b98-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="41b98-128">**Событие Аксвиндовсмедиаплайер. Кдромбурнмедиаеррор (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="41b98-128">**AxWindowsMediaPlayer.CdromBurnMediaError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[<span data-ttu-id="41b98-129">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="41b98-129">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





