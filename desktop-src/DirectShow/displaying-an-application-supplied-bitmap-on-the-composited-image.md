---
title: Отображение точечного рисунка, предоставляемого приложением, на составном изображении
description: Отображение точечного рисунка Application-Supplied на составном изображении
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536584"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a><span data-ttu-id="40f6d-103">Отображение точечного рисунка, предоставляемого приложением, на составном изображении</span><span class="sxs-lookup"><span data-stu-id="40f6d-103">Display an app-supplied bitmap on the composited image</span></span>

<span data-ttu-id="40f6d-104">Приложения могут использовать режим смешения VMR для показа логотипов каналов альфа-смешения, пользовательского интерфейса или рекламы частично или полностью в пределах прямоугольника видео.</span><span class="sxs-lookup"><span data-stu-id="40f6d-104">Applications can use the VMR's mixing mode to display alpha-blended channel logos, a user interface, or advertisements either partially or completely within the video rectangle.</span></span> <span data-ttu-id="40f6d-105">Так как смешивание выполняется с помощью графического процессора, существует минимальное влияние на производительность воспроизведения видеопотока, а также отсутствие обнаруживаемых помех или уничтожение артефактов.</span><span class="sxs-lookup"><span data-stu-id="40f6d-105">Because the blending is performed in hardware by the graphics processor, there is minimal impact to the playback performance of the Video Stream, and there are no detectable flicker or tearing artifacts.</span></span> <span data-ttu-id="40f6d-106">Приложения могут изменять отображаемое изображение так, как нужно.</span><span class="sxs-lookup"><span data-stu-id="40f6d-106">Applications can change the image displayed as frequently as they wish.</span></span> <span data-ttu-id="40f6d-107">Следует отметить, что изменения отражаются только на экране, когда граф фильтра DirectShow находится в состоянии выполняется.</span><span class="sxs-lookup"><span data-stu-id="40f6d-107">It should be noted that changes are only reflected on the screen when the DirectShow filter graph is in the running state.</span></span>

<span data-ttu-id="40f6d-108">VMR использует свой компонент микшера для наложения точечного рисунка на композитный образ.</span><span class="sxs-lookup"><span data-stu-id="40f6d-108">The VMR uses its mixer component to overlay the bitmap onto the composited image.</span></span> <span data-ttu-id="40f6d-109">С помощью VMR-7 приложение должно затребовать, чтобы VMR загрузил свое микшер, даже если имеется только один поток видео.</span><span class="sxs-lookup"><span data-stu-id="40f6d-109">With the VMR-7, the application must force the VMR to load its mixer, even if there is only a single video stream.</span></span> <span data-ttu-id="40f6d-110">Это не является обязательным для VMR-9, так как загружает микшер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40f6d-110">This is not necessary with the VMR-9 since it loads its mixer by default.</span></span>

<span data-ttu-id="40f6d-111">Для смешения статического растрового изображения с видеопотоком приложение создает VMR и добавляет его в граф, а затем вызывает [**ивмрфилтерконфиг:: сетнумберофстреамс**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="40f6d-111">To blend a static bitmap image with the video stream, the application creates the VMR and adds it to the graph, and then calls [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="40f6d-112">Значение, передаваемое этой функции, определяет количество входных ПИН-кодов, которые должен создать VMR.</span><span class="sxs-lookup"><span data-stu-id="40f6d-112">The value passed to this function identifies the number of input pins that the VMR should create.</span></span> <span data-ttu-id="40f6d-113">В приложениях можно указать любое значение от 1 до максимального количества \_ потоков микшера \_ ; Указание значения 1 допустимо, если приложение планирует отображать только один поток видео.</span><span class="sxs-lookup"><span data-stu-id="40f6d-113">Applications can specify any value between 1 and MAX\_MIXER\_STREAMS; specifying a value of 1 is valid if the application only intends to display a single video stream.</span></span> <span data-ttu-id="40f6d-114">Хотя фильтр VMR-7 по умолчанию имеет один входной ПИН-код, этот метод должен быть вызван для того, чтобы заставить его загрузить свой компонент микшера.</span><span class="sxs-lookup"><span data-stu-id="40f6d-114">Even though the VMR-7 has a single input pin by default, this method must be called in order to force it to load its mixer component.</span></span> <span data-ttu-id="40f6d-115">(VMR-9 загружает микшер и настраивает четыре контакта по умолчанию.)</span><span class="sxs-lookup"><span data-stu-id="40f6d-115">(The VMR-9 loads its mixer and sets up four pins by default.)</span></span>

<span data-ttu-id="40f6d-116">Чтобы задать точечный рисунок, используйте интерфейс [**ивмрмиксербитмап**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) на VMR-7 или интерфейс [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) на VMR-9.</span><span class="sxs-lookup"><span data-stu-id="40f6d-116">To set the bitmap, use the [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) interface on the VMR-7 or the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface on the VMR-9.</span></span>

<span data-ttu-id="40f6d-117">Точечный рисунок может быть задан либо с помощью маркера контекста устройства GDI (hDC), либо через интерфейс поверхности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="40f6d-117">The bitmap can be specified by either a handle to a GDI Device Context (hDC) or by a DirectDraw Surface interface.</span></span> <span data-ttu-id="40f6d-118">Если приложению требуется, чтобы изображение содержало внедренную альфа-информацию (также известную как на пиксель Alpha), данные изображения должны размещаться в интерфейсе поверхности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="40f6d-118">If the application wants the image to contain embedded alpha information (also known as per pixel alpha) it must place the image data in a DirectDraw Surface interface.</span></span> <span data-ttu-id="40f6d-119">Это связано с тем, что в настоящий момент невозможно разместить сведения о альфа-канале в контексте устройства GDI.</span><span class="sxs-lookup"><span data-stu-id="40f6d-119">This is because it is not currently possible to place per-pixel alpha information with a GDI Device Context.</span></span> <span data-ttu-id="40f6d-120">Поверхность DirectDraw должна быть либо RGB32, либо ARGB32, и, предпочтительнее, системной областью памяти.</span><span class="sxs-lookup"><span data-stu-id="40f6d-120">The DirectDraw surface must be either RGB32 or ARGB32, and should preferably be a system memory surface.</span></span> <span data-ttu-id="40f6d-121">Размеры поверхности не обязательно должны быть степенью 2.</span><span class="sxs-lookup"><span data-stu-id="40f6d-121">It is not necessary for the surface dimensions to be a power of 2.</span></span>

<span data-ttu-id="40f6d-122">VMR позволяет приложениям указывать расположение и общее значение прозрачности для образа.</span><span class="sxs-lookup"><span data-stu-id="40f6d-122">The VMR allows applications to specify the location and an overall transparency value for the image.</span></span> <span data-ttu-id="40f6d-123">В следующем коде показано, как передать данные изображения в VMR для последующего смешения:</span><span class="sxs-lookup"><span data-stu-id="40f6d-123">The following code shows how to pass image data down to the VMR for subsequent blending:</span></span>


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



<span data-ttu-id="40f6d-124">Основные понятия, описанные в этом разделе, показаны в примере приложения [вмрплайер](vmrplayer-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="40f6d-124">The concepts discussed in this topic are demonstrated in the [VMRPlayer Sample](vmrplayer-sample.md) sample application.</span></span>

<span data-ttu-id="40f6d-125">**Создание простых анимаций с помощью растрового изображения**</span><span class="sxs-lookup"><span data-stu-id="40f6d-125">**Creating Simple Animations with the Bitmap Image**</span></span>

<span data-ttu-id="40f6d-126">Чтобы создать простой анимированный логотип точечного рисунка, разместите все растровые кадры в одном изображении, как показано на следующей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="40f6d-126">To create a simple animated bitmap logo, put all of the bitmap "frames" into a single image, as shown in the following illustration.</span></span>

![полоса изображений VMR](images/vmr-image-strip.png)

<span data-ttu-id="40f6d-128">При первоначальном задании точечного рисунка с помощью [**ивмрмиксербитмап:: сеталфабитмап**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), если точечный рисунок находится в состоянии HDC, установите поле **rsrc** структуры **вмралфабитмап** , чтобы указать размер всей битовой карты в HDC.</span><span class="sxs-lookup"><span data-stu-id="40f6d-128">When you set the bitmap initially using [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), if the bitmap is in an HDC, set the **rSrc** field of the **VMRALPHABITMAP** structure to specify the size of the entire bitmap within the HDC.</span></span> <span data-ttu-id="40f6d-129">**Верхний** и **левый** элементы структуры имеют значение 0, а **правый** и **Нижний** элементы — ширина и высота растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="40f6d-129">The **top** and **left** members of the structure are set to 0, and the **right** and **bottom** members are the width and height of the bitmap.</span></span> <span data-ttu-id="40f6d-130">Если точечный рисунок находится в области DirectDraw, то известен размер поверхности, поэтому нет необходимости указывать rSrc в этом методе.</span><span class="sxs-lookup"><span data-stu-id="40f6d-130">If the bitmap is in a DirectDraw surface, then the size of the surface is known, so there is no need to specify rSrc in this method.</span></span>

<span data-ttu-id="40f6d-131">При вызове [**ивмрмиксербитмап:: упдатеалфабитмаппараметерс**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)используйте элемент **rsrc** для точечных рисунков HDC и DirectDraw, чтобы указать конкретный фрейм или прямоугольник в изображении, который требуется отобразить, и установите флаг **вмрбитмап \_ SRCRECT** в элементе **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="40f6d-131">When you call [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use the **rSrc** member for both HDC and DirectDraw bitmaps, to specify the particular frame or rectangle within the image that you wish to display, and set the **VMRBITMAP\_SRCRECT** flag in the **dwFlags** member.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40f6d-132">См. также</span><span class="sxs-lookup"><span data-stu-id="40f6d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f6d-133">Использование режима смешения VMR</span><span class="sxs-lookup"><span data-stu-id="40f6d-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



