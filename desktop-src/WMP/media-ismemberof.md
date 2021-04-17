---
title: Метод Media. isMemberOf
description: Метод isMemberOf возвращает значение, указывающее, является ли элемент мультимедиа элементом указанного списка воспроизведения.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- isMemberOf метод Windows Media Player
- isMemberOf метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694699"
---
# <a name="mediaismemberof-method"></a><span data-ttu-id="0d1db-106">Метод Media. isMemberOf</span><span class="sxs-lookup"><span data-stu-id="0d1db-106">Media.isMemberOf method</span></span>

<span data-ttu-id="0d1db-107">Метод **isMemberOf** возвращает значение, указывающее, является ли элемент мультимедиа элементом указанного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0d1db-107">The **isMemberOf** method returns a value indicating whether the media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1db-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d1db-108">Syntax</span></span>


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="0d1db-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d1db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d1db-110">*список воспроизведения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d1db-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d1db-111">Объект **списка воспроизведения** , который может содержать элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0d1db-111">**Playlist** object that might contain the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d1db-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d1db-112">Return value</span></span>

<span data-ttu-id="0d1db-113">Этот метод возвращает **логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="0d1db-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d1db-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d1db-114">Remarks</span></span>

<span data-ttu-id="0d1db-115">Этот метод не может проверять списки воспроизведения, полученные через объект **медиаколлектион** .</span><span class="sxs-lookup"><span data-stu-id="0d1db-115">This method is cannot check playlists retrieved through the **MediaCollection** object.</span></span> <span data-ttu-id="0d1db-116">Чтобы проверить, является ли элемент мультимедиа членом определенного списка воспроизведения, извлеките список воспроизведения с помощью *проигрывателя*. *плайлистколлектион*. **жетбинаме**(*имя*). **элемент**(0).</span><span class="sxs-lookup"><span data-stu-id="0d1db-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist with *player*.*playlistCollection*.**getByName**(*name*).**item**(0).</span></span> <span data-ttu-id="0d1db-117">Этот метод также можно использовать с списками воспроизведения компакт-дисков и списками воспроизведения метафайлов.</span><span class="sxs-lookup"><span data-stu-id="0d1db-117">This method can also be used with CD playlists and metafile playlists.</span></span>

<span data-ttu-id="0d1db-118">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="0d1db-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0d1db-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0d1db-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0d1db-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="0d1db-120">Examples</span></span>

<span data-ttu-id="0d1db-121">В следующем примере JScript используется *носитель*. **isMemberOf** , чтобы проверить, является ли текущий элемент мультимедиа членом списка воспроизведения с именем Sample Rename.</span><span class="sxs-lookup"><span data-stu-id="0d1db-121">The following JScript example uses *Media*.**isMemberOf** to test whether the current media item is a member of the playlist named Sample Playlist.</span></span> <span data-ttu-id="0d1db-122">Если это не так, текущий элемент мультимедиа добавляется к образцу списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0d1db-122">If it is not, the current media item is appended to the sample playlist.</span></span> <span data-ttu-id="0d1db-123">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="0d1db-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a><span data-ttu-id="0d1db-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0d1db-124">Requirements</span></span>



| <span data-ttu-id="0d1db-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0d1db-125">Requirement</span></span> | <span data-ttu-id="0d1db-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0d1db-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1db-127">Версия</span><span class="sxs-lookup"><span data-stu-id="0d1db-127">Version</span></span><br/> | <span data-ttu-id="0d1db-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0d1db-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0d1db-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0d1db-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d1db-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d1db-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d1db-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d1db-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1db-132">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="0d1db-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="0d1db-133">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="0d1db-133">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0d1db-134">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="0d1db-134">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="0d1db-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="0d1db-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0d1db-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="0d1db-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





