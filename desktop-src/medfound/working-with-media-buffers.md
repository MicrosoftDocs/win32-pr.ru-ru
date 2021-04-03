---
description: Работа с буферами мультимедиа
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Работа с буферами мультимедиа (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914163"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>Работа с буферами мультимедиа (Microsoft Media Foundation)

В этом разделе описывается использование интерфейса [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) для доступа к данным в буфере мультимедиа. Все буферы мультимедиа предоставляют **имфмедиабуффер**, предназначенный для любого типа данных. Несжатые видеоматериалы — это особый случай, описанный в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).

## <a name="buffer-size"></a>Размер буфера

С буфером мультимедиа связано два размера:

-   *Максимальная длина* — это физический размер памяти, выделенной для буфера. Это значение задается при создании буфера и не изменяется в течение времени существования буфера. Максимальная длина указывает, сколько данных может храниться в буфере. Чтобы найти максимальный размер, вызовите [**имфмедиабуффер:: @ MaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).

-   *Текущая длина* — это объем допустимых данных, которые в данный момент находятся в буфере. При первом выделении буфера Текущая длина равна нулю, так как в буфере нет допустимых данных. При записи данных в буфер необходимо обновить текущую длину, вызвав [**имфмедиабуффер:: сеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength). Например, если в буфер записывается 100 байт данных, вызовите **сеткуррентленгс** со значением 100. При чтении данных из буфера мультимедиа вызовите [**имфмедиабуффер:: жеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) , чтобы узнать, сколько данных в данный момент находится в буфере. Не читать после текущей длины. Текущая длина не может превышать максимальную длину буфера.

## <a name="accessing-the-buffer-memory"></a>Доступ к буферной памяти

Чтобы получить доступ к памяти в буфере, вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Этот метод возвращает указатель на начало блока памяти. Он также возвращает максимальную длину и текущую длину. По завершении использования указателя вызовите [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Для записи данных в буфер мультимедиа:

1.  Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , чтобы получить указатель на память. Метод также возвращает максимальную длину буфера.
2.  Запишите данные в память до максимальной длины буфера.
3.  Вызовите [**имфмедиабуффер:: сеткуррентленгс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) , чтобы обновить текущую длину. Установите текущую длину, равную объему данных, записанных на шаге 2.
4.  Вызовите метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) , чтобы разблокировать буфер.

Чтение данных из буфера мультимедиа:

1.  Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , чтобы получить указатель на память. Метод также возвращает текущую длину буфера (объем допустимых данных в буфере).
2.  Считывает содержимое памяти до текущей длины.
3.  Вызовите метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) , чтобы разблокировать буфер.

## <a name="creating-system-memory-buffers"></a>Создание буферов системной памяти

Буфер системной памяти — это буфер мультимедиа, который управляет блоком системной памяти. Чтобы создать экземпляр этого объекта, вызовите [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) или [**мфкреатеалигнедмеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) и укажите размер буфера. Обе функции выделяют блок памяти и возвращают указатель [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . Память автоматически освобождается, когда счетчик ссылок буфера мультимедиа достигает нуля и объект уничтожается.

В следующем примере показано, как создать буфер системной памяти и выполнить запись в буфер.


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Буферы мультимедиа](media-buffers.md)
</dt> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> </dl>

 

 



