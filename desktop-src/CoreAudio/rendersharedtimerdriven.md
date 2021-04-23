---
description: Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: рендершаредтимердривен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807553"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="0e991-103">рендершаредтимердривен</span><span class="sxs-lookup"><span data-stu-id="0e991-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="0e991-104">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="0e991-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="0e991-105">В этом примере демонстрируется буферизация, управляемая таймером, для клиента отрисовки в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="0e991-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="0e991-106">Для потока общего режима клиент совместно использует буфер конечной точки с обработчиком аудио.</span><span class="sxs-lookup"><span data-stu-id="0e991-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="0e991-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0e991-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0e991-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0e991-108">Description</span></span>](#description)
-   [<span data-ttu-id="0e991-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0e991-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0e991-110">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0e991-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0e991-111">Создание примера</span><span class="sxs-lookup"><span data-stu-id="0e991-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0e991-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0e991-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="0e991-113">См. также</span><span class="sxs-lookup"><span data-stu-id="0e991-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="0e991-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0e991-114">Description</span></span>

<span data-ttu-id="0e991-115">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="0e991-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="0e991-116">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="0e991-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="0e991-117">ВАСАПИ для операций управления потоком.</span><span class="sxs-lookup"><span data-stu-id="0e991-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e991-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0e991-118">Requirements</span></span>



| <span data-ttu-id="0e991-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="0e991-119">Product</span></span>                                                        | <span data-ttu-id="0e991-120">Version</span><span class="sxs-lookup"><span data-stu-id="0e991-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0e991-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0e991-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0e991-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e991-122">Windows 7</span></span> |
| <span data-ttu-id="0e991-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0e991-123">Visual Studio</span></span>                                                  | <span data-ttu-id="0e991-124">2008</span><span class="sxs-lookup"><span data-stu-id="0e991-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0e991-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0e991-125">Downloading the Sample</span></span>

<span data-ttu-id="0e991-126">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="0e991-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="0e991-127">Расположение</span><span class="sxs-lookup"><span data-stu-id="0e991-127">Location</span></span>    | <span data-ttu-id="0e991-128">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="0e991-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e991-129">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0e991-129">Windows SDK</span></span> | <span data-ttu-id="0e991-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ рендершаредтимердривен \\ ...</span><span class="sxs-lookup"><span data-stu-id="0e991-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="0e991-131">Построение образца</span><span class="sxs-lookup"><span data-stu-id="0e991-131">Building the Sample</span></span>

<span data-ttu-id="0e991-132">Чтобы создать пример Рендершаредтимердривен, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e991-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="0e991-133">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров Рендершаредтимердривен.</span><span class="sxs-lookup"><span data-stu-id="0e991-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="0e991-134">Выполните команду `start WASAPIRenderSharedTimerDriven.sln` в каталоге рендершаредтимердривен, чтобы открыть проект васапирендершаредтимердривен в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0e991-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="0e991-135">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="0e991-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="0e991-136">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="0e991-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="0e991-137">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Васапирендершаредтимердривен. vcproj.</span><span class="sxs-lookup"><span data-stu-id="0e991-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0e991-138">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="0e991-138">Running the Sample</span></span>

<span data-ttu-id="0e991-139">При успешном создании демонстрационного приложения создается исполняемый файл WASAPIRenderSharedTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="0e991-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="0e991-140">Чтобы запустить его, введите `WASAPIRenderSharedTimerDriven` в командном окне, а затем обязательные или необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="0e991-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="0e991-141">В следующем примере показано, как запустить пример, указав длительность воспроизведения на устройстве мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e991-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="0e991-142">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="0e991-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="0e991-143">Аргумент</span><span class="sxs-lookup"><span data-stu-id="0e991-143">Argument</span></span>        | <span data-ttu-id="0e991-144">Описание</span><span class="sxs-lookup"><span data-stu-id="0e991-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="0e991-145">-?</span><span class="sxs-lookup"><span data-stu-id="0e991-145">-?</span></span>              | <span data-ttu-id="0e991-146">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="0e991-146">Shows help.</span></span>                                                |
| <span data-ttu-id="0e991-147">-H</span><span class="sxs-lookup"><span data-stu-id="0e991-147">-h</span></span>              | <span data-ttu-id="0e991-148">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="0e991-148">Shows help.</span></span>                                                |
| <span data-ttu-id="0e991-149">-f</span><span class="sxs-lookup"><span data-stu-id="0e991-149">-f</span></span>              | <span data-ttu-id="0e991-150">Синус частоты волны в Гц.</span><span class="sxs-lookup"><span data-stu-id="0e991-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="0e991-151">-l</span><span class="sxs-lookup"><span data-stu-id="0e991-151">-l</span></span>              | <span data-ttu-id="0e991-152">Задержка визуализации звука в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="0e991-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="0e991-153">-d</span><span class="sxs-lookup"><span data-stu-id="0e991-153">-d</span></span>              | <span data-ttu-id="0e991-154">Синус длительности WAV в секундах.</span><span class="sxs-lookup"><span data-stu-id="0e991-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="0e991-155">-M</span><span class="sxs-lookup"><span data-stu-id="0e991-155">-m</span></span>              | <span data-ttu-id="0e991-156">Отключает использование MMCSS.</span><span class="sxs-lookup"><span data-stu-id="0e991-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="0e991-157">-Console</span><span class="sxs-lookup"><span data-stu-id="0e991-157">-console</span></span>        | <span data-ttu-id="0e991-158">Использовать консольное устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e991-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="0e991-159">-связь</span><span class="sxs-lookup"><span data-stu-id="0e991-159">-communications</span></span> | <span data-ttu-id="0e991-160">Используйте устройство связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e991-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="0e991-161">— мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0e991-161">-multimedia</span></span>     | <span data-ttu-id="0e991-162">Используйте устройство мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e991-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="0e991-163">— Конечная точка</span><span class="sxs-lookup"><span data-stu-id="0e991-163">-endpoint</span></span>       | <span data-ttu-id="0e991-164">Используйте идентификатор конечной точки, указанный в значении переключателя.</span><span class="sxs-lookup"><span data-stu-id="0e991-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="0e991-165">Если приложение запускается без аргументов, оно перечисляет доступные устройства и предлагает пользователю выбрать устройство для сеанса подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0e991-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="0e991-166">После того как пользователь назначит устройство, оно выводит синус в 440 Гц в течение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="0e991-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="0e991-167">Эти значения можно изменить, указав значения параметра-f и-d.</span><span class="sxs-lookup"><span data-stu-id="0e991-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="0e991-168">Рендершаредтимердривен демонстрирует буферизацию, управляемую таймером.</span><span class="sxs-lookup"><span data-stu-id="0e991-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="0e991-169">В этом режиме клиент должен подождать некоторое время (половина задержки, заданную параметром-d, в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="0e991-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="0e991-170">Когда клиент выходит из спящего режима, в два раза через период обработки он извлекает следующий набор примеров из подсистемы.</span><span class="sxs-lookup"><span data-stu-id="0e991-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="0e991-171">Перед каждым проходом обработки в цикле буферизации клиент должен определить объем данных для подготовки к просмотру, чтобы данные не передавали буфер.</span><span class="sxs-lookup"><span data-stu-id="0e991-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="0e991-172">Звуковые данные, которые будут воспроизводиться на указанном устройстве, можно обработать, включив буферизацию, управляемую событиями.</span><span class="sxs-lookup"><span data-stu-id="0e991-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="0e991-173">Этот режим показан в примере [рендершаредевентдривен](rendersharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="0e991-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="0e991-174">Дополнительные сведения о визуализации потока см. в разделе [Визуализация потока](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="0e991-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e991-175">См. также</span><span class="sxs-lookup"><span data-stu-id="0e991-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e991-176">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="0e991-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



