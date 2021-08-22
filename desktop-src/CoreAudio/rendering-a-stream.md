---
description: Отрисовка потока
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Отрисовка потока
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a49632e89e42e4e353cec48ee993f990904bc4557c0f63fcaec4d13bed5becf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318574"
---
# <a name="rendering-a-stream"></a>Отрисовка потока

Клиент вызывает методы в интерфейсе [**иаудиорендерклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) для записи данных отрисовки в буфер конечной точки. Для потока общего режима клиент совместно использует буфер конечной точки с обработчиком аудио. Для потока с монопольным режимом клиент использует буфер конечной точки с звуковым устройством. Чтобы запросить буфер конечной точки определенного размера, клиент вызывает метод [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Чтобы получить размер выделенного буфера, который может отличаться от запрошенного размера, клиент вызывает метод [**иаудиоклиент:: жетбуфферсизе**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Чтобы переместить поток данных отрисовки через буфер конечной точки, клиент дополнительно вызывает метод [**иаудиорендерклиент::-buffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) и метод [**Иаудиорендерклиент:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) . Клиент обращается к данным в буфере конечной точки как к ряду пакетов данных. Вызов **метода** GetNext извлекает следующий пакет, чтобы клиент мог заполнить его данными отрисовки. После записи данных в пакет клиент вызывает **релеасебуффер** , чтобы добавить завершенный пакет в очередь отрисовки.

Для буфера отрисовки значение заполнения, сообщаемое методом [**иаудиоклиент:: жеткуррентпаддинг**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) , представляет объем данных отрисовки, поставленных в очередь для воспроизведения в буфере. Приложение отрисовки может использовать значение заполнения, чтобы определить, сколько новых данных оно может безопасно записывать в буфер без риска перезаписи ранее записанных данных, которые обработчик аудиозаписей еще не прочитал из буфера. Доступное пространство — это просто размер буфера, за вычетом размера заполнения. Клиент может запросить размер пакета, представляющий некоторое или все доступное пространство в [**следующем вызове**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) метода GetNext.

Размер пакета выражается в *звуковых кадрах*. Звуковая рамка в потоке PCM — это набор образцов (набор содержит один выбор для каждого канала в потоке), которые воспроизводят или записываются в одно и то же время (такт часов). Таким же размером, размер звукового фрейма — это размер выборки, умноженный на число каналов в потоке. Например, размер кадра для стерео (2-канального) потока с 16-разрядными примерами составляет четыре байта.

В следующем примере кода показано, как воспроизвести аудиопоток на устройстве отрисовки по умолчанию.


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



В предыдущем примере функция Плайаудиостреам принимает один параметр, `pMySource` который является указателем на объект, принадлежащий определяемому клиентом классу, мяудиосаурце с двумя функциями-членами, LoadData и сетформат. Пример кода не включает реализацию Мяудиосаурце, поскольку:

-   Ни один из членов класса не взаимодействует напрямую с каким бы то ни было из методов в интерфейсах в ВАСАПИ.
-   Класс может быть реализован различными способами в зависимости от требований клиента. (Например, он может считывать данные отрисовки из WAV-файла и выполнять оперативное преобразование в формат потока.)

Однако некоторые сведения о работе двух функций полезны для понимания примера.

Функция LoadData записывает указанное число звуковых кадров (первый параметр) в указанное место в буфере (второй параметр). (Размер звукового кадра — это число каналов в потоке, умноженное на размер выборки.) Функция Плайаудиостреам использует LoadData для заполнения частей общего буфера с помощью звуковых данных. Функция Сетформат указывает формат функции LoadData, которая будет использоваться для данных. Если функция LoadData может записать по меньшей мере один кадр в указанное место в буфере, но закончит работу с данными до того, как записал указанное число кадров, он записывает тишину в оставшиеся кадры.

Пока LoadData проходит по крайней мере один кадр реальных данных (а не тишины) в указанное место в буфере, он выводит 0 через третий параметр, который в предыдущем примере кода является указателем вывода на `flags` переменную. Если LoadData находится за пределами данных и не может записывать даже один кадр в указанное место в буфере, он ничего не записывает в буфер (а не тишину) и записывает значение АУДКЛНТ \_ буфферфлагс \_ Silent в `flags` переменную. `flags`Переменная передает это значение методу [**иаудиорендерклиент:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , который отвечает, заполняя указанное число кадров в буфере тишиной.

При вызове метода [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) функция плайаудиостреам в предыдущем примере запрашивает общий буфер с длительностью в одну секунду. (Размер выделенного буфера может немного превышать длительность.) В своих первоначальных вызовах методов [**иаудиорендерклиент::**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) Иаудиорендерклиент и [**:: релеасебуффер**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) функция заполняет весь буфер до вызова метода [**иаудиоклиент:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) , чтобы начать воспроизведение буфера.

В рамках главного цикла функция последовательно заполняет половину буфера с интервалами в половину секунды. непосредственно перед каждым вызовом функции Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) в главном цикле буфер заполнен или почти заполнен. При возвращении вызова **спящего режима** буфер находится около половины места. Цикл завершается после последнего вызова функции LoadData, в результате чего переменной присваивается `flags` значение аудклнт \_ буфферфлагс \_ Silent. На этом этапе в буфере содержится по крайней мере один кадр реальных данных, и он может содержать до половины секунды реальных данных. Оставшаяся часть буфера содержит тишину. Вызов **спящего режима** , следующий за циклом, предоставляет достаточно времени (половина секунды) для воспроизведения всех оставшихся данных. Тишина, следующая за данными, предотвращает нежелательные звуки перед вызовом метода [**иаудиоклиент:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) , который останавливает аудиопоток. дополнительные сведения о **спящем режиме** см. в документации по Windows SDK.

После вызова метода [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) поток остается открытым до тех пор, пока клиент не освободит все ссылки на интерфейс [**иаудиоклиент**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) и все ссылки на интерфейсы служб, полученные клиентом с помощью метода [**иаудиоклиент::-Service**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . Окончательный вызов [**выпуска**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) закрывает поток.

Функция Плайаудиостреам в предыдущем примере кода вызывает функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать перечислитель для устройств конечных точек аудио в системе. Если вызывающая программа ранее не вызывала функцию **CoCreateInstance** или [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM, вызов **CoCreateInstance** завершится ошибкой. дополнительные сведения о **cocreateinstance**, **cocreateinstance** и **CoInitializeEx** см. в документации по Windows SDK.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Управление потоками](stream-management.md)
</dt> </dl>

 

 
