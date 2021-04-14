---
description: Несжатые буферы видео
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Несжатые буферы видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692773"
---
# <a name="uncompressed-video-buffers"></a>Несжатые буферы видео

В этой статье описывается работа с буферами мультимедиа, которые содержат кадры видео без сжатия. В порядке предпочтения доступны следующие параметры. Не каждый буфер мультимедиа поддерживает каждый параметр.

1.  Используйте базовую поверхность Direct3D. (Применяется только к видеокадрам, хранящимся на поверхности Direct3D.)
2.  Используйте интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
3.  Используйте интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .

## <a name="use-the-underlying-direct3d-surface"></a>Использование базовой поверхности Direct3D

Кадр видео может храниться в области Direct3D. Если это так, можно получить указатель на поверхность, вызвав [**имфжетсервице::**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) GetObject или [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) в объекте буфера мультимедиа. Используйте службу "MR buffer" идентификатора службы \_ \_ . Этот подход рекомендуется, когда компонент, обращающийся к видеокадру, предназначен для использования Direct3D. Например, этот подход следует использовать для видеодекодера, поддерживающего ускорение видео DirectX.

В следующем коде показано, как получить указатель **IDirect3DSurface9** из буфера мультимедиа.


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



Служба **\_ \_ службы буфера MR** поддерживает следующие объекты:

-   [Буфер поверхности DirectX](directx-surface-buffer.md)
-   [Образцы видео](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a>Использование интерфейса IMF2DBuffer

Если видеокадр не хранится в области Direct3D или компонент не предназначен для использования Direct3D, следующий рекомендуемый способ доступа к видеокадру — запросить буфер для интерфейса [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Этот интерфейс разработан специально для данных изображения. Чтобы получить указатель на этот интерфейс, вызовите **QueryInterface** в буфере мультимедиа. Этот интерфейс предоставляется не для всех объектов буфера мультимедиа. Но если буфер мультимедиа предоставляет интерфейс **IMF2DBuffer** , следует использовать этот интерфейс для доступа к данным, если это возможно, а не использовать [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer). Вы по-прежнему можете использовать интерфейс **имфмедиабуффер** , но это может быть менее эффективным.

1.  Вызовите **QueryInterface** в буфере мультимедиа, чтобы получить интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
2.  Вызовите [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) , чтобы получить доступ к памяти для буфера. Этот метод возвращает указатель на первый байт верхней строки пикселей. Он также возвращает шаг изображения, который представляет число байтов от начала строки пикселей до начала следующей строки. Буфер может содержать символы заполнения после каждой строки пикселей, поэтому шаг может быть шире, чем ширина изображения в байтах. Шаг также может быть отрицательным, если изображение ориентировано снизу вверх в памяти. Дополнительные сведения см. в разделе [Шаг с изображением](image-stride.md).
3.  Не Заблокируйте буфер, пока требуется доступ к памяти. Разблокируйте буфер, вызвав [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).

Не каждый буфер мультимедиа реализует интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Если буфер мультимедиа не реализует этот интерфейс (то есть объект buffer возвращает E \_ -интерфейс в шаге 1), необходимо использовать интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , описанный далее.

## <a name="use-the-imfmediabuffer-interface"></a>Использование интерфейса Имфмедиабуффер

Если буфер мультимедиа не предоставляет интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , используйте интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . Общая семантика этого интерфейса описана в разделе [Работа с буферами мультимедиа](working-with-media-buffers.md).

1.  Вызовите **QueryInterface** в буфере мультимедиа, чтобы получить интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
2.  Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) для доступа к буферной памяти. Этот метод возвращает указатель на буферную память. При использовании метода **Lock** шаг всегда является минимальным шагом для рассматриваемого видеоформата, без дополнительных байтов заполнения.
3.  Не Заблокируйте буфер, пока требуется доступ к памяти. Разблокируйте буфер, вызвав метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Следует всегда избегать вызова [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , если буфер предоставляет [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), поскольку метод **Lock** может принудительно применить объект буфера к видеокадру в смежный блок памяти, а затем снова выполнить его. С другой стороны, если буфер не поддерживает **IMF2DBuffer**, то **Имфмедиабуффер:: Lock** , скорее всего, не приведет к созданию копии.

Вычислите минимальный шаг из типа мультимедиа следующим образом:

-   Минимальный шаг может храниться в атрибуте [**\_ \_ \_ STRIDE по умолчанию MF MT**](mf-mt-default-stride-attribute.md) .
-   Если не задан атрибут **\_ \_ \_ STRIDE по умолчанию MF MT** , вызовите функцию [**мфжетстридефорбитмапинфохеадер**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) , чтобы вычислить шаг для большинства распространенных форматов видео.
-   Если функция [**мфжетстридефорбитмапинфохеадер**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) не распознает формат, необходимо вычислить шаг на основе определения формата. В этом случае общее правило отсутствует. необходимо знать сведения об определении формата.

В следующем коде показано, как получить шаг по умолчанию для наиболее распространенных форматов видео.


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



В зависимости от приложения вы можете заранее определить, поддерживает ли данный буфер мультимедиа [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (например, если вы создали буфер). В противном случае необходимо подготовиться к использованию любого из двух интерфейсов буфера.

В следующем примере показан вспомогательный класс, который скрывает некоторые из этих сведений. Этот класс имеет метод Локкбуффер, который вызывает [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) или [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) и возвращает указатель на начало первой строки пикселей. (Это поведение соответствует методу **Lock2D** .) Метод Локкбуффер принимает в качестве входного параметра шаг по умолчанию и возвращает фактический шаг в качестве выходного параметра.


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Шаг изображения](image-stride.md)
</dt> <dt>

[Буферы мультимедиа](media-buffers.md)
</dt> </dl>

 

 



