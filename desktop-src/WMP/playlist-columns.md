---
title: Список воспроизведения. столбцы
description: Атрибут columns определяет столбцы, которые отображаются в элементе списка воспроизведения.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- Список воспроизведения. столбцы Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704196"
---
# <a name="playlistcolumns"></a><span data-ttu-id="7e397-104">Список воспроизведения. столбцы</span><span class="sxs-lookup"><span data-stu-id="7e397-104">PLAYLIST.columns</span></span>

<span data-ttu-id="7e397-105">Атрибут **Columns** определяет столбцы, которые отображаются в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="7e397-105">The **columns** attribute defines the columns that appear in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.columns
```

## <a name="possible-values"></a><span data-ttu-id="7e397-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="7e397-106">Possible Values</span></span>

<span data-ttu-id="7e397-107">Этот атрибут является **строкой** для чтения и записи в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="7e397-107">This attribute is a read/write **String** in the following format:</span></span>

<span data-ttu-id="7e397-108">имя базы данных \_ = понятное \_ имя; имя базы данных \_ = понятное \_ имя;</span><span class="sxs-lookup"><span data-stu-id="7e397-108">DB\_NAME=FRIENDLY\_NAME;DB\_NAME=FRIENDLY\_NAME;</span></span>

<span data-ttu-id="7e397-109">ПОНЯТНОе \_ имя — это значение, отображаемое в заголовке столбца элемента списка воспроизведения, а имя базы данных \_ — значение из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="7e397-109">FRIENDLY\_NAME is the value shown in the column header of the PLAYLIST element, and DB\_NAME is a value from the following table.</span></span> <span data-ttu-id="7e397-110">Обратите внимание, что элемент списка воспроизведения может быть элементом мультимедиа из библиотеки или с компакт-диска или другим **списком воспроизведения** , созданным пользователем или полученным с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-110">Note that a Playlist item might be a media item from the library or from a CD, or it might be another **Playlist** that is either user-created or taken from a CD.</span></span> <span data-ttu-id="7e397-111">Некоторые столбцы действительны только с определенными элементами списка воспроизведения, как указано в столбце Описание.</span><span class="sxs-lookup"><span data-stu-id="7e397-111">Some columns are valid only with certain Playlist items as indicated in the Description column.</span></span>



| <span data-ttu-id="7e397-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7e397-112">Value</span></span>             | <span data-ttu-id="7e397-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7e397-113">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e397-114">Музыкальных</span><span class="sxs-lookup"><span data-stu-id="7e397-114">Album</span></span>             | <span data-ttu-id="7e397-115">Имя альбома.</span><span class="sxs-lookup"><span data-stu-id="7e397-115">The name of the album.</span></span> <span data-ttu-id="7e397-116">Используется только с элементами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7e397-116">Used with media items only.</span></span>                                                                      |
| <span data-ttu-id="7e397-117">Исполнител</span><span class="sxs-lookup"><span data-stu-id="7e397-117">Artist</span></span>            | <span data-ttu-id="7e397-118">Имя исполнителя.</span><span class="sxs-lookup"><span data-stu-id="7e397-118">The name of the artist.</span></span> <span data-ttu-id="7e397-119">Не используется с списками воспроизведения, созданными пользователем.</span><span class="sxs-lookup"><span data-stu-id="7e397-119">Not used with user-created playlists.</span></span>                                                           |
| <span data-ttu-id="7e397-120">Автор</span><span class="sxs-lookup"><span data-stu-id="7e397-120">Author</span></span>            | <span data-ttu-id="7e397-121">Имя исполнителя.</span><span class="sxs-lookup"><span data-stu-id="7e397-121">The name of the artist.</span></span>                                                                                                 |
| <span data-ttu-id="7e397-122">Bitrate</span><span class="sxs-lookup"><span data-stu-id="7e397-122">Bitrate</span></span>           | <span data-ttu-id="7e397-123">Битовая скорость содержимого.</span><span class="sxs-lookup"><span data-stu-id="7e397-123">The bit rate of the content.</span></span> <span data-ttu-id="7e397-124">Используется только с элементами мультимедиа из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7e397-124">Used only with media items from the library.</span></span>                                               |
| <span data-ttu-id="7e397-125">кдтраккенаблед</span><span class="sxs-lookup"><span data-stu-id="7e397-125">CDTrackEnabled</span></span>    | <span data-ttu-id="7e397-126">Указывает, включена ли запись компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-126">Indicates whether the CD track is enabled.</span></span> <span data-ttu-id="7e397-127">Используется только с элементами носителя компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-127">Used only with CD media items.</span></span>                                               |
| <span data-ttu-id="7e397-128">Флажок установлен</span><span class="sxs-lookup"><span data-stu-id="7e397-128">Checked</span></span>           | <span data-ttu-id="7e397-129">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7e397-129">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="7e397-130">Авторские права</span><span class="sxs-lookup"><span data-stu-id="7e397-130">Copyright</span></span>         | <span data-ttu-id="7e397-131">Авторские права на список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7e397-131">The copyright of the playlist.</span></span> <span data-ttu-id="7e397-132">Не используется с списками воспроизведения компакт-дисков или элементами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7e397-132">Not used with CD playlists or media items.</span></span>                                               |
| <span data-ttu-id="7e397-133">CreationDate</span><span class="sxs-lookup"><span data-stu-id="7e397-133">CreationDate</span></span>      | <span data-ttu-id="7e397-134">Дата и время создания записи в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7e397-134">The date and time that the entry in the library was created.</span></span> <span data-ttu-id="7e397-135">Используется только с элементами из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7e397-135">Used only with items from the library.</span></span>                     |
| <span data-ttu-id="7e397-136">дигиталлисекуре</span><span class="sxs-lookup"><span data-stu-id="7e397-136">DigitallySecure</span></span>   | <span data-ttu-id="7e397-137">Указывает, защищен ли элемент с помощью диспетчера прав Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7e397-137">Indicates whether the item is protected with Windows Media Rights Manager.</span></span> <span data-ttu-id="7e397-138">Используется только с элементами мультимедиа из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7e397-138">Used only with media items from the library.</span></span> |
| <span data-ttu-id="7e397-139">Duration</span><span class="sxs-lookup"><span data-stu-id="7e397-139">Duration</span></span>          | <span data-ttu-id="7e397-140">Длительность элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7e397-140">The duration of the media item.</span></span>                                                                                         |
| <span data-ttu-id="7e397-141">FileType</span><span class="sxs-lookup"><span data-stu-id="7e397-141">FileType</span></span>          | <span data-ttu-id="7e397-142">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7e397-142">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="7e397-143">Genre</span><span class="sxs-lookup"><span data-stu-id="7e397-143">Genre</span></span>             | <span data-ttu-id="7e397-144">Жанр списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7e397-144">The genre of the playlist.</span></span> <span data-ttu-id="7e397-145">Не используется с списками воспроизведения с компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="7e397-145">Not used with playlists from CDs.</span></span>                                                            |
| <span data-ttu-id="7e397-146">медиааттрибуте</span><span class="sxs-lookup"><span data-stu-id="7e397-146">MediaAttribute</span></span>    | <span data-ttu-id="7e397-147">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7e397-147">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="7e397-148">MediaType</span><span class="sxs-lookup"><span data-stu-id="7e397-148">MediaType</span></span>         | <span data-ttu-id="7e397-149">Тип элемента мультимедиа (аудио или видео).</span><span class="sxs-lookup"><span data-stu-id="7e397-149">The type of the media item (audio or video).</span></span>                                                                            |
| <span data-ttu-id="7e397-150">метадатасаурце</span><span class="sxs-lookup"><span data-stu-id="7e397-150">MetadataSource</span></span>    | <span data-ttu-id="7e397-151">Источник метаданных для этой записи компакт-дисков (АМГ, WindowsMedia.com и т. д.).</span><span class="sxs-lookup"><span data-stu-id="7e397-151">The source of the metadata for this CD track (AMG, WindowsMedia.com, and so on).</span></span> <span data-ttu-id="7e397-152">Используется только с элементами носителя компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-152">Used only with CD media items.</span></span>         |
| <span data-ttu-id="7e397-153">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="7e397-153">ModifiedBy</span></span>        | <span data-ttu-id="7e397-154">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7e397-154">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="7e397-155">Имя</span><span class="sxs-lookup"><span data-stu-id="7e397-155">Name</span></span>              | <span data-ttu-id="7e397-156">Имя списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7e397-156">The name of the playlist.</span></span>                                                                                               |
| <span data-ttu-id="7e397-157">оригиналиндекс</span><span class="sxs-lookup"><span data-stu-id="7e397-157">OriginalIndex</span></span>     | <span data-ttu-id="7e397-158">Если применимо, соответствующий идентификатор записи компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-158">If applicable, the corresponding CD track identifier.</span></span> <span data-ttu-id="7e397-159">Используется только с элементами носителя компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-159">Used only with CD media items.</span></span>                                    |
| <span data-ttu-id="7e397-160">плайкаунт</span><span class="sxs-lookup"><span data-stu-id="7e397-160">PlayCount</span></span>         | <span data-ttu-id="7e397-161">Количество операций воспроизведения содержимого до конца.</span><span class="sxs-lookup"><span data-stu-id="7e397-161">The number of times the content has been played through to the end.</span></span> <span data-ttu-id="7e397-162">Используется только с элементами мультимедиа из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7e397-162">Used only with media items from the library.</span></span>        |
| <span data-ttu-id="7e397-163">плайлистаттрибуте</span><span class="sxs-lookup"><span data-stu-id="7e397-163">PlaylistAttribute</span></span> | <span data-ttu-id="7e397-164">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7e397-164">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="7e397-165">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="7e397-165">Rating</span></span>            | <span data-ttu-id="7e397-166">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7e397-166">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="7e397-167">саурцеурл</span><span class="sxs-lookup"><span data-stu-id="7e397-167">SourceURL</span></span>         | <span data-ttu-id="7e397-168">Путь или URL-адрес содержимого.</span><span class="sxs-lookup"><span data-stu-id="7e397-168">The path or URL to the content.</span></span> <span data-ttu-id="7e397-169">Используется только с элементами мультимедиа из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7e397-169">Used only with media items from the library.</span></span>                                            |
| <span data-ttu-id="7e397-170">Состояние</span><span class="sxs-lookup"><span data-stu-id="7e397-170">Status</span></span>            | <span data-ttu-id="7e397-171">Состояние копирования копируемой записи компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-171">The copying status of a CD track being copied.</span></span> <span data-ttu-id="7e397-172">Используется только с элементами носителя компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7e397-172">Used only with CD media items.</span></span>                                           |
| <span data-ttu-id="7e397-173">Стиль</span><span class="sxs-lookup"><span data-stu-id="7e397-173">Style</span></span>             | <span data-ttu-id="7e397-174">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7e397-174">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="7e397-175">ОГЛАВЛЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e397-175">TOC</span></span>               | <span data-ttu-id="7e397-176">Если применимо, соответствующая таблица CD идентификатор содержимого.</span><span class="sxs-lookup"><span data-stu-id="7e397-176">If applicable, the corresponding CD Table of Contents Identifier.</span></span> <span data-ttu-id="7e397-177">Не используется с списками воспроизведения, созданными пользователем.</span><span class="sxs-lookup"><span data-stu-id="7e397-177">Not used with user-created playlists.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="7e397-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e397-178">Remarks</span></span>

<span data-ttu-id="7e397-179">Если один из столбцов не существует в библиотеке, он остается пустым.</span><span class="sxs-lookup"><span data-stu-id="7e397-179">If one of the columns does not exist in the library, it is left blank.</span></span>

<span data-ttu-id="7e397-180">Может быть указано не более 31 столбцов.</span><span class="sxs-lookup"><span data-stu-id="7e397-180">A maximum of 31 columns may be specified.</span></span>

<span data-ttu-id="7e397-181">При указании повторяющегося столбца данные в первом столбце будут выставляться по левому краю, но все остальные дублирующиеся столбцы будут выставляться по правому краю.</span><span class="sxs-lookup"><span data-stu-id="7e397-181">If you specify a duplicate column, the data in the first column will be left-aligned but all other duplicate columns will be right-aligned.</span></span> <span data-ttu-id="7e397-182">Например, если имеется два столбца длительности, то данные будут выставляться по левому краю в первом и по правому краю во втором.</span><span class="sxs-lookup"><span data-stu-id="7e397-182">For example, if you have two duration columns, the data will be left-aligned in the first and right-aligned in the second.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e397-183">Требования</span><span class="sxs-lookup"><span data-stu-id="7e397-183">Requirements</span></span>



| <span data-ttu-id="7e397-184">Требование</span><span class="sxs-lookup"><span data-stu-id="7e397-184">Requirement</span></span> | <span data-ttu-id="7e397-185">Значение</span><span class="sxs-lookup"><span data-stu-id="7e397-185">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7e397-186">Версия</span><span class="sxs-lookup"><span data-stu-id="7e397-186">Version</span></span><br/> | <span data-ttu-id="7e397-187">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="7e397-187">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e397-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e397-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e397-189">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="7e397-189">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="7e397-190">**Список воспроизведения. Колумнсвисибле**</span><span class="sxs-lookup"><span data-stu-id="7e397-190">**PLAYLIST.columnsVisible**</span></span>](playlist-columnsvisible.md)
</dt> </dl>

 

 





