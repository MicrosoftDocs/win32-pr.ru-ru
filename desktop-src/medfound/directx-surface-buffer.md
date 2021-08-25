---
description: Буфер поверхности DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Буфер поверхности DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cff1489a644fd5c4144c8c0d923f11e5ca4555886e8defbce3b9b26a16a35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828274"
---
# <a name="directx-surface-buffer"></a>Буфер поверхности DirectX

Объект буфера поверхности DirectX — это буфер мультимедиа, который управляет поверхностью Direct3D. Чтобы создать экземпляр этого объекта, вызовите [**мфкреатедкссурфацебуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) и передайте указатель на поверхность DirectX. Буфер поверхности DirectX предоставляет следующие интерфейсы:

-   [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

Существует несколько способов доступа к памяти Surface из объекта buffer:

-   Рекомендуется: вызовите [**имфжетсервице:: WebService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) в буфере. Используйте **\_ \_ службу "Mr buffer**" идентификатора службы. Метод возвращает указатель на базовую поверхность Direct3D.
-   Вызовите [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d). Этот метод вызывает **IDirect3DSurface9:: локкрект** непосредственно на поверхности. Метод [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) вызывает **унлоккрект** на поверхности.
-   Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Как правило, это не рекомендуется, поскольку он заставляет объект копировать память из поверхности Direct3D, а затем обратно. Метод [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) более эффективен.

[**Блокировка**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) и [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) могут завершаться ошибкой, если базовая поверхность не является блокируемой. Буфер поверхности DirectX реализует эти два метода в основном для компонентов, которые не предназначены для работы с областями Direct3D.

Расширенный обработчик видео (Евр) создает буферы поверхности DirectX, если декодер не настроен для ускорения видео DirectX (ДКСВА). Дополнительные сведения см. в разделе [**имфвидеосамплеаллокатор**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).

### <a name="obtaining-the-direct3d-surface"></a>Получение поверхности Direct3D

Чтобы получить поверхность Direct3D из примера видео, выполните следующие действия.

1.  Вызовите [**имфсампле:: жетбуффербиндекс**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) со значением индекса, равным нулю.
2.  Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) и укажите идентификатор службы **\_ буфера \_ MR** .

Следующий код показывает эти действия.


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Буферы мультимедиа](media-buffers.md)
</dt> <dt>

[Образцы видео](video-samples.md)
</dt> </dl>

 

 



