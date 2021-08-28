---
description: Использование сопоставителя источников
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Использование сопоставителя источников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81265f2edeb573ccdfb2b4ea8f2664d08f9bca8a2170459c9c53890ecd3b52cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887151"
---
# <a name="using-the-source-resolver"></a>Использование сопоставителя источников

Средство выбора источника принимает URL-адрес или поток байтов и создает соответствующий источник мультимедиа для этого контента. Чтобы создать сопоставитель источника, вызовите [**мфкреатесаурцересолвер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver). Эта функция возвращает указатель на интерфейс [**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .

Сопоставитель источников имеет как синхронные, так и асинхронные методы. Если вы используете сопоставитель источника из основного потока приложения, асинхронные методы приводят к более быстрому реагированию пользовательского интерфейса. Синхронные методы могут блокироваться в течение длительного времени, особенно если сопоставитель источника должен открыть сетевой ресурс.

Синхронные методы:

-   [**Имфсаурцересолвер:: Креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [**Имфсаурцересолвер:: Креатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

Асинхронные методы:

-   [**Имфсаурцересолвер:: Бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [**Имфсаурцересолвер:: Бегинкреатеобжектфромбитестреам**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

Для асинхронных методов каждый метод имеет соответствующий **End...** метод для завершения асинхронного запроса и метод **Cancel...** для отмены ожидающего запроса. Дополнительные сведения о асинхронных методах в Media Foundation см. в разделе [асинхронные методы обратного вызова](asynchronous-callback-methods.md).

В следующем примере кода создается источник мультимедиа на основе URL-адреса. В этом примере используется синхронный метод.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сопоставитель источников](source-resolver.md)
</dt> </dl>

 

 



