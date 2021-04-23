---
title: Плайлистколлектион. Импортплайлист, метод
description: Метод Импортплайлист добавляет статический список воспроизведения в библиотеку. | Плайлистколлектион. Импортплайлист, метод
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- Импортплайлист метод Windows Media Player
- Импортплайлист метод Windows Media Player, класс Плайлистколлектион
- Класс Плайлистколлектион Windows Media Player, метод Импортплайлист
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717966"
---
# <a name="playlistcollectionimportplaylist-method"></a><span data-ttu-id="10166-107">Плайлистколлектион. Импортплайлист, метод</span><span class="sxs-lookup"><span data-stu-id="10166-107">PlaylistCollection.importPlaylist method</span></span>

<span data-ttu-id="10166-108">Метод **импортплайлист** добавляет статический список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="10166-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="10166-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10166-109">Syntax</span></span>


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="10166-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="10166-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10166-111">*список воспроизведения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10166-111">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10166-112">Добавляемый объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="10166-112">**Playlist** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10166-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10166-113">Return value</span></span>

<span data-ttu-id="10166-114">Этот метод возвращает добавленный объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="10166-114">This method returns the **Playlist** object that was added.</span></span>

## <a name="remarks"></a><span data-ttu-id="10166-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10166-115">Remarks</span></span>

<span data-ttu-id="10166-116">Списки воспроизведения, которые не содержат элементов мультимедиа, не могут быть добавлены в библиотеку с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="10166-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="10166-117">Чтобы создать пустой список воспроизведения в библиотеке, используйте метод **невплайлист** .</span><span class="sxs-lookup"><span data-stu-id="10166-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="10166-118">Затем можно заполнить полученный список воспроизведения элементами мультимедиа с помощью *списка воспроизведения*. **аппендитем** или *список воспроизведения*. **insertItem**.</span><span class="sxs-lookup"><span data-stu-id="10166-118">You can then fill the resulting playlist with media items by using *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="10166-119">Если передать этот метод автоматическому списку воспроизведения, запрос выполняется один раз, а результат добавляется в библиотеку в виде статического списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="10166-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="10166-120">Чтобы добавить автоматический список воспроизведения в библиотеку и сохранить его автоматическое поведение, используйте *медиаколлектион*. **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="10166-120">To add an auto playlist to the library and preserve its automatic behavior, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="10166-121">Дополнительные сведения см. в разделе [статические и автоматические списки воспроизведения](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="10166-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="10166-122">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="10166-122">To use this method, full access to the library is required.</span></span> <span data-ttu-id="10166-123">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="10166-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10166-124">Требования</span><span class="sxs-lookup"><span data-stu-id="10166-124">Requirements</span></span>



| <span data-ttu-id="10166-125">Требование</span><span class="sxs-lookup"><span data-stu-id="10166-125">Requirement</span></span> | <span data-ttu-id="10166-126">Значение</span><span class="sxs-lookup"><span data-stu-id="10166-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10166-127">Версия</span><span class="sxs-lookup"><span data-stu-id="10166-127">Version</span></span><br/> | <span data-ttu-id="10166-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="10166-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="10166-129">DLL</span><span class="sxs-lookup"><span data-stu-id="10166-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="10166-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10166-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10166-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10166-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10166-132">**Управление списками воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="10166-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="10166-133">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="10166-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="10166-134">**Медиаколлектион. Add**</span><span class="sxs-lookup"><span data-stu-id="10166-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="10166-135">**Список воспроизведения. Аппендитем**</span><span class="sxs-lookup"><span data-stu-id="10166-135">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="10166-136">**Список воспроизведения. insertItem**</span><span class="sxs-lookup"><span data-stu-id="10166-136">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="10166-137">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="10166-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="10166-138">**Плайлистколлектион. Невплайлист**</span><span class="sxs-lookup"><span data-stu-id="10166-138">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="10166-139">**Плайлистколлектион. Remove**</span><span class="sxs-lookup"><span data-stu-id="10166-139">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="10166-140">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="10166-140">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="10166-141">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="10166-141">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





