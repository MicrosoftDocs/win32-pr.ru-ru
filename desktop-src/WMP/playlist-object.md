---
title: Объект списка воспроизведения
description: Объект списка воспроизведения предоставляет способ организации мультимедийных элементов в списке для простоты работы с помощью следующих свойств и методов.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Проигрыватель Windows Media, объект списка воспроизведения
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068774"
---
# <a name="playlist-object"></a><span data-ttu-id="8642b-104">Объект списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="8642b-104">Playlist Object</span></span>

<span data-ttu-id="8642b-105">Объект **списка воспроизведения** предоставляет способ организации мультимедийных элементов в списке для простоты работы с помощью следующих свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="8642b-105">The **Playlist** object provides a way to organize media items in a list for easy manipulation by using the following properties and methods.</span></span>

<span data-ttu-id="8642b-106">Объект **списка воспроизведения** поддерживает следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8642b-106">The **Playlist** object supports the following properties.</span></span>



| <span data-ttu-id="8642b-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="8642b-107">Property</span></span>                                      | <span data-ttu-id="8642b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8642b-108">Description</span></span>                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="8642b-109">аттрибутекаунт</span><span class="sxs-lookup"><span data-stu-id="8642b-109">attributeCount</span></span>](playlist-attributecount.md) | <span data-ttu-id="8642b-110">Извлекает количество атрибутов, связанных с списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-110">Retrieves the number of attributes associated with the playlist.</span></span> |
| [<span data-ttu-id="8642b-111">attributeName</span><span class="sxs-lookup"><span data-stu-id="8642b-111">attributeName</span></span>](playlist-attributename.md)   | <span data-ttu-id="8642b-112">Возвращает имя атрибута, указанного индексом.</span><span class="sxs-lookup"><span data-stu-id="8642b-112">Retrieves the name of an attribute specified by an index.</span></span>        |
| [<span data-ttu-id="8642b-113">count</span><span class="sxs-lookup"><span data-stu-id="8642b-113">count</span></span>](playlist-count.md)                   | <span data-ttu-id="8642b-114">Возвращает число элементов в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-114">Retrieves the number of items in the playlist.</span></span>                   |
| [<span data-ttu-id="8642b-115">name</span><span class="sxs-lookup"><span data-stu-id="8642b-115">name</span></span>](playlist-name.md)                     | <span data-ttu-id="8642b-116">Указывает или получает имя списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-116">Specifies or retrieves the name of the playlist.</span></span>                 |



 

<span data-ttu-id="8642b-117">Объект **списка воспроизведения** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8642b-117">The **Playlist** object supports the following methods.</span></span>



| <span data-ttu-id="8642b-118">Метод</span><span class="sxs-lookup"><span data-stu-id="8642b-118">Method</span></span>                                  | <span data-ttu-id="8642b-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8642b-119">Description</span></span>                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8642b-120">аппендитем</span><span class="sxs-lookup"><span data-stu-id="8642b-120">appendItem</span></span>](playlist-appenditem.md)   | <span data-ttu-id="8642b-121">Добавляет элемент мультимедиа в конец списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-121">Adds a media item to the end of the playlist.</span></span>                                                          |
| <span data-ttu-id="8642b-122">**пусто**</span><span class="sxs-lookup"><span data-stu-id="8642b-122">**clear**</span></span>                               | <span data-ttu-id="8642b-123">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="8642b-123">Reserved for future use.</span></span>                                                                               |
| [<span data-ttu-id="8642b-124">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="8642b-124">getItemInfo</span></span>](playlist-getiteminfo.md) | <span data-ttu-id="8642b-125">Возвращает значение атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-125">Retrieves the value of a playlist attribute.</span></span>                                                           |
| [<span data-ttu-id="8642b-126">insertItem</span><span class="sxs-lookup"><span data-stu-id="8642b-126">insertItem</span></span>](playlist-insertitem.md)   | <span data-ttu-id="8642b-127">Вставляет элемент мультимедиа в список воспроизведения в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="8642b-127">Inserts a media item into the playlist at the specified location.</span></span>                                      |
| [<span data-ttu-id="8642b-128">Идентично</span><span class="sxs-lookup"><span data-stu-id="8642b-128">isIdentical</span></span>](playlist-isidentical.md) | <span data-ttu-id="8642b-129">Извлекает значение, указывающее, идентичен ли переданный объект **списка воспроизведения** текущему.</span><span class="sxs-lookup"><span data-stu-id="8642b-129">Retrieves a value indicating whether the supplied **Playlist** object is identical to the current one.</span></span> |
| [<span data-ttu-id="8642b-130">Item</span><span class="sxs-lookup"><span data-stu-id="8642b-130">item</span></span>](playlist-item.md)               | <span data-ttu-id="8642b-131">Извлекает элемент мультимедиа по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="8642b-131">Retrieves the media item at the specified index.</span></span>                                                       |
| [<span data-ttu-id="8642b-132">мовеитем</span><span class="sxs-lookup"><span data-stu-id="8642b-132">moveItem</span></span>](playlist-moveitem.md)       | <span data-ttu-id="8642b-133">Изменяет расположение элемента в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-133">Changes the location of an item in the playlist.</span></span>                                                       |
| [<span data-ttu-id="8642b-134">removeItem</span><span class="sxs-lookup"><span data-stu-id="8642b-134">removeItem</span></span>](playlist-removeitem.md)   | <span data-ttu-id="8642b-135">Удаляет указанный элемент из списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-135">Removes the specified item from the playlist.</span></span>                                                          |
| [<span data-ttu-id="8642b-136">сетитеминфо</span><span class="sxs-lookup"><span data-stu-id="8642b-136">setItemInfo</span></span>](playlist-setiteminfo.md) | <span data-ttu-id="8642b-137">Задает значение атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8642b-137">Specifies the value of a playlist attribute.</span></span>                                                           |



 

<span data-ttu-id="8642b-138">Доступ к объекту **списка воспроизведения** осуществляется с помощью следующих свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="8642b-138">The **Playlist** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="8642b-139">Объект</span><span class="sxs-lookup"><span data-stu-id="8642b-139">Object</span></span>                                              | <span data-ttu-id="8642b-140">Свойство или метод</span><span class="sxs-lookup"><span data-stu-id="8642b-140">Property or method</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8642b-141">ROM</span><span class="sxs-lookup"><span data-stu-id="8642b-141">Cdrom</span></span>](cdrom-object.md)                           | [<span data-ttu-id="8642b-142">список воспроизведения</span><span class="sxs-lookup"><span data-stu-id="8642b-142">playlist</span></span>](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8642b-143">медиаколлектион</span><span class="sxs-lookup"><span data-stu-id="8642b-143">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="8642b-144">[жеталл](mediacollection-getall.md), [жетбялбум](mediacollection-getbyalbum.md), [жетбяттрибуте](mediacollection-getbyattribute.md), [жетбяусор](mediacollection-getbyauthor.md), [жетбиженре](mediacollection-getbygenre.md), [жетбинаме](mediacollection-getbyname.md)</span><span class="sxs-lookup"><span data-stu-id="8642b-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span></span> |
| [<span data-ttu-id="8642b-145">Игрок</span><span class="sxs-lookup"><span data-stu-id="8642b-145">Player</span></span>](player-object.md)                         | <span data-ttu-id="8642b-146">[куррентплайлист](player-currentplaylist.md), [невплайлист](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="8642b-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="8642b-147">плайлистаррай</span><span class="sxs-lookup"><span data-stu-id="8642b-147">PlaylistArray</span></span>](playlistarray-object.md)           | [<span data-ttu-id="8642b-148">Item</span><span class="sxs-lookup"><span data-stu-id="8642b-148">item</span></span>](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="8642b-149">плайлистколлектион</span><span class="sxs-lookup"><span data-stu-id="8642b-149">PlaylistCollection</span></span>](playlistcollection-object.md) | [<span data-ttu-id="8642b-150">невплайлист</span><span class="sxs-lookup"><span data-stu-id="8642b-150">newPlaylist</span></span>](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

<span data-ttu-id="8642b-151">Так как это наиболее распространенные средства доступа, *Player*. **куррентплайлист** используется в целях иллюстрации в разделах синтаксиса Reference.</span><span class="sxs-lookup"><span data-stu-id="8642b-151">Because it is the most common means of access, *player*.**currentPlaylist** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="8642b-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8642b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8642b-153">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="8642b-153">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




