---
description: В этом примере используются основные API аудио для записи высококачественного голосового потока. Образец поддерживает отмену акустического эха (AEC) и обработку массива микрофона с помощью контекста AEC DMO, также называемого модулем создания данных о речи (DSP), предоставляемых корпорацией Майкрософт.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: аекмикаррай
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142793"
---
# <a name="aecmicarray"></a><span data-ttu-id="67235-104">аекмикаррай</span><span class="sxs-lookup"><span data-stu-id="67235-104">AECMicArray</span></span>

<span data-ttu-id="67235-105">В этом примере используются основные API аудио для записи высококачественного голосового потока.</span><span class="sxs-lookup"><span data-stu-id="67235-105">This sample uses the Core Audio APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="67235-106">Образец поддерживает отмену акустического эха (AEC) и обработку массива микрофона с помощью контекста AEC DMO, также называемого модулем создания данных о речи (DSP), предоставляемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="67235-106">The sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO, also called the Voice capture DSP, provided by Microsoft .</span></span>

<span data-ttu-id="67235-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="67235-107">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="67235-108">Описание</span><span class="sxs-lookup"><span data-stu-id="67235-108">Description</span></span>](#description)
-   [<span data-ttu-id="67235-109">Требования</span><span class="sxs-lookup"><span data-stu-id="67235-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="67235-110">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="67235-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="67235-111">Создание примера</span><span class="sxs-lookup"><span data-stu-id="67235-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="67235-112">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="67235-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="67235-113">См. также</span><span class="sxs-lookup"><span data-stu-id="67235-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="67235-114">Описание</span><span class="sxs-lookup"><span data-stu-id="67235-114">Description</span></span>

<span data-ttu-id="67235-115">В этом образце демонстрируются следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="67235-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="67235-116">[Ммдевице](mmdevice-api.md) для перечисления устройств мультимедиа и выбора.</span><span class="sxs-lookup"><span data-stu-id="67235-116">[MMDevice](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="67235-117">[Васапи](wasapi.md) для операций управления потоком, таких как запуск и остановка потока, переключение потоков.</span><span class="sxs-lookup"><span data-stu-id="67235-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, stream switching.</span></span>
-   <span data-ttu-id="67235-118">[Девицетопологи](devicetopology-api.md) для перечисления звуковых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="67235-118">[DeviceTopology](devicetopology-api.md) for enumerating audio adapters.</span></span>
-   <span data-ttu-id="67235-119">[Ендпоинтволуме](endpointvolume-api.md) управляет уровнями громкости [звуковых сеансов](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="67235-119">[EndpointVolume](endpointvolume-api.md) control the volume levels of [audio sessions](audio-sessions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67235-120">Требования</span><span class="sxs-lookup"><span data-stu-id="67235-120">Requirements</span></span>



| <span data-ttu-id="67235-121">Продукт</span><span class="sxs-lookup"><span data-stu-id="67235-121">Product</span></span>                                                        | <span data-ttu-id="67235-122">Version</span><span class="sxs-lookup"><span data-stu-id="67235-122">Version</span></span>                     |
|----------------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="67235-123">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="67235-123">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="67235-124">Windows Vista или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="67235-124">Windows Vista or later</span></span>      |
| <span data-ttu-id="67235-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67235-125">Visual Studio</span></span>                                                  | <span data-ttu-id="67235-126">2005 (не выпуски Express)</span><span class="sxs-lookup"><span data-stu-id="67235-126">2005 (non-express editions)</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="67235-127">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="67235-127">Downloading the Sample</span></span>

<span data-ttu-id="67235-128">Этот образец доступен в следующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="67235-128">This sample is available in the following locations.</span></span>



| <span data-ttu-id="67235-129">Расположение</span><span class="sxs-lookup"><span data-stu-id="67235-129">Location</span></span>    | <span data-ttu-id="67235-130">Путь или URL-адрес</span><span class="sxs-lookup"><span data-stu-id="67235-130">Path/URL</span></span>                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67235-131">Пакет Windows SDK</span><span class="sxs-lookup"><span data-stu-id="67235-131">Windows SDK</span></span> | <span data-ttu-id="67235-132">\\Program Files \\ Microsoft SDK \\ Windows \\ v \\ 7.0 Samples \\ мультимедиа \\ Audio \\ аекмикаррай \\ ...</span><span class="sxs-lookup"><span data-stu-id="67235-132">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\AECMicArray\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="67235-133">Построение образца</span><span class="sxs-lookup"><span data-stu-id="67235-133">Building the Sample</span></span>

<span data-ttu-id="67235-134">Чтобы создать пример Аексдкдемо, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="67235-134">To build the AecSDKDemo sample, use the following steps:</span></span>

1.  <span data-ttu-id="67235-135">Откройте окно командной строки пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="67235-135">Open an SDK command window.</span></span>
2.  <span data-ttu-id="67235-136">Введите **компакт-диск% мссдк% \\ Setup**.</span><span class="sxs-lookup"><span data-stu-id="67235-136">Type **cd %MSSDK%\\Setup**.</span></span>
3.  <span data-ttu-id="67235-137">Запустите VCIntegrate.exe.</span><span class="sxs-lookup"><span data-stu-id="67235-137">Run VCIntegrate.exe.</span></span>

    <span data-ttu-id="67235-138">С этого момента командные окна будут иметь правильные параметры среды для создания приложения, которое использует преимущества пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="67235-138">From this point forward, command windows will have the proper environment settings to build an application that takes advantage of the SDK.</span></span>

4.  <span data-ttu-id="67235-139">Выполните сборку примера.</span><span class="sxs-lookup"><span data-stu-id="67235-139">Build the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="67235-140">Запуск примера</span><span class="sxs-lookup"><span data-stu-id="67235-140">Running the Sample</span></span>

<span data-ttu-id="67235-141">Если построение демонстрационного приложения выполнено успешно, создается исполняемый файл AecSDKDemo.exe.</span><span class="sxs-lookup"><span data-stu-id="67235-141">If you build the demo application successfully, an executable file, AecSDKDemo.exe is generated.</span></span> <span data-ttu-id="67235-142">Чтобы запустить его, введите `AecSDKDemo` в командном окне, а затем обязательные или необязательные аргументы, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="67235-142">To run it, type `AecSDKDemo` in a command window followed by required or optional arguments as described below.</span></span>

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

<span data-ttu-id="67235-143">В следующей таблице показаны аргументы.</span><span class="sxs-lookup"><span data-stu-id="67235-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="67235-144">Аргумент</span><span class="sxs-lookup"><span data-stu-id="67235-144">Argument</span></span>  | <span data-ttu-id="67235-145">Описание</span><span class="sxs-lookup"><span data-stu-id="67235-145">Description</span></span>                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67235-146">-out</span><span class="sxs-lookup"><span data-stu-id="67235-146">-out</span></span>      | <span data-ttu-id="67235-147">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="67235-147">Required.</span></span> <span data-ttu-id="67235-148">Указывает имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="67235-148">Specifies output file name.</span></span>                                                                                                 |
| <span data-ttu-id="67235-149">-Mod</span><span class="sxs-lookup"><span data-stu-id="67235-149">-mod</span></span>      | <span data-ttu-id="67235-150">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="67235-150">Required.</span></span> <span data-ttu-id="67235-151">Указывает режим системы записи голоса.</span><span class="sxs-lookup"><span data-stu-id="67235-151">Specifies voice capture system mode.</span></span> <span data-ttu-id="67235-152">Дополнительные сведения см. в подразделе "Настройка DMO для записи голоса" в образце файла readme.</span><span class="sxs-lookup"><span data-stu-id="67235-152">Refer to "Configuring the voice capture DMO" section in the sample readme for details.</span></span> |
| <span data-ttu-id="67235-153">-достижением</span><span class="sxs-lookup"><span data-stu-id="67235-153">-feat</span></span>     | <span data-ttu-id="67235-154">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="67235-154">Optional.</span></span> <span data-ttu-id="67235-155">Включает режим компонента (1) или выключен (0).</span><span class="sxs-lookup"><span data-stu-id="67235-155">Turns feature mode on (1) or off (0).</span></span>                                                                                       |
| <span data-ttu-id="67235-156">— NS</span><span class="sxs-lookup"><span data-stu-id="67235-156">-ns</span></span>       | <span data-ttu-id="67235-157">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="67235-157">Optional.</span></span> <span data-ttu-id="67235-158">Включение подавления шума в (1) или выключено (0).</span><span class="sxs-lookup"><span data-stu-id="67235-158">Turns noise suppression on (1) or off (0).</span></span> <span data-ttu-id="67235-159">Для указания этого параметра должен быть включен режим компонента.</span><span class="sxs-lookup"><span data-stu-id="67235-159">Feature mode must be on for specifying this.</span></span>                                     |
| <span data-ttu-id="67235-160">-АГК</span><span class="sxs-lookup"><span data-stu-id="67235-160">-agc</span></span>      | <span data-ttu-id="67235-161">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="67235-161">Optional.</span></span> <span data-ttu-id="67235-162">Включает цифровую АГК (1) или OFF (0).</span><span class="sxs-lookup"><span data-stu-id="67235-162">Turns digital AGC on (1) or off (0).</span></span> <span data-ttu-id="67235-163">Для указания этого параметра должен быть включен режим компонента.</span><span class="sxs-lookup"><span data-stu-id="67235-163">Feature mode must be on for specifying this.</span></span>                                           |
| <span data-ttu-id="67235-164">-кнтрклип</span><span class="sxs-lookup"><span data-stu-id="67235-164">-cntrclip</span></span> | <span data-ttu-id="67235-165">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="67235-165">Optional.</span></span> <span data-ttu-id="67235-166">Выключает вырезание по центру (1) или выключено (0).</span><span class="sxs-lookup"><span data-stu-id="67235-166">Turns center clipping on (1) or off (0).</span></span> <span data-ttu-id="67235-167">Для указания этого параметра должен быть включен режим компонента.</span><span class="sxs-lookup"><span data-stu-id="67235-167">Feature mode must be on for specifying this.</span></span>                                       |
| <span data-ttu-id="67235-168">-спкдев</span><span class="sxs-lookup"><span data-stu-id="67235-168">-spkdev</span></span>   | <span data-ttu-id="67235-169">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="67235-169">Optional.</span></span> <span data-ttu-id="67235-170">Указывает индекс устройства динамика.</span><span class="sxs-lookup"><span data-stu-id="67235-170">Specifies speaker device index.</span></span> <span data-ttu-id="67235-171">Если не указано, пользователю будет предложено выбрать.</span><span class="sxs-lookup"><span data-stu-id="67235-171">If not specified, the user will be asked to select.</span></span>                                         |
| <span data-ttu-id="67235-172">-микдев</span><span class="sxs-lookup"><span data-stu-id="67235-172">-micdev</span></span>   | <span data-ttu-id="67235-173">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="67235-173">Optional.</span></span> <span data-ttu-id="67235-174">Указывает индекс устройства для микрофона.</span><span class="sxs-lookup"><span data-stu-id="67235-174">Specifies microphone device index.</span></span> <span data-ttu-id="67235-175">Если не указано, пользователю будет предложено выбрать.</span><span class="sxs-lookup"><span data-stu-id="67235-175">If not specified, the user will be asked to select.</span></span>                                      |
| <span data-ttu-id="67235-176">— Длительность</span><span class="sxs-lookup"><span data-stu-id="67235-176">-duration</span></span> | <span data-ttu-id="67235-177">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="67235-177">Optional.</span></span> <span data-ttu-id="67235-178">Указывает, как долго выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="67235-178">Specifies how long the application runs.</span></span>                                                                                    |



 

<span data-ttu-id="67235-179">Этот пример приложения не воспроизводит сигналы.</span><span class="sxs-lookup"><span data-stu-id="67235-179">This sample application does not play any signals.</span></span> <span data-ttu-id="67235-180">Чтобы правильно запустить демонстрацию для режимов с поддержкой AEC (Mode 0 и 4), пользователи должны воспроизводить некоторые звуковые сигналы через то же устройство динамика, которое указано для DMO (то есть устройство, указанное параметром "-спкдев"), которое имитирует дальнее действие в двустороннем сценарии.</span><span class="sxs-lookup"><span data-stu-id="67235-180">To run the demo properly for AEC enabled modes (mode 0 and 4), users must play some audio signals through the same speaker device specified for the DMO (that is, the device specified by the "-spkdev" option), which simulates the far-end voice in a two-way chatting scenario.</span></span> <span data-ttu-id="67235-181">Пользователи могут использовать любой игрок для воспроизведения звуковых сигналов.</span><span class="sxs-lookup"><span data-stu-id="67235-181">Users can use any player to play any audio signals.</span></span> <span data-ttu-id="67235-182">Если на выбранном устройстве динамика нет активного потока отрисовки, то DMO не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="67235-182">If there is no active render stream on the selected speaker device, the DMO will fail to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67235-183">См. также</span><span class="sxs-lookup"><span data-stu-id="67235-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67235-184">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="67235-184">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



