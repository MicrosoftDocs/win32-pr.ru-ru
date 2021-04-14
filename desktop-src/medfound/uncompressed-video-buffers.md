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
# <a name="uncompressed-video-buffers"></a><span data-ttu-id="979e3-103">Несжатые буферы видео</span><span class="sxs-lookup"><span data-stu-id="979e3-103">Uncompressed Video Buffers</span></span>

<span data-ttu-id="979e3-104">В этой статье описывается работа с буферами мультимедиа, которые содержат кадры видео без сжатия.</span><span class="sxs-lookup"><span data-stu-id="979e3-104">This article describes how to work with media buffers that contain uncompressed video frames.</span></span> <span data-ttu-id="979e3-105">В порядке предпочтения доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="979e3-105">In order of preference, the following options are available.</span></span> <span data-ttu-id="979e3-106">Не каждый буфер мультимедиа поддерживает каждый параметр.</span><span class="sxs-lookup"><span data-stu-id="979e3-106">Not every media buffer supports each option.</span></span>

1.  <span data-ttu-id="979e3-107">Используйте базовую поверхность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="979e3-107">Use the underlying Direct3D surface.</span></span> <span data-ttu-id="979e3-108">(Применяется только к видеокадрам, хранящимся на поверхности Direct3D.)</span><span class="sxs-lookup"><span data-stu-id="979e3-108">(Applies only to video frames stored in Direct3D surfaces.)</span></span>
2.  <span data-ttu-id="979e3-109">Используйте интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="979e3-109">Use the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
3.  <span data-ttu-id="979e3-110">Используйте интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="979e3-110">Use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

## <a name="use-the-underlying-direct3d-surface"></a><span data-ttu-id="979e3-111">Использование базовой поверхности Direct3D</span><span class="sxs-lookup"><span data-stu-id="979e3-111">Use the Underlying Direct3D Surface</span></span>

<span data-ttu-id="979e3-112">Кадр видео может храниться в области Direct3D.</span><span class="sxs-lookup"><span data-stu-id="979e3-112">The video frame might be stored inside a Direct3D surface.</span></span> <span data-ttu-id="979e3-113">Если это так, можно получить указатель на поверхность, вызвав [**имфжетсервице::**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) GetObject или [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) в объекте буфера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="979e3-113">If so, you can get a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) or [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media buffer object.</span></span> <span data-ttu-id="979e3-114">Используйте службу "MR buffer" идентификатора службы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="979e3-114">Use the service identifier MR\_BUFFER\_SERVICE.</span></span> <span data-ttu-id="979e3-115">Этот подход рекомендуется, когда компонент, обращающийся к видеокадру, предназначен для использования Direct3D.</span><span class="sxs-lookup"><span data-stu-id="979e3-115">This approach is recommended when the component accessing the video frame is designed to use Direct3D.</span></span> <span data-ttu-id="979e3-116">Например, этот подход следует использовать для видеодекодера, поддерживающего ускорение видео DirectX.</span><span class="sxs-lookup"><span data-stu-id="979e3-116">For example, a video decoder that supports DirectX Video Acceleration should use this approach.</span></span>

<span data-ttu-id="979e3-117">В следующем коде показано, как получить указатель **IDirect3DSurface9** из буфера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="979e3-117">The following code shows how to get the **IDirect3DSurface9** pointer from a media buffer.</span></span>


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



<span data-ttu-id="979e3-118">Служба **\_ \_ службы буфера MR** поддерживает следующие объекты:</span><span class="sxs-lookup"><span data-stu-id="979e3-118">The following objects support the **MR\_BUFFER\_SERVICE** service:</span></span>

-   [<span data-ttu-id="979e3-119">Буфер поверхности DirectX</span><span class="sxs-lookup"><span data-stu-id="979e3-119">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)
-   [<span data-ttu-id="979e3-120">Образцы видео</span><span class="sxs-lookup"><span data-stu-id="979e3-120">Video Samples</span></span>](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a><span data-ttu-id="979e3-121">Использование интерфейса IMF2DBuffer</span><span class="sxs-lookup"><span data-stu-id="979e3-121">Use the IMF2DBuffer Interface</span></span>

<span data-ttu-id="979e3-122">Если видеокадр не хранится в области Direct3D или компонент не предназначен для использования Direct3D, следующий рекомендуемый способ доступа к видеокадру — запросить буфер для интерфейса [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="979e3-122">If the video frame is not stored inside a Direct3D surface, or the component is not designed to use Direct3D, the next recommended way to access the video frame is to query the buffer for the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="979e3-123">Этот интерфейс разработан специально для данных изображения.</span><span class="sxs-lookup"><span data-stu-id="979e3-123">This interface is designed specifically for image data.</span></span> <span data-ttu-id="979e3-124">Чтобы получить указатель на этот интерфейс, вызовите **QueryInterface** в буфере мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="979e3-124">To get a pointer to this interface, call **QueryInterface** on the media buffer.</span></span> <span data-ttu-id="979e3-125">Этот интерфейс предоставляется не для всех объектов буфера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="979e3-125">Not all media buffer objects expose this interface.</span></span> <span data-ttu-id="979e3-126">Но если буфер мультимедиа предоставляет интерфейс **IMF2DBuffer** , следует использовать этот интерфейс для доступа к данным, если это возможно, а не использовать [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span><span class="sxs-lookup"><span data-stu-id="979e3-126">But if a media buffer does expose the **IMF2DBuffer** interface, you should use that interface to access the data, if possible, rather than using [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span></span> <span data-ttu-id="979e3-127">Вы по-прежнему можете использовать интерфейс **имфмедиабуффер** , но это может быть менее эффективным.</span><span class="sxs-lookup"><span data-stu-id="979e3-127">You can still use the **IMFMediaBuffer** interface, but it might be less efficient.</span></span>

1.  <span data-ttu-id="979e3-128">Вызовите **QueryInterface** в буфере мультимедиа, чтобы получить интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="979e3-128">Call **QueryInterface** on the media buffer to get the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
2.  <span data-ttu-id="979e3-129">Вызовите [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) , чтобы получить доступ к памяти для буфера.</span><span class="sxs-lookup"><span data-stu-id="979e3-129">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) to access the memory for the buffer.</span></span> <span data-ttu-id="979e3-130">Этот метод возвращает указатель на первый байт верхней строки пикселей.</span><span class="sxs-lookup"><span data-stu-id="979e3-130">This method returns a pointer to the first byte of the top row of pixels.</span></span> <span data-ttu-id="979e3-131">Он также возвращает шаг изображения, который представляет число байтов от начала строки пикселей до начала следующей строки.</span><span class="sxs-lookup"><span data-stu-id="979e3-131">It also returns the image stride, which is the number of bytes from the start of a row of pixels to the start of the next row.</span></span> <span data-ttu-id="979e3-132">Буфер может содержать символы заполнения после каждой строки пикселей, поэтому шаг может быть шире, чем ширина изображения в байтах.</span><span class="sxs-lookup"><span data-stu-id="979e3-132">The buffer might contain padding bytes after each row of pixels, so the stride might be wider than the image width in bytes.</span></span> <span data-ttu-id="979e3-133">Шаг также может быть отрицательным, если изображение ориентировано снизу вверх в памяти.</span><span class="sxs-lookup"><span data-stu-id="979e3-133">Stride can also be negative if the image is oriented bottom-up in memory.</span></span> <span data-ttu-id="979e3-134">Дополнительные сведения см. в разделе [Шаг с изображением](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="979e3-134">For more information, see [Image Stride](image-stride.md).</span></span>
3.  <span data-ttu-id="979e3-135">Не Заблокируйте буфер, пока требуется доступ к памяти.</span><span class="sxs-lookup"><span data-stu-id="979e3-135">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="979e3-136">Разблокируйте буфер, вызвав [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span><span class="sxs-lookup"><span data-stu-id="979e3-136">Unlock the buffer by calling [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span></span>

<span data-ttu-id="979e3-137">Не каждый буфер мультимедиа реализует интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="979e3-137">Not every media buffer implements the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="979e3-138">Если буфер мультимедиа не реализует этот интерфейс (то есть объект buffer возвращает E \_ -интерфейс в шаге 1), необходимо использовать интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , описанный далее.</span><span class="sxs-lookup"><span data-stu-id="979e3-138">If the media buffer does not implement this interface (that is, the buffer object returns E\_NOINTERFACE in step 1), you must use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface interface, described next.</span></span>

## <a name="use-the-imfmediabuffer-interface"></a><span data-ttu-id="979e3-139">Использование интерфейса Имфмедиабуффер</span><span class="sxs-lookup"><span data-stu-id="979e3-139">Use the IMFMediaBuffer Interface</span></span>

<span data-ttu-id="979e3-140">Если буфер мультимедиа не предоставляет интерфейс [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , используйте интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="979e3-140">If a media buffer does not expose the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="979e3-141">Общая семантика этого интерфейса описана в разделе [Работа с буферами мультимедиа](working-with-media-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="979e3-141">The general semantics of this interface are described in the topic [Working with Media Buffers](working-with-media-buffers.md).</span></span>

1.  <span data-ttu-id="979e3-142">Вызовите **QueryInterface** в буфере мультимедиа, чтобы получить интерфейс [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="979e3-142">Call **QueryInterface** on the media buffer to get the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>
2.  <span data-ttu-id="979e3-143">Вызовите [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) для доступа к буферной памяти.</span><span class="sxs-lookup"><span data-stu-id="979e3-143">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to access the buffer memory.</span></span> <span data-ttu-id="979e3-144">Этот метод возвращает указатель на буферную память.</span><span class="sxs-lookup"><span data-stu-id="979e3-144">This method returns a pointer to the buffer memory.</span></span> <span data-ttu-id="979e3-145">При использовании метода **Lock** шаг всегда является минимальным шагом для рассматриваемого видеоформата, без дополнительных байтов заполнения.</span><span class="sxs-lookup"><span data-stu-id="979e3-145">When the **Lock** method is used, the stride is always the minimum stride for the video format in question, with no extra padding bytes.</span></span>
3.  <span data-ttu-id="979e3-146">Не Заблокируйте буфер, пока требуется доступ к памяти.</span><span class="sxs-lookup"><span data-stu-id="979e3-146">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="979e3-147">Разблокируйте буфер, вызвав метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span><span class="sxs-lookup"><span data-stu-id="979e3-147">Unlock the buffer by calling [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="979e3-148">Следует всегда избегать вызова [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , если буфер предоставляет [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), поскольку метод **Lock** может принудительно применить объект буфера к видеокадру в смежный блок памяти, а затем снова выполнить его.</span><span class="sxs-lookup"><span data-stu-id="979e3-148">You should always avoid calling [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) if the buffer exposes [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), because the **Lock** method can force the buffer object to the video frame into a contiguous memory block and then back again.</span></span> <span data-ttu-id="979e3-149">С другой стороны, если буфер не поддерживает **IMF2DBuffer**, то **Имфмедиабуффер:: Lock** , скорее всего, не приведет к созданию копии.</span><span class="sxs-lookup"><span data-stu-id="979e3-149">On the other hand, if the buffer does not support **IMF2DBuffer**, then **IMFMediaBuffer::Lock** will probably not result in a copy.</span></span>

<span data-ttu-id="979e3-150">Вычислите минимальный шаг из типа мультимедиа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="979e3-150">Calculate the minimum stride from the media type as follows:</span></span>

-   <span data-ttu-id="979e3-151">Минимальный шаг может храниться в атрибуте [**\_ \_ \_ STRIDE по умолчанию MF MT**](mf-mt-default-stride-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="979e3-151">The minimum stride might be stored in the [**MF\_MT\_DEFAULT\_STRIDE**](mf-mt-default-stride-attribute.md) attribute.</span></span>
-   <span data-ttu-id="979e3-152">Если не задан атрибут **\_ \_ \_ STRIDE по умолчанию MF MT** , вызовите функцию [**мфжетстридефорбитмапинфохеадер**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) , чтобы вычислить шаг для большинства распространенных форматов видео.</span><span class="sxs-lookup"><span data-stu-id="979e3-152">If the **MF\_MT\_DEFAULT\_STRIDE** attribute is not set, call the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function to calculate the stride for most common video formats.</span></span>
-   <span data-ttu-id="979e3-153">Если функция [**мфжетстридефорбитмапинфохеадер**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) не распознает формат, необходимо вычислить шаг на основе определения формата.</span><span class="sxs-lookup"><span data-stu-id="979e3-153">If the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function does not recognize the format, you must calculate the stride based on the definition of the format.</span></span> <span data-ttu-id="979e3-154">В этом случае общее правило отсутствует. необходимо знать сведения об определении формата.</span><span class="sxs-lookup"><span data-stu-id="979e3-154">In that case, there is no general rule; you need to know the details of the format definition.</span></span>

<span data-ttu-id="979e3-155">В следующем коде показано, как получить шаг по умолчанию для наиболее распространенных форматов видео.</span><span class="sxs-lookup"><span data-stu-id="979e3-155">The following code shows how to get the default stride for the most common video formats.</span></span>


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



<span data-ttu-id="979e3-156">В зависимости от приложения вы можете заранее определить, поддерживает ли данный буфер мультимедиа [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (например, если вы создали буфер).</span><span class="sxs-lookup"><span data-stu-id="979e3-156">Depending on your application, you might know in advance whether a given media buffer supports [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (for example, if you created the buffer).</span></span> <span data-ttu-id="979e3-157">В противном случае необходимо подготовиться к использованию любого из двух интерфейсов буфера.</span><span class="sxs-lookup"><span data-stu-id="979e3-157">Otherwise, you must be prepared to use either of the two buffer interfaces.</span></span>

<span data-ttu-id="979e3-158">В следующем примере показан вспомогательный класс, который скрывает некоторые из этих сведений.</span><span class="sxs-lookup"><span data-stu-id="979e3-158">The following example shows a helper class that hides some of these details.</span></span> <span data-ttu-id="979e3-159">Этот класс имеет метод Локкбуффер, который вызывает [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) или [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) и возвращает указатель на начало первой строки пикселей.</span><span class="sxs-lookup"><span data-stu-id="979e3-159">This class has a LockBuffer method that calls either [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) or [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and returns a pointer to the start of the first row of pixels.</span></span> <span data-ttu-id="979e3-160">(Это поведение соответствует методу **Lock2D** .) Метод Локкбуффер принимает в качестве входного параметра шаг по умолчанию и возвращает фактический шаг в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="979e3-160">(This behavior matches the **Lock2D** method.) The LockBuffer method takes the default stride as an input parameter and returns the actual stride as an output parameter.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="979e3-161">См. также</span><span class="sxs-lookup"><span data-stu-id="979e3-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="979e3-162">Шаг изображения</span><span class="sxs-lookup"><span data-stu-id="979e3-162">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="979e3-163">Буферы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="979e3-163">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



