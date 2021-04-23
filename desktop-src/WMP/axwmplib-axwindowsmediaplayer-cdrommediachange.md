---
title: Событие Кдроммедиачанже объекта Аксвиндовсмедиаплайер
description: Событие Кдроммедиачанже возникает при вставке или извлечении компакт-диска или DVD-диска из дисковода CD или DVD. | Событие Кдроммедиачанже объекта Аксвиндовсмедиаплайер
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Событие Кдроммедиачанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694387"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2798f-105">Событие Кдроммедиачанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="2798f-105">CdromMediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2798f-106">Событие **кдроммедиачанже** возникает при вставке или ИЗВЛЕЧЕНии компакт-диска или DVD-диска из дисковода CD или DVD.</span><span class="sxs-lookup"><span data-stu-id="2798f-106">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a><span data-ttu-id="2798f-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="2798f-107">Event Data</span></span>

<span data-ttu-id="2798f-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кдроммедиачанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="2798f-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEventHandler**.</span></span> <span data-ttu-id="2798f-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кдроммедиачанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="2798f-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="2798f-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="2798f-110">Property</span></span> | <span data-ttu-id="2798f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2798f-111">Description</span></span>                                                        |
|----------|--------------------------------------------------------------------|
| <span data-ttu-id="2798f-112">кдромнум</span><span class="sxs-lookup"><span data-stu-id="2798f-112">CdromNum</span></span> | <span data-ttu-id="2798f-113">System. Int32Specifies. индекс компакт-диска или DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="2798f-113">System.Int32Specifies the index of the CD or DVD drive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2798f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2798f-114">Remarks</span></span>

<span data-ttu-id="2798f-115">Индекс дисковода компакт-дисков соответствует индексу интерфейса Ивмпкдром, доступного через интерфейс Ивмпкдромколлектион.</span><span class="sxs-lookup"><span data-stu-id="2798f-115">The index of the CD drive corresponds to the index of an IWMPCdrom interface accessible through the IWMPCdromCollection interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2798f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2798f-116">Requirements</span></span>



| <span data-ttu-id="2798f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2798f-117">Requirement</span></span> | <span data-ttu-id="2798f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2798f-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2798f-119">Версия</span><span class="sxs-lookup"><span data-stu-id="2798f-119">Version</span></span><br/>   | <span data-ttu-id="2798f-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2798f-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2798f-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2798f-121">Namespace</span></span><br/> | <span data-ttu-id="2798f-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="2798f-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2798f-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="2798f-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2798f-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2798f-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2798f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2798f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2798f-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2798f-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2798f-127">**Интерфейс Ивмпкдром (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2798f-127">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2798f-128">**Интерфейс Ивмпкдромколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2798f-128">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





