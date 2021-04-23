---
description: Отрисовка потока
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Отрисовка потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96e720bab43c75b0a3958bb3b6137d3a3d9ef6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496362"
---
# <a name="rendering-a-stream"></a><span data-ttu-id="e7c34-103">Отрисовка потока</span><span class="sxs-lookup"><span data-stu-id="e7c34-103">Rendering a Stream</span></span>

<span data-ttu-id="e7c34-104">Клиент вызывает методы в интерфейсе [**иаудиорендерклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) для записи данных отрисовки в буфер конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e7c34-104">The client calls the methods in the [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) interface to write rendering data to an endpoint buffer.</span></span> <span data-ttu-id="e7c34-105">Для потока общего режима клиент совместно использует буфер конечной точки с обработчиком аудио.</span><span class="sxs-lookup"><span data-stu-id="e7c34-105">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span> <span data-ttu-id="e7c34-106">Для потока с монопольным режимом клиент использует буфер конечной точки с звуковым устройством.</span><span class="sxs-lookup"><span data-stu-id="e7c34-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span> <span data-ttu-id="e7c34-107">Чтобы запросить буфер конечной точки определенного размера, клиент вызывает метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="e7c34-107">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="e7c34-108">Чтобы получить размер выделенного буфера, который может отличаться от запрошенного размера, клиент вызывает метод [**иаудиоклиент:: жетбуфферсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="e7c34-108">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="e7c34-109">Чтобы переместить поток данных отрисовки через буфер конечной точки, клиент дополнительно вызывает метод [**иаудиорендерклиент::-buffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) и метод [**Иаудиорендерклиент:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="e7c34-109">To move a stream of rendering data through the endpoint buffer, the client alternately calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method and the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method.</span></span> <span data-ttu-id="e7c34-110">Клиент обращается к данным в буфере конечной точки как к ряду пакетов данных.</span><span class="sxs-lookup"><span data-stu-id="e7c34-110">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="e7c34-111">Вызов **метода** GetNext извлекает следующий пакет, чтобы клиент мог заполнить его данными отрисовки.</span><span class="sxs-lookup"><span data-stu-id="e7c34-111">The **GetBuffer** call retrieves the next packet so that the client can fill it with rendering data.</span></span> <span data-ttu-id="e7c34-112">После записи данных в пакет клиент вызывает **релеасебуффер** , чтобы добавить завершенный пакет в очередь отрисовки.</span><span class="sxs-lookup"><span data-stu-id="e7c34-112">After writing the data to the packet, the client calls **ReleaseBuffer** to add the completed packet to the rendering queue.</span></span>

<span data-ttu-id="e7c34-113">Для буфера отрисовки значение заполнения, сообщаемое методом [**иаудиоклиент:: жеткуррентпаддинг**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) , представляет объем данных отрисовки, поставленных в очередь для воспроизведения в буфере.</span><span class="sxs-lookup"><span data-stu-id="e7c34-113">For a rendering buffer, the padding value that is reported by the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method represents the amount of rendering data that is queued up to play in the buffer.</span></span> <span data-ttu-id="e7c34-114">Приложение отрисовки может использовать значение заполнения, чтобы определить, сколько новых данных оно может безопасно записывать в буфер без риска перезаписи ранее записанных данных, которые обработчик аудиозаписей еще не прочитал из буфера.</span><span class="sxs-lookup"><span data-stu-id="e7c34-114">A rendering application can use the padding value to determine how much new data it can safely write to the buffer without the risk of overwriting previously written data that the audio engine has not yet read from the buffer.</span></span> <span data-ttu-id="e7c34-115">Доступное пространство — это просто размер буфера, за вычетом размера заполнения.</span><span class="sxs-lookup"><span data-stu-id="e7c34-115">The available space is simply the buffer size minus the padding size.</span></span> <span data-ttu-id="e7c34-116">Клиент может запросить размер пакета, представляющий некоторое или все доступное пространство в [**следующем вызове**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) метода GetNext.</span><span class="sxs-lookup"><span data-stu-id="e7c34-116">The client can request a packet size that represents some or all of this available space in its next [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) call.</span></span>

<span data-ttu-id="e7c34-117">Размер пакета выражается в *звуковых кадрах*.</span><span class="sxs-lookup"><span data-stu-id="e7c34-117">The size of a packet is expressed in *audio frames*.</span></span> <span data-ttu-id="e7c34-118">Звуковая рамка в потоке PCM — это набор образцов (набор содержит один выбор для каждого канала в потоке), которые воспроизводят или записываются в одно и то же время (такт часов).</span><span class="sxs-lookup"><span data-stu-id="e7c34-118">An audio frame in a PCM stream is a set of samples (the set contains one sample for each channel in the stream) that play or are recorded at the same time (clock tick).</span></span> <span data-ttu-id="e7c34-119">Таким же размером, размер звукового фрейма — это размер выборки, умноженный на число каналов в потоке.</span><span class="sxs-lookup"><span data-stu-id="e7c34-119">Thus, the size of an audio frame is the sample size multiplied by the number of channels in the stream.</span></span> <span data-ttu-id="e7c34-120">Например, размер кадра для стерео (2-канального) потока с 16-разрядными примерами составляет четыре байта.</span><span class="sxs-lookup"><span data-stu-id="e7c34-120">For example, the frame size for a stereo (2-channel) stream with 16-bit samples is four bytes.</span></span>

<span data-ttu-id="e7c34-121">В следующем примере кода показано, как воспроизвести аудиопоток на устройстве отрисовки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7c34-121">The following code example shows how to play an audio stream on the default rendering device:</span></span>


```C++
//-----------------------------------------------------------
// Play an audio stream on the default audio rendering
// device. The PlayAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data to the
// rendering device. The inner loop runs every 1/2 second.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayAudioStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    UINT32 numFramesPadding;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetMixFormat(&pwfx);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_SHARED,
                         0,
                         hnsRequestedDuration,
                         0,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Get the actual size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // Grab the entire buffer for the initial fill operation.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    // Load the initial data into the shared buffer.
    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                        bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Sleep for half the buffer duration.
        Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

        // See how much buffer space is available.
        hr = pAudioClient->GetCurrentPadding(&numFramesPadding);
        EXIT_ON_ERROR(hr)

        numFramesAvailable = bufferFrameCount - numFramesPadding;

        // Grab all the available space in the shared buffer.
        hr = pRenderClient->GetBuffer(numFramesAvailable, &pData);
        EXIT_ON_ERROR(hr)

        // Get next 1/2-second of data from the audio source.
        hr = pMySource->LoadData(numFramesAvailable, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(numFramesAvailable, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for last data in buffer to play before stopping.
    Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="e7c34-122">В предыдущем примере функция Плайаудиостреам принимает один параметр, `pMySource` который является указателем на объект, принадлежащий определяемому клиентом классу, мяудиосаурце с двумя функциями-членами, LoadData и сетформат.</span><span class="sxs-lookup"><span data-stu-id="e7c34-122">In the preceding example, the PlayAudioStream function takes a single parameter, `pMySource`, which is a pointer to an object that belongs to a client-defined class, MyAudioSource, with two member functions, LoadData and SetFormat.</span></span> <span data-ttu-id="e7c34-123">Пример кода не включает реализацию Мяудиосаурце, поскольку:</span><span class="sxs-lookup"><span data-stu-id="e7c34-123">The example code does not include the implementation of MyAudioSource because:</span></span>

-   <span data-ttu-id="e7c34-124">Ни один из членов класса не взаимодействует напрямую с каким бы то ни было из методов в интерфейсах в ВАСАПИ.</span><span class="sxs-lookup"><span data-stu-id="e7c34-124">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="e7c34-125">Класс может быть реализован различными способами в зависимости от требований клиента.</span><span class="sxs-lookup"><span data-stu-id="e7c34-125">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="e7c34-126">(Например, он может считывать данные отрисовки из WAV-файла и выполнять оперативное преобразование в формат потока.)</span><span class="sxs-lookup"><span data-stu-id="e7c34-126">(For example, it might read the rendering data from a WAV file and perform on-the-fly conversion to the stream format.)</span></span>

<span data-ttu-id="e7c34-127">Однако некоторые сведения о работе двух функций полезны для понимания примера.</span><span class="sxs-lookup"><span data-stu-id="e7c34-127">However, some information about the operation of the two functions is useful for understanding the example.</span></span>

<span data-ttu-id="e7c34-128">Функция LoadData записывает указанное число звуковых кадров (первый параметр) в указанное место в буфере (второй параметр).</span><span class="sxs-lookup"><span data-stu-id="e7c34-128">The LoadData function writes a specified number of audio frames (first parameter) to a specified buffer location (second parameter).</span></span> <span data-ttu-id="e7c34-129">(Размер звукового кадра — это число каналов в потоке, умноженное на размер выборки.) Функция Плайаудиостреам использует LoadData для заполнения частей общего буфера с помощью звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="e7c34-129">(The size of an audio frame is the number of channels in the stream multiplied by the sample size.) The PlayAudioStream function uses LoadData to fill portions of the shared buffer with audio data.</span></span> <span data-ttu-id="e7c34-130">Функция Сетформат указывает формат функции LoadData, которая будет использоваться для данных.</span><span class="sxs-lookup"><span data-stu-id="e7c34-130">The SetFormat function specifies the format for the LoadData function to use for the data.</span></span> <span data-ttu-id="e7c34-131">Если функция LoadData может записать по меньшей мере один кадр в указанное место в буфере, но закончит работу с данными до того, как записал указанное число кадров, он записывает тишину в оставшиеся кадры.</span><span class="sxs-lookup"><span data-stu-id="e7c34-131">If the LoadData function is able to write at least one frame to the specified buffer location but runs out of data before it has written the specified number of frames, then it writes silence to the remaining frames.</span></span>

<span data-ttu-id="e7c34-132">Пока LoadData проходит по крайней мере один кадр реальных данных (а не тишины) в указанное место в буфере, он выводит 0 через третий параметр, который в предыдущем примере кода является указателем вывода на `flags` переменную.</span><span class="sxs-lookup"><span data-stu-id="e7c34-132">As long as LoadData succeeds in writing at least one frame of real data (not silence) to the specified buffer location, it outputs 0 through its third parameter, which, in the preceding code example, is an output pointer to the `flags` variable.</span></span> <span data-ttu-id="e7c34-133">Если LoadData находится за пределами данных и не может записывать даже один кадр в указанное место в буфере, он ничего не записывает в буфер (а не тишину) и записывает значение АУДКЛНТ \_ буфферфлагс \_ Silent в `flags` переменную.</span><span class="sxs-lookup"><span data-stu-id="e7c34-133">When LoadData is out of data and cannot write even a single frame to the specified buffer location, it writes nothing to the buffer (not even silence), and it writes the value AUDCLNT\_BUFFERFLAGS\_SILENT to the `flags` variable.</span></span> <span data-ttu-id="e7c34-134">`flags`Переменная передает это значение методу [**иаудиорендерклиент:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , который отвечает, заполняя указанное число кадров в буфере тишиной.</span><span class="sxs-lookup"><span data-stu-id="e7c34-134">The `flags` variable conveys this value to the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method, which responds by filling the specified number of frames in the buffer with silence.</span></span>

<span data-ttu-id="e7c34-135">При вызове метода [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) функция плайаудиостреам в предыдущем примере запрашивает общий буфер с длительностью в одну секунду.</span><span class="sxs-lookup"><span data-stu-id="e7c34-135">In its call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the PlayAudioStream function in the preceding example requests a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="e7c34-136">(Размер выделенного буфера может немного превышать длительность.) В своих первоначальных вызовах методов [**иаудиорендерклиент::**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) Иаудиорендерклиент и [**:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) функция заполняет весь буфер до вызова метода [**иаудиоклиент:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) , чтобы начать воспроизведение буфера.</span><span class="sxs-lookup"><span data-stu-id="e7c34-136">(The allocated buffer might have a slightly longer duration.) In its initial calls to the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) and [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) methods, the function fills the entire buffer before calling the [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) method to begin playing the buffer.</span></span>

<span data-ttu-id="e7c34-137">В рамках главного цикла функция последовательно заполняет половину буфера с интервалами в половину секунды.</span><span class="sxs-lookup"><span data-stu-id="e7c34-137">Within the main loop, the function iteratively fills half of the buffer at half-second intervals.</span></span> <span data-ttu-id="e7c34-138">Непосредственно перед каждым вызовом функции [**спящего режима**](/windows/win32/api/synchapi/nf-synchapi-sleep) Windows в главном цикле буфер заполнен или почти заполнен.</span><span class="sxs-lookup"><span data-stu-id="e7c34-138">Just before each call to the Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function in the main loop, the buffer is full or nearly full.</span></span> <span data-ttu-id="e7c34-139">При возвращении вызова **спящего режима** буфер находится около половины места.</span><span class="sxs-lookup"><span data-stu-id="e7c34-139">When the **Sleep** call returns, the buffer is about half full.</span></span> <span data-ttu-id="e7c34-140">Цикл завершается после последнего вызова функции LoadData, в результате чего переменной присваивается `flags` значение аудклнт \_ буфферфлагс \_ Silent.</span><span class="sxs-lookup"><span data-stu-id="e7c34-140">The loop ends after the final call to the LoadData function sets the `flags` variable to the value AUDCLNT\_BUFFERFLAGS\_SILENT.</span></span> <span data-ttu-id="e7c34-141">На этом этапе в буфере содержится по крайней мере один кадр реальных данных, и он может содержать до половины секунды реальных данных.</span><span class="sxs-lookup"><span data-stu-id="e7c34-141">At that point, the buffer contains at least one frame of real data, and it might contain as much as a half second of real data.</span></span> <span data-ttu-id="e7c34-142">Оставшаяся часть буфера содержит тишину.</span><span class="sxs-lookup"><span data-stu-id="e7c34-142">The remainder of the buffer contains silence.</span></span> <span data-ttu-id="e7c34-143">Вызов **спящего режима** , следующий за циклом, предоставляет достаточно времени (половина секунды) для воспроизведения всех оставшихся данных.</span><span class="sxs-lookup"><span data-stu-id="e7c34-143">The **Sleep** call that follows the loop provides sufficient time (a half second) to play all of the remaining data.</span></span> <span data-ttu-id="e7c34-144">Тишина, следующая за данными, предотвращает нежелательные звуки перед вызовом метода [**иаудиоклиент:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) , который останавливает аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="e7c34-144">The silence that follows the data prevents unwanted sounds before the call to the [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) method stops the audio stream.</span></span> <span data-ttu-id="e7c34-145">Дополнительные сведения о **спящем режиме** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e7c34-145">For more information about **Sleep**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="e7c34-146">После вызова метода [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) поток остается открытым до тех пор, пока клиент не освободит все ссылки на интерфейс [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) и все ссылки на интерфейсы служб, полученные клиентом с помощью метода [**иаудиоклиент::-Service**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="e7c34-146">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="e7c34-147">Окончательный вызов [**выпуска**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) закрывает поток.</span><span class="sxs-lookup"><span data-stu-id="e7c34-147">The final [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

<span data-ttu-id="e7c34-148">Функция Плайаудиостреам в предыдущем примере кода вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать перечислитель для устройств конечных точек аудио в системе.</span><span class="sxs-lookup"><span data-stu-id="e7c34-148">The PlayAudioStream function in the preceding code example calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="e7c34-149">Если вызывающая программа ранее не вызывала функцию **CoCreateInstance** или [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM, вызов **CoCreateInstance** завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e7c34-149">Unless the calling program previously called either the **CoCreateInstance** or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="e7c34-150">Дополнительные сведения о **CoCreateInstance**, **CoCreateInstance** и **CoInitializeEx** см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e7c34-150">For more information about **CoCreateInstance**, **CoCreateInstance**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7c34-151">См. также</span><span class="sxs-lookup"><span data-stu-id="e7c34-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7c34-152">Управление потоками</span><span class="sxs-lookup"><span data-stu-id="e7c34-152">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
