---
title: Соглашение о задании BITS проигрывателя Windows Media
description: Проигрыватель Windows Media может автоматически скачивать и добавлять цифровые мультимедийные элементы в библиотеку, если используется фоновая интеллектуальная служба передачи (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Интернет-магазины проигрывателя Windows Media, фоновая интеллектуальная служба передачи (BITS)
- Интернет-магазины, фоновая интеллектуальная служба передачи (BITS)
- Тип 2 Интернет-магазинов, фоновая интеллектуальная служба передачи (BITS)
- Фоновая интеллектуальная служба передачи (BITS)
- БИТ (фоновая интеллектуальная служба передачи)
- Интернет-магазины проигрывателя Windows Media, соглашение о заданиях BITS
- Интернет-магазины, соглашение о заданиях BITS
- Тип 2 Интернет-магазинов, соглашение о задании BITS
- Соглашение о задании BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260977"
---
# <a name="windows-media-player-bits-job-convention"></a><span data-ttu-id="62d4e-112">Соглашение о задании BITS проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="62d4e-112">Windows Media Player BITS Job Convention</span></span>

<span data-ttu-id="62d4e-113">Проигрыватель Windows Media может автоматически скачивать и добавлять цифровые мультимедийные элементы в библиотеку, если используется [Фоновая интеллектуальная служба передачи (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span><span class="sxs-lookup"><span data-stu-id="62d4e-113">Windows Media Player can automatically download and add digital media items to the library if you use [Background Intelligent Transfer Service (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span></span> <span data-ttu-id="62d4e-114">Чтобы воспользоваться этой функцией, необходимо добавить задание в очередь передачи BITS и вызвать **использованием метода ibackgroundcopyjob:: SetDescription**, указав строку описания, которая использует правильный формат.</span><span class="sxs-lookup"><span data-stu-id="62d4e-114">To take advantage of this feature, you must add your job to the BITS transfer queue and call **IBackgroundCopyJob::SetDescription**, providing a description string that uses the correct format.</span></span>

> [!Note]  
> <span data-ttu-id="62d4e-115">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="62d4e-115">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="62d4e-116">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="62d4e-116">Use of this functionality outside the context of an online store is not supported.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="62d4e-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62d4e-117">Syntax</span></span>

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a><span data-ttu-id="62d4e-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="62d4e-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d4e-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span><span class="sxs-lookup"><span data-stu-id="62d4e-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-120">Генерируемое случайным образом 32-разрядное значение, используемое проигрывателем Windows Media для обнаружения службы.</span><span class="sxs-lookup"><span data-stu-id="62d4e-120">A randomly generated 32-bit value that Windows Media Player uses to identify the service.</span></span>

</dd> <dt>

<span data-ttu-id="62d4e-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Поставщики*</span><span class="sxs-lookup"><span data-stu-id="62d4e-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-122">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="62d4e-122">The provider name.</span></span> <span data-ttu-id="62d4e-123">Это значение должно совпадать с допустимым именем ключа Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="62d4e-123">This value must match a valid online store key name.</span></span>

</dd> <dt>

<span data-ttu-id="62d4e-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*албумартист*</span><span class="sxs-lookup"><span data-stu-id="62d4e-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-125">Имя основного исполнителя для альбома.</span><span class="sxs-lookup"><span data-stu-id="62d4e-125">The name of the primary artist for the album.</span></span>

</dd> <dt>

<span data-ttu-id="62d4e-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*албумтитле*</span><span class="sxs-lookup"><span data-stu-id="62d4e-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-127">Название альбома.</span><span class="sxs-lookup"><span data-stu-id="62d4e-127">The title of the album.</span></span>

</dd> <dt>

<span data-ttu-id="62d4e-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*траккнумбер*</span><span class="sxs-lookup"><span data-stu-id="62d4e-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-129">Номер записи компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="62d4e-129">The CD track number.</span></span>

</dd> <dt>

<span data-ttu-id="62d4e-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Титуль*</span><span class="sxs-lookup"><span data-stu-id="62d4e-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Title*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-131">Заголовок содержимого.</span><span class="sxs-lookup"><span data-stu-id="62d4e-131">The title of the content.</span></span>

</dd> <dt>

<span data-ttu-id="62d4e-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Длитель*</span><span class="sxs-lookup"><span data-stu-id="62d4e-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-133">Длительность содержимого.</span><span class="sxs-lookup"><span data-stu-id="62d4e-133">The duration of the content.</span></span>

</dd> <dt>

<span data-ttu-id="62d4e-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Звездочк*</span><span class="sxs-lookup"><span data-stu-id="62d4e-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Rating*</span></span>
</dt> <dd>

<span data-ttu-id="62d4e-135">Оценка содержимого.</span><span class="sxs-lookup"><span data-stu-id="62d4e-135">The rating for the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62d4e-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62d4e-136">Remarks</span></span>

<span data-ttu-id="62d4e-137">Когда проигрыватель Windows Media 10 или более поздней версии использует BITS для загрузки содержимого, он перечисляет задания в очереди передачи и проверяет строку описания для каждого задания.</span><span class="sxs-lookup"><span data-stu-id="62d4e-137">When Windows Media Player 10 or later uses BITS to download content, it enumerates the jobs in the transfer queue and inspects the description string for each job.</span></span> <span data-ttu-id="62d4e-138">Если строка описания соответствует ожидаемому соглашению, проигрыватель Windows Media загрузит содержимое.</span><span class="sxs-lookup"><span data-stu-id="62d4e-138">If the description string matches the expected convention, Windows Media Player downloads the content.</span></span>

<span data-ttu-id="62d4e-139">Необходимо добавить только один файл цифрового мультимедиа для скачивания в каждое задание BITS.</span><span class="sxs-lookup"><span data-stu-id="62d4e-139">You must add only one digital media file for download to each BITS job.</span></span>

<span data-ttu-id="62d4e-140">После запуска задания BITS с использованием этого соглашения необходимо разрешить проигрывателю Windows Media завершить задание.</span><span class="sxs-lookup"><span data-stu-id="62d4e-140">After you start a BITS job using this convention, you must let Windows Media Player complete the job.</span></span> <span data-ttu-id="62d4e-141">Проигрыватель Windows Media также удалит задание из очереди BITS, переместит скачанный файл в расположение, где сохраняется музыкальная музыка, и добавит скачанный файл в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="62d4e-141">Windows Media Player will also remove the job from the BITS queue, move the downloaded file to the location where ripped music is saved, and add the downloaded file to the library.</span></span>

<span data-ttu-id="62d4e-142">Параметр *serviceId* должен содержать ненулевое 32-разрядное значение.</span><span class="sxs-lookup"><span data-stu-id="62d4e-142">The *serviceId* parameter must contain a nonzero 32-bit value.</span></span> <span data-ttu-id="62d4e-143">Для создания этого значения рекомендуется использовать функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="62d4e-143">We recommend that you use the function [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) to create this value.</span></span>

<span data-ttu-id="62d4e-144">Имя файла, указанное с помощью параметра *LocalName* **использованием метода ibackgroundcopyjob:: AddFile** , должно иметь расширение. WMA,. WMV,. mp3 или. ASF.</span><span class="sxs-lookup"><span data-stu-id="62d4e-144">The file name you specify using the *localName* parameter of **IBackgroundCopyJob::AddFile** must have a .wma, .wmv, .mp3, or .asf file name extension.</span></span>

<span data-ttu-id="62d4e-145">Остальные параметры предназначены для хранения значений метаданных, связанных с содержимым.</span><span class="sxs-lookup"><span data-stu-id="62d4e-145">The remaining parameters are designed to contain metadata values related to the content.</span></span> <span data-ttu-id="62d4e-146">Эти значения можно получить на веб-странице Интернет-магазина с помощью **довнлоадитем. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="62d4e-146">You can retrieve these values from your online store webpage by using **DownloadItem.getItemInfo**.</span></span> <span data-ttu-id="62d4e-147">Правильную коллекцию загрузки можно получить, вызвав **довнлоадманажер. жетдовнлоадколлектион** и указав *serviceId* в качестве параметра *CollectionID* .</span><span class="sxs-lookup"><span data-stu-id="62d4e-147">You can retrieve the correct download collection by calling **DownloadManager.getDownloadCollection** and providing *serviceId* as the *collectionId* parameter.</span></span>

<span data-ttu-id="62d4e-148">Проигрыватель Windows Media периодически проверяет очередь BITS во время работы проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="62d4e-148">Windows Media Player inspects the BITS queue periodically while the Player is running.</span></span> <span data-ttu-id="62d4e-149">Чтобы проигрыватель Windows Media проверял очередь BITS для заданий скачивания, необходимо создать значение в следующем подразделе реестра:</span><span class="sxs-lookup"><span data-stu-id="62d4e-149">To ensure that Windows Media Player checks the BITS queue for download jobs, you should create a value in the following registry subkey:</span></span>

<span data-ttu-id="62d4e-150">**HKEY \_ текущее \_ пользовательское \\ программное обеспечение \\ \\ службы Microsoft MediaPlayer \\**</span><span class="sxs-lookup"><span data-stu-id="62d4e-150">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Services**</span></span>

<span data-ttu-id="62d4e-151">Значение должно быть создано следующим образом.</span><span class="sxs-lookup"><span data-stu-id="62d4e-151">The value should be created as follows.</span></span>



| <span data-ttu-id="62d4e-152">Имя</span><span class="sxs-lookup"><span data-stu-id="62d4e-152">Name</span></span>                | <span data-ttu-id="62d4e-153">Тип</span><span class="sxs-lookup"><span data-stu-id="62d4e-153">Type</span></span>      | <span data-ttu-id="62d4e-154">Описание</span><span class="sxs-lookup"><span data-stu-id="62d4e-154">Description</span></span>                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d4e-155">**рефрешдовнлоад**</span><span class="sxs-lookup"><span data-stu-id="62d4e-155">**RefreshDownload**</span></span> | <span data-ttu-id="62d4e-156">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="62d4e-156">**DWORD**</span></span> | <span data-ttu-id="62d4e-157">Указывает, должен ли проигрыватель Windows Media проверять очередь BITS для загрузки заданий.</span><span class="sxs-lookup"><span data-stu-id="62d4e-157">Specifies whether Windows Media Player should inspect the BITS queue for download jobs.</span></span> <span data-ttu-id="62d4e-158">Если значение равно нулю, проигрыватель не будет проверять очередь BITS.</span><span class="sxs-lookup"><span data-stu-id="62d4e-158">If the value is zero, the Player will not inspect the BITS queue.</span></span> <span data-ttu-id="62d4e-159">Проигрыватель должен проверить очередь, если значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="62d4e-159">The Player must inspect the queue if the value is nonzero.</span></span> |



 

<span data-ttu-id="62d4e-160">Можно использовать следующий альтернативный синтаксис для добавления заданий BITS, которые не удается завершить проигрывателем Windows Media, но для которого он просто отображает сведения о состоянии:</span><span class="sxs-lookup"><span data-stu-id="62d4e-160">You can use the following alternate syntax to add BITS jobs that Windows Media Player does not complete, but for which it simply shows status information:</span></span>

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

<span data-ttu-id="62d4e-161">При использовании предыдущего синтаксиса необходимо написать код для завершения загрузки BITS, организации содержимого на компьютере пользователя и добавления содержимого в библиотеку при необходимости.</span><span class="sxs-lookup"><span data-stu-id="62d4e-161">When you use the preceding syntax, you must write code to complete the BITS download, organize the content on the user's computer, and add the content to the library, if desired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62d4e-162">См. также</span><span class="sxs-lookup"><span data-stu-id="62d4e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62d4e-163">CryptGenRandom</span><span class="sxs-lookup"><span data-stu-id="62d4e-163">CryptGenRandom</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[<span data-ttu-id="62d4e-164">**Довнлоадитем. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="62d4e-164">**DownloadItem.getItemInfo**</span></span>](downloaditem-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="62d4e-165">**Довнлоадманажер. Жетдовнлоадколлектион**</span><span class="sxs-lookup"><span data-stu-id="62d4e-165">**DownloadManager.getDownloadCollection**</span></span>](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="62d4e-166">**Справочные материалы по интернет-магазинам типа 2**</span><span class="sxs-lookup"><span data-stu-id="62d4e-166">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 