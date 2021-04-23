---
title: Событие Либрариконнект объекта Аксвиндовсмедиаплайер
description: Событие Либрариконнект возникает, когда библиотека станет доступной.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Событие Либрариконнект в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699025"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8ef34-104">Событие Либрариконнект объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="8ef34-104">LibraryConnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8ef34-105">Событие Либрариконнект возникает, когда библиотека станет доступной.</span><span class="sxs-lookup"><span data-stu-id="8ef34-105">The LibraryConnect event occurs when a library becomes available.</span></span>

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a><span data-ttu-id="8ef34-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="8ef34-106">Event Data</span></span>

<span data-ttu-id="8ef34-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ либрариконнектевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="8ef34-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEventHandler**.</span></span> <span data-ttu-id="8ef34-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ либрариконнектевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="8ef34-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="8ef34-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="8ef34-109">Property</span></span> | <span data-ttu-id="8ef34-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8ef34-110">Description</span></span>                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef34-111">плибрари</span><span class="sxs-lookup"><span data-stu-id="8ef34-111">pLibrary</span></span> | <span data-ttu-id="8ef34-112">**Вмплиб. ивмплибрари** Интерфейс, представляющий подключаемую библиотеку.</span><span class="sxs-lookup"><span data-stu-id="8ef34-112">**WMPLib.IWMPLibrary** The interface that represents the library that connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ef34-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ef34-113">Remarks</span></span>

<span data-ttu-id="8ef34-114">Это событие не происходит для локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="8ef34-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef34-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8ef34-115">Requirements</span></span>



| <span data-ttu-id="8ef34-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8ef34-116">Requirement</span></span> | <span data-ttu-id="8ef34-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8ef34-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef34-118">Версия</span><span class="sxs-lookup"><span data-stu-id="8ef34-118">Version</span></span><br/>   | <span data-ttu-id="8ef34-119">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="8ef34-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="8ef34-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ef34-120">Namespace</span></span><br/> | <span data-ttu-id="8ef34-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="8ef34-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8ef34-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="8ef34-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8ef34-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8ef34-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ef34-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ef34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef34-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8ef34-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ef34-126">**Интерфейс Ивмплибрари (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="8ef34-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





