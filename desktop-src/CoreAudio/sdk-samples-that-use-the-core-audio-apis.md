---
description: Примеры пакетов SDK, использующих основные API аудио
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Примеры пакетов SDK, использующих основные API аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990613"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a><span data-ttu-id="0b318-103">Примеры пакетов SDK, использующих основные API аудио</span><span class="sxs-lookup"><span data-stu-id="0b318-103">SDK Samples That Use the Core Audio APIs</span></span>

<span data-ttu-id="0b318-104">Windows SDK содержит следующие примеры кода, демонстрирующие использование основных API аудио.</span><span class="sxs-lookup"><span data-stu-id="0b318-104">The Windows SDK includes the following code samples that demonstrate the use of the Core Audio APIs.</span></span> <span data-ttu-id="0b318-105">Следующие примеры находятся в каталоге% Мссдк% \\ Samples \\ мультимедиа \\ Audio, где% мссдк% — это корневой каталог установки Windows SDK на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0b318-105">The following samples are located in the directory %MSSdk%\\samples\\multimedia\\audio, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b318-106">Образец</span><span class="sxs-lookup"><span data-stu-id="0b318-106">Sample</span></span></th>
<th><span data-ttu-id="0b318-107">деаскриптион</span><span class="sxs-lookup"><span data-stu-id="0b318-107">Deascription</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b318-108"><a href="aecmicarray.md">аекмикаррай</a></span><span class="sxs-lookup"><span data-stu-id="0b318-108"><a href="aecmicarray.md">AECMicArray</a></span></span></td>
<td><span data-ttu-id="0b318-109">В этом примере используются интерфейсы API Ммдевице, ВАСАПИ, Девицетопологи и Ендпоинтволуме для записи высококачественного потока голоса.</span><span class="sxs-lookup"><span data-stu-id="0b318-109">This sample uses the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="0b318-110">Пример Tне поддерживает отмену акустического эха (AEC) и обработку массивов микрофона с помощью контекста AEC DMO, также называемого DSP-модулем записи речи, предоставляемыми корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0b318-110">TThe sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO also called the Voice capture DSP provided by Microsoft .</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b318-111"><a href="capturesharedeventdriven.md">каптурешаредевентдривен</a></span><span class="sxs-lookup"><span data-stu-id="0b318-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="0b318-112">Этот пример приложения использует основные API аудио для записи звуковых данных с входного устройства, указанного пользователем, и записывает их в уникальное имя. Файл WAV в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="0b318-112">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="0b318-113">В этом примере демонстрируется буферизация, управляемая событиями.</span><span class="sxs-lookup"><span data-stu-id="0b318-113">This sample demonstrates event-driven buffering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b318-114"><a href="capturesharedtimerdriven.md">каптурешаредтимердривен</a></span><span class="sxs-lookup"><span data-stu-id="0b318-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="0b318-115">Этот пример приложения использует основные API аудио для записи звуковых данных с входного устройства, указанного пользователем, и записывает их в уникальное имя. Файл WAV в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="0b318-115">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="0b318-116">В этом примере демонстрируется буферизация, управляемая таймером.</span><span class="sxs-lookup"><span data-stu-id="0b318-116">This sample demonstrates timer-driven buffering.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b318-117"><a href="duckingcapturesample.md">дуккингкаптуресампле</a></span><span class="sxs-lookup"><span data-stu-id="0b318-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span></span></td>
<td><span data-ttu-id="0b318-118">Этот пример приложения демонстрирует открытие и закрытие потоков связи и вызов событий дуккинг, которые приложение может получить для реализации затухания потока.</span><span class="sxs-lookup"><span data-stu-id="0b318-118">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="0b318-119">Это приложение реализует чат-клиент, который использует основные API-интерфейсы для чтения звуковых данных с коммуникационного устройства и воспроизведения на выходном устройстве.</span><span class="sxs-lookup"><span data-stu-id="0b318-119">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b318-120"><a href="endpointvolume.md">ендпоинтволуме</a></span><span class="sxs-lookup"><span data-stu-id="0b318-120"><a href="endpointvolume.md">EndpointVolume</a></span></span></td>
<td><span data-ttu-id="0b318-121">Этот пример приложения использует основные API аудио для изменения объема устройства, указанного пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b318-121">This sample application uses the Core Audio APIs to change the volume of the device, specified by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b318-122"><a href="osd.md">ОПЕРАЦИОННОЙ</a></span><span class="sxs-lookup"><span data-stu-id="0b318-122"><a href="osd.md">OSD</a></span></span></td>
<td><span data-ttu-id="0b318-123">В этом примере используются API Ммдевице и Ендпоинтволуме для реализации экранного экрана, в котором показаны изменения тома в потоке вывода, который воспроизводится через устройство конечной точки рендеринга звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0b318-123">This sample uses the MMDevice and EndpointVolume APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="0b318-124">Экран отображается, когда пользователь корректирует уровень громкости в программе управления громкостью Windows Sndvol.exe и исчезает после того, как уровень тома остается неизменным в течение короткого периода.</span><span class="sxs-lookup"><span data-stu-id="0b318-124">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b318-125"><a href="renderexclusiveeventdriven.md">рендерексклусививентдривен</a></span><span class="sxs-lookup"><span data-stu-id="0b318-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span></span></td>
<td><span data-ttu-id="0b318-126">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b318-126">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="0b318-127">В этом примере демонстрируется буферизация, управляемая событиями, для клиента отрисовки в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="0b318-127">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="0b318-128">Для потока с монопольным режимом клиент использует буфер конечной точки с звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="0b318-128">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b318-129"><a href="renderexclusivetimerdriven.md">рендерексклусиветимердривен</a></span><span class="sxs-lookup"><span data-stu-id="0b318-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span></span></td>
<td><span data-ttu-id="0b318-130">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b318-130">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="0b318-131">В этом примере демонстрируется буферизация, управляемая таймером, для клиента отрисовки в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="0b318-131">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="0b318-132">Для потока с монопольным режимом клиент использует буфер конечной точки с звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="0b318-132">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b318-133"><a href="rendersharedeventdriven.md">рендершаредевентдривен</a></span><span class="sxs-lookup"><span data-stu-id="0b318-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="0b318-134">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b318-134">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="0b318-135">В этом примере демонстрируется буферизация, управляемая событиями, для клиента отрисовки в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="0b318-135">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="0b318-136">Для потока общего режима клиент совместно использует буфер конечной точки с обработчиком аудио.</span><span class="sxs-lookup"><span data-stu-id="0b318-136">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b318-137"><a href="rendersharedtimerdriven.md">рендершаредтимердривен</a></span><span class="sxs-lookup"><span data-stu-id="0b318-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="0b318-138">Этот пример приложения использует основные API аудио для отображения звуковых данных на устройстве вывода, указанном пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b318-138">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="0b318-139">В этом примере демонстрируется буферизация, управляемая таймером, для клиента отрисовки в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="0b318-139">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="0b318-140">Для потока общего режима клиент совместно использует буфер конечной точки с обработчиком аудио.</span><span class="sxs-lookup"><span data-stu-id="0b318-140">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b318-141">винаудио</span><span class="sxs-lookup"><span data-stu-id="0b318-141">WinAudio</span></span></td>
<td><span data-ttu-id="0b318-142">В этом примере используется API Ммдевице и ВАСАПИ для воспроизведения и записи звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="0b318-142">This sample uses the MMDevice API and WASAPI to play and capture audio streams.</span></span> <span data-ttu-id="0b318-143">Пользовательский интерфейс этого примера приложения позволяет пользователям выбирать устройства конечных точек аудио, изменять уровень громкости локального сеанса аудио, а также воспроизводить файлы WAV и микрофон.</span><span class="sxs-lookup"><span data-stu-id="0b318-143">The user interface of this sample application enables users to select audio endpoint devices, to change the volume level of the local audio session, and to play .wav files and microphone input.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="0b318-144">Этот пример является устаревшим в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b318-144">This sample has been deprecated in Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0b318-145">Вы можете скачать Windows SDK с веб-сайта [центра загрузки Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .</span><span class="sxs-lookup"><span data-stu-id="0b318-145">You can download the Windows SDK from the [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) website.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b318-146">См. также</span><span class="sxs-lookup"><span data-stu-id="0b318-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b318-147">Об API аудио Windows Core</span><span class="sxs-lookup"><span data-stu-id="0b318-147">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




