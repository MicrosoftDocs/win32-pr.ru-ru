---
description: Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: рендершаредевентдривен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9901896b962717ed72fd36d022eef9510d7cb916
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896070"
---
# <a name="rendersharedeventdriven"></a><span data-ttu-id="d04cb-103">рендершаредевентдривен</span><span class="sxs-lookup"><span data-stu-id="d04cb-103">RenderSharedEventDriven</span></span>

<span data-ttu-id="d04cb-104">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="d04cb-104">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="d04cb-105">В этом примере демонстрируется буферизация, управляемая событиями, для клиента отрисовки в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="d04cb-105">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="d04cb-106">Для потока общего режима клиент совместно использует буфер конечной точки с обработчиком аудио.</span><span class="sxs-lookup"><span data-stu-id="d04cb-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="d04cb-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="d04cb-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d04cb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d04cb-108">Description</span></span>](#description)
-   [<span data-ttu-id="d04cb-109">Требования</span><span class="sxs-lookup"><span data-stu-id="d04cb-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d04cb-110">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="d04cb-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d04cb-111">Создание примера</span><span class="sxs-lookup"><span data-stu-id="d04cb-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d04cb-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="d04cb-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d04cb-113">См. также</span><span class="sxs-lookup"><span data-stu-id="d04cb-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="d04cb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d04cb-114">Description</span></span>

<span data-ttu-id="d04cb-115">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="d04cb-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="d04cb-116">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="d04cb-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="d04cb-117">ВАСАПИ для операций управления потоком.</span><span class="sxs-lookup"><span data-stu-id="d04cb-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04cb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d04cb-118">Requirements</span></span>



| <span data-ttu-id="d04cb-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="d04cb-119">Product</span></span>                                                        | <span data-ttu-id="d04cb-120">Version</span><span class="sxs-lookup"><span data-stu-id="d04cb-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d04cb-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d04cb-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d04cb-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d04cb-122">Windows 7</span></span> |
| <span data-ttu-id="d04cb-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d04cb-123">Visual Studio</span></span>                                                  | <span data-ttu-id="d04cb-124">2008</span><span class="sxs-lookup"><span data-stu-id="d04cb-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d04cb-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="d04cb-125">Downloading the Sample</span></span>

<span data-ttu-id="d04cb-126">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="d04cb-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="d04cb-127">Расположение</span><span class="sxs-lookup"><span data-stu-id="d04cb-127">Location</span></span>    | <span data-ttu-id="d04cb-128">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d04cb-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d04cb-129">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d04cb-129">Windows SDK</span></span> | <span data-ttu-id="d04cb-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ рендершаредевентдривен \\ ...</span><span class="sxs-lookup"><span data-stu-id="d04cb-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="d04cb-131">Построение образца</span><span class="sxs-lookup"><span data-stu-id="d04cb-131">Building the Sample</span></span>

<span data-ttu-id="d04cb-132">Чтобы создать пример Рендершаредевентдривен, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d04cb-132">To build the RenderSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="d04cb-133">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров Рендершаредевентдривен.</span><span class="sxs-lookup"><span data-stu-id="d04cb-133">Open the CMD shell for the Windows SDK and change to the RenderSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="d04cb-134">Выполните команду `start WASAPIRenderSharedEventDriven.sln` в каталоге рендершаредевентдривен, чтобы открыть проект васапирендершаредевентдривен в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d04cb-134">Run the command `start WASAPIRenderSharedEventDriven.sln` in the RenderSharedEventDriven directory to open the WASAPIRenderSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="d04cb-135">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="d04cb-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="d04cb-136">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="d04cb-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="d04cb-137">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Васапирендершаредевентдривен. vcproj.</span><span class="sxs-lookup"><span data-stu-id="d04cb-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d04cb-138">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="d04cb-138">Running the Sample</span></span>

<span data-ttu-id="d04cb-139">При успешном создании демонстрационного приложения создается исполняемый файл WASAPIRenderSharedEventDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="d04cb-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="d04cb-140">Чтобы запустить его, введите `WASAPIRenderSharedEventDriven` в командном окне, а затем обязательные или необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="d04cb-140">To run it, type `WASAPIRenderSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="d04cb-141">В следующем примере показано, как запустить пример, указав длительность воспроизведения на устройстве мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d04cb-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="d04cb-142">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="d04cb-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="d04cb-143">Аргумент</span><span class="sxs-lookup"><span data-stu-id="d04cb-143">Argument</span></span>        | <span data-ttu-id="d04cb-144">Описание</span><span class="sxs-lookup"><span data-stu-id="d04cb-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="d04cb-145">-?</span><span class="sxs-lookup"><span data-stu-id="d04cb-145">-?</span></span>              | <span data-ttu-id="d04cb-146">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="d04cb-146">Shows help.</span></span>                                                |
| <span data-ttu-id="d04cb-147">-H</span><span class="sxs-lookup"><span data-stu-id="d04cb-147">-h</span></span>              | <span data-ttu-id="d04cb-148">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="d04cb-148">Shows help.</span></span>                                                |
| <span data-ttu-id="d04cb-149">-f</span><span class="sxs-lookup"><span data-stu-id="d04cb-149">-f</span></span>              | <span data-ttu-id="d04cb-150">Синус частоты волны в Гц.</span><span class="sxs-lookup"><span data-stu-id="d04cb-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="d04cb-151">-l</span><span class="sxs-lookup"><span data-stu-id="d04cb-151">-l</span></span>              | <span data-ttu-id="d04cb-152">Задержка визуализации звука в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="d04cb-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="d04cb-153">-d</span><span class="sxs-lookup"><span data-stu-id="d04cb-153">-d</span></span>              | <span data-ttu-id="d04cb-154">Синус длительности WAV в секундах.</span><span class="sxs-lookup"><span data-stu-id="d04cb-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="d04cb-155">-M</span><span class="sxs-lookup"><span data-stu-id="d04cb-155">-m</span></span>              | <span data-ttu-id="d04cb-156">Отключает использование MMCSS.</span><span class="sxs-lookup"><span data-stu-id="d04cb-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="d04cb-157">-Console</span><span class="sxs-lookup"><span data-stu-id="d04cb-157">-console</span></span>        | <span data-ttu-id="d04cb-158">Использовать консольное устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d04cb-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="d04cb-159">-связь</span><span class="sxs-lookup"><span data-stu-id="d04cb-159">-communications</span></span> | <span data-ttu-id="d04cb-160">Используйте устройство связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d04cb-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="d04cb-161">— мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d04cb-161">-multimedia</span></span>     | <span data-ttu-id="d04cb-162">Используйте устройство мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d04cb-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="d04cb-163">— Конечная точка</span><span class="sxs-lookup"><span data-stu-id="d04cb-163">-endpoint</span></span>       | <span data-ttu-id="d04cb-164">Используйте идентификатор конечной точки, указанный в значении переключателя.</span><span class="sxs-lookup"><span data-stu-id="d04cb-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="d04cb-165">Если приложение запускается без аргументов, оно перечисляет доступные устройства и предлагает пользователю выбрать устройство для сеанса подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="d04cb-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="d04cb-166">После того как пользователь назначит устройство, оно выводит синус в 440 Гц в течение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="d04cb-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="d04cb-167">Эти значения можно изменить, указав значения параметра-f и-d.</span><span class="sxs-lookup"><span data-stu-id="d04cb-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="d04cb-168">Рендершаредевентдривен демонстрирует буферизацию, управляемую событиями.</span><span class="sxs-lookup"><span data-stu-id="d04cb-168">RenderSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="d04cb-169">В этом примере показано, как:</span><span class="sxs-lookup"><span data-stu-id="d04cb-169">The sample shows how to:</span></span>

-   <span data-ttu-id="d04cb-170">Создайте экземпляр аудио клиента, настройте его для работы в монопольном режиме и включите управляемую событиями буферизацию, установив флаг **аудклнт \_ стреамфлагс \_ вложенный EventCallback** в вызове [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="d04cb-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="d04cb-171">Свяжите клиент с образцами, готовыми к просмотру, предоставив обработчик событий системе, вызвав метод [**иаудиоклиент:: сетевенсандле**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="d04cb-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="d04cb-172">Создайте поток отрисовки для обработки образцов из обработчика аудио.</span><span class="sxs-lookup"><span data-stu-id="d04cb-172">Create a render thread to proces samples from the audio engine.</span></span>
-   <span data-ttu-id="d04cb-173">Проверьте формат Mix конечной точки устройства, чтобы определить, можно ли отобразить образцы.</span><span class="sxs-lookup"><span data-stu-id="d04cb-173">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="d04cb-174">Если устройство не поддерживает формат Mix, данные преобразуются в PCM.</span><span class="sxs-lookup"><span data-stu-id="d04cb-174">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="d04cb-175">Обрабатывайте переключение потоков.</span><span class="sxs-lookup"><span data-stu-id="d04cb-175">Handle stream switching.</span></span>

<span data-ttu-id="d04cb-176">После начала сеанса подготовки к просмотру и запуска потока обработчик звука передает указанный обработчик событий в уведомление клиента каждый раз, когда буфер будет готов к обработке клиентом.</span><span class="sxs-lookup"><span data-stu-id="d04cb-176">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="d04cb-177">Звуковые данные также могут обрабатываться в цикле, управляемом таймером.</span><span class="sxs-lookup"><span data-stu-id="d04cb-177">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="d04cb-178">Этот режим показан в примере [рендершаредтимердривен](rendersharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="d04cb-178">This mode is demonstrated in the [RenderSharedTimerDriven](rendersharedtimerdriven.md) sample.</span></span>

<span data-ttu-id="d04cb-179">Дополнительные сведения о визуализации потока см. в разделе [Визуализация потока](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="d04cb-179">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d04cb-180">См. также</span><span class="sxs-lookup"><span data-stu-id="d04cb-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d04cb-181">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="d04cb-181">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



