---
title: Событие Warning объекта Аксвиндовсмедиаплайер
description: Событие предупреждения зарезервировано для будущего использования.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Событие предупреждения проигрывателя Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698847"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e86c2-104">Событие Warning объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="e86c2-104">Warning Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e86c2-105">Событие предупреждения зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="e86c2-105">The Warning event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a><span data-ttu-id="e86c2-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="e86c2-106">Event Data</span></span>

<span data-ttu-id="e86c2-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ варнинжевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="e86c2-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_WarningEventHandler**.</span></span> <span data-ttu-id="e86c2-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ варнинжевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="e86c2-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_WarningEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="e86c2-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="e86c2-109">Property</span></span>    | <span data-ttu-id="e86c2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e86c2-110">Description</span></span>                                |
|-------------|--------------------------------------------|
| <span data-ttu-id="e86c2-111">варнингтипе</span><span class="sxs-lookup"><span data-stu-id="e86c2-111">warningType</span></span> | <span data-ttu-id="e86c2-112">**System. Int32** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e86c2-112">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="e86c2-113">param</span><span class="sxs-lookup"><span data-stu-id="e86c2-113">param</span></span>       | <span data-ttu-id="e86c2-114">**System. Int32** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e86c2-114">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="e86c2-115">description;</span><span class="sxs-lookup"><span data-stu-id="e86c2-115">description</span></span> | <span data-ttu-id="e86c2-116">**System. String** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e86c2-116">**System.String** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e86c2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e86c2-117">Remarks</span></span>

<span data-ttu-id="e86c2-118">Это событие зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="e86c2-118">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86c2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e86c2-119">Requirements</span></span>



| <span data-ttu-id="e86c2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e86c2-120">Requirement</span></span> | <span data-ttu-id="e86c2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e86c2-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e86c2-122">Версия</span><span class="sxs-lookup"><span data-stu-id="e86c2-122">Version</span></span><br/>   | <span data-ttu-id="e86c2-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e86c2-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e86c2-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e86c2-124">Namespace</span></span><br/> | <span data-ttu-id="e86c2-125">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="e86c2-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e86c2-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="e86c2-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e86c2-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e86c2-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86c2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e86c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86c2-129">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e86c2-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





