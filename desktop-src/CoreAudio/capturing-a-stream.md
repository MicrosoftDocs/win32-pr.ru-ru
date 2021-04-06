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
# <a name="capturing-a-stream"></a>Запись потока

Клиент вызывает методы в интерфейсе [**иаудиокаптуреклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) для чтения захваченных данных из буфера конечной точки. Клиент использует буфер конечной точки с подсистемой аудио в общем режиме, а также с звуковым устройством в монопольном режиме. Чтобы запросить буфер конечной точки определенного размера, клиент вызывает метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Чтобы получить размер выделенного буфера, который может отличаться от запрошенного размера, клиент вызывает метод [**иаудиоклиент:: жетбуфферсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Чтобы переместить поток захваченных данных через буфер конечной точки, клиент дополнительно вызывает метод [**иаудиокаптуреклиент::-buffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) и метод [**Иаудиокаптуреклиент:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) . Клиент обращается к данным в буфере конечной точки как к ряду пакетов данных. Вызов **метода** GetNext извлекает следующий пакет захваченных данных из буфера. После считывания данных из пакета клиент вызывает **релеасебуффер** , чтобы освободить пакет и сделать его доступным для более новых захваченных данных.

Размер пакета может отличаться [**от одного вызова**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) функции GetNext к следующему. Перед **вызовом метода GetNext** клиент имеет возможность вызвать метод [**Иаудиокаптуреклиент:: жетнекстпаккетсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) , чтобы получить размер следующего пакета заранее. Кроме того, клиент может вызвать метод [**иаудиоклиент:: жеткуррентпаддинг**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) , чтобы получить общий объем захваченных данных, доступных в буфере. В любой момент размер пакета всегда меньше или равен общему объему захваченных данных в буфере.

На каждом этапе обработки клиент может обрабатывать захваченные данные одним из следующих способов:

-   Клиент [**Дополнительно вызывает метод**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) [**релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)и, считывая по одному пакету каждой пары вызовов **, до тех** пор, пока метод аудкнт \_ не вернет \_ буфферемпти, что означает, что буфер пуст.
-   Клиент вызывает [**жетнекстпаккетсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) перед каждой парой вызовов к методам [**buffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) и [**релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) , пока **жетнекстпаккетсизе** сообщает размер пакета 0, что означает, что буфер пуст.

Два метода дают эквивалентные результаты.

В следующем примере кода показано, как записать звуковой поток из устройства для записи по умолчанию.


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



В предыдущем примере функция Рекордаудиостреам принимает один параметр, `pMySink` который является указателем на объект, принадлежащий определяемому клиентом классу, мяудиосинк с двумя функциями, copydata и сетформат. Пример кода не включает реализацию Мяудиосинк, поскольку:

-   Ни один из членов класса не взаимодействует напрямую с каким бы то ни было из методов в интерфейсах в ВАСАПИ.
-   Класс может быть реализован различными способами в зависимости от требований клиента. (Например, он может записать данные записи в WAV-файл.)

Однако сведения о работе двух методов полезны для понимания примера.

Функция CopyData Копирует указанное число звуковых кадров из указанного места в буфере. Функция Рекордаудиостреам использует функцию CopyData для чтения и сохранения звуковых данных из общего буфера. Функция Сетформат указывает формат функции CopyData, которая будет использоваться для данных.

Пока для объекта Мяудиосинк требуются дополнительные данные, функция CopyData выводит значение **false** через третий параметр, который в предыдущем примере кода является указателем на переменную `bDone` . Если объект Мяудиосинк содержит все необходимые данные, функция CopyData устанавливает `bDone` **значение true**, что приводит к завершению цикла в функции рекордаудиостреам.

Функция Рекордаудиостреам выделяет общий буфер с длительностью в одну секунду. (Размер выделенного буфера может немного превышать длительность.) В рамках главного цикла вызов функции [**спящего режима**](/windows/desktop/api/synchapi/nf-synchapi-sleep) Windows вызывает ожидание программы в течение половины секунды. В начале каждого вызова **спящего режима** общий буфер пуст или почти пуст. К моменту возвращения вызова **спящего режима** общий буфер составляет около половины, заполненной данными отслеживания.

После вызова метода [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) поток остается открытым до тех пор, пока клиент не освободит все ссылки на интерфейс [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) и все ссылки на интерфейсы служб, полученные клиентом с помощью метода [**иаудиоклиент::-Service**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . Окончательный вызов [**выпуска**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) закрывает поток.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление потоками](stream-management.md)
</dt> </dl>

 

 
