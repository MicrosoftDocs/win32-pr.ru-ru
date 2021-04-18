---
title: Объект Медиаколлектион
description: Объект Медиаколлектион предоставляет способ организации большой коллекции элементов мультимедиа. Его можно запросить для автоматического создания списков воспроизведения.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Проигрыватель Windows Media Object Медиаколлектион
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681556"
---
# <a name="mediacollection-object"></a><span data-ttu-id="011f2-105">Объект Медиаколлектион</span><span class="sxs-lookup"><span data-stu-id="011f2-105">MediaCollection Object</span></span>

<span data-ttu-id="011f2-106">Объект **медиаколлектион** предоставляет способ организации большой коллекции элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="011f2-106">The **MediaCollection** object provides a way to organize a large collection of media items.</span></span> <span data-ttu-id="011f2-107">Его можно запросить для автоматического создания списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="011f2-107">It can be queried to generate playlists automatically.</span></span>

<span data-ttu-id="011f2-108">Объект **медиаколлектион** поддерживает следующие методы.</span><span class="sxs-lookup"><span data-stu-id="011f2-108">The **MediaCollection** object supports the following methods.</span></span>



| <span data-ttu-id="011f2-109">Метод</span><span class="sxs-lookup"><span data-stu-id="011f2-109">Method</span></span>                                                                           | <span data-ttu-id="011f2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="011f2-110">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="011f2-111">add</span><span class="sxs-lookup"><span data-stu-id="011f2-111">add</span></span>](mediacollection-add.md)                                                   | <span data-ttu-id="011f2-112">Добавляет новый элемент мультимедиа или список воспроизведения в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="011f2-112">Adds a new media item or playlist to the library.</span></span>                                                                                                              |
| [<span data-ttu-id="011f2-113">createQuery</span><span class="sxs-lookup"><span data-stu-id="011f2-113">createQuery</span></span>](mediacollection-createquery.md)                                   | <span data-ttu-id="011f2-114">Создает новый объект [запроса](query-object.md) .</span><span class="sxs-lookup"><span data-stu-id="011f2-114">Creates a new [Query](query-object.md) object.</span></span>                                                                                                                |
| [<span data-ttu-id="011f2-115">жеталл</span><span class="sxs-lookup"><span data-stu-id="011f2-115">getAll</span></span>](mediacollection-getall.md)                                             | <span data-ttu-id="011f2-116">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="011f2-116">Retrieves a [Playlist](playlist-object.md) object containing all media items in the library.</span></span>                                                                  |
| [<span data-ttu-id="011f2-117">жетаттрибутестрингколлектион</span><span class="sxs-lookup"><span data-stu-id="011f2-117">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) | <span data-ttu-id="011f2-118">Извлекает объект [StringCollection](stringcollection-object.md) , представляющий набор всех значений для указанного атрибута в указанном типе носителя.</span><span class="sxs-lookup"><span data-stu-id="011f2-118">Retrieves a [StringCollection](stringcollection-object.md) object representing the set of all values for a specified attribute within a specified media type.</span></span> |
| [<span data-ttu-id="011f2-119">жетбялбум</span><span class="sxs-lookup"><span data-stu-id="011f2-119">getByAlbum</span></span>](mediacollection-getbyalbum.md)                                     | <span data-ttu-id="011f2-120">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий элементы мультимедиа из указанного альбома.</span><span class="sxs-lookup"><span data-stu-id="011f2-120">Retrieves a [Playlist](playlist-object.md) object containing media items from the specified album.</span></span>                                                            |
| [<span data-ttu-id="011f2-121">жетбяттрибуте</span><span class="sxs-lookup"><span data-stu-id="011f2-121">getByAttribute</span></span>](mediacollection-getbyattribute.md)                             | <span data-ttu-id="011f2-122">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий элементы мультимедиа с указанным атрибутом, имеющим указанное значение.</span><span class="sxs-lookup"><span data-stu-id="011f2-122">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified attribute having the specified value.</span></span>                             |
| [<span data-ttu-id="011f2-123">жетбяттрибутеандмедиатипе</span><span class="sxs-lookup"><span data-stu-id="011f2-123">getByAttributeAndMediaType</span></span>](mediacollection-getbyattributeandmediatype.md)     | <span data-ttu-id="011f2-124">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий объекты [мультимедиа](media-object.md) с указанным атрибутом и типом носителя.</span><span class="sxs-lookup"><span data-stu-id="011f2-124">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects having the specified attribute and media type.</span></span>                 |
| [<span data-ttu-id="011f2-125">жетбяусор</span><span class="sxs-lookup"><span data-stu-id="011f2-125">getByAuthor</span></span>](mediacollection-getbyauthor.md)                                   | <span data-ttu-id="011f2-126">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий элементы мультимедиа по указанному автору.</span><span class="sxs-lookup"><span data-stu-id="011f2-126">Retrieves a [Playlist](playlist-object.md) object containing media items by the specified author.</span></span>                                                             |
| [<span data-ttu-id="011f2-127">жетбиженре</span><span class="sxs-lookup"><span data-stu-id="011f2-127">getByGenre</span></span>](mediacollection-getbygenre.md)                                     | <span data-ttu-id="011f2-128">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий элементы мультимедиа с указанным жанром.</span><span class="sxs-lookup"><span data-stu-id="011f2-128">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified genre.</span></span>                                                            |
| [<span data-ttu-id="011f2-129">жетбинаме</span><span class="sxs-lookup"><span data-stu-id="011f2-129">getByName</span></span>](mediacollection-getbyname.md)                                       | <span data-ttu-id="011f2-130">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий элементы мультимедиа с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="011f2-130">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified name.</span></span>                                                             |
| [<span data-ttu-id="011f2-131">жетмедиаатом</span><span class="sxs-lookup"><span data-stu-id="011f2-131">getMediaAtom</span></span>](mediacollection-getmediaatom.md)                                 | <span data-ttu-id="011f2-132">Возвращает индекс, по которому заданное свойство находится в наборе доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="011f2-132">Retrieves the index at which a specified property resides within the set of available properties.</span></span>                                                              |
| [<span data-ttu-id="011f2-133">жетплайлистбикуери</span><span class="sxs-lookup"><span data-stu-id="011f2-133">getPlaylistByQuery</span></span>](mediacollection-getplaylistbyquery.md)                     | <span data-ttu-id="011f2-134">Извлекает объект [списка воспроизведения](playlist-object.md) , содержащий объекты [мультимедиа](media-object.md) , соответствующие условиям запроса.</span><span class="sxs-lookup"><span data-stu-id="011f2-134">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects that match the query conditions.</span></span>                               |
| [<span data-ttu-id="011f2-135">жетстрингколлектионбикуери</span><span class="sxs-lookup"><span data-stu-id="011f2-135">getStringCollectionByQuery</span></span>](mediacollection-getstringcollectionbyquery.md)     | <span data-ttu-id="011f2-136">Извлекает объект [StringCollection](stringcollection-object.md) , содержащий строки, соответствующие условиям запроса.</span><span class="sxs-lookup"><span data-stu-id="011f2-136">Retrieves a [StringCollection](stringcollection-object.md) object containing strings that match the query conditions.</span></span>                                         |
| [<span data-ttu-id="011f2-137">isDeleted</span><span class="sxs-lookup"><span data-stu-id="011f2-137">isDeleted</span></span>](mediacollection-isdeleted.md)                                       | <span data-ttu-id="011f2-138">Получает значение, указывающее, находится ли указанный элемент мультимедиа в папке удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="011f2-138">Retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>                                                                  |
| [<span data-ttu-id="011f2-139">remove</span><span class="sxs-lookup"><span data-stu-id="011f2-139">remove</span></span>](mediacollection-remove.md)                                             | <span data-ttu-id="011f2-140">Удаляет элемент из коллекции носителей.</span><span class="sxs-lookup"><span data-stu-id="011f2-140">Removes an item from the media collection.</span></span>                                                                                                                     |
| [<span data-ttu-id="011f2-141">сетделетед</span><span class="sxs-lookup"><span data-stu-id="011f2-141">setDeleted</span></span>](mediacollection-setdeleted.md)                                     | <span data-ttu-id="011f2-142">Перемещает указанный элемент мультимедиа в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="011f2-142">Moves the specified media item to the deleted items folder.</span></span>                                                                                                    |



 

<span data-ttu-id="011f2-143">Доступ к объекту **медиаколлектион** осуществляется через следующее свойство.</span><span class="sxs-lookup"><span data-stu-id="011f2-143">The **MediaCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="011f2-144">Объект</span><span class="sxs-lookup"><span data-stu-id="011f2-144">Object</span></span>                      | <span data-ttu-id="011f2-145">Свойство</span><span class="sxs-lookup"><span data-stu-id="011f2-145">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="011f2-146">Игрок</span><span class="sxs-lookup"><span data-stu-id="011f2-146">Player</span></span>](player-object.md) | [<span data-ttu-id="011f2-147">медиаколлектион</span><span class="sxs-lookup"><span data-stu-id="011f2-147">mediaCollection</span></span>](player-mediacollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="011f2-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="011f2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011f2-149">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="011f2-149">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




