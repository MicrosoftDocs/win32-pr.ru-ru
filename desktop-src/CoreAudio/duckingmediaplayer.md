---
description: В этом примере приложения демонстрируется потоковая затухание путем реализации проигрывателя мультимедиа, который показывает поведение по умолчанию, предоставляемое системой, выводит события дуккинг и реализует настраиваемую обработку при получении событий дуккинг.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: дуккингмедиаплайер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105656727"
---
# <a name="duckingmediaplayer"></a><span data-ttu-id="867a3-103">дуккингмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="867a3-103">DuckingMediaPlayer</span></span>

<span data-ttu-id="867a3-104">В этом примере приложения демонстрируется потоковая затухание путем реализации проигрывателя мультимедиа, который показывает поведение по умолчанию, предоставляемое системой, выводит события дуккинг и реализует настраиваемую обработку при получении событий дуккинг.</span><span class="sxs-lookup"><span data-stu-id="867a3-104">This sample application demonstrates stream attenuation by implementing a media player that shows the default attenuation behavior provided by the system, opts out of ducking events, and implements custom handling when ducking events are received.</span></span> <span data-ttu-id="867a3-105">Этот пример необходимо использовать в сочетании с [дуккингкаптуресампле](duckingcapturesample.md).</span><span class="sxs-lookup"><span data-stu-id="867a3-105">This sample must be used in conjuction with [DuckingCaptureSample](duckingcapturesample.md).</span></span> <span data-ttu-id="867a3-106">Дополнительные сведения о дуккинг или ослаблении потока см. в разделе [Дуккинг по умолчанию](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="867a3-106">For more information about ducking or stream attenuation, see [Default Ducking Experience](stream-attenuation.md).</span></span>

<span data-ttu-id="867a3-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="867a3-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="867a3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="867a3-108">Description</span></span>](#description)
-   [<span data-ttu-id="867a3-109">Требования</span><span class="sxs-lookup"><span data-stu-id="867a3-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="867a3-110">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="867a3-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="867a3-111">Создание примера</span><span class="sxs-lookup"><span data-stu-id="867a3-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="867a3-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="867a3-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="867a3-113">См. также</span><span class="sxs-lookup"><span data-stu-id="867a3-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="867a3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="867a3-114">Description</span></span>

<span data-ttu-id="867a3-115">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="867a3-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="867a3-116">DirectShow для воспроизведения файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="867a3-116">DirectShow to play a media file.</span></span>
-   <span data-ttu-id="867a3-117">[Васапи](wasapi.md) для управления потоками и обработки событий дуккинг.</span><span class="sxs-lookup"><span data-stu-id="867a3-117">[WASAPI](wasapi.md) for stream management and handling ducking events.</span></span>

## <a name="requirements"></a><span data-ttu-id="867a3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="867a3-118">Requirements</span></span>



| <span data-ttu-id="867a3-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="867a3-119">Product</span></span>                                                        | <span data-ttu-id="867a3-120">Version</span><span class="sxs-lookup"><span data-stu-id="867a3-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="867a3-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="867a3-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="867a3-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="867a3-122">Windows 7</span></span> |
| <span data-ttu-id="867a3-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="867a3-123">Visual Studio</span></span>                                                  | <span data-ttu-id="867a3-124">2008</span><span class="sxs-lookup"><span data-stu-id="867a3-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="867a3-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="867a3-125">Downloading the Sample</span></span>

<span data-ttu-id="867a3-126">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="867a3-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="867a3-127">Расположение</span><span class="sxs-lookup"><span data-stu-id="867a3-127">Location</span></span>    | <span data-ttu-id="867a3-128">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="867a3-128">Path/URL</span></span>                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="867a3-129">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="867a3-129">Windows SDK</span></span> | <span data-ttu-id="867a3-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ дуккингмедиаплайер \\ ...</span><span class="sxs-lookup"><span data-stu-id="867a3-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingMediaPlayer\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="867a3-131">Построение образца</span><span class="sxs-lookup"><span data-stu-id="867a3-131">Building the Sample</span></span>

<span data-ttu-id="867a3-132">Чтобы создать пример Дуккингмедиаплайер, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="867a3-132">To build the DuckingMediaPlayer sample, use the following steps:</span></span>

1.  <span data-ttu-id="867a3-133">Откройте Дуккингмедиаплайер. sln в Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="867a3-133">Open the DuckingMediaPlayer.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="867a3-134">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="867a3-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="867a3-135">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="867a3-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="867a3-136">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Дуккингмедиаплайер. vcproj.</span><span class="sxs-lookup"><span data-stu-id="867a3-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingMediaPlayer.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="867a3-137">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="867a3-137">Running the Sample</span></span>

<span data-ttu-id="867a3-138">Если приложение успешно построено, создается исполняемый файл DuckingMediaPlayer.exe.</span><span class="sxs-lookup"><span data-stu-id="867a3-138">If you build the application successfully, an executable file, DuckingMediaPlayer.exe, is generated.</span></span> <span data-ttu-id="867a3-139">Чтобы запустить его, выберите команду **начать отладку** или **запустить без отладки** из меню **Отладка** или введите `DuckingMediaPlayer` в командном окне.</span><span class="sxs-lookup"><span data-stu-id="867a3-139">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingMediaPlayer` in a command window.</span></span>

<span data-ttu-id="867a3-140">Чтобы просмотреть демонстрацию дуккинг, необходимо одновременно выполнить Дуккингмедиаплайер и Дуккингкаптуресампле.</span><span class="sxs-lookup"><span data-stu-id="867a3-140">To view a demonstration of ducking, you must execute DuckingMediaPlayer and DuckingCaptureSample simultaneously.</span></span> <span data-ttu-id="867a3-141">Дуккингкаптуресампле открывает поток связи и сигнализирует системе создать событие дуккинг.</span><span class="sxs-lookup"><span data-stu-id="867a3-141">DuckingCaptureSample opens a communication stream and signals the system to generate a ducking event.</span></span> <span data-ttu-id="867a3-142">Дуккингмедиаплайер уведомляется от системы при возникновении события дуккинг, и проигрыватель мультимедиа выполняет запрошенное пользователем действие.</span><span class="sxs-lookup"><span data-stu-id="867a3-142">The DuckingMediaPlayer is notified by the system when a ducking event occurs, and the media player performs the action requested by the user.</span></span>

<span data-ttu-id="867a3-143">Чтобы отключить поведение дуккинг, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="867a3-143">To disable ducking behavior:</span></span>

1.  <span data-ttu-id="867a3-144">В окне Дуккингкаптуресампле выберите **использовать устройство ввода по умолчанию** и нажмите кнопку **запустить** , чтобы запустить сеанс записи с коммуникационного устройства.</span><span class="sxs-lookup"><span data-stu-id="867a3-144">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="867a3-145">На Дуккингмедиаплайер выберите файл мультимедиа для воспроизведения и укажите параметр дуккинг в качестве **отказаться от дуккинг**.</span><span class="sxs-lookup"><span data-stu-id="867a3-145">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Opt out of Ducking**.</span></span>

<span data-ttu-id="867a3-146">Обратите внимание, что файл мультимедиа воспроизводится без прерывания.</span><span class="sxs-lookup"><span data-stu-id="867a3-146">Notice that the media file is played without any interruption.</span></span> <span data-ttu-id="867a3-147">События, создаваемые системой при открытии коммуникационного потока, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="867a3-147">The events generated by the system when the communication stream opened are ignored.</span></span>

<span data-ttu-id="867a3-148">Чтобы продемонстрировать поведение дуккинг по умолчанию, предоставляемое системой, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="867a3-148">To demonstrate the default ducking behavior provided by the system, do the following:</span></span>

1.  <span data-ttu-id="867a3-149">Выберите параметр **звуки** на панели управления.</span><span class="sxs-lookup"><span data-stu-id="867a3-149">Select the **Sounds** option from the control panel.</span></span> <span data-ttu-id="867a3-150">На вкладке **связи** установите флажок **уменьшить громкость других звуков на 80%**.</span><span class="sxs-lookup"><span data-stu-id="867a3-150">On the **Communications** tab, select **Reduce the volume of other sounds by 80%**.</span></span>
2.  <span data-ttu-id="867a3-151">В окне Дуккингкаптуресампле выберите **использовать устройство ввода по умолчанию** и нажмите кнопку **запустить** , чтобы запустить сеанс записи с коммуникационного устройства.</span><span class="sxs-lookup"><span data-stu-id="867a3-151">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
3.  <span data-ttu-id="867a3-152">На Дуккингмедиаплайер выберите файл мультимедиа для воспроизведения без выбора параметров дуккинг.</span><span class="sxs-lookup"><span data-stu-id="867a3-152">On the DuckingMediaPlayer, select a media file to play, without choosing any of the ducking options.</span></span>
4.  <span data-ttu-id="867a3-153">В окне Дуккингкаптуресампле нажмите кнопку " **прерывать** ", чтобы прерывать поток связи.</span><span class="sxs-lookup"><span data-stu-id="867a3-153">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="867a3-154">Обратите внимание, что когда Дуккингкаптуресампле открывает поток связи, файл мультимедиа, воспроизводимый Дуккингмедиаплайер, воспроизводится без прерывания, но уровень громкости уменьшается.</span><span class="sxs-lookup"><span data-stu-id="867a3-154">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer plays without interruption, but the volume level is lowered.</span></span> <span data-ttu-id="867a3-155">Когда сеанс связи остановлен, том сбрасывается до исходного.</span><span class="sxs-lookup"><span data-stu-id="867a3-155">When the communication session is stopped, the volume is reset to the original setting.</span></span> <span data-ttu-id="867a3-156">Это поведение дуккинг по умолчанию, реализуемое системой.</span><span class="sxs-lookup"><span data-stu-id="867a3-156">This stream attenuation behavior is the default ducking behavior implemented by the system.</span></span>

<span data-ttu-id="867a3-157">Чтобы просмотреть настроенное поведение дуккинг, реализованное проигрывателем мультимедиа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="867a3-157">To view a customized ducking behavior implemented by the media player:</span></span>

1.  <span data-ttu-id="867a3-158">В окне Дуккингкаптуресампле выберите **использовать устройство ввода по умолчанию** и нажмите кнопку **запустить** , чтобы запустить сеанс записи с коммуникационного устройства.</span><span class="sxs-lookup"><span data-stu-id="867a3-158">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="867a3-159">На Дуккингмедиаплайер выберите файл мультимедиа для воспроизведения и укажите параметр дуккинг в качестве **паузы в утка**.</span><span class="sxs-lookup"><span data-stu-id="867a3-159">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Pause on Duck**.</span></span>
3.  <span data-ttu-id="867a3-160">В окне Дуккингкаптуресампле нажмите кнопку " **прерывать** ", чтобы прерывать поток связи.</span><span class="sxs-lookup"><span data-stu-id="867a3-160">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="867a3-161">Обратите внимание, что когда Дуккингкаптуресампле открывает поток связи, файл мультимедиа, воспроизводимый Дуккингмедиаплайер, приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="867a3-161">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer is paused.</span></span> <span data-ttu-id="867a3-162">Воспроизведение возобновляется после остановки сеанса связи.</span><span class="sxs-lookup"><span data-stu-id="867a3-162">The playback resumes when the communication session is stopped.</span></span> <span data-ttu-id="867a3-163">Это поведение при ослаблении в потоке — это поведение дуккинг, реализованное проигрывателем мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="867a3-163">This stream attenuation behavior is the ducking behavior implemented by the media player.</span></span>

<span data-ttu-id="867a3-164">Дуккингмедиаплайер также демонстрирует, как интегрировать регулятор громкости для каждого приложения с помощью микшера тома.</span><span class="sxs-lookup"><span data-stu-id="867a3-164">DuckingMediaPlayer also demonstrates how to integrate volume control for each application with the volume mixer.</span></span>

<span data-ttu-id="867a3-165">Дополнительные сведения о функции затухания потока см. в разделе [Дуккинг по умолчанию](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="867a3-165">For more information about the stream attenuation feature, see [Default Ducking Experience](stream-attenuation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="867a3-166">См. также</span><span class="sxs-lookup"><span data-stu-id="867a3-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="867a3-167">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="867a3-167">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



