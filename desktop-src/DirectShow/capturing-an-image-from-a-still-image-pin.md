---
description: Запись изображения из образа по-прежнему
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Запись изображения из образа по-прежнему
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab750fb6b847bc39d28c8906df8dcb982278f7a4447bfc3d79631ee58eb574e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158666"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>Запись изображения из образа по-прежнему

Некоторые камеры могут создать изображение, отделенное от потока записи, и часто изображение по-прежнему имеет более высокое качество, чем образы, созданные потоком записи. Камера может иметь кнопку, которая выступает в качестве аппаратного триггера или может поддерживать программное активирование. Камера, которая поддерживает изображения по-прежнему, будет предоставлять ПИН-код изображения, который \_ по-прежнему имеет ПИН-код категории \_ .

для получения изображений с устройства по-прежнему рекомендуется использовать интерфейсы api Windowsного получения изображений (WIA). дополнительные сведения см. в разделе «получение образа Windows» в документации по пакету Platform SDK. однако для записи образа можно также использовать DirectShow.

Чтобы активировать по-прежнему ПИН-код, используйте метод [**иамвидеоконтрол:: SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) при выполнении графа следующим образом:


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



Запросите фильтр записи для [**иамвидеоконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol). Если интерфейс поддерживается, получите указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) с тем же ПИН-кодом, вызвав метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , как показано в предыдущем примере. Затем вызовите [**иамвидеоконтрол:: SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) с указателем **Ипин** и \_ флагом триггера видеоконтролфлаг.

> [!Note]  
> В зависимости от камеры может потребоваться отобразить ПИН-код захвата ( \_ \_ захват категории) перед тем, как будет подключен ПИН-код.

 

### <a name="example-using-the-sample-grabber-filter"></a>Пример. Использование фильтра захвата образца

Одним из способов захвата образа является [**Пример фильтра захвата**](sample-grabber-filter.md) . Образец захвата использует определяемую приложением функцию обратного вызова для обработки изображения. Дополнительные сведения об образце фильтра захвата см. в разделе [Использование средства захвата образцов](using-the-sample-grabber.md).

В следующем примере предполагается, что по-прежнему ПИН-код доставляет несжатое изображение RGB. Сначала определите класс, который будет реализовывать интерфейс обратного вызова примера средства захвата, [**исамплеграбберкб**](isamplegrabbercb.md):


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



Реализация класса описана в ближайшее время.

Затем подключите закрепление к образцу модуля захвата и подключите образец захвата к фильтру модуля [**подготовки отчетов NULL**](null-renderer-filter.md) . Модуль подготовки отчетов со значением NULL просто отклоняет получаемые примеры мультимедиа. Фактическая работа будет выполнена в обратном вызове. (Единственная причина для модуля подготовки к отображению NULL заключается в том, чтобы подключить закрепление образца захвата к чему-либо.) Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания образца средства захвата и фильтров визуализации NULL и вызовите [**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить оба фильтра в граф:


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



Вы можете использовать метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) для подключения всех трех фильтров в одном вызове метода, перейдя по прежнему на закрепление к образцу, а также из образца захвата в модуль подготовки к просмотру со значением NULL:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



Теперь используйте интерфейс [**исамплеграббер**](isamplegrabber.md) , чтобы настроить образец области захвата таким образом, чтобы он замещает образцы в буфер:


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



Задайте интерфейс обратного вызова с указателем на объект обратного вызова:


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



Получите тип носителя, который по-прежнему используется для подключения с помощью образца средства захвата:


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



Этот тип мультимедиа будет содержать структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , определяющую формат изображения по прежнему. Освободите тип мультимедиа перед выходом из приложения:


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



Ниже приведен пример класса обратного вызова. Обратите внимание, что класс реализует **IUnknown**, который он наследует через интерфейс [**исамплеграббер**](isamplegrabber.md) , но не сохраняет счетчик ссылок. Это является надежным, поскольку приложение создает объект в стеке, и объект остается в области действия на протяжении всего времени существования графа фильтра.

Вся работа выполняется в методе [**буфферкб**](isamplegrabbercb-buffercb.md) , который вызывается примером захвата, когда он получает новый пример. В следующем примере метод записывает точечный рисунок в файл:


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Задачи записи видео](video-capture-tasks.md)
</dt> </dl>

 

 
