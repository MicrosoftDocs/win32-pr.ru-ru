---
title: Событие Медиачанже объекта Аксвиндовсмедиаплайер
description: Событие Медиачанже возникает при изменении элемента мультимедиа. | Событие Медиачанже объекта Аксвиндовсмедиаплайер
ms.assetid: 0a2380ff-df50-4092-a952-812184822719
keywords:
- Событие Медиачанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175a7ed6ca57e3083d307cfe218d09233410053c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695169"
---
# <a name="mediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="de838-105">Событие Медиачанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="de838-105">MediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="de838-106">Событие Медиачанже возникает при изменении элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="de838-106">The MediaChange event occurs when a media item changes.</span></span>

``` syntax
[C#]
private void player_MediaChange(
  object sender,
  _WMPOCXEvents_MediaChangeEvent e
)

[Visual Basic]
Private Sub player_MediaChange(  
  sender As Object,  
  e As _WMPOCXEvents_MediaChangeEvent
) Handles player.MediaChange
```

## <a name="event-data"></a><span data-ttu-id="de838-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="de838-107">Event Data</span></span>

<span data-ttu-id="de838-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиачанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="de838-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEventHandler**.</span></span> <span data-ttu-id="de838-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиачанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="de838-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="de838-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="de838-110">Property</span></span> | <span data-ttu-id="de838-111">Описание</span><span class="sxs-lookup"><span data-stu-id="de838-111">Description</span></span>                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de838-112">Item</span><span class="sxs-lookup"><span data-stu-id="de838-112">Item</span></span>     | <span data-ttu-id="de838-113">Измененный элемент мультимедиа System. Обжектсе.</span><span class="sxs-lookup"><span data-stu-id="de838-113">System.ObjectThe media item that changed.</span></span> <span data-ttu-id="de838-114">Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="de838-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="de838-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="de838-115">Examples</span></span>

<span data-ttu-id="de838-116">В следующем примере для вывода имени текущего элемента мультимедиа используется метка.</span><span class="sxs-lookup"><span data-stu-id="de838-116">The following example uses a label to display the name of the current media item.</span></span> <span data-ttu-id="de838-117">Код обновляет текст в метке с каждым вхождением события Медиачанже.</span><span class="sxs-lookup"><span data-stu-id="de838-117">The code updates the text in the label with each occurrence of the MediaChange Event.</span></span> <span data-ttu-id="de838-118">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="de838-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the MediaChange event.
player.MediaChange += new AxWMPLib._WMPOCXEvents_MediaChangeEventHandler(player_MediaChange);

private void player_MediaChange(object sender, AxWMPLib._WMPOCXEvents_MediaChangeEvent e)
{
    // Get an interface to the changed media item that is returned in the event data. 
    WMPLib.IWMPMedia3 changedItem = (WMPLib.IWMPMedia3)e.item;

    // Display the name of the changed media item.
    mediaName.Text = changedItem.name;
}
```


```VB

Public Sub player_MediaChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_MediaChangeEvent) Handles player.MediaChange

    &#39; Get an interface to the changed media item that is returned in the event data.
    Dim changedItem As WMPLib.IWMPMedia3 = e.item

    &#39; Display the name of the changed media item.
    mediaName.Text = changedItem.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="de838-119">Требования</span><span class="sxs-lookup"><span data-stu-id="de838-119">Requirements</span></span>



| <span data-ttu-id="de838-120">Требование</span><span class="sxs-lookup"><span data-stu-id="de838-120">Requirement</span></span> | <span data-ttu-id="de838-121">Значение</span><span class="sxs-lookup"><span data-stu-id="de838-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de838-122">Версия</span><span class="sxs-lookup"><span data-stu-id="de838-122">Version</span></span><br/>   | <span data-ttu-id="de838-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="de838-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="de838-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="de838-124">Namespace</span></span><br/> | <span data-ttu-id="de838-125">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="de838-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="de838-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="de838-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="de838-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="de838-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de838-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de838-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de838-129">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="de838-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="de838-130">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="de838-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





