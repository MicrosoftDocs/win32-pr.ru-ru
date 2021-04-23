---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Интернет-магазины проигрывателя Windows Media, track.csv
- Интернет-магазины, track.csv
- Введите 1 Интернет-магазины, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330659"
---
# <a name="trackcsv"></a><span data-ttu-id="e7fa9-107">track.csv</span><span class="sxs-lookup"><span data-stu-id="e7fa9-107">track.csv</span></span>

<span data-ttu-id="e7fa9-108">Этот файл содержит запись для каждой записи в каталоге.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-108">This file contains an entry for each track in the catalog.</span></span> <span data-ttu-id="e7fa9-109">Каждая запись представляет собой строку, состоящую из полей, разделенных табуляцией, описанных в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="e7fa9-110">Поля должны присутствовать в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="e7fa9-111">В столбце Format в следующей таблице описывается способ форматирования каждого текстового поля в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="e7fa9-112">Он не ссылается на тип данных содержимого.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="e7fa9-113">Например, если в столбце Format указано целое число, это означает, что поле содержит строку в Юникоде, представляющую целочисленное значение, а не фактическое целое число.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7fa9-114">Поле</span><span class="sxs-lookup"><span data-stu-id="e7fa9-114">Field</span></span></th>
<th><span data-ttu-id="e7fa9-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="e7fa9-115">Required</span></span></th>
<th><span data-ttu-id="e7fa9-116">Формат</span><span class="sxs-lookup"><span data-stu-id="e7fa9-116">Format</span></span></th>
<th><span data-ttu-id="e7fa9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e7fa9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7fa9-118">TrackID</span><span class="sxs-lookup"><span data-stu-id="e7fa9-118">TrackID</span></span></td>
<td><span data-ttu-id="e7fa9-119">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-119">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-120">Неотрицательное целое число. Пример: 32789</span><span class="sxs-lookup"><span data-stu-id="e7fa9-120">Non-negative integer.Example: 32789</span></span><br/></td>
<td><span data-ttu-id="e7fa9-121">Уникальный идентификатор, предоставленный поставщиком содержимого.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-121">Unique identifier provided by the content provider.</span></span> <span data-ttu-id="e7fa9-122">Должно быть меньше 2 ^ 32. Совет по повышению производительности. Если идентификаторы, назначенные для дорожек из одного и того же альбома, нумеруются последовательно, сжатие каталога будет более эффективным.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-122">Must be less than 2^32.Performance tip: If the IDs assigned to tracks from the same album are numbered consecutively, catalog compression will be more efficient.</span></span> <span data-ttu-id="e7fa9-123">Однако последовательная нумерация записей альбомов не требуется.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-123">However, consecutive numbering of album tracks is not required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fa9-124">тракктитле</span><span class="sxs-lookup"><span data-stu-id="e7fa9-124">TrackTitle</span></span></td>
<td><span data-ttu-id="e7fa9-125">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-125">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-126">Строка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-126">Unicode string.</span></span> <span data-ttu-id="e7fa9-127">Пример: Raygun отсылает Робберс ' Blues</span><span class="sxs-lookup"><span data-stu-id="e7fa9-127">Example: Raygun Robbers' Blues</span></span></td>
<td><span data-ttu-id="e7fa9-128">Имя дорожки.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-128">Name of the track.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fa9-129">Duration</span><span class="sxs-lookup"><span data-stu-id="e7fa9-129">Duration</span></span></td>
<td><span data-ttu-id="e7fa9-130">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-130">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-131">Неотрицательное целое число. Пример: 543</span><span class="sxs-lookup"><span data-stu-id="e7fa9-131">Non-negative integer.Example: 543</span></span><br/></td>
<td><span data-ttu-id="e7fa9-132">Длительность записи в секундах.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-132">Duration of the track in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fa9-133">траккнумбер</span><span class="sxs-lookup"><span data-stu-id="e7fa9-133">TrackNumber</span></span></td>
<td><span data-ttu-id="e7fa9-134">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-134">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-135">Неотрицательное целое число. Пример: 7</span><span class="sxs-lookup"><span data-stu-id="e7fa9-135">Non-negative integer.Example: 7</span></span><br/></td>
<td><span data-ttu-id="e7fa9-136">Номер записи в альбоме записи.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-136">Track number on the track's album.</span></span> <span data-ttu-id="e7fa9-137">Номера записей начинаются с 1 и увеличиваются между наборами дисков.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-137">Track numbers begin at 1 and increase across disc sets.</span></span> <span data-ttu-id="e7fa9-138">Номер записи должен быть меньше 256.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-138">The track number must be less than 256.</span></span> <span data-ttu-id="e7fa9-139">Номер записи, который больше или равен 256, приведет к непредвиденному поведению в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-139">A track number greater than or equal to 256 will cause unexpected behavior in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fa9-140">траккприце</span><span class="sxs-lookup"><span data-stu-id="e7fa9-140">TrackPrice</span></span></td>
<td><span data-ttu-id="e7fa9-141">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-141">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-142">Строка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-142">Unicode string.</span></span> <span data-ttu-id="e7fa9-143">Пример: $0,99.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-143">Example: $0.99.</span></span></td>
<td><span data-ttu-id="e7fa9-144">Отслеживание цены.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-144">Track price.</span></span> <span data-ttu-id="e7fa9-145">Необходимо добавить символ валюты.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-145">The currency symbol should be included.</span></span> <span data-ttu-id="e7fa9-146">Пустая строка, 0 и — имеют специальное значение.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-146">The empty string, 0, and - have special meaning.</span></span> <span data-ttu-id="e7fa9-147">Пустая строка указывает, что цена неизвестна.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-147">An empty string indicates that the price is unknown.</span></span> <span data-ttu-id="e7fa9-148">Ноль в этом поле означает, что запись свободна, а дефис (-) указывает, что эту запись невозможно купить.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-148">A zero in this field means the track is free, and a hyphen (-) indicates that the track cannot be bought.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fa9-149">канстреам</span><span class="sxs-lookup"><span data-stu-id="e7fa9-149">CanStream</span></span></td>
<td><span data-ttu-id="e7fa9-150">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-150">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-151">Логическое.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-151">Boolean.</span></span> <span data-ttu-id="e7fa9-152">Может иметь значение 0 или 1. Пример: 0</span><span class="sxs-lookup"><span data-stu-id="e7fa9-152">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="e7fa9-153">Указывает, может ли записываться потоковая передача.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-153">Indicates whether the track can be streamed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fa9-154">кандовнлоад</span><span class="sxs-lookup"><span data-stu-id="e7fa9-154">CanDownload</span></span></td>
<td><span data-ttu-id="e7fa9-155">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-155">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-156">Логическое.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-156">Boolean.</span></span> <span data-ttu-id="e7fa9-157">Может иметь значение 0 или 1. Пример: 0</span><span class="sxs-lookup"><span data-stu-id="e7fa9-157">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="e7fa9-158">Указывает, можно ли загрузить запись.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-158">Indicates whether the track can be downloaded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fa9-159">хаспревиевклип</span><span class="sxs-lookup"><span data-stu-id="e7fa9-159">HasPreviewClip</span></span></td>
<td><span data-ttu-id="e7fa9-160">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-160">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-161">Логическое.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-161">Boolean.</span></span> <span data-ttu-id="e7fa9-162">Может иметь значение 0 или 1. Пример: 0</span><span class="sxs-lookup"><span data-stu-id="e7fa9-162">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="e7fa9-163">Указывает, имеет ли запись клип предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-163">Indicates whether the track has a preview clip.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fa9-164">хасвидеоклип</span><span class="sxs-lookup"><span data-stu-id="e7fa9-164">HasVideoClip</span></span></td>
<td><span data-ttu-id="e7fa9-165">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-165">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-166">Логическое.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-166">Boolean.</span></span> <span data-ttu-id="e7fa9-167">Может иметь значение 0 или 1. Пример: 0</span><span class="sxs-lookup"><span data-stu-id="e7fa9-167">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="e7fa9-168">Указывает, содержит ли дорожку видеоклип.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-168">Indicates whether the track has a video clip.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fa9-169">паренталратинг</span><span class="sxs-lookup"><span data-stu-id="e7fa9-169">ParentalRating</span></span></td>
<td><span data-ttu-id="e7fa9-170">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-170">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-171">Перечисление.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-171">Enumeration.</span></span> <span data-ttu-id="e7fa9-172">Может быть N, E или C. Пример: N</span><span class="sxs-lookup"><span data-stu-id="e7fa9-172">Can be N, E, or C.Example: N</span></span><br/></td>
<td><span data-ttu-id="e7fa9-173">Указывает рейтинг родительских рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-173">Indicates the Parental Advisory Rating.</span></span> <span data-ttu-id="e7fa9-174">Значения N, E и C заменяются для обычных, явных и чистых.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-174">The values N, E, and C stand for Normal, Explicit, and Clean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fa9-175">линкедалбумид</span><span class="sxs-lookup"><span data-stu-id="e7fa9-175">LinkedAlbumID</span></span></td>
<td><span data-ttu-id="e7fa9-176">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-176">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-177">Неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-177">Non-negative integer.</span></span> <span data-ttu-id="e7fa9-178">Должен быть ИДЕНТИФИКАТОРом альбома.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-178">Must be the ID of an Album.</span></span> <span data-ttu-id="e7fa9-179">Пример: 32423</span><span class="sxs-lookup"><span data-stu-id="e7fa9-179">Example: 32423</span></span></td>
<td><span data-ttu-id="e7fa9-180">ИДЕНТИФИКАТОР альбома, который содержит эту запись.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-180">The ID of the album that contains this track.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e7fa9-181">Каждая запись должна принадлежать к альбому.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-181">Every track must belong to an album.</span></span> <span data-ttu-id="e7fa9-182">То есть для каждой записи поле Линкедалбумид должно быть равно одному из идентификаторов альбома в файле album.csv.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-182">That is, for each track, the LinkedAlbumID field must be equal to one of the album IDs in the album.csv file.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fa9-183">LinkedTrackArtist_ArtistIDs</span><span class="sxs-lookup"><span data-stu-id="e7fa9-183">LinkedTrackArtist_ArtistIDs</span></span></td>
<td><span data-ttu-id="e7fa9-184">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-184">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-185">Список целых чисел.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-185">List of integers.</span></span> <span data-ttu-id="e7fa9-186">Список содержит идентификаторы исполнителей, разделенные точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-186">The list contains artist IDs, separated by semicolons.</span></span> <span data-ttu-id="e7fa9-187">Пример: 41322; 12321; 82123;</span><span class="sxs-lookup"><span data-stu-id="e7fa9-187">Example: 41322;12321; 82123;</span></span></td>
<td><span data-ttu-id="e7fa9-188">Список идентификаторов, соответствующих участвующим исполнителям.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-188">A list of IDs corresponding to the contributing artists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fa9-189">Composer</span><span class="sxs-lookup"><span data-stu-id="e7fa9-189">Composer</span></span></td>
<td><span data-ttu-id="e7fa9-190">Нет</span><span class="sxs-lookup"><span data-stu-id="e7fa9-190">No</span></span></td>
<td><span data-ttu-id="e7fa9-191">Строка в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-191">Unicode string.</span></span> <span data-ttu-id="e7fa9-192">Пример: Бисовен</span><span class="sxs-lookup"><span data-stu-id="e7fa9-192">Example: Beethoven</span></span></td>
<td><span data-ttu-id="e7fa9-193">Композитор курса. Если в жанре записи не установлен набор полей Хаскомпосер, значение поля Composer будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-193">The composer of the track. If the track's genre does not have the HasComposer field set, the value of the Composer field will be ignored.</span></span> <span data-ttu-id="e7fa9-194">Обычно используется только для «джаз» или «классическая» дорожек.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-194">Typically used only for jazz or classical tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fa9-195">Популярность</span><span class="sxs-lookup"><span data-stu-id="e7fa9-195">Popularity</span></span></td>
<td><span data-ttu-id="e7fa9-196">Да</span><span class="sxs-lookup"><span data-stu-id="e7fa9-196">Yes</span></span></td>
<td><span data-ttu-id="e7fa9-197">Неотрицательное целое число или float. Пример: 1252,6</span><span class="sxs-lookup"><span data-stu-id="e7fa9-197">Non-negative integer or Float.Example: 1252.6</span></span><br/></td>
<td><span data-ttu-id="e7fa9-198">Определяет расположение записи в списке при сортировке по популярности.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-198">Determines the position of the track in the list when sorted by popularity.</span></span> <span data-ttu-id="e7fa9-199">Меньшее число указывает на более высокую популярность.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-199">A lower number indicates higher popularity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fa9-200">StarRating</span><span class="sxs-lookup"><span data-stu-id="e7fa9-200">StarRating</span></span></td>
<td><span data-ttu-id="e7fa9-201">Нет</span><span class="sxs-lookup"><span data-stu-id="e7fa9-201">No</span></span></td>
<td><span data-ttu-id="e7fa9-202">Float. Пример: 4,21</span><span class="sxs-lookup"><span data-stu-id="e7fa9-202">Float.Example: 4.21</span></span><br/></td>
<td><span data-ttu-id="e7fa9-203">Перед отображением в пользовательском интерфейсе проигрывателя Windows Media оценка будет округляться до ближайшей звезды с 1/4.</span><span class="sxs-lookup"><span data-stu-id="e7fa9-203">The star rating will be rounded to the nearest 1/4 star by Windows Media Player before being displayed in the Windows Media Player user interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 





