---
title: Событие Куррентитемчанже объекта Аксвиндовсмедиаплайер
description: Событие Куррентитемчанже возникает при изменении значения Ивмпконтролс. currentItem.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Событие Куррентитемчанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c33bb3e9c4c1e512e742c0e679f3c5b53a29735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694636"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4f001-104">Событие Куррентитемчанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="4f001-104">CurrentItemChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4f001-105">Событие Куррентитемчанже возникает, когда значение Ивмпконтролс. **currentItem** изменения.</span><span class="sxs-lookup"><span data-stu-id="4f001-105">The CurrentItemChange event occurs when the value of IWMPControls.**currentItem** changes.</span></span>

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a><span data-ttu-id="4f001-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="4f001-106">Event Data</span></span>

<span data-ttu-id="4f001-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ куррентитемчанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="4f001-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEventHandler**.</span></span> <span data-ttu-id="4f001-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ куррентитемчанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="4f001-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="4f001-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="4f001-109">Property</span></span>   | <span data-ttu-id="4f001-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4f001-110">Description</span></span>                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f001-111">пдиспмедиа</span><span class="sxs-lookup"><span data-stu-id="4f001-111">pdispMedia</span></span> | <span data-ttu-id="4f001-112">Новый текущий элемент мультимедиа System. Обжектсе.</span><span class="sxs-lookup"><span data-stu-id="4f001-112">System.ObjectThe new current media item.</span></span> <span data-ttu-id="4f001-113">Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="4f001-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4f001-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="4f001-114">Examples</span></span>

<span data-ttu-id="4f001-115">В следующем примере демонстрируется обработчик события Куррентитемчанже.</span><span class="sxs-lookup"><span data-stu-id="4f001-115">The following example demonstrates an event handler for the CurrentItemChange event.</span></span> <span data-ttu-id="4f001-116">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="4f001-116">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4f001-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4f001-117">Requirements</span></span>



| <span data-ttu-id="4f001-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4f001-118">Requirement</span></span> | <span data-ttu-id="4f001-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4f001-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f001-120">Версия</span><span class="sxs-lookup"><span data-stu-id="4f001-120">Version</span></span><br/>   | <span data-ttu-id="4f001-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="4f001-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4f001-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f001-122">Namespace</span></span><br/> | <span data-ttu-id="4f001-123">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="4f001-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4f001-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="4f001-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4f001-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4f001-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f001-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f001-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f001-127">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4f001-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f001-128">**Ивмпконтролс. currentItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4f001-128">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4f001-129">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4f001-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





