---
title: Плайлистколлектион. Невплайлист, метод
description: Метод Невплайлист создает новый список воспроизведения в библиотеке.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- Невплайлист метод Windows Media Player
- Невплайлист метод Windows Media Player, класс Плайлистколлектион
- Класс Плайлистколлектион Windows Media Player, метод Невплайлист
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708437"
---
# <a name="playlistcollectionnewplaylist-method"></a><span data-ttu-id="d8260-106">Плайлистколлектион. Невплайлист, метод</span><span class="sxs-lookup"><span data-stu-id="d8260-106">PlaylistCollection.newPlaylist method</span></span>

<span data-ttu-id="d8260-107">Метод **невплайлист** создает новый список воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d8260-107">The **newPlaylist** method creates a new playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8260-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8260-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="d8260-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8260-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8260-110">*имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8260-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8260-111">**Строка** , содержащая имя создаваемого списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d8260-111">**String** containing the name of the playlist to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8260-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8260-112">Return value</span></span>

<span data-ttu-id="d8260-113">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="d8260-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8260-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8260-114">Remarks</span></span>

<span data-ttu-id="d8260-115">Этот метод создает пустой список воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d8260-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="d8260-116">Чтобы заполнить список воспроизведения с помощью элементов мультимедиа, используйте *список воспроизведения*. **аппендитем** или *список воспроизведения*. **insertItem**.</span><span class="sxs-lookup"><span data-stu-id="d8260-116">To fill the playlist with media items, use *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="d8260-117">В библиотеке разрешено несколько списков воспроизведения с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="d8260-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="d8260-118">Чтобы избежать создания дубликата имени списка воспроизведения с помощью этого метода, используйте **жетбинаме** и *плайлистаррай*. **число** , определяющее, существует ли уже список воспроизведения с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="d8260-118">To avoid creating a duplicate playlist name with this method, use **getByName** and *PlaylistArray*.**count** to determine whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="d8260-119">Начальные и конечные пробелы не допускаются в именах списков воспроизведения и автоматически удаляются из значения, указанного для параметра *Name* .</span><span class="sxs-lookup"><span data-stu-id="d8260-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *name* parameter.</span></span>

<span data-ttu-id="d8260-120">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d8260-120">To use this method, full access to the library is required.</span></span> <span data-ttu-id="d8260-121">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d8260-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d8260-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="d8260-122">Examples</span></span>

<span data-ttu-id="d8260-123">В следующем примере JScript создается пустой список воспроизведения с именем «Срилист».</span><span class="sxs-lookup"><span data-stu-id="d8260-123">The following JScript example creates a new empty playlist called "ThreeList".</span></span> <span data-ttu-id="d8260-124">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="d8260-124">The **Player** object was created with ID="Player".</span></span>


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a><span data-ttu-id="d8260-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d8260-125">Requirements</span></span>



| <span data-ttu-id="d8260-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d8260-126">Requirement</span></span> | <span data-ttu-id="d8260-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d8260-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8260-128">Версия</span><span class="sxs-lookup"><span data-stu-id="d8260-128">Version</span></span><br/> | <span data-ttu-id="d8260-129">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d8260-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d8260-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d8260-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8260-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8260-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8260-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8260-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8260-133">**Медиаколлектион. Add**</span><span class="sxs-lookup"><span data-stu-id="d8260-133">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="d8260-134">**Список воспроизведения. Аппендитем**</span><span class="sxs-lookup"><span data-stu-id="d8260-134">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="d8260-135">**Список воспроизведения. insertItem**</span><span class="sxs-lookup"><span data-stu-id="d8260-135">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="d8260-136">**Плайлистаррай. Count**</span><span class="sxs-lookup"><span data-stu-id="d8260-136">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="d8260-137">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="d8260-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="d8260-138">**Плайлистколлектион. Жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="d8260-138">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="d8260-139">**Плайлистколлектион. Импортплайлист**</span><span class="sxs-lookup"><span data-stu-id="d8260-139">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="d8260-140">**Плайлистколлектион. Remove**</span><span class="sxs-lookup"><span data-stu-id="d8260-140">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="d8260-141">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="d8260-141">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d8260-142">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="d8260-142">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





