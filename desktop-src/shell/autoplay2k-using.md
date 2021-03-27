---
description: Когда оболочка обнаруживает вставку нового носителя или вложение устройства горячего подключения, определяется содержимое устройства или носителя. Автозапуск, в зависимости от текущих параметров, выполняет одно из следующих действий.
title: Использование и Настройка автоматического запуска
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808878"
---
# <a name="using-and-configuring-autoplay"></a><span data-ttu-id="8fe28-104">Использование и Настройка автоматического запуска</span><span class="sxs-lookup"><span data-stu-id="8fe28-104">Using and Configuring AutoPlay</span></span>

<span data-ttu-id="8fe28-105">Когда оболочка обнаруживает вставку нового носителя или вложение устройства горячего подключения, определяется содержимое устройства или носителя.</span><span class="sxs-lookup"><span data-stu-id="8fe28-105">When the Shell detects the insertion of new media or the attachment of a hot-plug device, the contents of the device or media are determined.</span></span> <span data-ttu-id="8fe28-106">Автозапуск, в зависимости от текущих параметров, выполняет одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="8fe28-106">AutoPlay, depending on its current settings, does one of the following.</span></span>

-   <span data-ttu-id="8fe28-107">Автоматически воспроизводит содержимое.</span><span class="sxs-lookup"><span data-stu-id="8fe28-107">Plays the content automatically.</span></span>
-   <span data-ttu-id="8fe28-108">Отображает диалоговое окно, предлагающее пользователю выбрать обработчик по умолчанию для одного типа содержимого.</span><span class="sxs-lookup"><span data-stu-id="8fe28-108">Displays a dialog box prompting the user to choose a default handler for a single content type.</span></span>
-   <span data-ttu-id="8fe28-109">Представляет, в случае смешанного содержимого, список доступных приложений обработчика для запуска.</span><span class="sxs-lookup"><span data-stu-id="8fe28-109">Presents, in the case of mixed content, a list of available handler applications to launch.</span></span> <span data-ttu-id="8fe28-110">Затем выбранный обработчик автоматически воспроизводит связанный с ним тип содержимого.</span><span class="sxs-lookup"><span data-stu-id="8fe28-110">The chosen handler then automatically plays its associated content type.</span></span>
-   <span data-ttu-id="8fe28-111">Отображает стандартное представление файлов в виде папки.</span><span class="sxs-lookup"><span data-stu-id="8fe28-111">Displays a standard folder view of the files.</span></span>
-   <span data-ttu-id="8fe28-112">Ничего не делает, если, ранее пользователь выбрал параметр **не предпринимать никаких действий** для этого типа содержимого, а также **выбранное действие всегда выполняется**.</span><span class="sxs-lookup"><span data-stu-id="8fe28-112">Does nothing if, earlier, the user had chosen **Take no action** for that content type as well as specified **Always do the selected action**.</span></span>

<span data-ttu-id="8fe28-113">Если содержимое не соответствует критериям автозапуска, событие затем передается в функцию получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="8fe28-113">If the contents do not meet the criteria for AutoPlay, the event is then passed to Windows Image Acquisition (WIA).</span></span>

<span data-ttu-id="8fe28-114">В следующих разделах обсуждается настройка и использование автозапуска.</span><span class="sxs-lookup"><span data-stu-id="8fe28-114">The following topics discuss the setup and use of AutoPlay.</span></span>

-   [<span data-ttu-id="8fe28-115">Подготовка оборудования и программного обеспечения для использования с автозапуском</span><span class="sxs-lookup"><span data-stu-id="8fe28-115">Preparing Hardware and Software for Use with AutoPlay</span></span>](#preparing-hardware-and-software-for-use-with-autoplay)
-   [<span data-ttu-id="8fe28-116">Как автозапуск ищет мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8fe28-116">How AutoPlay Searches Media</span></span>](#how-autoplay-searches-media)
-   [<span data-ttu-id="8fe28-117">Определение одного и смешанного типа содержимого</span><span class="sxs-lookup"><span data-stu-id="8fe28-117">Defining Single and Mixed Content Types</span></span>](#defining-single-and-mixed-content-types)
-   [<span data-ttu-id="8fe28-118">Примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="8fe28-118">Sample Scenarios</span></span>](#sample-scenarios)
    -   [<span data-ttu-id="8fe28-119">Автозапуск устройств хранения с изображениями мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8fe28-119">AutoPlay for Storage Devices with Picture Media</span></span>](#autoplay-for-storage-devices-with-picture-media)
    -   [<span data-ttu-id="8fe28-120">Автозапуск для устройств воспроизведения музыкальных файлов и запоминающих устройств, содержащих музыкальные носители</span><span class="sxs-lookup"><span data-stu-id="8fe28-120">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [<span data-ttu-id="8fe28-121">Автозапуск воспроизведения видео при первой презентации</span><span class="sxs-lookup"><span data-stu-id="8fe28-121">AutoPlay for Video Playback on First Presentation</span></span>](#autoplay-for-video-playback-on-first-presentation)
-   [<span data-ttu-id="8fe28-122">Назначение приложений обработчика по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8fe28-122">Assigning Default Handler Applications</span></span>](#assigning-default-handler-applications)
-   [<span data-ttu-id="8fe28-123">Обработка мультимедиа, содержащего смешанные типы содержимого</span><span class="sxs-lookup"><span data-stu-id="8fe28-123">Handling Media Containing Mixed Content Types</span></span>](#handling-media-containing-mixed-content-types)
-   [<span data-ttu-id="8fe28-124">Пользовательские интерфейсы автозапуска</span><span class="sxs-lookup"><span data-stu-id="8fe28-124">AutoPlay User Interfaces</span></span>](#autoplay-user-interfaces)
    -   [<span data-ttu-id="8fe28-125">Диалоговое окно «один тип содержимого»</span><span class="sxs-lookup"><span data-stu-id="8fe28-125">Single Content Type Dialog Box</span></span>](#single-content-type-dialog-box)
    -   [<span data-ttu-id="8fe28-126">Диалоговое окно "смешанный носитель"</span><span class="sxs-lookup"><span data-stu-id="8fe28-126">Mixed Media Dialog Box</span></span>](#mixed-media-dialog-box)
    -   [<span data-ttu-id="8fe28-127">Страница свойств</span><span class="sxs-lookup"><span data-stu-id="8fe28-127">Property Page</span></span>](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a><span data-ttu-id="8fe28-128">Подготовка оборудования и программного обеспечения для использования с автозапуском</span><span class="sxs-lookup"><span data-stu-id="8fe28-128">Preparing Hardware and Software for Use with AutoPlay</span></span>

<span data-ttu-id="8fe28-129">Для работы функции автозапуска необходимо, чтобы в реестре отображалось несколько фрагментов данных.</span><span class="sxs-lookup"><span data-stu-id="8fe28-129">Several pieces of information need to appear in the registry for AutoPlay to function.</span></span> <span data-ttu-id="8fe28-130">Эти части информации взаимодействуют друг с другом для формирования полной среды автозапуска.</span><span class="sxs-lookup"><span data-stu-id="8fe28-130">These pieces of information interact and reference each other to form the full AutoPlay environment.</span></span> <span data-ttu-id="8fe28-131">В этом документе описывается настройка каждого из этих фрагментов данных в качестве отдельной изолированной процедуры.</span><span class="sxs-lookup"><span data-stu-id="8fe28-131">This document presents the setup of each of these pieces of information as an individual stand-alone procedure.</span></span>

<span data-ttu-id="8fe28-132">Дополнительные инструкции см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="8fe28-132">See the following topics for additional instructions.</span></span>

-   [<span data-ttu-id="8fe28-133">Назначение обработчика устройства устройству</span><span class="sxs-lookup"><span data-stu-id="8fe28-133">How To Assign a Device Handler to a Device</span></span>](how-to-assign-a-device-handler-to-a-device.md)
-   [<span data-ttu-id="8fe28-134">Указание значка, метки или обработчика устройства для устройства с помощью группы устройств</span><span class="sxs-lookup"><span data-stu-id="8fe28-134">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [<span data-ttu-id="8fe28-135">Указание значка, метки или обработчика устройства для устройства с помощью класса устройств</span><span class="sxs-lookup"><span data-stu-id="8fe28-135">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [<span data-ttu-id="8fe28-136">Как предотвратить автозапуск для компонента</span><span class="sxs-lookup"><span data-stu-id="8fe28-136">How To Prevent AutoPlay for a Component</span></span>](how-to-prevent-autoplay-for-a-component.md)
-   [<span data-ttu-id="8fe28-137">Регистрация обработчика для события устройства</span><span class="sxs-lookup"><span data-stu-id="8fe28-137">How To Register a Handler for a Device Event</span></span>](how-to-register-a-handler-for-a-device-event.md)
-   [<span data-ttu-id="8fe28-138">Использование событий автозапуска в выполняющихся приложениях</span><span class="sxs-lookup"><span data-stu-id="8fe28-138">How To Use AutoPlay Events in Running Applications</span></span>](how-to-use-autoplay-events-in-running-applications.md)
-   [<span data-ttu-id="8fe28-139">Регистрация обработчика событий</span><span class="sxs-lookup"><span data-stu-id="8fe28-139">How To Register an Event Handler</span></span>](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a><span data-ttu-id="8fe28-140">Как автозапуск ищет мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8fe28-140">How AutoPlay Searches Media</span></span>

<span data-ttu-id="8fe28-141">Автозапуск ищет файлы мультимедиа на четырех уровнях ниже корневого каталога для поиска известных типов файлов.</span><span class="sxs-lookup"><span data-stu-id="8fe28-141">AutoPlay searches for media four directory levels below the root directory to find known file types.</span></span> <span data-ttu-id="8fe28-142">Он использует значение PerceivedType, связанное с расширением имени файла в реестре, для определения категории файлов, будь то изображение, звуковой файл или видеофайл.</span><span class="sxs-lookup"><span data-stu-id="8fe28-142">It uses the PerceivedType value associated with a file name extension in the registry to determine the file category, whether it is an image, an audio file, or a video file.</span></span> <span data-ttu-id="8fe28-143">С помощью этой информации Автозапуск запускает соответствующий обработчик для этого устройства и типа файла.</span><span class="sxs-lookup"><span data-stu-id="8fe28-143">With this information, AutoPlay launches the appropriate handler for that device and file type.</span></span> <span data-ttu-id="8fe28-144">Дополнительные сведения см. в разделе [наблюдаемые типы и регистрация приложений](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="8fe28-144">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="defining-single-and-mixed-content-types"></a><span data-ttu-id="8fe28-145">Определение одного и смешанного типа содержимого</span><span class="sxs-lookup"><span data-stu-id="8fe28-145">Defining Single and Mixed Content Types</span></span>

<span data-ttu-id="8fe28-146">Автозапуск определяет три основные категории содержимого.</span><span class="sxs-lookup"><span data-stu-id="8fe28-146">AutoPlay defines three main content categories.</span></span>

-   <span data-ttu-id="8fe28-147">Изображения</span><span class="sxs-lookup"><span data-stu-id="8fe28-147">Pictures</span></span>
-   <span data-ttu-id="8fe28-148">Музыка</span><span class="sxs-lookup"><span data-stu-id="8fe28-148">Music</span></span>
-   <span data-ttu-id="8fe28-149">Видео</span><span class="sxs-lookup"><span data-stu-id="8fe28-149">Video</span></span>

<span data-ttu-id="8fe28-150">Предполагается, что носитель содержит один тип содержимого, если все файлы на носителе попадают только в одну из этих трех категорий.</span><span class="sxs-lookup"><span data-stu-id="8fe28-150">A medium is considered to contain a single content type if all of the files on the medium fall into only one of these three categories.</span></span> <span data-ttu-id="8fe28-151">Обратите внимание, что это не означает, что файлы должны иметь один и *тот же тип файлов;* JPG, GIF и. bmp имеют разные типы файлов, но один тип содержимого (рисунки).</span><span class="sxs-lookup"><span data-stu-id="8fe28-151">Note that this does not mean that the files must be of the same *file* type; .jpg, .gif, and .bmp are different file types, but one content type (pictures).</span></span>

<span data-ttu-id="8fe28-152">Если на носителе имеются Поддерживаемые типы содержимого, но ни один тип содержимого не может учитывать 100 процентов от общего числа, то предполагается, что носитель содержит смешанный тип содержимого и обрабатывается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8fe28-152">If supported content types are present on the medium, but no single content type can account for 100 percent of the total, then the medium is considered to contain mixed content type and is handled accordingly.</span></span> <span data-ttu-id="8fe28-153">Дополнительные сведения см. в разделе [Обработка мультимедиа, содержащего смешанные типы содержимого](#handling-media-containing-mixed-content-types).</span><span class="sxs-lookup"><span data-stu-id="8fe28-153">For more information, see [Handling Media Containing Mixed Content Types](#handling-media-containing-mixed-content-types).</span></span>

## <a name="sample-scenarios"></a><span data-ttu-id="8fe28-154">Примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="8fe28-154">Sample Scenarios</span></span>

<span data-ttu-id="8fe28-155">Приведенные ниже сценарии предоставляют основные сведения о том, что следует ждать от автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="8fe28-155">The following scenarios provide a basic understanding of what to expect from AutoPlay.</span></span>

### <a name="autoplay-for-storage-devices-with-picture-media"></a><span data-ttu-id="8fe28-156">Автозапуск устройств хранения с изображениями мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8fe28-156">AutoPlay for Storage Devices with Picture Media</span></span>

1.  <span data-ttu-id="8fe28-157">Пользователь подключает устройство USB СанДиск CompactFlash Reader, в котором уже вставлен носитель с типом содержимого изображения 100% в виде JPG-файлов.</span><span class="sxs-lookup"><span data-stu-id="8fe28-157">The user attaches a USB SanDisk CompactFlash reader device that already has media inserted containing 100 percent picture content type in the form of .jpg files.</span></span>
2.  <span data-ttu-id="8fe28-158">В уведомлении **обнаружено новое оборудование-СанДиск имажемате**.</span><span class="sxs-lookup"><span data-stu-id="8fe28-158">Notification displays **Found New Hardware - SanDisk ImageMate**.</span></span>
3.  <span data-ttu-id="8fe28-159">Автозапуск запускает соответствующее приложение Image.</span><span class="sxs-lookup"><span data-stu-id="8fe28-159">AutoPlay launches the appropriate image application.</span></span>

<span data-ttu-id="8fe28-160">Аналогично, когда пользователь вставляет тот же адаптер CompactFlash в модуль чтения, когда модуль чтения уже подключен к системе, событие вставки носителя также вызывает автозапуск для запуска изображения слайд-шоу.</span><span class="sxs-lookup"><span data-stu-id="8fe28-160">Similarly, when the user inserts that same CompactFlash media into the reader when the reader is already attached to the system, the media insert event also causes AutoPlay to launch the image slide show application.</span></span> <span data-ttu-id="8fe28-161">Пользователь имеет возможность перейти на страницу свойств устройства мультимедиа СанДиск, чтобы изменить значение по умолчанию на другое зарегистрированное приложение автозапуска, например мастер сканера и камеры, или Picture!.</span><span class="sxs-lookup"><span data-stu-id="8fe28-161">The user has the option of going to the Properties page of the SanDisk media device to change the default to another registered AutoPlay application, such as the Scanner and Camera Wizard or Picture It!.</span></span>

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a><span data-ttu-id="8fe28-162">Автозапуск для устройств воспроизведения музыкальных файлов и запоминающих устройств, содержащих музыкальные носители</span><span class="sxs-lookup"><span data-stu-id="8fe28-162">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>

1.  <span data-ttu-id="8fe28-163">Пользователь присоединяет проигрыватель USB-ромба Рио MP3.</span><span class="sxs-lookup"><span data-stu-id="8fe28-163">The user attaches a USB Diamond Rio MP3 Player.</span></span>
2.  <span data-ttu-id="8fe28-164">В уведомлении **обнаружено новое оборудование-ромб Рио MP3 Player**.</span><span class="sxs-lookup"><span data-stu-id="8fe28-164">Notification displays **Found New Hardware - Diamond Rio MP3 Player**.</span></span>
3.  <span data-ttu-id="8fe28-165">Автозапуск воспроизводит файлы с помощью зарегистрированного обработчика по умолчанию (например, проигрывателя Windows Media).</span><span class="sxs-lookup"><span data-stu-id="8fe28-165">AutoPlay plays the files using its registered default handler—for instance, Windows Media Player.</span></span>

<span data-ttu-id="8fe28-166">Аналогичным образом, если пользователь вставит носитель, содержащий MP3-файлы (например, CompactFlash, Смартмедиа, память или компакт-диск), который учитывает 100 процентов общего поддерживаемого содержимого на устройстве хранения, событие вставки носителя также приведет к воспроизведению файлов с помощью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8fe28-166">Similarly, if the user inserts any media containing .mp3 files (for example, CompactFlash, SmartMedia, Memory Stick, or CD-ROM) that account for 100 percent of the total supported content into a storage device, the media insert event would also cause AutoPlay to play the files using the Windows Media Player.</span></span> <span data-ttu-id="8fe28-167">Пользователь может получить доступ к странице свойств устройства хранения и изменить действие по умолчанию на другое зарегистрированное приложение автозапуска, например винамп или Real Player.</span><span class="sxs-lookup"><span data-stu-id="8fe28-167">The user can access the property sheet of the storage device and change the default action to another registered AutoPlay application, such as WinAmp or Real Player.</span></span>

### <a name="autoplay-for-video-playback-on-first-presentation"></a><span data-ttu-id="8fe28-168">Автозапуск воспроизведения видео при первой презентации</span><span class="sxs-lookup"><span data-stu-id="8fe28-168">AutoPlay for Video Playback on First Presentation</span></span>

1.  <span data-ttu-id="8fe28-169">Пользователь подключается к цифровой видеокамере 1394 в первый раз.</span><span class="sxs-lookup"><span data-stu-id="8fe28-169">The user plugs in a 1394 digital video camera for the first time.</span></span>
2.  <span data-ttu-id="8fe28-170">Пользователю предоставляется простое диалоговое окно с запросом на запуск приложения.</span><span class="sxs-lookup"><span data-stu-id="8fe28-170">The user is presented with a simple dialog box that asks what application to run.</span></span> <span data-ttu-id="8fe28-171">Можно выбрать Запуск одного из зарегистрированных приложений автозапуска или открытие папки для просмотра файлов.</span><span class="sxs-lookup"><span data-stu-id="8fe28-171">The choices are to run one of the registered AutoPlay applications or to open a folder to view files.</span></span> <span data-ttu-id="8fe28-172">Пользователь может указать, что выбранное поведение будет сохранено в качестве действия по умолчанию для последующего события горячего подключения цифровой видеокамеры.</span><span class="sxs-lookup"><span data-stu-id="8fe28-172">The user may set the selected behavior to be saved as the default action for later digital video camera hot-plug events.</span></span>

## <a name="assigning-default-handler-applications"></a><span data-ttu-id="8fe28-173">Назначение приложений обработчика по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8fe28-173">Assigning Default Handler Applications</span></span>

<span data-ttu-id="8fe28-174">Новая установка Windows находит Автозапуск с набором зарегистрированных приложений обработчиков.</span><span class="sxs-lookup"><span data-stu-id="8fe28-174">A fresh installation of Windows finds AutoPlay with a set of registered handler applications.</span></span> <span data-ttu-id="8fe28-175">Приложения, зарегистрированные по умолчанию во время установки Windows, приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="8fe28-175">Applications registered by default during a Windows installation are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8fe28-176">Тип носителя</span><span class="sxs-lookup"><span data-stu-id="8fe28-176">Media Type</span></span></th>
<th><span data-ttu-id="8fe28-177">Приложения</span><span class="sxs-lookup"><span data-stu-id="8fe28-177">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fe28-178">Изображения</span><span class="sxs-lookup"><span data-stu-id="8fe28-178">Pictures</span></span></td>
<td><ul>
<li><span data-ttu-id="8fe28-179">Слайд-шоу (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fe28-179">Slide Show (default)</span></span></li>
<li><span data-ttu-id="8fe28-180">Мастер настройки камеры и сканера</span><span class="sxs-lookup"><span data-stu-id="8fe28-180">Camera and Scanner Wizard</span></span></li>
<li><span data-ttu-id="8fe28-181">Мастер печати</span><span class="sxs-lookup"><span data-stu-id="8fe28-181">Printing Wizard</span></span></li>
<li><span data-ttu-id="8fe28-182">Открытие папки</span><span class="sxs-lookup"><span data-stu-id="8fe28-182">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fe28-183">Музыка</span><span class="sxs-lookup"><span data-stu-id="8fe28-183">Music</span></span></td>
<td><ul>
<li><span data-ttu-id="8fe28-184">Проигрыватель Windows Media (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fe28-184">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="8fe28-185">Открытие папки</span><span class="sxs-lookup"><span data-stu-id="8fe28-185">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8fe28-186">Видео</span><span class="sxs-lookup"><span data-stu-id="8fe28-186">Video</span></span></td>
<td><ul>
<li><span data-ttu-id="8fe28-187">Проигрыватель Windows Media (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fe28-187">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="8fe28-188">Открытие папки</span><span class="sxs-lookup"><span data-stu-id="8fe28-188">Open folder</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8fe28-189">В случае неподдерживаемых типов пользователям предлагается назначить значение по умолчанию для действия автозапуска, связанного с каждым устройством хранения, при первом вводе в систему.</span><span class="sxs-lookup"><span data-stu-id="8fe28-189">In the case of non-supported types, users are asked to assign the default setting for the AutoPlay action associated with each storage device on its first introduction to the system.</span></span> <span data-ttu-id="8fe28-190">В это время пользователю предлагается выбрать действие из предоставленного списка зарегистрированных приложений или отобразить представление папки с перечнем содержимого носителя.</span><span class="sxs-lookup"><span data-stu-id="8fe28-190">At that time, the user is prompted to choose an action from a provided list of registered applications or to display a folder view listing the media content.</span></span> <span data-ttu-id="8fe28-191">Пользователь также имеет возможность выбирать при каждом обнаружении типа носителя, а не сохранять какое-либо конкретное приложение в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8fe28-191">The user also has the option of choosing to be prompted each time the media type is detected rather than saving any particular application as a default.</span></span>

> [!Note]  
> <span data-ttu-id="8fe28-192">Производители устройств имеют возможность регистрации и назначения приложений по умолчанию для использования с определенными продуктами.</span><span class="sxs-lookup"><span data-stu-id="8fe28-192">Device manufacturers have the option of registering and assigning default applications to be used with their particular products.</span></span> <span data-ttu-id="8fe28-193">В таких случаях диалоговое окно, предлагающее выбрать пользователя, не отображается.</span><span class="sxs-lookup"><span data-stu-id="8fe28-193">In these cases, the dialog box offering a choice to the user is not displayed.</span></span>

 

<span data-ttu-id="8fe28-194">Для предоставления в качестве параметра обработчика автозапуска недавно установленные приложения должны регистрироваться в реестре.</span><span class="sxs-lookup"><span data-stu-id="8fe28-194">To be offered as a handler option by AutoPlay, newly installed applications must register themselves in the registry.</span></span> <span data-ttu-id="8fe28-195">Дополнительные сведения см. в разделе [Подготовка оборудования и программного обеспечения для использования при автозапуске](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="8fe28-195">For details, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

<span data-ttu-id="8fe28-196">Пользователи всегда могут изменять обработчик автозапуска по умолчанию для любого устройства хранения или типа содержимого.</span><span class="sxs-lookup"><span data-stu-id="8fe28-196">Users can always change the default AutoPlay handler for any storage device or content type.</span></span> <span data-ttu-id="8fe28-197">Страница свойств автозапуска доступна для изменения на вкладке свойств устройства хранения в **Мой компьютер**.</span><span class="sxs-lookup"><span data-stu-id="8fe28-197">The AutoPlay property page is accessible for change in the property sheet of the storage device in **My Computer**.</span></span>

<span data-ttu-id="8fe28-198">Примеры пользовательских запросов и страниц свойств см. в разделе [Автозапуск пользовательских интерфейсов](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="8fe28-198">For examples of user prompts and property pages, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="handling-media-containing-mixed-content-types"></a><span data-ttu-id="8fe28-199">Обработка мультимедиа, содержащего смешанные типы содержимого</span><span class="sxs-lookup"><span data-stu-id="8fe28-199">Handling Media Containing Mixed Content Types</span></span>

<span data-ttu-id="8fe28-200">Когда автозапуск представлен со смешанным носителем содержимого, он требует ввода данных пользователем, прежде чем он сможет принять меры.</span><span class="sxs-lookup"><span data-stu-id="8fe28-200">When AutoPlay is presented with a mixed content medium, it requires user input before it can take action.</span></span> <span data-ttu-id="8fe28-201">В этом случае пользователю предоставляется диалоговое окно, содержащее отфильтрованный список всех соответствующих зарегистрированных приложений, доступных для типов содержимого, имеющихся на носителе.</span><span class="sxs-lookup"><span data-stu-id="8fe28-201">In this case, the user is presented with a dialog box containing a filtered list of all appropriate registered applications available for the content types present on the media.</span></span> <span data-ttu-id="8fe28-202">Пользователь может выбрать одно из этих приложений для автоматического запуска определенного типа содержимого, а остальные остаются нетронутыми.</span><span class="sxs-lookup"><span data-stu-id="8fe28-202">The user can choose one of these applications to AutoPlay that particular content type, while the rest remain untouched.</span></span> <span data-ttu-id="8fe28-203">Так как композиция смешанного содержимого мультимедиа зависит от каждого отдельного диска, нет возможности сохранить этот выбор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8fe28-203">As the composition of mixed content media varies with each individual disc, there is no option to save this choice as a default.</span></span>

<span data-ttu-id="8fe28-204">Примеры запросов пользователей см. в разделе [Автозапуск пользовательских интерфейсов](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="8fe28-204">For examples of user prompts, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="autoplay-user-interfaces"></a><span data-ttu-id="8fe28-205">Пользовательские интерфейсы автозапуска</span><span class="sxs-lookup"><span data-stu-id="8fe28-205">AutoPlay User Interfaces</span></span>

<span data-ttu-id="8fe28-206">Существует три возможных пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8fe28-206">There are three possible user interfaces.</span></span>

-   <span data-ttu-id="8fe28-207">Диалоговое окно, предлагающее пользователю ввести действие для одного типа содержимого</span><span class="sxs-lookup"><span data-stu-id="8fe28-207">A dialog box that prompts the user to enter an action for a single content type</span></span>
-   <span data-ttu-id="8fe28-208">Диалоговое окно, предлагающее пользователю ввести действие для смешанных типов содержимого</span><span class="sxs-lookup"><span data-stu-id="8fe28-208">A dialog box that prompts the user to enter an action for mixed content types</span></span>
-   <span data-ttu-id="8fe28-209">Страница свойств</span><span class="sxs-lookup"><span data-stu-id="8fe28-209">A property page</span></span>

### <a name="single-content-type-dialog-box"></a><span data-ttu-id="8fe28-210">Диалоговое окно «один тип содержимого»</span><span class="sxs-lookup"><span data-stu-id="8fe28-210">Single Content Type Dialog Box</span></span>

<span data-ttu-id="8fe28-211">Диалоговое окно, аналогичное приведенному ниже, отображается, если системе не предоставлены какие-либо Поддерживаемые носители.</span><span class="sxs-lookup"><span data-stu-id="8fe28-211">A dialog box similar to the following is displayed when any supported media not yet assigned a default AutoPlay action is presented to the system.</span></span>

![снимок экрана — диалоговое окно "тип отдельного содержимого"](images/pix.png)

<span data-ttu-id="8fe28-213">Пользователи могут выполнить одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="8fe28-213">Users can do one of the following.</span></span>

-   <span data-ttu-id="8fe28-214">Выберите действие из списка зарегистрированных приложений.</span><span class="sxs-lookup"><span data-stu-id="8fe28-214">Choose an action from the list of registered applications.</span></span>
-   <span data-ttu-id="8fe28-215">Вывод списка файлов на носителе в обычном представлении папки.</span><span class="sxs-lookup"><span data-stu-id="8fe28-215">List the files on the medium in a normal folder view.</span></span>
-   <span data-ttu-id="8fe28-216">Не предпринимать никаких действий.</span><span class="sxs-lookup"><span data-stu-id="8fe28-216">Take no action.</span></span>

<span data-ttu-id="8fe28-217">Пользователь также может сохранить выбор в качестве действия по умолчанию для этого среднего, установив флажок **всегда выполнять выбранное действие** .</span><span class="sxs-lookup"><span data-stu-id="8fe28-217">A user can also save a choice as the default action for this medium by clicking the **Always do the selected action** box.</span></span> <span data-ttu-id="8fe28-218">После этого диалоговое окно снова не отображается.</span><span class="sxs-lookup"><span data-stu-id="8fe28-218">Once this choice is made, the dialog is not shown again.</span></span> <span data-ttu-id="8fe28-219">Однако в Windows XP с пакетом обновления 1 (SP1), если на компьютер добавляется новое приложение, способное работать с определенным типом носителя, диалоговое окно снова отображается пользователю, давая ему возможность выбрать новое приложение в качестве действия автозапуска по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8fe28-219">However, in Windows XP Service Pack 1 (SP1), if a new application that can handle a particular media type is added to the computer, the dialog is once again presented to the user, giving them the opportunity to select the new application as the default AutoPlay action.</span></span> <span data-ttu-id="8fe28-220">Приложения также могут устанавливаться по умолчанию при их установке.</span><span class="sxs-lookup"><span data-stu-id="8fe28-220">Applications can also set themselves as the default selection when they are installed.</span></span>

<span data-ttu-id="8fe28-221">В Windows XP с пакетом обновления 1 (SP1) также добавляется функция, сохраняющая пользовательское действие автозапуска, если не щелкнуть поле **всегда выполнять выбранное действие** .</span><span class="sxs-lookup"><span data-stu-id="8fe28-221">Windows XP SP1 also adds a feature that retains the user's choice of AutoPlay action if they do not click the **Always do the selected action** box.</span></span> <span data-ttu-id="8fe28-222">Если пользователь выбирает действие автозапуска для одного экземпляра, при следующем отображении этого диалогового окна для этого типа носителя это действие будет выбрано по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8fe28-222">If a user chooses an AutoPlay action for a single instance, the next time that dialog is presented for that media type, the same action is the default selection.</span></span>

<span data-ttu-id="8fe28-223">Чтобы приложение включалось в список возможных действий, оно должно быть зарегистрировано с помощью автозапуска.</span><span class="sxs-lookup"><span data-stu-id="8fe28-223">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="8fe28-224">Дополнительные сведения см. в разделе [Подготовка оборудования и программного обеспечения для использования при автозапуске](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="8fe28-224">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="mixed-media-dialog-box"></a><span data-ttu-id="8fe28-225">Диалоговое окно "смешанный носитель"</span><span class="sxs-lookup"><span data-stu-id="8fe28-225">Mixed Media Dialog Box</span></span>

<span data-ttu-id="8fe28-226">Если в системе представлен любой носитель, содержащий сочетание поддерживаемых типов файлов, отображается следующее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8fe28-226">The following dialog box is displayed when any medium containing a mix of supported file types is presented to the system.</span></span> <span data-ttu-id="8fe28-227">По сути, это то же самое, что и диалоговое окно одно содержимое, но с двумя значительными различиями.</span><span class="sxs-lookup"><span data-stu-id="8fe28-227">This is essentially the same as the single content medium dialog box but with two significant differences.</span></span> <span data-ttu-id="8fe28-228">Во-первых, доступные параметры действия состоят из отфильтрованного списка приложений, соответствующих всем типам содержимого, присутствующим на носителе.</span><span class="sxs-lookup"><span data-stu-id="8fe28-228">First, the available action options consist of a filtered list of applications relevant to all content types present on the medium.</span></span> <span data-ttu-id="8fe28-229">Во-вторых, нет возможности выбрать постоянное действие по умолчанию, так как типы содержимого и процентные доли носителя со смешанным содержимым слишком непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="8fe28-229">Second, there is no option to choose a permanent default action because the content types and percentages of mixed content media are too unpredictable.</span></span>

![снимок экрана — диалоговое окно "смешанный носитель"](images/mix.png)

<span data-ttu-id="8fe28-231">Чтобы приложение включалось в список возможных действий, оно должно быть зарегистрировано с помощью автозапуска.</span><span class="sxs-lookup"><span data-stu-id="8fe28-231">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="8fe28-232">Дополнительные сведения см. в разделе [Подготовка оборудования и программного обеспечения для использования при автозапуске](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="8fe28-232">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="property-page"></a><span data-ttu-id="8fe28-233">Страница свойств</span><span class="sxs-lookup"><span data-stu-id="8fe28-233">Property Page</span></span>

<span data-ttu-id="8fe28-234">Ниже приведен пример страницы свойств автозапуска для устройства DVD/CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="8fe28-234">The following is a sample AutoPlay property page for a DVD/CD-ROM device.</span></span>

![снимок экрана со страницей свойств](images/apdlg.png)

<span data-ttu-id="8fe28-236">Каждый тип устройства предлагает соответствующее подмножество типов содержимого для настройки автозапуска.</span><span class="sxs-lookup"><span data-stu-id="8fe28-236">Each device type offers an appropriate subset of content types for AutoPlay configuration.</span></span> <span data-ttu-id="8fe28-237">В свою очередь, каждый тип содержимого, если он выбран, предлагает соответствующий список параметров действий в списке.</span><span class="sxs-lookup"><span data-stu-id="8fe28-237">In turn, each content type, when selected, offers an appropriate list of action options in the list box.</span></span> <span data-ttu-id="8fe28-238">Для каждого типа содержимого можно выбрать другое действие.</span><span class="sxs-lookup"><span data-stu-id="8fe28-238">A different action can be chosen for each content type.</span></span>

 

 



