---
title: Сведения о метаданных
description: Сведения о метаданных
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Проигрыватель Windows Media, метаданные
- метаданные, сведения
- метаданные, атрибуты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328520"
---
# <a name="about-the-metadata"></a><span data-ttu-id="a982b-106">Сведения о метаданных</span><span class="sxs-lookup"><span data-stu-id="a982b-106">About the Metadata</span></span>

<span data-ttu-id="a982b-107">Проигрыватель Windows Media 10 или более поздней версии пытается синхронизировать следующие атрибуты метаданных.</span><span class="sxs-lookup"><span data-stu-id="a982b-107">Windows Media Player 10 or later attempts to synchronize the following metadata attributes.</span></span>



| <span data-ttu-id="a982b-108">Атрибут Player</span><span class="sxs-lookup"><span data-stu-id="a982b-108">Player attribute</span></span> | <span data-ttu-id="a982b-109">Глобальная константа ВМДМ</span><span class="sxs-lookup"><span data-stu-id="a982b-109">WMDM global constant</span></span>  | <span data-ttu-id="a982b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a982b-110">Description</span></span>                                                                                                 | <span data-ttu-id="a982b-111">Требуемая версия</span><span class="sxs-lookup"><span data-stu-id="a982b-111">Required version</span></span>                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="a982b-112">албумартист</span><span class="sxs-lookup"><span data-stu-id="a982b-112">AlbumArtist</span></span>      | <span data-ttu-id="a982b-113">g \_ всзвмдмалбумартист</span><span class="sxs-lookup"><span data-stu-id="a982b-113">g\_wszWMDMAlbumArtist</span></span> | <span data-ttu-id="a982b-114">**Строка** , заканчивающаяся нулем и содержащая имя основного исполнителя для альбома.</span><span class="sxs-lookup"><span data-stu-id="a982b-114">Null-terminated **string** containing the name of the primary artist for the album.</span></span>                         | <span data-ttu-id="a982b-115">Проигрыватель Windows Media 11 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-115">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="a982b-116">Музыкальных</span><span class="sxs-lookup"><span data-stu-id="a982b-116">Album</span></span>            | <span data-ttu-id="a982b-117">g \_ всзвмдмалбумтитле</span><span class="sxs-lookup"><span data-stu-id="a982b-117">g\_wszWMDMAlbumTitle</span></span>  | <span data-ttu-id="a982b-118">**Строка** , заканчивающаяся нулем и содержащая название альбома, в котором первоначально было выпущено содержимое.</span><span class="sxs-lookup"><span data-stu-id="a982b-118">Null-terminated **string** containing the title of the album on which the content was originally released.</span></span>  | <span data-ttu-id="a982b-119">Проигрыватель Windows Media 11 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-119">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="a982b-120">Автор</span><span class="sxs-lookup"><span data-stu-id="a982b-120">Author</span></span>           | <span data-ttu-id="a982b-121">g \_ всзвмдмаусор</span><span class="sxs-lookup"><span data-stu-id="a982b-121">g\_wszWMDMAuthor</span></span>      | <span data-ttu-id="a982b-122">**Строка** , заканчивающаяся нулем, содержащая имя исполнителя или субъекта мультимедиа, связанного с содержимым.</span><span class="sxs-lookup"><span data-stu-id="a982b-122">Null-terminated **string** containing the name of the media artist or actor associated with the content.</span></span>    | <span data-ttu-id="a982b-123">Проигрыватель Windows Media 11 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-123">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="a982b-124">буйнов</span><span class="sxs-lookup"><span data-stu-id="a982b-124">BuyNow</span></span>           | <span data-ttu-id="a982b-125">g \_ всзвмдмбуйнов</span><span class="sxs-lookup"><span data-stu-id="a982b-125">g\_wszWMDMBuyNow</span></span>      | <span data-ttu-id="a982b-126">**Логическое значение** , указывающее, выбрал ли пользователь приобретать содержимое.</span><span class="sxs-lookup"><span data-stu-id="a982b-126">**Boolean** indicating whether the user has chosen to purchase the content.</span></span>                                 | <span data-ttu-id="a982b-127">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-127">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="a982b-128">WM/жанр</span><span class="sxs-lookup"><span data-stu-id="a982b-128">WM/Genre</span></span>         | <span data-ttu-id="a982b-129">g \_ всзвмдмженре</span><span class="sxs-lookup"><span data-stu-id="a982b-129">g\_wszWMDMGenre</span></span>       | <span data-ttu-id="a982b-130">**Строка** , заканчивающаяся нулем, содержащая жанр содержимого.</span><span class="sxs-lookup"><span data-stu-id="a982b-130">Null-terminated **string** containing the genre of the content.</span></span>                                             | <span data-ttu-id="a982b-131">Проигрыватель Windows Media 11 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-131">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="a982b-132">усерплайкаунт</span><span class="sxs-lookup"><span data-stu-id="a982b-132">UserPlayCount</span></span>    | <span data-ttu-id="a982b-133">g \_ всзвмдмплайкаунт</span><span class="sxs-lookup"><span data-stu-id="a982b-133">g\_wszWMDMPlayCount</span></span>   | <span data-ttu-id="a982b-134">Значение **типа DWORD** , которое содержит количество раз, когда пользователь воспроизвел файл цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a982b-134">**DWORD** containing the number of times the user has played the digital media file.</span></span>                        | <span data-ttu-id="a982b-135">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-135">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="a982b-136">ReleaseDate</span><span class="sxs-lookup"><span data-stu-id="a982b-136">ReleaseDate</span></span>      | <span data-ttu-id="a982b-137">g \_ всзвмдмеар</span><span class="sxs-lookup"><span data-stu-id="a982b-137">g\_wszWMDMYear</span></span>        | <span data-ttu-id="a982b-138">Дата исходного выпуска элемента.</span><span class="sxs-lookup"><span data-stu-id="a982b-138">The date of the original release of the item.</span></span>                                                               | <span data-ttu-id="a982b-139">Проигрыватель Windows Media 11 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-139">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="a982b-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a982b-140">Title</span></span>            | <span data-ttu-id="a982b-141">g \_ всзвмдмтитле</span><span class="sxs-lookup"><span data-stu-id="a982b-141">g\_wszWMDMTitle</span></span>       | <span data-ttu-id="a982b-142">**Строка** , заканчивающаяся нулем, содержащая заголовок.</span><span class="sxs-lookup"><span data-stu-id="a982b-142">Null-terminated **string** containing the title.</span></span>                                                            | <span data-ttu-id="a982b-143">Проигрыватель Windows Media 11 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-143">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="a982b-144">WM/Траккнумбер</span><span class="sxs-lookup"><span data-stu-id="a982b-144">WM/TrackNumber</span></span>   | <span data-ttu-id="a982b-145">g \_ всзвмдмтракк</span><span class="sxs-lookup"><span data-stu-id="a982b-145">g\_wszWMDMTrack</span></span>       | <span data-ttu-id="a982b-146">Значение **типа DWORD** , содержащее номер записи в альбоме, в котором он был первоначально выпущен.</span><span class="sxs-lookup"><span data-stu-id="a982b-146">**DWORD** containing the track number of the item on the album on which it was originally released.</span></span>         | <span data-ttu-id="a982b-147">Проигрыватель Windows Media 11 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-147">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="a982b-148">UserRating</span><span class="sxs-lookup"><span data-stu-id="a982b-148">UserRating</span></span>       | <span data-ttu-id="a982b-149">g \_ всзвмдмусерратинг</span><span class="sxs-lookup"><span data-stu-id="a982b-149">g\_wszWMDMUserRating</span></span>  | <span data-ttu-id="a982b-150">**Параметр DWORD** , содержащий значение, представляющее оценку, указанную пользователем для файла цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a982b-150">**DWORD** containing a value that represents the star rating the user specified for the digital media file.</span></span> | <span data-ttu-id="a982b-151">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a982b-151">Windows Media Player 10 or later.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a982b-152">См. также</span><span class="sxs-lookup"><span data-stu-id="a982b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a982b-153">**Расширения устройств для ускоренной пересылки метаданных**</span><span class="sxs-lookup"><span data-stu-id="a982b-153">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




