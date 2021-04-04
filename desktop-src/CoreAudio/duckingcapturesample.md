---
description: Этот пример приложения демонстрирует открытие и закрытие потоков связи и вызов событий дуккинг, которые приложение может получить для реализации затухания потока.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: дуккингкаптуресампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896458"
---
# <a name="duckingcapturesample"></a><span data-ttu-id="18d15-103">дуккингкаптуресампле</span><span class="sxs-lookup"><span data-stu-id="18d15-103">DuckingCaptureSample</span></span>

<span data-ttu-id="18d15-104">Этот пример приложения демонстрирует открытие и закрытие потоков связи и вызов событий дуккинг, которые приложение может получить для реализации затухания потока.</span><span class="sxs-lookup"><span data-stu-id="18d15-104">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="18d15-105">Это приложение реализует чат-клиент, который использует основные API-интерфейсы для чтения звуковых данных с коммуникационного устройства и воспроизведения на выходном устройстве.</span><span class="sxs-lookup"><span data-stu-id="18d15-105">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span>

<span data-ttu-id="18d15-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="18d15-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="18d15-107">Описание</span><span class="sxs-lookup"><span data-stu-id="18d15-107">Description</span></span>](#description)
-   [<span data-ttu-id="18d15-108">Требования</span><span class="sxs-lookup"><span data-stu-id="18d15-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="18d15-109">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="18d15-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="18d15-110">Создание примера</span><span class="sxs-lookup"><span data-stu-id="18d15-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="18d15-111">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="18d15-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="18d15-112">См. также</span><span class="sxs-lookup"><span data-stu-id="18d15-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="18d15-113">Описание</span><span class="sxs-lookup"><span data-stu-id="18d15-113">Description</span></span>

<span data-ttu-id="18d15-114">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="18d15-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="18d15-115">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="18d15-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="18d15-116">[Васапи](wasapi.md) для доступа к устройству записи и отрисовки данных, операциям управления потоком и обработке событий дуккинг.</span><span class="sxs-lookup"><span data-stu-id="18d15-116">[WASAPI](wasapi.md) for accessing the communications capture and render device, stream management operations, and handling ducking events.</span></span>
-   <span data-ttu-id="18d15-117">[API-интерфейсы Wave](/previous-versions//ms713499(v=vs.85)) для доступа к коммуникационному устройству и записи звукового ввода.</span><span class="sxs-lookup"><span data-stu-id="18d15-117">[WAVE APIs](/previous-versions//ms713499(v=vs.85)) for accessing the communications device and capturing audio input.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d15-118">Требования</span><span class="sxs-lookup"><span data-stu-id="18d15-118">Requirements</span></span>



| <span data-ttu-id="18d15-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="18d15-119">Product</span></span>                                                        | <span data-ttu-id="18d15-120">Version</span><span class="sxs-lookup"><span data-stu-id="18d15-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="18d15-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="18d15-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="18d15-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="18d15-122">Windows 7</span></span> |
| <span data-ttu-id="18d15-123">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="18d15-123">Visual Studio 2008</span></span>                                             |           |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="18d15-124">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="18d15-124">Downloading the Sample</span></span>

<span data-ttu-id="18d15-125">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="18d15-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="18d15-126">Расположение</span><span class="sxs-lookup"><span data-stu-id="18d15-126">Location</span></span>    | <span data-ttu-id="18d15-127">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="18d15-127">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d15-128">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="18d15-128">Windows SDK</span></span> | <span data-ttu-id="18d15-129">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ дуккингкаптуресампле \\ ...</span><span class="sxs-lookup"><span data-stu-id="18d15-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingCaptureSample\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="18d15-130">Построение образца</span><span class="sxs-lookup"><span data-stu-id="18d15-130">Building the Sample</span></span>

<span data-ttu-id="18d15-131">Чтобы создать пример Дуккингкаптуресампле, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="18d15-131">To build the DuckingCaptureSample sample, use the following steps:</span></span>

1.  <span data-ttu-id="18d15-132">Откройте Дуккингкаптуресампле. sln в Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="18d15-132">Open the DuckingCaptureSample.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="18d15-133">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="18d15-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="18d15-134">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="18d15-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="18d15-135">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Дуккингкаптуресампле. vcproj.</span><span class="sxs-lookup"><span data-stu-id="18d15-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingCaptureSample.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="18d15-136">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="18d15-136">Running the Sample</span></span>

<span data-ttu-id="18d15-137">Если приложение успешно построено, создается исполняемый файл DuckingCaptureSample.exe.</span><span class="sxs-lookup"><span data-stu-id="18d15-137">If you build the application successfully, an executable file, DuckingCaptureSample.exe, is generated.</span></span> <span data-ttu-id="18d15-138">Чтобы запустить его, выберите команду **начать отладку** или **запустить без отладки** из меню **Отладка** или введите `DuckingCaptureSample` в командном окне.</span><span class="sxs-lookup"><span data-stu-id="18d15-138">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingCaptureSample` in a command window.</span></span>

<span data-ttu-id="18d15-139">Дуккингкаптуресампле предоставляет пользователю две реализации для записи звука из консольного устройства по умолчанию: ВАСАПИ и Wave API.</span><span class="sxs-lookup"><span data-stu-id="18d15-139">DuckingCaptureSample provides the user with two implementations to capture audio from the default console device: WASAPI and Wave APIs.</span></span> <span data-ttu-id="18d15-140">Чтобы запустить сеанс записи, выберите режим и нажмите кнопку **запустить** в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="18d15-140">To start a capture session, select a mode and click **Start** on the application's user interface.</span></span> <span data-ttu-id="18d15-141">Чтобы завершить сеанс, нажмите кнопку " **прекратить**".</span><span class="sxs-lookup"><span data-stu-id="18d15-141">To end the session, click **Stop**.</span></span> <span data-ttu-id="18d15-142">В зависимости от устройства, указанного пользователем (входные или выходные данные), приложение использует API Ммдевице для получения ссылки на устройство для передачи данных по умолчанию или для записи.</span><span class="sxs-lookup"><span data-stu-id="18d15-142">Depending on the device specified by the user (input or output), the application uses MMDevice API to get a reference to the default rendering or capture communication device.</span></span> <span data-ttu-id="18d15-143">После того как пользователь запустит сеанс разговора, приложение выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="18d15-143">After the user starts a chat session, the application performs the following tasks:</span></span>

-   <span data-ttu-id="18d15-144">Создает и инициализирует аудио клиент в режиме, управляемом событиями.</span><span class="sxs-lookup"><span data-stu-id="18d15-144">Creates and initializes an audio client in event-driven mode.</span></span>
-   <span data-ttu-id="18d15-145">Связывает клиент с обработчиком событий, который сигнализирует, что образцы готовы для записи или подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="18d15-145">Associates the client with the event handle that signals that samples are ready for capture or rendering.</span></span>
-   <span data-ttu-id="18d15-146">Настраивает Клиент отслеживания и клиент отрисовки для транспорта.</span><span class="sxs-lookup"><span data-stu-id="18d15-146">Sets up a capture client and a rendering client for the transport.</span></span>
-   <span data-ttu-id="18d15-147">Создает поток разговора и запускает обработчик аудио.</span><span class="sxs-lookup"><span data-stu-id="18d15-147">Creates the chat thread and starts the audio engine.</span></span>

<span data-ttu-id="18d15-148">Для записи звуковых данных с каждым проходом обработки в примере используется клиент отслеживания для получения общего объема захваченных данных, доступных в буфере, считывания данных из устройства ввода по умолчанию и освобождения пакета и предоставления буфера для чтения следующего набора захваченных данных.</span><span class="sxs-lookup"><span data-stu-id="18d15-148">For capturing audio data, with each processing pass, the sample uses the capture client to get the total amount of captured data that is available in the buffer, read data from the default input device, and release the packet and make the buffer available for reading the next set of captured data.</span></span>

<span data-ttu-id="18d15-149">Для подготовки к просмотру приложение определяет объем данных, которые помещаются в очередь для воспроизведения в буфере конечной точки записи.</span><span class="sxs-lookup"><span data-stu-id="18d15-149">For rendering, the application determines the amount of data that is queued up to play in the capture endpoint buffer.</span></span> <span data-ttu-id="18d15-150">Он соответствующим образом записывает данные в буфер и освобождает буфер в процессе подготовки к следующей обработке до тех пор, пока не будут записаны все сведения.</span><span class="sxs-lookup"><span data-stu-id="18d15-150">It accordingly writes to the buffer and releases the buffer in preparation for the next processing pass until all of the data has been written.</span></span> <span data-ttu-id="18d15-151">Для подготовки к просмотру невыполненные кадры преобразуются в предустановки, чтобы предотвратить сбой обработчика звука при запуске.</span><span class="sxs-lookup"><span data-stu-id="18d15-151">For rendering, silent frames are prerolled to prevent the audio engine from glitching on startup.</span></span> <span data-ttu-id="18d15-152">Дуккингкаптуресампле также показывает, как скрыть поток отрисовки из микшера тома.</span><span class="sxs-lookup"><span data-stu-id="18d15-152">DuckingCaptureSample also shows how to hide the render stream from the volume mixer.</span></span>

<span data-ttu-id="18d15-153">Дополнительные сведения о функции затухания потока см. в разделе [Использование коммуникационного устройства](using-the-communication-device.md).</span><span class="sxs-lookup"><span data-stu-id="18d15-153">For more information about the stream attenuation feature, see [Using a Communication Device](using-the-communication-device.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="18d15-154">См. также</span><span class="sxs-lookup"><span data-stu-id="18d15-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18d15-155">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="18d15-155">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
