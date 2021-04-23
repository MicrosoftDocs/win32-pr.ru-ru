---
description: Запись изображения из образа по-прежнему
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Запись изображения из образа по-прежнему
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805716"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a><span data-ttu-id="e899f-103">Запись изображения из образа по-прежнему</span><span class="sxs-lookup"><span data-stu-id="e899f-103">Capturing an Image From a Still Image Pin</span></span>

<span data-ttu-id="e899f-104">Некоторые камеры могут создать изображение, отделенное от потока записи, и часто изображение по-прежнему имеет более высокое качество, чем образы, созданные потоком записи.</span><span class="sxs-lookup"><span data-stu-id="e899f-104">Some cameras can produce a still image separate from the capture stream, and often the still image is of higher quality than the images produced by the capture stream.</span></span> <span data-ttu-id="e899f-105">Камера может иметь кнопку, которая выступает в качестве аппаратного триггера или может поддерживать программное активирование.</span><span class="sxs-lookup"><span data-stu-id="e899f-105">The camera may have a button that acts as a hardware trigger, or it may support software triggering.</span></span> <span data-ttu-id="e899f-106">Камера, которая поддерживает изображения по-прежнему, будет предоставлять ПИН-код изображения, который \_ по-прежнему имеет ПИН-код категории \_ .</span><span class="sxs-lookup"><span data-stu-id="e899f-106">A camera that supports still images will expose a still image pin, which is pin category PIN\_CATEGORY\_STILL.</span></span>

<span data-ttu-id="e899f-107">Чтобы получить изображения с устройства по-прежнему, рекомендуется использовать интерфейсы API для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="e899f-107">The recommended way to get still images from the device is to use the Windows Image Acquisition (WIA) APIs.</span></span> <span data-ttu-id="e899f-108">Дополнительные сведения см. в разделе "получение образа Windows" в документации по Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="e899f-108">For more information, see "Windows Image Acquisition" in the Platform SDK documentation.</span></span> <span data-ttu-id="e899f-109">Однако для записи образа можно также использовать DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e899f-109">However, you can also use DirectShow to capture an image.</span></span>

<span data-ttu-id="e899f-110">Чтобы активировать по-прежнему ПИН-код, используйте метод [**иамвидеоконтрол:: SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) при выполнении графа следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e899f-110">To trigger the still pin, use the [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) method when the graph is running, as follows:</span></span>


```C++
IAMVideoControl *pAMVidControl = NULL;

hr = pControl->Run(); // Run the graph.
if (FAILED(hr))
{
    // Handle error.
}

hr = pCap->QueryInterface(IID_IAMVideoControl, (void**)&pAMVidControl);

if (SUCCEEDED(hr))
{
    // Find the still pin.
    IPin *pPin = NULL;

    // pBuild is an ICaptureGraphBuilder2 pointer.

    hr = pBuild->FindPin(
        pCap,                  // Filter.
        PINDIR_OUTPUT,         // Look for an output pin.
        &PIN_CATEGORY_STILL,   // Pin category.
        NULL,                  // Media type (don't care).
        FALSE,                 // Pin must be unconnected.
        0,                     // Get the 0'th pin.
        &pPin                  // Receives a pointer to thepin.
        );

    if (SUCCEEDED(hr))
    {
        hr = pAMVidControl->SetMode(pPin, VideoControlFlag_Trigger);
        pPin->Release();
    }
    pAMVidControl->Release();
}
```



<span data-ttu-id="e899f-111">Запросите фильтр записи для [**иамвидеоконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span><span class="sxs-lookup"><span data-stu-id="e899f-111">Query the capture filter for [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span></span> <span data-ttu-id="e899f-112">Если интерфейс поддерживается, получите указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) с тем же ПИН-кодом, вызвав метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , как показано в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="e899f-112">If the interface is supported, get a pointer to the still pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface by calling the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method, as shown in the previous example.</span></span> <span data-ttu-id="e899f-113">Затем вызовите [**иамвидеоконтрол:: SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) с указателем **Ипин** и \_ флагом триггера видеоконтролфлаг.</span><span class="sxs-lookup"><span data-stu-id="e899f-113">Then call [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) with the **IPin** pointer and the VideoControlFlag\_Trigger flag.</span></span>

> [!Note]  
> <span data-ttu-id="e899f-114">В зависимости от камеры может потребоваться отобразить ПИН-код захвата ( \_ \_ захват категории) перед тем, как будет подключен ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="e899f-114">Depending on the camera, you might need to render the capture pin (PIN\_CATEGORY\_CAPTURE) before the still pin will connect.</span></span>

 

### <a name="example-using-the-sample-grabber-filter"></a><span data-ttu-id="e899f-115">Пример. Использование фильтра захвата образца</span><span class="sxs-lookup"><span data-stu-id="e899f-115">Example: Using the Sample Grabber Filter</span></span>

<span data-ttu-id="e899f-116">Одним из способов захвата образа является [**Пример фильтра захвата**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e899f-116">One way to capture the image is with the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="e899f-117">Образец захвата использует определяемую приложением функцию обратного вызова для обработки изображения.</span><span class="sxs-lookup"><span data-stu-id="e899f-117">The Sample Grabber uses an application-defined callback function to process the image.</span></span> <span data-ttu-id="e899f-118">Дополнительные сведения об образце фильтра захвата см. в разделе [Использование средства захвата образцов](using-the-sample-grabber.md).</span><span class="sxs-lookup"><span data-stu-id="e899f-118">For more information about the Sample Grabber filter, see [Using the Sample Grabber](using-the-sample-grabber.md).</span></span>

<span data-ttu-id="e899f-119">В следующем примере предполагается, что по-прежнему ПИН-код доставляет несжатое изображение RGB.</span><span class="sxs-lookup"><span data-stu-id="e899f-119">The following example assumes that the still pin delivers an uncompressed RGB image.</span></span> <span data-ttu-id="e899f-120">Сначала определите класс, который будет реализовывать интерфейс обратного вызова примера средства захвата, [**исамплеграбберкб**](isamplegrabbercb.md):</span><span class="sxs-lookup"><span data-stu-id="e899f-120">First, define a class that will implement the Sample Grabber's callback interface, [**ISampleGrabberCB**](isamplegrabbercb.md):</span></span>


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



<span data-ttu-id="e899f-121">Реализация класса описана в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="e899f-121">The implementation of the class is described shortly.</span></span>

<span data-ttu-id="e899f-122">Затем подключите закрепление к образцу модуля захвата и подключите образец захвата к фильтру модуля [**подготовки отчетов NULL**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e899f-122">Next, connect the still pin to the Sample Grabber, and connect the Sample Grabber to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span> <span data-ttu-id="e899f-123">Модуль подготовки отчетов со значением NULL просто отклоняет получаемые примеры мультимедиа. Фактическая работа будет выполнена в обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="e899f-123">The Null Renderer simply discards media samples that it receives; the actual work will be done within the callback.</span></span> <span data-ttu-id="e899f-124">(Единственная причина для модуля подготовки к отображению NULL заключается в том, чтобы подключить закрепление образца захвата к чему-либо.) Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания образца средства захвата и фильтров визуализации NULL и вызовите [**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить оба фильтра в граф:</span><span class="sxs-lookup"><span data-stu-id="e899f-124">(The only reason for the Null Renderer is to connect the Sample Grabber's output pin to something.) Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Sample Grabber and Null Renderer filters, and call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add both filters to the graph:</span></span>


```C++
// Add the Sample Grabber filter to the graph.
IBaseFilter *pSG_Filter;
hr = CoCreateInstance(
    CLSID_SampleGrabber, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pSG_Filter
    );

hr = pGraph->AddFilter(pSG_Filter, L"SampleGrab");

// Add the Null Renderer filter to the graph.
IBaseFilter *pNull;

hr = CoCreateInstance(
    CLSID_NullRenderer, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pNull
    );

hr = pGraph->AddFilter(pNull, L"NullRender");
```



<span data-ttu-id="e899f-125">Вы можете использовать метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) для подключения всех трех фильтров в одном вызове метода, перейдя по прежнему на закрепление к образцу, а также из образца захвата в модуль подготовки к просмотру со значением NULL:</span><span class="sxs-lookup"><span data-stu-id="e899f-125">You can use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect all three filters in one method call, going from the still pin to the Sample Grabber, and from the Sample Grabber to the Null Renderer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



<span data-ttu-id="e899f-126">Теперь используйте интерфейс [**исамплеграббер**](isamplegrabber.md) , чтобы настроить образец области захвата таким образом, чтобы он замещает образцы в буфер:</span><span class="sxs-lookup"><span data-stu-id="e899f-126">Now use the [**ISampleGrabber**](isamplegrabber.md) interface to configure the Sample Grabber so that it buffers samples:</span></span>


```C++
// Configure the Sample Grabber.
ISampleGrabber *pSG = NULL;

hr = pSG_Filter->QueryInterface(IID_ISampleGrabber, (void**)&pSG);
if (SUCCEEDED(hr))
{
    hr = pSG->SetOneShot(FALSE);
    hr = pSG->SetBufferSamples(TRUE);

    ...
```



<span data-ttu-id="e899f-127">Задайте интерфейс обратного вызова с указателем на объект обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="e899f-127">Set the callback interface with a pointer to your callback object:</span></span>


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



<span data-ttu-id="e899f-128">Получите тип носителя, который по-прежнему используется для подключения с помощью образца средства захвата:</span><span class="sxs-lookup"><span data-stu-id="e899f-128">Get the media type that the still pin used to connect with the Sample Grabber:</span></span>


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



<span data-ttu-id="e899f-129">Этот тип мультимедиа будет содержать структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , определяющую формат изображения по прежнему.</span><span class="sxs-lookup"><span data-stu-id="e899f-129">This media type will contain the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the format of the still image.</span></span> <span data-ttu-id="e899f-130">Освободите тип мультимедиа перед выходом из приложения:</span><span class="sxs-lookup"><span data-stu-id="e899f-130">Free the media type before the application exits:</span></span>


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



<span data-ttu-id="e899f-131">Ниже приведен пример класса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e899f-131">What follows is an example of the callback class.</span></span> <span data-ttu-id="e899f-132">Обратите внимание, что класс реализует **IUnknown**, который он наследует через интерфейс [**исамплеграббер**](isamplegrabber.md) , но не сохраняет счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="e899f-132">Note that the class implements **IUnknown**, which it inherits through the [**ISampleGrabber**](isamplegrabber.md) interface, but it does not keep a reference count.</span></span> <span data-ttu-id="e899f-133">Это является надежным, поскольку приложение создает объект в стеке, и объект остается в области действия на протяжении всего времени существования графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="e899f-133">This is safe because the application creates the object on the stack, and the object remains in scope throughout the lifetime of the filter graph.</span></span>

<span data-ttu-id="e899f-134">Вся работа выполняется в методе [**буфферкб**](isamplegrabbercb-buffercb.md) , который вызывается примером захвата, когда он получает новый пример.</span><span class="sxs-lookup"><span data-stu-id="e899f-134">All of the work happens in the [**BufferCB**](isamplegrabbercb-buffercb.md) method, which is called by the Sample Grabber whenever it gets a new sample.</span></span> <span data-ttu-id="e899f-135">В следующем примере метод записывает точечный рисунок в файл:</span><span class="sxs-lookup"><span data-stu-id="e899f-135">In the following example, the method writes the bitmap to a file:</span></span>


```C++
class SampleGrabberCallback : public ISampleGrabberCB
{
public:
    // Fake referance counting.
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 2; }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject) return E_POINTER;
        if (riid == __uuidof(IUnknown))
        {
            *ppvObject = static_cast<IUnknown*>(this);
             return S_OK;
        }
        if (riid == __uuidof(ISampleGrabberCB))
        {
            *ppvObject = static_cast<ISampleGrabberCB*>(this);
             return S_OK;
        }
        return E_NOTIMPL;
    }

    STDMETHODIMP SampleCB(double Time, IMediaSample *pSample)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP BufferCB(double Time, BYTE *pBuffer, long BufferLen)
    {
        if ((g_StillMediaType.majortype != MEDIATYPE_Video) ||
            (g_StillMediaType.formattype != FORMAT_VideoInfo) ||
            (g_StillMediaType.cbFormat < sizeof(VIDEOINFOHEADER)) ||
            (g_StillMediaType.pbFormat == NULL))
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
        HANDLE hf = CreateFile("C:\\Example.bmp", GENERIC_WRITE, 
        FILE_SHARE_WRITE, NULL, CREATE_ALWAYS, 0, NULL);
        if (hf == INVALID_HANDLE_VALUE)
        {
            return E_FAIL;
        }
        long cbBitmapInfoSize = g_StillMediaType.cbFormat - SIZE_PREHEADER;
        VIDEOINFOHEADER *pVideoHeader =
           (VIDEOINFOHEADER*)g_StillMediaType.pbFormat;

        BITMAPFILEHEADER bfh;
        ZeroMemory(&bfh, sizeof(bfh));
        bfh.bfType = 'MB';  // Little-endian for "BM".
        bfh.bfSize = sizeof( bfh ) + BufferLen + cbBitmapInfoSize;
        bfh.bfOffBits = sizeof( BITMAPFILEHEADER ) + cbBitmapInfoSize;
        
        // Write the file header.
        DWORD dwWritten = 0;
        WriteFile( hf, &bfh, sizeof( bfh ), &dwWritten, NULL );
        WriteFile(hf, HEADER(pVideoHeader), cbBitmapInfoSize, &dwWritten, NULL);        
        WriteFile( hf, pBuffer, BufferLen, &dwWritten, NULL );
        CloseHandle( hf );
        return S_OK;

    }
};
```



## <a name="related-topics"></a><span data-ttu-id="e899f-136">См. также</span><span class="sxs-lookup"><span data-stu-id="e899f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e899f-137">Задачи записи видео</span><span class="sxs-lookup"><span data-stu-id="e899f-137">Video Capture Tasks</span></span>](video-capture-tasks.md)
</dt> </dl>

 

 
