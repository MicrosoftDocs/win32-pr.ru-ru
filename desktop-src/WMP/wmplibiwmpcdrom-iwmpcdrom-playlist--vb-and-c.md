---
title: Свойство списка воспроизведения Ивмпкдром
description: Свойство списка воспроизведения получает интерфейс Ивмпплайлист, представляющий дорожки на компакт-диске в данный момент в дисководе компакт-дисков или записи заголовка корневого уровня для DVD-диска.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Проигрыватель Windows Media, свойство списка воспроизведения
- Свойство списка воспроизведения проигрыватель Windows Media Player, интерфейс Ивмпкдром
- Интерфейс Ивмпкдром Windows Media Player, свойство списка воспроизведения
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717995"
---
# <a name="iwmpcdromplaylist-property"></a><span data-ttu-id="c9ab1-106">Ивмпкдром: свойство лайлист:P</span><span class="sxs-lookup"><span data-stu-id="c9ab1-106">IWMPCdrom::Playlist property</span></span>

<span data-ttu-id="c9ab1-107">Свойство **списка воспроизведения** получает интерфейс **ивмпплайлист** , представляющий дорожки на компакт-диске в данный момент в дисководе компакт-дисков или записи заголовка КОРНЕВого уровня для DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-107">The **Playlist** property gets an **IWMPPlaylist** interface representing the tracks on the CD currently in the CD drive or the root-level title entries for a DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ab1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9ab1-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="c9ab1-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c9ab1-109">Property value</span></span>

<span data-ttu-id="c9ab1-110">Интерфейс **вмплиб. ивмпплайлист** .</span><span class="sxs-lookup"><span data-stu-id="c9ab1-110">A **WMPLib.IWMPPlaylist** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9ab1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9ab1-111">Remarks</span></span>

<span data-ttu-id="c9ab1-112">Как правило, содержимое на DVD-диске организовано в заголовки.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-112">Typically, DVD-based content organized into titles.</span></span> <span data-ttu-id="c9ab1-113">Каждое название содержит одну или несколько глав.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-113">Each title contains one or more chapters.</span></span> <span data-ttu-id="c9ab1-114">Каждый DVD-диск создан по-разному, поэтому использование заголовков и глав имеет автор содержимого.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-114">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="c9ab1-115">Для DVD это свойство получает список воспроизведения, который содержит как первый элемент интерфейса **ивмпмедиа** с именем "DVD".</span><span class="sxs-lookup"><span data-stu-id="c9ab1-115">For a DVD, this property gets a playlist that contains as the first item an **IWMPMedia** interface named "DVD".</span></span> <span data-ttu-id="c9ab1-116">Этот интерфейс представляет DVD-носитель.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-116">This interface represents the DVD media.</span></span> <span data-ttu-id="c9ab1-117">Воспроизведение элемента приводит к тому, что DVD-диск воспроизводится с начала, если он впервые воспроизводится после вставки нового DVD-диска, или возобновляется воспроизведение, если DVD-диск совпадает с последним просмотренным DVD-диском.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-117">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="c9ab1-118">При установке этого элемента в качестве текущего элемента во время воспроизведения DVD-диск воспроизводится с самого начала.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-118">Setting this item as the current item during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="c9ab1-119">Дополнительные элементы (представленные интерфейсами **ивмпмедиа** ) в списке воспроизведения — это заголовки DVD, представленные вложенными списками воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-119">Additional items (represented by **IWMPMedia** interfaces) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="c9ab1-120">Если **ивмпконтролс. currentItem** устанавливается равным одному из этих вложенных элементов списка воспроизведения, проигрыватель Windows Media автоматически устанавливает вложенный список воспроизведения в качестве текущего списка воспроизведения после начала воспроизведения главы.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-120">When you set **IWMPControls.currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as the current playlist after chapter playback begins.</span></span> <span data-ttu-id="c9ab1-121">Затем можно использовать свойства интерфейса **ивмпплайлист** , методы и связанные события для работы с главами DVD, которые также являются элементами списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-121">You can then use the **IWMPPlaylist** interface properties, methods and associated events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="c9ab1-122">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-122">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="c9ab1-123">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c9ab1-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c9ab1-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="c9ab1-124">Examples</span></span>

<span data-ttu-id="c9ab1-125">В следующем примере используется **список воспроизведения** для заполнения многострочного текстового поля с именем myText с списком дорожек аудио компакт-диска, находящегося в данный момент на первом компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-125">The following example uses **Playlist** to fill a multi-line text box, named myText, with the track list of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="c9ab1-126">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="c9ab1-126">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a><span data-ttu-id="c9ab1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c9ab1-127">Requirements</span></span>



| <span data-ttu-id="c9ab1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c9ab1-128">Requirement</span></span> | <span data-ttu-id="c9ab1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c9ab1-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ab1-130">Версия</span><span class="sxs-lookup"><span data-stu-id="c9ab1-130">Version</span></span><br/>   | <span data-ttu-id="c9ab1-131">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c9ab1-131">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c9ab1-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9ab1-132">Namespace</span></span><br/> | <span data-ttu-id="c9ab1-133">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="c9ab1-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c9ab1-134">Сборка</span><span class="sxs-lookup"><span data-stu-id="c9ab1-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c9ab1-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c9ab1-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ab1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9ab1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ab1-137">**Интерфейс Ивмпкдром (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c9ab1-137">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9ab1-138">**Ивмпконтролс. currentItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c9ab1-138">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9ab1-139">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c9ab1-139">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9ab1-140">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c9ab1-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9ab1-141">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c9ab1-141">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9ab1-142">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c9ab1-142">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





