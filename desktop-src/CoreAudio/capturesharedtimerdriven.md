---
description: Этот пример приложения использует основные API аудио для записи звуковых данных с устройства ввода, указанного пользователем, и записывает их в WAV-файл с уникальным именем в текущем каталоге. В этом примере демонстрируется буферизация, управляемая таймером.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: каптурешаредтимердривен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072460"
---
# <a name="capturesharedtimerdriven"></a><span data-ttu-id="52f24-104">каптурешаредтимердривен</span><span class="sxs-lookup"><span data-stu-id="52f24-104">CaptureSharedTimerDriven</span></span>

<span data-ttu-id="52f24-105">Этот пример приложения использует основные API аудио для записи звуковых данных с устройства ввода, указанного пользователем, и записывает их в WAV-файл с уникальным именем в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="52f24-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="52f24-106">В этом примере демонстрируется буферизация, управляемая таймером.</span><span class="sxs-lookup"><span data-stu-id="52f24-106">This sample demonstrates timer-driven buffering.</span></span>

<span data-ttu-id="52f24-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="52f24-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="52f24-108">Описание</span><span class="sxs-lookup"><span data-stu-id="52f24-108">Description</span></span>](#description)
-   [<span data-ttu-id="52f24-109">Требования</span><span class="sxs-lookup"><span data-stu-id="52f24-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="52f24-110">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="52f24-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="52f24-111">Создание примера</span><span class="sxs-lookup"><span data-stu-id="52f24-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="52f24-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="52f24-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="52f24-113">См. также</span><span class="sxs-lookup"><span data-stu-id="52f24-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="52f24-114">Описание</span><span class="sxs-lookup"><span data-stu-id="52f24-114">Description</span></span>

<span data-ttu-id="52f24-115">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="52f24-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="52f24-116">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="52f24-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="52f24-117">[Васапи](wasapi.md) для операций управления потоком.</span><span class="sxs-lookup"><span data-stu-id="52f24-117">[WASAPI](wasapi.md) for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f24-118">Требования</span><span class="sxs-lookup"><span data-stu-id="52f24-118">Requirements</span></span>



| <span data-ttu-id="52f24-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="52f24-119">Product</span></span>                                                        | <span data-ttu-id="52f24-120">Version</span><span class="sxs-lookup"><span data-stu-id="52f24-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="52f24-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="52f24-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="52f24-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52f24-122">Windows 7</span></span> |
| <span data-ttu-id="52f24-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52f24-123">Visual Studio</span></span>                                                  | <span data-ttu-id="52f24-124">2008</span><span class="sxs-lookup"><span data-stu-id="52f24-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="52f24-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="52f24-125">Downloading the Sample</span></span>

<span data-ttu-id="52f24-126">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="52f24-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="52f24-127">Расположение</span><span class="sxs-lookup"><span data-stu-id="52f24-127">Location</span></span>    | <span data-ttu-id="52f24-128">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="52f24-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f24-129">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="52f24-129">Windows SDK</span></span> | <span data-ttu-id="52f24-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ каптурешаредтимердривен \\ ...</span><span class="sxs-lookup"><span data-stu-id="52f24-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="52f24-131">Построение образца</span><span class="sxs-lookup"><span data-stu-id="52f24-131">Building the Sample</span></span>

<span data-ttu-id="52f24-132">Чтобы создать пример Каптурешаредтимердривен, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="52f24-132">To build the CaptureSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="52f24-133">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров Каптурешаредтимердривен.</span><span class="sxs-lookup"><span data-stu-id="52f24-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="52f24-134">Выполните команду `start WASAPICaptureSharedTimerDriven.sln` в каталоге каптурешаредтимердривен, чтобы открыть проект васапикаптурешаредтимердривен в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="52f24-134">Run the command `start WASAPICaptureSharedTimerDriven.sln` in the CaptureSharedTimerDriven directory to open the WASAPICaptureSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="52f24-135">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="52f24-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="52f24-136">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="52f24-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="52f24-137">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Васапикаптурешаредтимердривен. vcproj.</span><span class="sxs-lookup"><span data-stu-id="52f24-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="52f24-138">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="52f24-138">Running the Sample</span></span>

<span data-ttu-id="52f24-139">При успешном создании демонстрационного приложения создается исполняемый файл WASAPICaptureSharedTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="52f24-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="52f24-140">Чтобы запустить его, введите `WASAPICaptureSharedTimerDriven` в командном окне, а затем обязательные или необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="52f24-140">To run it, type `WASAPICaptureSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="52f24-141">В следующем примере показано, как запустить пример, указав длительность записи на устройстве мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52f24-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="52f24-142">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="52f24-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="52f24-143">Аргумент</span><span class="sxs-lookup"><span data-stu-id="52f24-143">Argument</span></span>        | <span data-ttu-id="52f24-144">Описание</span><span class="sxs-lookup"><span data-stu-id="52f24-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="52f24-145">-?</span><span class="sxs-lookup"><span data-stu-id="52f24-145">-?</span></span>              | <span data-ttu-id="52f24-146">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="52f24-146">Shows help.</span></span>                                                |
| <span data-ttu-id="52f24-147">-H</span><span class="sxs-lookup"><span data-stu-id="52f24-147">-h</span></span>              | <span data-ttu-id="52f24-148">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="52f24-148">Shows help.</span></span>                                                |
| <span data-ttu-id="52f24-149">-l</span><span class="sxs-lookup"><span data-stu-id="52f24-149">-l</span></span>              | <span data-ttu-id="52f24-150">Задержка записи звука в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="52f24-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="52f24-151">-d</span><span class="sxs-lookup"><span data-stu-id="52f24-151">-d</span></span>              | <span data-ttu-id="52f24-152">Длительность записи звука в секундах.</span><span class="sxs-lookup"><span data-stu-id="52f24-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="52f24-153">-M</span><span class="sxs-lookup"><span data-stu-id="52f24-153">-m</span></span>              | <span data-ttu-id="52f24-154">Отключает использование MMCSS.</span><span class="sxs-lookup"><span data-stu-id="52f24-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="52f24-155">-Console</span><span class="sxs-lookup"><span data-stu-id="52f24-155">-console</span></span>        | <span data-ttu-id="52f24-156">Использовать консольное устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52f24-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="52f24-157">-связь</span><span class="sxs-lookup"><span data-stu-id="52f24-157">-communications</span></span> | <span data-ttu-id="52f24-158">Используйте устройство связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52f24-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="52f24-159">— мультимедиа</span><span class="sxs-lookup"><span data-stu-id="52f24-159">-multimedia</span></span>     | <span data-ttu-id="52f24-160">Используйте устройство мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52f24-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="52f24-161">— Конечная точка</span><span class="sxs-lookup"><span data-stu-id="52f24-161">-endpoint</span></span>       | <span data-ttu-id="52f24-162">Используйте идентификатор конечной точки, указанный в значении переключателя.</span><span class="sxs-lookup"><span data-stu-id="52f24-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="52f24-163">Если приложение запускается без аргументов, оно перечисляет доступные устройства и предлагает пользователю выбрать устройство для сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="52f24-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="52f24-164">Далее перечислены устройства, используемые по умолчанию для консоли, обмена данными и мультимедиа, а также идентификаторы конечных точек.</span><span class="sxs-lookup"><span data-stu-id="52f24-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="52f24-165">Если длительность не указана, аудиопоток из указанного устройства записывается в течение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="52f24-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="52f24-166">Приложение записывает записанные данные в файл. WAV с уникальным именем.</span><span class="sxs-lookup"><span data-stu-id="52f24-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="52f24-167">Каптурешаредтимердривен демонстрирует буферизацию, управляемую таймером.</span><span class="sxs-lookup"><span data-stu-id="52f24-167">CaptureSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="52f24-168">В этом режиме клиент должен подождать некоторое время (половина задержки, заданную параметром-d, в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="52f24-168">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="52f24-169">Когда клиент выходит из спящего режима, в два раза через период обработки он извлекает следующий набор примеров из подсистемы.</span><span class="sxs-lookup"><span data-stu-id="52f24-169">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="52f24-170">Перед каждым проходом обработки в цикле буферизации клиент должен определить объем доступных данных отслеживания, чтобы данные не передавали буфер записи.</span><span class="sxs-lookup"><span data-stu-id="52f24-170">Before each processing pass in the buffering loop, the client must find out the amount of capture data available so that the data does not overrun the capture buffer.</span></span> <span data-ttu-id="52f24-171">Звуковые данные, записываемые с указанного устройства, можно обработать, включив буферизацию, управляемую событиями.</span><span class="sxs-lookup"><span data-stu-id="52f24-171">The audio data that is captured from the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="52f24-172">Этот режим показан в примере [каптурешаредевентдривен](capturesharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="52f24-172">This mode is demonstrated in the [CaptureSharedEventDriven](capturesharedeventdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52f24-173">См. также</span><span class="sxs-lookup"><span data-stu-id="52f24-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f24-174">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="52f24-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



