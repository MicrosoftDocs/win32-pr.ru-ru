---
title: Событие Куррентплайлистчанже объекта Аксвиндовсмедиаплайер
description: Событие Куррентплайлистчанже возникает при изменении в текущем списке воспроизведения. | Событие Куррентплайлистчанже объекта Аксвиндовсмедиаплайер
ms.assetid: 1f9c99a4-7d10-48bf-b5ff-b1c1d6753b20
keywords:
- Событие Куррентплайлистчанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99f34f0e02d03352a61bbfca6767295d63d59a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694410"
---
# <a name="currentplaylistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="024a7-105">Событие Куррентплайлистчанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="024a7-105">CurrentPlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="024a7-106">Событие Куррентплайлистчанже возникает при изменении в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="024a7-106">The CurrentPlaylistChange event occurs when something changes within the current playlist.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistChange(
  object sender,
  _WMPOCXEvents_CurrentPlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistChangeEvent
) Handles player.CurrentPlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="024a7-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="024a7-107">Event Data</span></span>

<span data-ttu-id="024a7-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ куррентплайлистчанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="024a7-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEventHandler**.</span></span> <span data-ttu-id="024a7-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ куррентплайлистчанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="024a7-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="024a7-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="024a7-110">Property</span></span> | <span data-ttu-id="024a7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="024a7-111">Description</span></span>                                                                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024a7-112">Изменить</span><span class="sxs-lookup"><span data-stu-id="024a7-112">change</span></span>   | <span data-ttu-id="024a7-113">Значение перечисления Вмплиб. Вмпплайлистчанжеевенттипеан, указывающее тип изменения, произошедшего в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="024a7-113">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="024a7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="024a7-114">Remarks</span></span>

<span data-ttu-id="024a7-115">Это событие не происходит, если другой список воспроизведения попадает в текущий список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="024a7-115">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="024a7-116">Это происходит только в том случае, если изменение происходит в текущем списке воспроизведения, например при добавлении элемента мультимедиа в список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="024a7-116">It occurs only when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="024a7-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="024a7-117">Examples</span></span>

<span data-ttu-id="024a7-118">В следующем примере отображаются имена всех элементов мультимедиа в текущем списке воспроизведения в ответ на событие Куррентплайлистчанже.</span><span class="sxs-lookup"><span data-stu-id="024a7-118">The following example displays the names of all the media items in the current playlist in response to the CurrentPlaylistChange Event.</span></span> <span data-ttu-id="024a7-119">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="024a7-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentPlaylistChange event.
player.CurrentPlaylistChange += new AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEventHandler(player_CurrentPlaylistChange);  


private void player_CurrentPlaylistChange(object sender, AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent e)
{
    switch(e.change)
    {
        // Only update the list for the move, delete, insert, and append event types.
        case WMPLib.WMPPlaylistChangeEventType.wmplcMove:    // Value = 3
        case WMPLib.WMPPlaylistChangeEventType.wmplcDelete:  // Value = 4
        case WMPLib.WMPPlaylistChangeEventType.wmplcInsert:  // Value = 5
        case WMPLib.WMPPlaylistChangeEventType.wmplcAppend:  // Value = 6

        // Create a string array large enough to hold all of the media item names.
        int count = player.currentPlaylist.count;
        string[] mediaItems = new string[count];

        // Clear any previous contents of the text box.
        playlistItems.Clear();

        // Loop through the playlist and store each media item name.
        for (int i = 0; i < count; i++)
        {
            mediaItems[i] = player.currentPlaylist.get_Item(i).name;
        }

        // Display the media item names.
        playlistItems.Lines = mediaItems;
        break;
      
        default:
            break;
    }
}
```


```VB

Public Sub player_CurrentPlaylistChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentPlaylistChangeEvent) Handles player.CurrentPlaylistChange

    Select Case e.change

        &#39; Only update the list for the move, delete, insert, and append event types.
        Case WMPLib.WMPPlaylistChangeEventType.wmplcMove   &#39; Value = 3
        Case WMPLib.WMPPlaylistChangeEventType.wmplcDelete &#39; Value = 4
        Case WMPLib.WMPPlaylistChangeEventType.wmplcInsert &#39; Value = 5
        Case WMPLib.WMPPlaylistChangeEventType.wmplcAppend &#39; Value = 6

            &#39; Create a string array large enough to hold all of the media item names.
            Dim count As Integer = player.currentPlaylist.count
            Dim mediaItems(count) As String

            &#39; Clear any previous contents of the text box.
            playlistItems.Clear()

            &#39; Loop through the playlist and store each media item name.
            For i As Integer = 0 To (count - 1)

                mediaItems(i) = player.currentPlaylist.Item(i).name

            Next i

            &#39; Display the media item names.
            playlistItems.Lines = mediaItems
    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="024a7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="024a7-120">Requirements</span></span>



| <span data-ttu-id="024a7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="024a7-121">Requirement</span></span> | <span data-ttu-id="024a7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="024a7-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024a7-123">Версия</span><span class="sxs-lookup"><span data-stu-id="024a7-123">Version</span></span><br/>   | <span data-ttu-id="024a7-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="024a7-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="024a7-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="024a7-125">Namespace</span></span><br/> | <span data-ttu-id="024a7-126">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="024a7-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="024a7-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="024a7-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="024a7-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="024a7-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024a7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="024a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024a7-130">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="024a7-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="024a7-131">**Аксвиндовсмедиаплайер. Куррентплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="024a7-131">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="024a7-132">**Событие Аксвиндовсмедиаплайер. Плайлистчанже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="024a7-132">**AxWindowsMediaPlayer.PlaylistChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistchange.md)
</dt> <dt>

[<span data-ttu-id="024a7-133">**вмпплайлистчанжеевенттипе**</span><span class="sxs-lookup"><span data-stu-id="024a7-133">**WMPPlaylistChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaylistchangeeventtype)
</dt> </dl>

 

 





