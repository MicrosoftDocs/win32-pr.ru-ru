---
title: Событие Либраридисконнект объекта Аксвиндовсмедиаплайер
description: Событие Либраридисконнект возникает, когда библиотека больше недоступна.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Событие Либраридисконнект в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699023"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="36ee4-104">Событие Либраридисконнект объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="36ee4-104">LibraryDisconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="36ee4-105">Событие Либраридисконнект возникает, когда библиотека больше недоступна.</span><span class="sxs-lookup"><span data-stu-id="36ee4-105">The LibraryDisconnect event occurs when a library is no longer available.</span></span>

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a><span data-ttu-id="36ee4-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="36ee4-106">Event Data</span></span>

<span data-ttu-id="36ee4-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ либраридисконнектевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="36ee4-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEventHandler**.</span></span> <span data-ttu-id="36ee4-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ либраридисконнектевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="36ee4-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="36ee4-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="36ee4-109">Property</span></span> | <span data-ttu-id="36ee4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="36ee4-110">Description</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ee4-111">плибрари</span><span class="sxs-lookup"><span data-stu-id="36ee4-111">pLibrary</span></span> | <span data-ttu-id="36ee4-112">**Вмплиб. ивмплибрари** Интерфейс, представляющий библиотеку, которая была отключена.</span><span class="sxs-lookup"><span data-stu-id="36ee4-112">**WMPLib.IWMPLibrary** The interface that represents the library that disconnected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36ee4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36ee4-113">Remarks</span></span>

<span data-ttu-id="36ee4-114">Это событие не происходит для локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="36ee4-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ee4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="36ee4-115">Requirements</span></span>



| <span data-ttu-id="36ee4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="36ee4-116">Requirement</span></span> | <span data-ttu-id="36ee4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="36ee4-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ee4-118">Версия</span><span class="sxs-lookup"><span data-stu-id="36ee4-118">Version</span></span><br/>   | <span data-ttu-id="36ee4-119">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="36ee4-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="36ee4-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="36ee4-120">Namespace</span></span><br/> | <span data-ttu-id="36ee4-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="36ee4-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="36ee4-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="36ee4-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="36ee4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="36ee4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36ee4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36ee4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ee4-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="36ee4-126">**Интерфейс Ивмплибрари (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="36ee4-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





