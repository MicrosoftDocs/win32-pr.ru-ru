---
description: Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем. В этом примере демонстрируется буферизация, управляемая таймером, для клиента отрисовки в монопольном режиме.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: рендерексклусиветимердривен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496365"
---
# <a name="renderexclusivetimerdriven"></a><span data-ttu-id="0197b-104">рендерексклусиветимердривен</span><span class="sxs-lookup"><span data-stu-id="0197b-104">RenderExclusiveTimerDriven</span></span>

<span data-ttu-id="0197b-105">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="0197b-105">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="0197b-106">В этом примере демонстрируется буферизация, управляемая таймером, для клиента отрисовки в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="0197b-106">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="0197b-107">Для потока с монопольным режимом клиент использует буфер конечной точки с звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="0197b-107">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="0197b-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0197b-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0197b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0197b-109">Description</span></span>](#description)
-   [<span data-ttu-id="0197b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="0197b-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0197b-111">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0197b-111">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0197b-112">Создание примера</span><span class="sxs-lookup"><span data-stu-id="0197b-112">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0197b-113">Просмотр примеров файлов</span><span class="sxs-lookup"><span data-stu-id="0197b-113">View the Sample Files</span></span>](#view-the-sample-files)
-   [<span data-ttu-id="0197b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="0197b-114">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="0197b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="0197b-115">Description</span></span>

<span data-ttu-id="0197b-116">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="0197b-116">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="0197b-117">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="0197b-117">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="0197b-118">ВАСАПИ для операций управления потоком.</span><span class="sxs-lookup"><span data-stu-id="0197b-118">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="0197b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0197b-119">Requirements</span></span>



| <span data-ttu-id="0197b-120">Продукт</span><span class="sxs-lookup"><span data-stu-id="0197b-120">Product</span></span>                                                        | <span data-ttu-id="0197b-121">Version</span><span class="sxs-lookup"><span data-stu-id="0197b-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0197b-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0197b-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0197b-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0197b-123">Windows 7</span></span> |
| <span data-ttu-id="0197b-124">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0197b-124">Visual Studio</span></span>                                                  | <span data-ttu-id="0197b-125">2008</span><span class="sxs-lookup"><span data-stu-id="0197b-125">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0197b-126">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0197b-126">Downloading the Sample</span></span>

<span data-ttu-id="0197b-127">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="0197b-127">This sample is available in the following locations.</span></span>



| <span data-ttu-id="0197b-128">Расположение</span><span class="sxs-lookup"><span data-stu-id="0197b-128">Location</span></span>    | <span data-ttu-id="0197b-129">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="0197b-129">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0197b-130">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0197b-130">Windows SDK</span></span> | <span data-ttu-id="0197b-131">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ рендерексклусиветимердривен \\ ...</span><span class="sxs-lookup"><span data-stu-id="0197b-131">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="0197b-132">Построение образца</span><span class="sxs-lookup"><span data-stu-id="0197b-132">Building the Sample</span></span>

<span data-ttu-id="0197b-133">Чтобы создать пример Рендерексклусиветимердривен, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0197b-133">To build the RenderExclusiveTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="0197b-134">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров Рендерексклусиветимердривен.</span><span class="sxs-lookup"><span data-stu-id="0197b-134">Open the CMD shell for the Windows SDK and change to the RenderExclusiveTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="0197b-135">Выполните команду `start WASAPIRenderExclusiveTimerDriven.sln` в каталоге рендерексклусиветимердривен, чтобы открыть проект васапирендерексклусиветимердривен в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0197b-135">Run the command `start WASAPIRenderExclusiveTimerDriven.sln` in the RenderExclusiveTimerDriven directory to open the WASAPIRenderExclusiveTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="0197b-136">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="0197b-136">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="0197b-137">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="0197b-137">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="0197b-138">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Васапирендерексклусиветимердривен. vcproj.</span><span class="sxs-lookup"><span data-stu-id="0197b-138">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveTimerDriven.vcproj.</span></span>

## <a name="view-the-sample-files"></a><span data-ttu-id="0197b-139">Просмотр примеров файлов</span><span class="sxs-lookup"><span data-stu-id="0197b-139">View the Sample Files</span></span>

<span data-ttu-id="0197b-140">При успешном создании демонстрационного приложения создается исполняемый файл WASAPIRenderExclusiveTimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="0197b-140">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveTimerDriven.exe, is generated.</span></span> <span data-ttu-id="0197b-141">Чтобы запустить его, введите `WASAPIRenderExclusiveTimerDriven` в командном окне, а затем обязательные или необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="0197b-141">To run it, type `WASAPIRenderExclusiveTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="0197b-142">В следующем примере показано, как запустить пример, указав длительность воспроизведения на консольном устройстве по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0197b-142">The following example shows how to run the sample by a specifying playback duration on the default console device.</span></span>

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

<span data-ttu-id="0197b-143">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="0197b-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="0197b-144">Аргумент</span><span class="sxs-lookup"><span data-stu-id="0197b-144">Argument</span></span>        | <span data-ttu-id="0197b-145">Описание</span><span class="sxs-lookup"><span data-stu-id="0197b-145">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="0197b-146">-?</span><span class="sxs-lookup"><span data-stu-id="0197b-146">-?</span></span>              | <span data-ttu-id="0197b-147">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="0197b-147">Shows help.</span></span>                                                |
| <span data-ttu-id="0197b-148">-H</span><span class="sxs-lookup"><span data-stu-id="0197b-148">-h</span></span>              | <span data-ttu-id="0197b-149">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="0197b-149">Shows help.</span></span>                                                |
| <span data-ttu-id="0197b-150">-f</span><span class="sxs-lookup"><span data-stu-id="0197b-150">-f</span></span>              | <span data-ttu-id="0197b-151">Синус частоты волны в Гц.</span><span class="sxs-lookup"><span data-stu-id="0197b-151">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="0197b-152">-l</span><span class="sxs-lookup"><span data-stu-id="0197b-152">-l</span></span>              | <span data-ttu-id="0197b-153">Задержка визуализации звука в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="0197b-153">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="0197b-154">-d</span><span class="sxs-lookup"><span data-stu-id="0197b-154">-d</span></span>              | <span data-ttu-id="0197b-155">Синус длительности WAV в секундах.</span><span class="sxs-lookup"><span data-stu-id="0197b-155">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="0197b-156">-M</span><span class="sxs-lookup"><span data-stu-id="0197b-156">-m</span></span>              | <span data-ttu-id="0197b-157">Отключает использование MMCSS.</span><span class="sxs-lookup"><span data-stu-id="0197b-157">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="0197b-158">-Console</span><span class="sxs-lookup"><span data-stu-id="0197b-158">-console</span></span>        | <span data-ttu-id="0197b-159">Использовать консольное устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0197b-159">Use the default console device.</span></span>                            |
| <span data-ttu-id="0197b-160">-связь</span><span class="sxs-lookup"><span data-stu-id="0197b-160">-communications</span></span> | <span data-ttu-id="0197b-161">Используйте устройство связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0197b-161">Use the default communication device.</span></span>                      |
| <span data-ttu-id="0197b-162">— мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0197b-162">-multimedia</span></span>     | <span data-ttu-id="0197b-163">Используйте устройство мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0197b-163">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="0197b-164">— Конечная точка</span><span class="sxs-lookup"><span data-stu-id="0197b-164">-endpoint</span></span>       | <span data-ttu-id="0197b-165">Используйте идентификатор конечной точки, указанный в значении переключателя.</span><span class="sxs-lookup"><span data-stu-id="0197b-165">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="0197b-166">Если приложение запускается без аргументов, оно перечисляет доступные устройства и предлагает пользователю выбрать устройство для сеанса подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0197b-166">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="0197b-167">После того как пользователь назначит устройство, оно выводит синус в 440 Гц в течение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="0197b-167">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="0197b-168">Эти значения можно изменить, указав значения параметра-f и-d.</span><span class="sxs-lookup"><span data-stu-id="0197b-168">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="0197b-169">Рендерексклусиветимердривен демонстрирует буферизацию, управляемую таймером.</span><span class="sxs-lookup"><span data-stu-id="0197b-169">RenderExclusiveTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="0197b-170">В этом режиме клиент должен подождать некоторое время (половина задержки, заданную параметром-d, в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="0197b-170">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="0197b-171">Когда клиент выходит из спящего режима, в два раза через период обработки он извлекает следующий набор примеров из подсистемы.</span><span class="sxs-lookup"><span data-stu-id="0197b-171">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="0197b-172">Перед каждым проходом обработки в цикле буферизации клиент должен определить объем данных для подготовки к просмотру, чтобы данные не передавали буфер.</span><span class="sxs-lookup"><span data-stu-id="0197b-172">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="0197b-173">Звуковые данные, которые будут воспроизводиться на указанном устройстве, можно обработать, включив буферизацию, управляемую событиями.</span><span class="sxs-lookup"><span data-stu-id="0197b-173">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="0197b-174">Этот режим показан в примере Рендерексклусиветимердривен.</span><span class="sxs-lookup"><span data-stu-id="0197b-174">This mode is demonstrated in the RenderExclusiveTimerDriven sample.</span></span>

<span data-ttu-id="0197b-175">Дополнительные сведения о визуализации потока см. в разделе [Визуализация потока](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="0197b-175">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0197b-176">См. также</span><span class="sxs-lookup"><span data-stu-id="0197b-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0197b-177">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="0197b-177">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



