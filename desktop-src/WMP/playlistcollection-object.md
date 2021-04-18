---
title: Объект Плайлистколлектион
description: Объект Плайлистколлектион предоставляет способ организации списков воспроизведения.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Проигрыватель Windows Media Object Плайлистколлектион
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700739"
---
# <a name="playlistcollection-object"></a><span data-ttu-id="b07f3-104">Объект Плайлистколлектион</span><span class="sxs-lookup"><span data-stu-id="b07f3-104">PlaylistCollection Object</span></span>

<span data-ttu-id="b07f3-105">Объект **плайлистколлектион** предоставляет способ организации списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b07f3-105">The **PlaylistCollection** object provides a way to organize your playlists.</span></span>

<span data-ttu-id="b07f3-106">Объект **плайлистколлектион** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b07f3-106">The **PlaylistCollection** object supports the following methods.</span></span>



| <span data-ttu-id="b07f3-107">Метод</span><span class="sxs-lookup"><span data-stu-id="b07f3-107">Method</span></span>                                                  | <span data-ttu-id="b07f3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b07f3-108">Description</span></span>                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b07f3-109">жеталл</span><span class="sxs-lookup"><span data-stu-id="b07f3-109">getAll</span></span>](playlistcollection-getall.md)                 | <span data-ttu-id="b07f3-110">Извлекает объект [плайлистаррай](playlistarray-object.md) , содержащий все списки воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b07f3-110">Retrieves a [PlaylistArray](playlistarray-object.md) object containing all the playlists in the library.</span></span>                |
| [<span data-ttu-id="b07f3-111">жетбинаме</span><span class="sxs-lookup"><span data-stu-id="b07f3-111">getByName</span></span>](playlistcollection-getbyname.md)           | <span data-ttu-id="b07f3-112">Извлекает объект [плайлистаррай](playlistarray-object.md) , содержащий списки воспроизведения с указанным именем, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="b07f3-112">Retrieves a [PlaylistArray](playlistarray-object.md) object containing playlists with the specified name, if any exist.</span></span> |
| [<span data-ttu-id="b07f3-113">импортплайлист</span><span class="sxs-lookup"><span data-stu-id="b07f3-113">importPlaylist</span></span>](playlistcollection-importplaylist.md) | <span data-ttu-id="b07f3-114">Добавляет статический список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b07f3-114">Adds a static playlist to the library.</span></span>                                                                                   |
| [<span data-ttu-id="b07f3-115">isDeleted</span><span class="sxs-lookup"><span data-stu-id="b07f3-115">isDeleted</span></span>](playlistcollection-isdeleted.md)           | <span data-ttu-id="b07f3-116">Получает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="b07f3-116">Retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>                              |
| [<span data-ttu-id="b07f3-117">невплайлист</span><span class="sxs-lookup"><span data-stu-id="b07f3-117">newPlaylist</span></span>](playlistcollection-newplaylist.md)       | <span data-ttu-id="b07f3-118">Создает новый список воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b07f3-118">Creates a new playlist in the library.</span></span>                                                                                   |
| [<span data-ttu-id="b07f3-119">remove</span><span class="sxs-lookup"><span data-stu-id="b07f3-119">remove</span></span>](playlistcollection-remove.md)                 | <span data-ttu-id="b07f3-120">Удаляет список воспроизведения из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="b07f3-120">Removes a playlist from the library.</span></span>                                                                                     |
| [<span data-ttu-id="b07f3-121">сетделетед</span><span class="sxs-lookup"><span data-stu-id="b07f3-121">setDeleted</span></span>](playlistcollection-setdeleted.md)         | <span data-ttu-id="b07f3-122">Перемещает список воспроизведения в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="b07f3-122">Moves a playlist to the deleted items folder.</span></span>                                                                            |



 

<span data-ttu-id="b07f3-123">Доступ к объекту **плайлистколлектион** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="b07f3-123">The **PlaylistCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="b07f3-124">Объект</span><span class="sxs-lookup"><span data-stu-id="b07f3-124">Object</span></span>                      | <span data-ttu-id="b07f3-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="b07f3-125">Property</span></span>                                            |
|-----------------------------|-----------------------------------------------------|
| [<span data-ttu-id="b07f3-126">Игрок</span><span class="sxs-lookup"><span data-stu-id="b07f3-126">Player</span></span>](player-object.md) | [<span data-ttu-id="b07f3-127">плайлистколлектион</span><span class="sxs-lookup"><span data-stu-id="b07f3-127">playlistCollection</span></span>](player-playlistcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="b07f3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b07f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07f3-129">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="b07f3-129">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




