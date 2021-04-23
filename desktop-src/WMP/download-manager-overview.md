---
title: Обзор диспетчера загрузки
description: Обзор диспетчера загрузки
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Интернет-магазины проигрывателя Windows Media, Загрузка в режиме реального времени
- Интернет-магазины, Загрузка в режиме реального времени
- Тип 2 Интернет-магазинов, Загрузка в режиме реального времени
- Интернет-магазины проигрывателя Windows Media, Фоновая загрузка
- Интернет-магазины, Фоновая загрузка
- Тип 2 Интернет-магазинов, Фоновая загрузка
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
- Загрузка в режиме реального времени
- Фоновая загрузка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068519"
---
# <a name="download-manager-overview"></a><span data-ttu-id="b1bad-117">Обзор диспетчера загрузки</span><span class="sxs-lookup"><span data-stu-id="b1bad-117">Download Manager Overview</span></span>

<span data-ttu-id="b1bad-118">Проигрыватель Microsoft Windows Media предоставляет панели задач Интернет-магазина, содержащие размещенное окно браузера.</span><span class="sxs-lookup"><span data-stu-id="b1bad-118">Microsoft Windows Media Player provides online store task panes that contain a hosted browser window.</span></span> <span data-ttu-id="b1bad-119">С помощью Интернет-магазинов пользователи могут взаимодействовать с веб-страницами интерактивного магазина через Интернет.</span><span class="sxs-lookup"><span data-stu-id="b1bad-119">Through the online stores, users can interact with online store webpages across the Internet.</span></span>

<span data-ttu-id="b1bad-120">Диспетчер загрузки проигрывателя Windows Media предоставляет объектную модель, которую можно использовать для решения задач, связанных с загрузкой содержимого на компьютер пользователя из Microsoft службы IIS (IIS) по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="b1bad-120">The Windows Media Player Download Manager provides an object model that you can use to handle the tasks associated with downloading content to the user's computer from Microsoft Internet Information Services (IIS) using Hypertext Transfer Protocol (HTTP).</span></span> <span data-ttu-id="b1bad-121">С помощью диспетчера загрузки можно:</span><span class="sxs-lookup"><span data-stu-id="b1bad-121">With the Download Manager, you can:</span></span>

-   <span data-ttu-id="b1bad-122">Управлять несколькими загрузками одновременно в виде коллекции.</span><span class="sxs-lookup"><span data-stu-id="b1bad-122">Manage multiple downloads simultaneously as a collection.</span></span>
-   <span data-ttu-id="b1bad-123">Укажите URL-адрес для файла и запустите загрузку с помощью HTTP.</span><span class="sxs-lookup"><span data-stu-id="b1bad-123">Specify a URL for a file and start it downloading using HTTP.</span></span>
-   <span data-ttu-id="b1bad-124">Запросите состояние загрузки и ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1bad-124">Query for the download state and progress.</span></span>
-   <span data-ttu-id="b1bad-125">Приостановка, возобновление или Отмена скачивания.</span><span class="sxs-lookup"><span data-stu-id="b1bad-125">Pause, resume, or cancel a download.</span></span>
-   <span data-ttu-id="b1bad-126">Укажите, выполняется ли загрузка в фоновом режиме или в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="b1bad-126">Specify whether a download occurs in the background or in real time.</span></span> <span data-ttu-id="b1bad-127">(Фоновая загрузка доступна только в операционной системе Microsoft Windows XP.) См. [сведения о загрузке в фоновом режиме и в режиме реального времени](#about-background-and-real-time-downloading).</span><span class="sxs-lookup"><span data-stu-id="b1bad-127">(Background downloading is only available on the Microsoft Windows XP operating system.) See [About Background and Real-time Downloading](#about-background-and-real-time-downloading).</span></span>
-   <span data-ttu-id="b1bad-128">Укажите, как содержимое отображается в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b1bad-128">Specify how content is displayed in the library.</span></span> <span data-ttu-id="b1bad-129">См. раздел [об интеграции библиотек](#about-library-integration).</span><span class="sxs-lookup"><span data-stu-id="b1bad-129">See [About Library Integration](#about-library-integration).</span></span>

<span data-ttu-id="b1bad-130">Диспетчер загрузки — это решение для загрузки содержимого из кода сценария на размещенных веб-страницах.</span><span class="sxs-lookup"><span data-stu-id="b1bad-130">The Download Manager is the solution for downloading content from script code in hosted webpages.</span></span> <span data-ttu-id="b1bad-131">Чтобы загрузить содержимое с помощью кода C++, используйте фоновая интеллектуальная служба передачи Windows XP (BITS).</span><span class="sxs-lookup"><span data-stu-id="b1bad-131">To download content using C++ code, use the Windows XP Background Intelligent Transfer Service (BITS).</span></span> <span data-ttu-id="b1bad-132">Дополнительные сведения см. в разделе [службы BITS](bits.md).</span><span class="sxs-lookup"><span data-stu-id="b1bad-132">For more information, see [BITS](bits.md).</span></span>

## <a name="about-background-and-real-time-downloading"></a><span data-ttu-id="b1bad-133">Сведения о загрузке в фоновом режиме и в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="b1bad-133">About Background and Real-time Downloading</span></span>

<span data-ttu-id="b1bad-134">Диспетчер загрузки предлагает два типа загрузки: фоновый и режим реального времени.</span><span class="sxs-lookup"><span data-stu-id="b1bad-134">The Download Manager offers two types of downloading: background and real-time.</span></span> <span data-ttu-id="b1bad-135">Какой тип вы используете, вы можете разрешить пользователю выбрать тип загрузки также и.</span><span class="sxs-lookup"><span data-stu-id="b1bad-135">Which type you use is up to you, and it is possible to allow the user to select the download type as well.</span></span> <span data-ttu-id="b1bad-136">Если вы решили разрешить пользователю выбирать тип загрузки, объясните различия между двумя доступными типами.</span><span class="sxs-lookup"><span data-stu-id="b1bad-136">If you choose to allow the user to select the download type, be sure to explain the differences between the two available types.</span></span>

<span data-ttu-id="b1bad-137">Загрузка в режиме реального времени выполняется всего один раз.</span><span class="sxs-lookup"><span data-stu-id="b1bad-137">Real-time downloading occurs all at once.</span></span> <span data-ttu-id="b1bad-138">Когда пользователь запускает загрузку файла, весь файл передается на компьютер пользователя в одном непрерывном потоке.</span><span class="sxs-lookup"><span data-stu-id="b1bad-138">When the user starts a file download, the entire file is transferred to the user's computer in a single, continuous stream.</span></span> <span data-ttu-id="b1bad-139">Пользователь не может приостановить или иным образом прервать загрузку.</span><span class="sxs-lookup"><span data-stu-id="b1bad-139">The user cannot pause or otherwise interrupt the download.</span></span> <span data-ttu-id="b1bad-140">Если пользователь решит закрыть проигрыватель Windows Media до завершения скачивания, он теряет все незавершенные файлы и сначала загружает их с начала для получения содержимого.</span><span class="sxs-lookup"><span data-stu-id="b1bad-140">If the user chooses to close Windows Media Player before the download is finished, he or she loses any incomplete files and must download them from the beginning to acquire the content.</span></span>

<span data-ttu-id="b1bad-141">Основным преимуществом загрузки в режиме реального времени является то, что он позволяет пользователю получать содержимое быстрее, чем при фоновом скачивании.</span><span class="sxs-lookup"><span data-stu-id="b1bad-141">The main advantage of real-time downloading is that it allows the user to acquire the content faster than background downloading.</span></span> <span data-ttu-id="b1bad-142">Загрузка в режиме реального времени доступна пользователям Windows XP, но это единственный тип загрузки, доступный в версиях операционной системы Windows до Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1bad-142">Real-time downloading is available to users of Windows XP, but it is the only type of downloading available on versions of the Windows operating system prior to Windows XP.</span></span>

<span data-ttu-id="b1bad-143">Фоновая загрузка происходит поэтапным образом.</span><span class="sxs-lookup"><span data-stu-id="b1bad-143">Background downloading happens in a piecemeal fashion.</span></span> <span data-ttu-id="b1bad-144">Когда пользователь запускает фоновую загрузку, части файла передаются на компьютер пользователя при доступности процессора.</span><span class="sxs-lookup"><span data-stu-id="b1bad-144">When the user starts a background download, parts of the file are transferred to the user's computer when processor time is available.</span></span> <span data-ttu-id="b1bad-145">Можно приостановить и возобновить фоновую загрузку.</span><span class="sxs-lookup"><span data-stu-id="b1bad-145">It is possible to pause and resume a background download.</span></span> <span data-ttu-id="b1bad-146">Если пользователь откроет проигрыватель Windows Media перед завершением фоновой загрузки, то сохраняется состояние всех незавершенных файлов и загрузка может быть продолжена в фоновом режиме даже после перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="b1bad-146">If the user chooses to close Windows Media Player before background downloading is finished, the condition of any incomplete files is saved and the downloading can continue in the background, even after restarting the computer.</span></span>

<span data-ttu-id="b1bad-147">Загрузка в фоновом режиме может выполняться дольше, чем загрузка в режиме реального времени, так как процесс загрузки происходит только тогда, когда процессор не выполняет другие задачи.</span><span class="sxs-lookup"><span data-stu-id="b1bad-147">Background downloading can take longer than real-time downloading because the download process only happens when the processor is not performing other tasks.</span></span>

<span data-ttu-id="b1bad-148">Фоновая загрузка доступна только при использовании Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1bad-148">Background downloading is only available when using Windows XP.</span></span>

## <a name="about-library-integration"></a><span data-ttu-id="b1bad-149">Сведения об интеграции библиотеки</span><span class="sxs-lookup"><span data-stu-id="b1bad-149">About Library Integration</span></span>

<span data-ttu-id="b1bad-150">Проигрыватель Windows Media может автоматически упорядочивать содержимое Интернет-магазина в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="b1bad-150">Windows Media Player can automatically organize online store content in the library.</span></span> <span data-ttu-id="b1bad-151">Чтобы включить эту функцию, необходимо указать значение для атрибута **WM/контентдистрибутор** для каждого файла цифрового носителя.</span><span class="sxs-lookup"><span data-stu-id="b1bad-151">To enable this, you must specify a value for the **WM/ContentDistributor** attribute for each digital media file.</span></span> <span data-ttu-id="b1bad-152">При добавлении файла цифрового носителя в библиотеку, который происходит автоматически при использовании диспетчера загрузки, он автоматически отображается в узле **приобретенная музыка** или **Покупка видео** .</span><span class="sxs-lookup"><span data-stu-id="b1bad-152">When a digital media file is added to the library, which happens automatically when using the Download Manager, the file is listed in the **Purchased Music** or **Purchased Videos** node automatically.</span></span> <span data-ttu-id="b1bad-153">Например, если значение для **WM/контентдистрибутор** равно "Proseware", а файл цифрового мультимедиа содержит музыку, содержимое будет отображаться в библиотеке в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="b1bad-153">For example, if the value for **WM/ContentDistributor** is "Proseware" and the digital media file contains music, the content would appear in the library in the following location:</span></span>

<span data-ttu-id="b1bad-154">Музыка, приобретенная музыка или proseware</span><span class="sxs-lookup"><span data-stu-id="b1bad-154">All Music/Purchased Music/Proseware</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1bad-155">См. также</span><span class="sxs-lookup"><span data-stu-id="b1bad-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1bad-156">**Диспетчер загрузки**</span><span class="sxs-lookup"><span data-stu-id="b1bad-156">**Download Manager**</span></span>](download-manager.md)
</dt> <dt>

[<span data-ttu-id="b1bad-157">**Довнлоадколлектион. Стартдовнлоад**</span><span class="sxs-lookup"><span data-stu-id="b1bad-157">**DownloadCollection.startDownload**</span></span>](downloadcollection-startdownload.md)
</dt> </dl>

 

 




