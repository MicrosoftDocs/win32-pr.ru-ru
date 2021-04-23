---
title: CDROM. список воспроизведения
description: Свойство списка воспроизведения извлекает объект списка воспроизведения, который представляет дорожки на компакт-диске в данный момент в дисководе компакт-дисков или записи заголовка корневого уровня для DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Проигрыватель Windows Media CDROM. список воспроизведения
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691842"
---
# <a name="cdromplaylist"></a><span data-ttu-id="6c5f4-104">CDROM. список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="6c5f4-104">Cdrom.playlist</span></span>

<span data-ttu-id="6c5f4-105">Свойство **списка воспроизведения** извлекает объект **списка воспроизведения** , который представляет дорожки на компакт-диске в данный момент в дисководе компакт-дисков или записи заголовка корневого уровня для DVD.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-105">The **playlist** property retrieves a **Playlist** object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a><span data-ttu-id="6c5f4-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6c5f4-106">Possible Values</span></span>

<span data-ttu-id="6c5f4-107">Это свойство является объектом **списка воспроизведения** , предназначенным только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-107">This property is a read-only **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c5f4-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c5f4-108">Remarks</span></span>

<span data-ttu-id="6c5f4-109">Как правило, DVD-диски упорядочены по заголовкам.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-109">Typically, DVDs are organized into titles.</span></span> <span data-ttu-id="6c5f4-110">Каждое название содержит одну или несколько глав.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-110">Each title contains one or more chapters.</span></span> <span data-ttu-id="6c5f4-111">Каждый DVD-диск создан по-разному, поэтому использование заголовков и глав имеет автор содержимого.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-111">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="6c5f4-112">Для DVD этот метод извлекает список воспроизведения, который содержит в качестве первого элемента объект **мультимедиа** , представляющий DVD-носитель.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-112">For DVD, this method retrieves a playlist that contains as the first item a **Media** object that represents the DVD media.</span></span> <span data-ttu-id="6c5f4-113">Воспроизведение элемента приводит к тому, что DVD-диск воспроизводится с начала, если он впервые воспроизводится после вставки нового DVD-диска, или возобновляется воспроизведение, если DVD-диск совпадает с последним просмотренным DVD-диском.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-113">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="6c5f4-114">При установке этого элемента в качестве текущего во время воспроизведения DVD-диск воспроизводится с самого начала.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-114">Setting this item as the current one during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="6c5f4-115">Дополнительные элементы (объекты **мультимедиа** ) в списке воспроизведения представляют собой заголовки DVD, представленные вложенными списками воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-115">Additional items (**Media** objects) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="6c5f4-116">При указании *элементов управления*. **currentItem** один из этих вложенных элементов списка воспроизведения, проигрыватель Windows Media автоматически устанавливает вложенный список воспроизведения как *проигрыватель*. **куррентплайлист** после начала воспроизведения главы.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-116">When you specify *Controls*.**currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as *Player*.**currentPlaylist** after chapter playback begins.</span></span> <span data-ttu-id="6c5f4-117">Затем можно использовать свойства, методы и события объекта **куррентплайлист** для работы с главами DVD, которые также являются элементами списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-117">You can then use the **currentPlaylist** object properties, methods, and events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="6c5f4-118">Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-118">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="6c5f4-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6c5f4-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6c5f4-120">**Проигрыватель Windows Media 10 Mobile:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-120">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6c5f4-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="6c5f4-121">Examples</span></span>

<span data-ttu-id="6c5f4-122">В следующем примере используется *CDROM*. **список воспроизведения** для заполнения ТЕКСТОВОГО элемента HTML с именем myText с заголовками звукового компакт-диска, находящегося на первом компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-122">The following example uses *Cdrom*.**playlist** to fill an HTML text element, named myText, with the titles of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="6c5f4-123">Используйте *кдромколлектион*. **количество для определения** количества доступных ДИСКОВОДОВ компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-123">Use *CdromCollection*.**count** to determine the number of available CD drives.</span></span> <span data-ttu-id="6c5f4-124">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="6c5f4-124">The **Player** object was created with ID = "Player".</span></span>


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a><span data-ttu-id="6c5f4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6c5f4-125">Requirements</span></span>



| <span data-ttu-id="6c5f4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6c5f4-126">Requirement</span></span> | <span data-ttu-id="6c5f4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6c5f4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5f4-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c5f4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5f4-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6c5f4-129">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c5f4-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c5f4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5f4-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c5f4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c5f4-132">Версия</span><span class="sxs-lookup"><span data-stu-id="6c5f4-132">Version</span></span><br/>                  | <span data-ttu-id="6c5f4-133">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6c5f4-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6c5f4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6c5f4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c5f4-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c5f4-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5f4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c5f4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5f4-137">**Объект CDROM**</span><span class="sxs-lookup"><span data-stu-id="6c5f4-137">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="6c5f4-138">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="6c5f4-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6c5f4-139">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="6c5f4-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





