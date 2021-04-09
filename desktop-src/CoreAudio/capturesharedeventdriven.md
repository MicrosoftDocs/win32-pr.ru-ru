---
description: Этот пример приложения использует основные API аудио для записи звуковых данных с устройства ввода, указанного пользователем, и записывает их в WAV-файл с уникальным именем в текущем каталоге. В этом примере демонстрируется буферизация, управляемая событиями.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: каптурешаредевентдривен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141635"
---
# <a name="capturesharedeventdriven"></a><span data-ttu-id="f3b9f-104">каптурешаредевентдривен</span><span class="sxs-lookup"><span data-stu-id="f3b9f-104">CaptureSharedEventDriven</span></span>

<span data-ttu-id="f3b9f-105">Этот пример приложения использует основные API аудио для записи звуковых данных с устройства ввода, указанного пользователем, и записывает их в WAV-файл с уникальным именем в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="f3b9f-106">В этом примере демонстрируется буферизация, управляемая событиями.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-106">This sample demonstrates event-driven buffering.</span></span>

<span data-ttu-id="f3b9f-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f3b9f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f3b9f-108">Description</span></span>](#description)
-   [<span data-ttu-id="f3b9f-109">Требования</span><span class="sxs-lookup"><span data-stu-id="f3b9f-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f3b9f-110">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="f3b9f-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f3b9f-111">Создание примера</span><span class="sxs-lookup"><span data-stu-id="f3b9f-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f3b9f-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="f3b9f-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f3b9f-113">См. также</span><span class="sxs-lookup"><span data-stu-id="f3b9f-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="f3b9f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f3b9f-114">Description</span></span>

<span data-ttu-id="f3b9f-115">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="f3b9f-116">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="f3b9f-117">[Васапи](wasapi.md) для операций управления потоком, таких как запуск и остановка потока, и переключение потоков.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, and stream switching.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b9f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f3b9f-118">Requirements</span></span>



| <span data-ttu-id="f3b9f-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="f3b9f-119">Product</span></span>                                                        | <span data-ttu-id="f3b9f-120">Version</span><span class="sxs-lookup"><span data-stu-id="f3b9f-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="f3b9f-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f3b9f-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="f3b9f-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3b9f-122">Windows 7</span></span> |
| <span data-ttu-id="f3b9f-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3b9f-123">Visual Studio</span></span>                                                  | <span data-ttu-id="f3b9f-124">2008</span><span class="sxs-lookup"><span data-stu-id="f3b9f-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f3b9f-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="f3b9f-125">Downloading the Sample</span></span>

<span data-ttu-id="f3b9f-126">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="f3b9f-127">Расположение</span><span class="sxs-lookup"><span data-stu-id="f3b9f-127">Location</span></span>    | <span data-ttu-id="f3b9f-128">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="f3b9f-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b9f-129">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f3b9f-129">Windows SDK</span></span> | <span data-ttu-id="f3b9f-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ каптурешаредевентдривен \\ ...</span><span class="sxs-lookup"><span data-stu-id="f3b9f-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="f3b9f-131">Построение образца</span><span class="sxs-lookup"><span data-stu-id="f3b9f-131">Building the Sample</span></span>

<span data-ttu-id="f3b9f-132">Чтобы создать пример Каптурешаредевентдривен, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-132">To build the CaptureSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="f3b9f-133">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров Каптурешаредевентдривен.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="f3b9f-134">Выполните команду `start WASAPICaptureSharedEventDriven.sln` в каталоге каптурешаредевентдривен, чтобы открыть проект васапикаптурешаредевентдривен в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-134">Run the command `start WASAPICaptureSharedEventDriven.sln` in the CaptureSharedEventDriven directory to open the WASAPICaptureSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="f3b9f-135">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="f3b9f-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="f3b9f-136">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="f3b9f-137">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Васапикаптурешаредевентдривен. vcproj.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f3b9f-138">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="f3b9f-138">Running the Sample</span></span>

<span data-ttu-id="f3b9f-139">При успешном создании демонстрационного приложения создается исполняемый файл WASAPICaptureSharedEventDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="f3b9f-140">Чтобы запустить его, введите `WASAPICaptureSharedEventDriven` в командном окне, а затем обязательные или необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-140">To run it, type `WASAPICaptureSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="f3b9f-141">В следующем примере показано, как запустить пример, указав длительность записи на устройстве мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="f3b9f-142">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="f3b9f-143">Аргумент</span><span class="sxs-lookup"><span data-stu-id="f3b9f-143">Argument</span></span>        | <span data-ttu-id="f3b9f-144">Описание</span><span class="sxs-lookup"><span data-stu-id="f3b9f-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="f3b9f-145">-?</span><span class="sxs-lookup"><span data-stu-id="f3b9f-145">-?</span></span>              | <span data-ttu-id="f3b9f-146">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-146">Shows help.</span></span>                                                |
| <span data-ttu-id="f3b9f-147">-H</span><span class="sxs-lookup"><span data-stu-id="f3b9f-147">-h</span></span>              | <span data-ttu-id="f3b9f-148">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-148">Shows help.</span></span>                                                |
| <span data-ttu-id="f3b9f-149">-l</span><span class="sxs-lookup"><span data-stu-id="f3b9f-149">-l</span></span>              | <span data-ttu-id="f3b9f-150">Задержка записи звука в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="f3b9f-151">-d</span><span class="sxs-lookup"><span data-stu-id="f3b9f-151">-d</span></span>              | <span data-ttu-id="f3b9f-152">Длительность записи звука в секундах.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="f3b9f-153">-M</span><span class="sxs-lookup"><span data-stu-id="f3b9f-153">-m</span></span>              | <span data-ttu-id="f3b9f-154">Отключает использование MMCSS.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="f3b9f-155">-Console</span><span class="sxs-lookup"><span data-stu-id="f3b9f-155">-console</span></span>        | <span data-ttu-id="f3b9f-156">Использовать консольное устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="f3b9f-157">-связь</span><span class="sxs-lookup"><span data-stu-id="f3b9f-157">-communications</span></span> | <span data-ttu-id="f3b9f-158">Используйте устройство связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="f3b9f-159">— мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f3b9f-159">-multimedia</span></span>     | <span data-ttu-id="f3b9f-160">Используйте устройство мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="f3b9f-161">— Конечная точка</span><span class="sxs-lookup"><span data-stu-id="f3b9f-161">-endpoint</span></span>       | <span data-ttu-id="f3b9f-162">Используйте идентификатор конечной точки, указанный в значении переключателя.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="f3b9f-163">Если приложение запускается без аргументов, оно перечисляет доступные устройства и предлагает пользователю выбрать устройство для сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="f3b9f-164">Далее перечислены устройства, используемые по умолчанию для консоли, обмена данными и мультимедиа, а также идентификаторы конечных точек.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="f3b9f-165">Если длительность не указана, аудиопоток из указанного устройства записывается в течение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="f3b9f-166">Приложение записывает записанные данные в файл. WAV с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="f3b9f-167">Каптурешаредевентдривен демонстрирует буферизацию, управляемую событиями.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-167">CaptureSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="f3b9f-168">Экземпляр аудиопотока, созданный для этого примера, настроен для работы в общем режиме, и обработка звукового буфера клиентом осуществляется с помощью установки флага **аудклнт \_ стреамфлагс \_ вложенный EventCallback** в вызове [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="f3b9f-168">The audio client instantiated for this sample is configured to run in shared mode and the client's processing of the audio buffer is made event driven by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span> <span data-ttu-id="f3b9f-169">В примере показано, как клиент должен предоставить системе обработчик событий, вызвав метод [**иаудиоклиент:: сетевенсандле**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="f3b9f-169">The sample shows how the client must provide an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span> <span data-ttu-id="f3b9f-170">После начала сеанса записи и запуска потока обработчик звука передает указанный обработчик событий в уведомление клиента каждый раз, когда буфер будет готов к обработке клиентом.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-170">After the capture session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="f3b9f-171">Звуковые данные также могут обрабатываться в цикле, управляемом таймером.</span><span class="sxs-lookup"><span data-stu-id="f3b9f-171">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="f3b9f-172">Этот режим — демостратед в примере [каптурешаредтимердривен](capturesharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="f3b9f-172">This mode is demostrated in the [CaptureSharedTimerDriven](capturesharedtimerdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3b9f-173">См. также</span><span class="sxs-lookup"><span data-stu-id="f3b9f-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b9f-174">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="f3b9f-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



