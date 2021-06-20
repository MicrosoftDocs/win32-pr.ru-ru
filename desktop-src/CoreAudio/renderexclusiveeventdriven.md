---
description: Этот пример приложения, демонстрирующий буферизацию, управляемую событиями, использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: рендерексклусививентдривен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75553496219d0a4ddaf6685089de802e034f94cb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405137"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="bbf3e-103">рендерексклусививентдривен</span><span class="sxs-lookup"><span data-stu-id="bbf3e-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="bbf3e-104">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="bbf3e-105">В этом примере демонстрируется буферизация, управляемая событиями, для клиента отрисовки в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="bbf3e-106">Для потока с монопольным режимом клиент использует буфер конечной точки с звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="bbf3e-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bbf3e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bbf3e-108">Description</span></span>](#description)
-   [<span data-ttu-id="bbf3e-109">Требования</span><span class="sxs-lookup"><span data-stu-id="bbf3e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bbf3e-110">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="bbf3e-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="bbf3e-111">Создание примера</span><span class="sxs-lookup"><span data-stu-id="bbf3e-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="bbf3e-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="bbf3e-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="bbf3e-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bbf3e-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="bbf3e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bbf3e-114">Description</span></span>

<span data-ttu-id="bbf3e-115">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="bbf3e-116">[API ммдевице](mmdevice-api.md) для перечисления мультимедийных устройств и выбора.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="bbf3e-117">ВАСАПИ для операций управления потоком.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf3e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bbf3e-118">Requirements</span></span>



| <span data-ttu-id="bbf3e-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="bbf3e-119">Product</span></span>                                                        | <span data-ttu-id="bbf3e-120">Version</span><span class="sxs-lookup"><span data-stu-id="bbf3e-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="bbf3e-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bbf3e-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bbf3e-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbf3e-122">Windows 7</span></span> |
| <span data-ttu-id="bbf3e-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bbf3e-123">Visual Studio</span></span>                                                  | <span data-ttu-id="bbf3e-124">2008</span><span class="sxs-lookup"><span data-stu-id="bbf3e-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bbf3e-125">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="bbf3e-125">Downloading the Sample</span></span>

<span data-ttu-id="bbf3e-126">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="bbf3e-127">Расположение</span><span class="sxs-lookup"><span data-stu-id="bbf3e-127">Location</span></span>    | <span data-ttu-id="bbf3e-128">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="bbf3e-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf3e-129">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bbf3e-129">Windows SDK</span></span> | <span data-ttu-id="bbf3e-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ рендерексклусививентдривен \\ ...</span><span class="sxs-lookup"><span data-stu-id="bbf3e-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="bbf3e-131">Построение образца</span><span class="sxs-lookup"><span data-stu-id="bbf3e-131">Building the Sample</span></span>

<span data-ttu-id="bbf3e-132">Чтобы создать пример Рендерексклусививентдривен, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="bbf3e-133">Откройте командную оболочку для Windows SDK и перейдите в каталог примеров Рендерексклусививентдривен.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="bbf3e-134">Выполните команду `start WASAPIRenderExclusiveEventDriven.sln` в каталоге рендерексклусививентдривен, чтобы открыть проект васапирендерексклусививентдривен в окне Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="bbf3e-135">В окне выберите конфигурацию решения для **отладки** или **выпуска** , выберите меню **Сборка** в строке меню и выберите параметр **Сборка** .</span><span class="sxs-lookup"><span data-stu-id="bbf3e-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="bbf3e-136">Если не открыть Visual Studio из командной оболочки для пакета SDK, Visual Studio не сможет получить доступ к среде сборки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="bbf3e-137">В этом случае выборка не будет построена, если вы явно не настроили переменную среды Мссдк, которая используется в файле проекта Васапирендерексклусививентдривен. vcproj.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="bbf3e-138">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="bbf3e-138">Running the Sample</span></span>

<span data-ttu-id="bbf3e-139">При успешном создании демонстрационного приложения создается исполняемый файл WASAPIRenderExclusiveEventDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="bbf3e-140">Чтобы запустить его, введите `WASAPIRenderExclusiveEventDriven` в командном окне, а затем обязательные или необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="bbf3e-141">В следующем примере показано, как запустить пример, указав длительность воспроизведения на устройстве мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="bbf3e-142">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="bbf3e-143">Аргумент</span><span class="sxs-lookup"><span data-stu-id="bbf3e-143">Argument</span></span>        | <span data-ttu-id="bbf3e-144">Описание</span><span class="sxs-lookup"><span data-stu-id="bbf3e-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="bbf3e-145">-?</span><span class="sxs-lookup"><span data-stu-id="bbf3e-145">-?</span></span>              | <span data-ttu-id="bbf3e-146">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-146">Shows help.</span></span>                                                |
| <span data-ttu-id="bbf3e-147">-H</span><span class="sxs-lookup"><span data-stu-id="bbf3e-147">-h</span></span>              | <span data-ttu-id="bbf3e-148">Отображает справку.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-148">Shows help.</span></span>                                                |
| <span data-ttu-id="bbf3e-149">-f</span><span class="sxs-lookup"><span data-stu-id="bbf3e-149">-f</span></span>              | <span data-ttu-id="bbf3e-150">Синус частоты волны в Гц.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="bbf3e-151">-l</span><span class="sxs-lookup"><span data-stu-id="bbf3e-151">-l</span></span>              | <span data-ttu-id="bbf3e-152">Задержка визуализации звука в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="bbf3e-153">-d</span><span class="sxs-lookup"><span data-stu-id="bbf3e-153">-d</span></span>              | <span data-ttu-id="bbf3e-154">Синус длительности WAV в секундах.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="bbf3e-155">-M</span><span class="sxs-lookup"><span data-stu-id="bbf3e-155">-m</span></span>              | <span data-ttu-id="bbf3e-156">Отключает использование MMCSS.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="bbf3e-157">-Console</span><span class="sxs-lookup"><span data-stu-id="bbf3e-157">-console</span></span>        | <span data-ttu-id="bbf3e-158">Использовать консольное устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="bbf3e-159">-связь</span><span class="sxs-lookup"><span data-stu-id="bbf3e-159">-communications</span></span> | <span data-ttu-id="bbf3e-160">Используйте устройство связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="bbf3e-161">— мультимедиа</span><span class="sxs-lookup"><span data-stu-id="bbf3e-161">-multimedia</span></span>     | <span data-ttu-id="bbf3e-162">Используйте устройство мультимедиа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="bbf3e-163">— Конечная точка</span><span class="sxs-lookup"><span data-stu-id="bbf3e-163">-endpoint</span></span>       | <span data-ttu-id="bbf3e-164">Используйте идентификатор конечной точки, указанный в значении переключателя.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="bbf3e-165">Если приложение запускается без аргументов, оно перечисляет доступные устройства и предлагает пользователю выбрать устройство для сеанса подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="bbf3e-166">После того как пользователь назначит устройство, оно выводит синус в 440 Гц в течение 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="bbf3e-167">Эти значения можно изменить, указав значения параметра-f и-d.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="bbf3e-168">В примере Рендерексклусививентдривен демонстрируется буферизация, управляемая событиями.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="bbf3e-169">В этом примере показано, как:</span><span class="sxs-lookup"><span data-stu-id="bbf3e-169">The sample shows how to:</span></span>

-   <span data-ttu-id="bbf3e-170">Создайте экземпляр аудио клиента, настройте его для работы в монопольном режиме и включите управляемую событиями буферизацию, установив флаг **аудклнт \_ стреамфлагс \_ вложенный EventCallback** в вызове [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="bbf3e-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="bbf3e-171">Свяжите клиент с образцами, готовыми к просмотру, предоставив обработчик событий системе, вызвав метод [**иаудиоклиент:: сетевенсандле**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="bbf3e-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="bbf3e-172">Создайте поток отрисовки для обработки образцов из обработчика аудио.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="bbf3e-173">Правильно выровняйте буферы на границе 128 байт перед их отправкой на устройство.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="bbf3e-174">Это делается путем настройки периодичности подсистемы.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="bbf3e-175">Проверьте формат Mix конечной точки устройства, чтобы определить, можно ли отобразить образцы.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="bbf3e-176">Если устройство не поддерживает формат Mix, данные преобразуются в PCM.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="bbf3e-177">Обрабатывайте переключение потоков.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-177">Handle stream switching.</span></span>

<span data-ttu-id="bbf3e-178">После начала сеанса подготовки к просмотру и запуска потока обработчик звука передает указанный обработчик событий в уведомление клиента каждый раз, когда буфер будет готов к обработке клиентом.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="bbf3e-179">Звуковые данные также могут обрабатываться в цикле, управляемом таймером.</span><span class="sxs-lookup"><span data-stu-id="bbf3e-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="bbf3e-180">Этот режим показан в примере [рендерексклусиветимердривен](renderexclusivetimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf3e-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="bbf3e-181">Дополнительные сведения о визуализации потока см. в разделе [Визуализация потока](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="bbf3e-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbf3e-182">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bbf3e-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf3e-183">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="bbf3e-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



