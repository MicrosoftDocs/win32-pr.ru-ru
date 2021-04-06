---
description: Запись потока
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Запись потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895981"
---
# <a name="capturing-a-stream"></a><span data-ttu-id="5dd98-103">Запись потока</span><span class="sxs-lookup"><span data-stu-id="5dd98-103">Capturing a Stream</span></span>

<span data-ttu-id="5dd98-104">Клиент вызывает методы в интерфейсе [**иаудиокаптуреклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) для чтения захваченных данных из буфера конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5dd98-104">The client calls the methods in the [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface to read captured data from an endpoint buffer.</span></span> <span data-ttu-id="5dd98-105">Клиент использует буфер конечной точки с подсистемой аудио в общем режиме, а также с звуковым устройством в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="5dd98-105">The client shares the endpoint buffer with the audio engine in shared mode and with the audio device in exclusive mode.</span></span> <span data-ttu-id="5dd98-106">Чтобы запросить буфер конечной точки определенного размера, клиент вызывает метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="5dd98-106">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="5dd98-107">Чтобы получить размер выделенного буфера, который может отличаться от запрошенного размера, клиент вызывает метод [**иаудиоклиент:: жетбуфферсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="5dd98-107">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="5dd98-108">Чтобы переместить поток захваченных данных через буфер конечной точки, клиент дополнительно вызывает метод [**иаудиокаптуреклиент::-buffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) и метод [**Иаудиокаптуреклиент:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="5dd98-108">To move a stream of captured data through the endpoint buffer, the client alternately calls the [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) method and the [**IAudioCaptureClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) method.</span></span> <span data-ttu-id="5dd98-109">Клиент обращается к данным в буфере конечной точки как к ряду пакетов данных.</span><span class="sxs-lookup"><span data-stu-id="5dd98-109">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="5dd98-110">Вызов **метода** GetNext извлекает следующий пакет захваченных данных из буфера.</span><span class="sxs-lookup"><span data-stu-id="5dd98-110">The **GetBuffer** call retrieves the next packet of captured data from the buffer.</span></span> <span data-ttu-id="5dd98-111">После считывания данных из пакета клиент вызывает **релеасебуффер** , чтобы освободить пакет и сделать его доступным для более новых захваченных данных.</span><span class="sxs-lookup"><span data-stu-id="5dd98-111">After reading the data from the packet, the client calls **ReleaseBuffer** to release the packet and make it available for more captured data.</span></span>

<span data-ttu-id="5dd98-112">Размер пакета может отличаться [**от одного вызова**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) функции GetNext к следующему.</span><span class="sxs-lookup"><span data-stu-id="5dd98-112">The packet size can vary from one [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) call to the next.</span></span> <span data-ttu-id="5dd98-113">Перед **вызовом метода GetNext** клиент имеет возможность вызвать метод [**Иаудиокаптуреклиент:: жетнекстпаккетсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) , чтобы получить размер следующего пакета заранее.</span><span class="sxs-lookup"><span data-stu-id="5dd98-113">Before calling **GetBuffer**, the client has the option of calling the [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) method to get the size of the next packet in advance.</span></span> <span data-ttu-id="5dd98-114">Кроме того, клиент может вызвать метод [**иаудиоклиент:: жеткуррентпаддинг**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) , чтобы получить общий объем захваченных данных, доступных в буфере.</span><span class="sxs-lookup"><span data-stu-id="5dd98-114">In addition, the client can call the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method to get the total amount of captured data that is available in the buffer.</span></span> <span data-ttu-id="5dd98-115">В любой момент размер пакета всегда меньше или равен общему объему захваченных данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="5dd98-115">At any instant, the packet size is always less than or equal to the total amount of captured data in the buffer.</span></span>

<span data-ttu-id="5dd98-116">На каждом этапе обработки клиент может обрабатывать захваченные данные одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="5dd98-116">During each processing pass, the client has the option of processing the captured data in one of the following ways:</span></span>

-   <span data-ttu-id="5dd98-117">Клиент [**Дополнительно вызывает метод**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) [**релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)и, считывая по одному пакету каждой пары вызовов **, до тех** пор, пока метод аудкнт \_ не вернет \_ буфферемпти, что означает, что буфер пуст.</span><span class="sxs-lookup"><span data-stu-id="5dd98-117">The client alternately calls [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), reading one packet with each pair of calls, until **GetBuffer** returns AUDCNT\_S\_BUFFEREMPTY, indicating that the buffer is empty.</span></span>
-   <span data-ttu-id="5dd98-118">Клиент вызывает [**жетнекстпаккетсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) перед каждой парой вызовов к методам [**buffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) и [**релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) , пока **жетнекстпаккетсизе** сообщает размер пакета 0, что означает, что буфер пуст.</span><span class="sxs-lookup"><span data-stu-id="5dd98-118">The client calls [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) before each pair of calls to [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) until **GetNextPacketSize** reports a packet size of 0, indicating that the buffer is empty.</span></span>

<span data-ttu-id="5dd98-119">Два метода дают эквивалентные результаты.</span><span class="sxs-lookup"><span data-stu-id="5dd98-119">The two techniques yield equivalent results.</span></span>

<span data-ttu-id="5dd98-120">В следующем примере кода показано, как записать звуковой поток из устройства для записи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5dd98-120">The following code example shows how to record an audio stream from the default capture device:</span></span>


```C++
//-----------------------------------------------------------
// Record an audio stream from the default audio capture
// device. The RecordAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data from the
// capture device. The main loop runs every 1/2 second.
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
const IID IID_IAudioCaptureClient = __uuidof(IAudioCaptureClient);

HRESULT RecordAudioStream(MyAudioSink *pMySink)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioCaptureClient *pCaptureClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 packetLength = 0;
    BOOL bDone = FALSE;
    BYTE *pData;
    DWORD flags;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eCapture, eConsole, &pDevice);
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

    // Get the size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioCaptureClient,
                         (void**)&pCaptureClient);
    EXIT_ON_ERROR(hr)

    // Notify the audio sink which format to use.
    hr = pMySink->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                     bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start recording.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (bDone == FALSE)
    {
        // Sleep for half the buffer duration.
        Sleep(hnsActualDuration/REFTIMES_PER_MILLISEC/2);

        hr = pCaptureClient->GetNextPacketSize(&packetLength);
        EXIT_ON_ERROR(hr)

        while (packetLength != 0)
        {
            // Get the available data in the shared buffer.
            hr = pCaptureClient->GetBuffer(
                                   &pData,
                                   &numFramesAvailable,
                                   &flags, NULL, NULL);
            EXIT_ON_ERROR(hr)

            if (flags & AUDCLNT_BUFFERFLAGS_SILENT)
            {
                pData = NULL;  // Tell CopyData to write silence.
            }

            // Copy the available capture data to the audio sink.
            hr = pMySink->CopyData(
                              pData, numFramesAvailable, &bDone);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->ReleaseBuffer(numFramesAvailable);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->GetNextPacketSize(&packetLength);
            EXIT_ON_ERROR(hr)
        }
    }

    hr = pAudioClient->Stop();  // Stop recording.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pCaptureClient)

    return hr;
}
```



<span data-ttu-id="5dd98-121">В предыдущем примере функция Рекордаудиостреам принимает один параметр, `pMySink` который является указателем на объект, принадлежащий определяемому клиентом классу, мяудиосинк с двумя функциями, copydata и сетформат.</span><span class="sxs-lookup"><span data-stu-id="5dd98-121">In the preceding example, the RecordAudioStream function takes a single parameter, `pMySink`, which is a pointer to an object that belongs to a client-defined class, MyAudioSink, with two functions, CopyData and SetFormat.</span></span> <span data-ttu-id="5dd98-122">Пример кода не включает реализацию Мяудиосинк, поскольку:</span><span class="sxs-lookup"><span data-stu-id="5dd98-122">The example code does not include the implementation of MyAudioSink because:</span></span>

-   <span data-ttu-id="5dd98-123">Ни один из членов класса не взаимодействует напрямую с каким бы то ни было из методов в интерфейсах в ВАСАПИ.</span><span class="sxs-lookup"><span data-stu-id="5dd98-123">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="5dd98-124">Класс может быть реализован различными способами в зависимости от требований клиента.</span><span class="sxs-lookup"><span data-stu-id="5dd98-124">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="5dd98-125">(Например, он может записать данные записи в WAV-файл.)</span><span class="sxs-lookup"><span data-stu-id="5dd98-125">(For example, it might write the capture data to a WAV file.)</span></span>

<span data-ttu-id="5dd98-126">Однако сведения о работе двух методов полезны для понимания примера.</span><span class="sxs-lookup"><span data-stu-id="5dd98-126">However, information about the operation of the two methods is useful for understanding the example.</span></span>

<span data-ttu-id="5dd98-127">Функция CopyData Копирует указанное число звуковых кадров из указанного места в буфере.</span><span class="sxs-lookup"><span data-stu-id="5dd98-127">The CopyData function copies a specified number of audio frames from a specified buffer location.</span></span> <span data-ttu-id="5dd98-128">Функция Рекордаудиостреам использует функцию CopyData для чтения и сохранения звуковых данных из общего буфера.</span><span class="sxs-lookup"><span data-stu-id="5dd98-128">The RecordAudioStream function uses the CopyData function to read and save the audio data from the shared buffer.</span></span> <span data-ttu-id="5dd98-129">Функция Сетформат указывает формат функции CopyData, которая будет использоваться для данных.</span><span class="sxs-lookup"><span data-stu-id="5dd98-129">The SetFormat function specifies the format for the CopyData function to use for the data.</span></span>

<span data-ttu-id="5dd98-130">Пока для объекта Мяудиосинк требуются дополнительные данные, функция CopyData выводит значение **false** через третий параметр, который в предыдущем примере кода является указателем на переменную `bDone` .</span><span class="sxs-lookup"><span data-stu-id="5dd98-130">As long as the MyAudioSink object requires additional data, the CopyData function outputs the value **FALSE** through its third parameter, which, in the preceding code example, is a pointer to the variable `bDone`.</span></span> <span data-ttu-id="5dd98-131">Если объект Мяудиосинк содержит все необходимые данные, функция CopyData устанавливает `bDone` **значение true**, что приводит к завершению цикла в функции рекордаудиостреам.</span><span class="sxs-lookup"><span data-stu-id="5dd98-131">When the MyAudioSink object has all the data that it requires, the CopyData function sets `bDone` to **TRUE**, which causes the program to exit the loop in the RecordAudioStream function.</span></span>

<span data-ttu-id="5dd98-132">Функция Рекордаудиостреам выделяет общий буфер с длительностью в одну секунду.</span><span class="sxs-lookup"><span data-stu-id="5dd98-132">The RecordAudioStream function allocates a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="5dd98-133">(Размер выделенного буфера может немного превышать длительность.) В рамках главного цикла вызов функции [**спящего режима**](/windows/desktop/api/synchapi/nf-synchapi-sleep) Windows вызывает ожидание программы в течение половины секунды.</span><span class="sxs-lookup"><span data-stu-id="5dd98-133">(The allocated buffer might have a slightly longer duration.) Within the main loop, the call to the Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) function causes the program to wait for a half second.</span></span> <span data-ttu-id="5dd98-134">В начале каждого вызова **спящего режима** общий буфер пуст или почти пуст.</span><span class="sxs-lookup"><span data-stu-id="5dd98-134">At the start of each **Sleep** call, the shared buffer is empty or nearly empty.</span></span> <span data-ttu-id="5dd98-135">К моменту возвращения вызова **спящего режима** общий буфер составляет около половины, заполненной данными отслеживания.</span><span class="sxs-lookup"><span data-stu-id="5dd98-135">By the time the **Sleep** call returns, the shared buffer is about half filled with capture data.</span></span>

<span data-ttu-id="5dd98-136">После вызова метода [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) поток остается открытым до тех пор, пока клиент не освободит все ссылки на интерфейс [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) и все ссылки на интерфейсы служб, полученные клиентом с помощью метода [**иаудиоклиент::-Service**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="5dd98-136">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="5dd98-137">Окончательный вызов [**выпуска**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) закрывает поток.</span><span class="sxs-lookup"><span data-stu-id="5dd98-137">The final [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dd98-138">См. также</span><span class="sxs-lookup"><span data-stu-id="5dd98-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dd98-139">Управление потоками</span><span class="sxs-lookup"><span data-stu-id="5dd98-139">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
