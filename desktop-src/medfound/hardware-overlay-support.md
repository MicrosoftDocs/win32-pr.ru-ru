---
description: Описывает, как использовать наложение оборудования в Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Поддержка наложения оборудования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711352"
---
# <a name="hardware-overlay-support"></a><span data-ttu-id="52b64-103">Поддержка наложения оборудования</span><span class="sxs-lookup"><span data-stu-id="52b64-103">Hardware Overlay Support</span></span>

<span data-ttu-id="52b64-104">Наложение оборудования — это выделенная область видеопамяти, которая может быть наложена на основную поверхность.</span><span class="sxs-lookup"><span data-stu-id="52b64-104">A hardware overlay is a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="52b64-105">При отображении оверлея не выполняется ни одна копия.</span><span class="sxs-lookup"><span data-stu-id="52b64-105">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="52b64-106">Операция наложения выполняется в оборудовании без изменения данных на основной поверхности.</span><span class="sxs-lookup"><span data-stu-id="52b64-106">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="52b64-107">Использование наложения оборудования для воспроизведения видео было распространено в более ранних версиях Windows, так как наложение эффективно для видеосодержимого с высокой частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="52b64-107">The use of hardware overlays for video playback was common in earlier versions of Windows, because overlays are efficient for video content with a high frame rate.</span></span> <span data-ttu-id="52b64-108">Начиная с Windows 7 Direct3D 9 поддерживает наложение оборудования.</span><span class="sxs-lookup"><span data-stu-id="52b64-108">Starting in Windows 7, Direct3D 9 supports hardware overlays.</span></span> <span data-ttu-id="52b64-109">Эта поддержка предназначена в основном для воспроизведения видео и в некоторых отношениях отличается от предыдущих API-интерфейсов DirectDraw:</span><span class="sxs-lookup"><span data-stu-id="52b64-109">This support is intended primarily for video playback, and differs in some respects from earlier DirectDraw APIs:</span></span>

-   <span data-ttu-id="52b64-110">Наложение не может быть сжато, отражено или развышено.</span><span class="sxs-lookup"><span data-stu-id="52b64-110">The overlay cannot be shrunk, mirrored, or deinterlaced.</span></span>
-   <span data-ttu-id="52b64-111">Исходные цветовые ключи и альфа-смешение не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="52b64-111">Source color keys and alpha blending are not supported.</span></span>
-   <span data-ttu-id="52b64-112">Наложенные наложения можно растянуть, если наложение оборудования поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="52b64-112">Overlays can be stretched if the overlay hardware supports it.</span></span> <span data-ttu-id="52b64-113">В противном случае растяжение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="52b64-113">Otherwise, stretching is not supported.</span></span> <span data-ttu-id="52b64-114">На практике не все графические драйверы поддерживают растяжение.</span><span class="sxs-lookup"><span data-stu-id="52b64-114">In practice, not all graphics drivers support stretching.</span></span>
-   <span data-ttu-id="52b64-115">Каждое устройство поддерживает не более одного оверлея.</span><span class="sxs-lookup"><span data-stu-id="52b64-115">Each device supports at most one overlay.</span></span>
-   <span data-ttu-id="52b64-116">Наложение выполняется с использованием целевого цветового ключа, но среда выполнения Direct3D автоматически выбирает цвет и рисует прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="52b64-116">Overlay is performed using a destination color key, but the Direct3D runtime automatically selects the color and draws the destination rectangle.</span></span> <span data-ttu-id="52b64-117">Direct3D автоматически отслеживает расположение окна и обновляет расположение оверлея при каждом вызове **пресентекс** .</span><span class="sxs-lookup"><span data-stu-id="52b64-117">Direct3D automatically tracks the position of the window and updates the overlay position whenever the **PresentEx** is called.</span></span>

### <a name="creating-a-hardware-overlay-surface"></a><span data-ttu-id="52b64-118">Создание поверхности наложения оборудования</span><span class="sxs-lookup"><span data-stu-id="52b64-118">Creating a Hardware Overlay Surface</span></span>

<span data-ttu-id="52b64-119">Чтобы запросить поддержку наложения, вызовите **IDirect3D9:: жетдевицекапс**.</span><span class="sxs-lookup"><span data-stu-id="52b64-119">To query for overlay support, call **IDirect3D9::GetDeviceCaps**.</span></span> <span data-ttu-id="52b64-120">Если драйвер поддерживает наложение оборудования, в D3DCAPS9 задается флаг **\_ оверлея D3DCAPS** **. Элемент Caps** .</span><span class="sxs-lookup"><span data-stu-id="52b64-120">If the driver supports hardware overlay, the **D3DCAPS\_OVERLAY** flag is set in the **D3DCAPS9.Caps** member.</span></span>

<span data-ttu-id="52b64-121">Чтобы узнать, поддерживается ли конкретный формат оверлея для данного режима экрана, вызовите [**IDirect3D9ExOverlayExtension:: чеккдевицеоверлайтипе**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span><span class="sxs-lookup"><span data-stu-id="52b64-121">To find out whether a specific overlay format is supported for a given display mode, call [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span></span>

<span data-ttu-id="52b64-122">Чтобы создать наложение, вызовите **IDirect3D9Ex:: креатедевицеекс** и укажите результат переключения **D3DSWAPEFFECT \_ оверлея** .</span><span class="sxs-lookup"><span data-stu-id="52b64-122">To create the overlay, call **IDirect3D9Ex::CreateDeviceEx** and specify the **D3DSWAPEFFECT\_OVERLAY** swap effect.</span></span> <span data-ttu-id="52b64-123">Задний буфер может использовать формат, отличный от RGB, если он поддерживается оборудованием.</span><span class="sxs-lookup"><span data-stu-id="52b64-123">The back buffer can use a non-RGB format if the hardware supports it.</span></span>

<span data-ttu-id="52b64-124">Поверхности наложения имеют следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="52b64-124">Overlay surfaces have the following limitations:</span></span>

-   <span data-ttu-id="52b64-125">Приложение не может создать более одной цепочки перекрытия.</span><span class="sxs-lookup"><span data-stu-id="52b64-125">The application cannot create more than one overlay swap chain.</span></span>
-   <span data-ttu-id="52b64-126">Наложение следует использовать в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="52b64-126">The overlay must be used in windowed mode.</span></span> <span data-ttu-id="52b64-127">Его нельзя использовать в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="52b64-127">It cannot be used in fullscreen mode.</span></span>
-   <span data-ttu-id="52b64-128">В интерфейсе **IDirect3DDevice9Ex** должен использоваться результат переключения оверлея.</span><span class="sxs-lookup"><span data-stu-id="52b64-128">The overlay swap effect must be used with the **IDirect3DDevice9Ex** interface.</span></span> <span data-ttu-id="52b64-129">Он не поддерживается для **IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="52b64-129">It is not supported for **IDirect3DDevice9**.</span></span>
-   <span data-ttu-id="52b64-130">Невозможно использовать множественную выборку.</span><span class="sxs-lookup"><span data-stu-id="52b64-130">Multisampling cannot be used.</span></span>
-   <span data-ttu-id="52b64-131">Флаги **D3DPRESENT \_ Донотфлип** и **D3DPRESENT \_ флипрестарт** не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="52b64-131">The **D3DPRESENT\_DONOTFLIP** and **D3DPRESENT\_FLIPRESTART** flags are not supported.</span></span>
-   <span data-ttu-id="52b64-132">Статистика представления недоступна для поверхности наложения.</span><span class="sxs-lookup"><span data-stu-id="52b64-132">Presentation statistics are not available for the overlay surface.</span></span>

<span data-ttu-id="52b64-133">Если оборудование не поддерживает растяжение, рекомендуется создать цепочку подкачки, большую, чем режим экрана, чтобы размер окна можно было изменять в соответствии с любыми измерениями.</span><span class="sxs-lookup"><span data-stu-id="52b64-133">If the hardware does not support stretching, it is recommended to create a swap chain as large as the display mode, so that the window can be resized to any dimensions.</span></span> <span data-ttu-id="52b64-134">Повторное создание цепочки буферов не является оптимальным способом изменения размера окна, так как это может вызвать серьезные артефакты визуализации.</span><span class="sxs-lookup"><span data-stu-id="52b64-134">Recreating the swap chain is not an optimal way to handle resizing the window, because it can cause severe rendering artifacts.</span></span> <span data-ttu-id="52b64-135">Кроме того, из-за способа, которым графический процессор управляет памятью наложения, повторное создание цепочки буферов может привести к тому, что приложение закончит работу с видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="52b64-135">Also, because of the way the GPU manages the overlay memory, recreating the swap chain can potentially cause an application to run out of video memory.</span></span>

### <a name="new-d3dpresent_parameters-flags"></a><span data-ttu-id="52b64-136">Новые \_ флаги параметров D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="52b64-136">New D3DPRESENT\_PARAMETERS Flags</span></span>

<span data-ttu-id="52b64-137">Для создания наложений определены следующие флаги **\_ параметров D3DPRESENT** .</span><span class="sxs-lookup"><span data-stu-id="52b64-137">The following **D3DPRESENT\_PARAMETERS** flags are defined for creating overlays.</span></span>



| <span data-ttu-id="52b64-138">Flag</span><span class="sxs-lookup"><span data-stu-id="52b64-138">Flag</span></span>                                      | <span data-ttu-id="52b64-139">Описание</span><span class="sxs-lookup"><span data-stu-id="52b64-139">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b64-140">**\_Лимитедргб ОВЕРЛЕЯ \_ D3DPRESENTFLAG**</span><span class="sxs-lookup"><span data-stu-id="52b64-140">**D3DPRESENTFLAG\_OVERLAY\_LIMITEDRGB**</span></span>   | <span data-ttu-id="52b64-141">Диапазон RGB — 16 – 235.</span><span class="sxs-lookup"><span data-stu-id="52b64-141">The RGB range is 16–235.</span></span> <span data-ttu-id="52b64-142">Значение по умолчанию — 0 – 255.</span><span class="sxs-lookup"><span data-stu-id="52b64-142">The default is 0–255.</span></span> <br/> <span data-ttu-id="52b64-143">Требуется возможность **D3DOVERLAYCAPS \_ лимитедранжергб** .</span><span class="sxs-lookup"><span data-stu-id="52b64-143">Requires the **D3DOVERLAYCAPS\_LIMITEDRANGERGB** capability.</span></span><br/>                                                 |
| <span data-ttu-id="52b64-144">**D3DPRESENTFLAG \_ Overlay \_ икбкр \_ BT709**</span><span class="sxs-lookup"><span data-stu-id="52b64-144">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_BT709**</span></span> | <span data-ttu-id="52b64-145">Цвета YUV используют определение BT. 709.</span><span class="sxs-lookup"><span data-stu-id="52b64-145">YUV colors use the BT.709 definition.</span></span> <span data-ttu-id="52b64-146">Значение по умолчанию — BT. 601.</span><span class="sxs-lookup"><span data-stu-id="52b64-146">The default is BT.601.</span></span> <br/> <span data-ttu-id="52b64-147">Требуется возможность **D3DOVERLAYCAPS \_ икбкр \_ BT709** .</span><span class="sxs-lookup"><span data-stu-id="52b64-147">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT709** capability.</span></span><br/>                                      |
| <span data-ttu-id="52b64-148">**D3DPRESENTFLAG \_ Overlay \_ икбкр \_ ксвикк**</span><span class="sxs-lookup"><span data-stu-id="52b64-148">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_xvYCC**</span></span> | <span data-ttu-id="52b64-149">Вывод данных с помощью расширенного Икбкр (Ксвикк).</span><span class="sxs-lookup"><span data-stu-id="52b64-149">Output the data by using extended YCbCr (xvYCC).</span></span><br/> <span data-ttu-id="52b64-150">Требует возможности **D3DOVERLAYCAPS \_ икбкр \_ BT601 \_ ксвикк** или **D3DOVERLAYCAPS \_ икбкр \_ \_** BT709 ксвикк.</span><span class="sxs-lookup"><span data-stu-id="52b64-150">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT601\_xvYCC** or **D3DOVERLAYCAPS\_YCbCr\_BT709\_xvYCC** capability.</span></span><br/> |



 

### <a name="using-hardware-overlays"></a><span data-ttu-id="52b64-151">Использование наложения оборудования</span><span class="sxs-lookup"><span data-stu-id="52b64-151">Using Hardware Overlays</span></span>

<span data-ttu-id="52b64-152">Чтобы отобразить область наложения, приложение вызывает **IDirect3DDevice9Ex::P ресентекс**.</span><span class="sxs-lookup"><span data-stu-id="52b64-152">To display the overlay surface, the application calls **IDirect3DDevice9Ex::PresentEx**.</span></span> <span data-ttu-id="52b64-153">Среда выполнения Direct3D автоматически рисует ключ цвета назначения.</span><span class="sxs-lookup"><span data-stu-id="52b64-153">The Direct3D runtime automatically draws the destination color key.</span></span>

<span data-ttu-id="52b64-154">Для наложений определены следующие флаги **пресентекс** .</span><span class="sxs-lookup"><span data-stu-id="52b64-154">The following **PresentEx** flags are defined for overlays.</span></span>



| <span data-ttu-id="52b64-155">Flag</span><span class="sxs-lookup"><span data-stu-id="52b64-155">Flag</span></span>                              | <span data-ttu-id="52b64-156">Описание</span><span class="sxs-lookup"><span data-stu-id="52b64-156">Description</span></span>                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b64-157">**D3DPRESENT \_ упдатеколоркэй**</span><span class="sxs-lookup"><span data-stu-id="52b64-157">**D3DPRESENT\_UPDATECOLORKEY**</span></span>    | <span data-ttu-id="52b64-158">Установите этот флаг, если композиция диспетчер окон рабочего стола (DWM) отключена.</span><span class="sxs-lookup"><span data-stu-id="52b64-158">Set this flag if Desktop Window Manager (DWM) composition is disabled.</span></span> <span data-ttu-id="52b64-159">Этот флаг заставляет Direct3D перерисовывать цветовую клавишу.</span><span class="sxs-lookup"><span data-stu-id="52b64-159">This flag causes Direct3D to redraw the color key.</span></span><br/> <span data-ttu-id="52b64-160">Если DWM включен, этот флаг не является обязательным, так как Direct3D рисует ключ цвета один раз на поверхности, которая используется DWM для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="52b64-160">If DWM is enabled, this flag is not required, because Direct3D draws the color key once on the surface that DWM uses for redirection.</span></span><br/> |
| <span data-ttu-id="52b64-161">**D3DPRESENT \_ хидеоверлай**</span><span class="sxs-lookup"><span data-stu-id="52b64-161">**D3DPRESENT\_HIDEOVERLAY**</span></span>       | <span data-ttu-id="52b64-162">Скрывает наложение.</span><span class="sxs-lookup"><span data-stu-id="52b64-162">Hides the overlay.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="52b64-163">**D3DPRESENT \_ упдатеоверлайонли**</span><span class="sxs-lookup"><span data-stu-id="52b64-163">**D3DPRESENT\_UPDATEOVERLAYONLY**</span></span> | <span data-ttu-id="52b64-164">Обновляет наложение без изменения содержимого.</span><span class="sxs-lookup"><span data-stu-id="52b64-164">Updates the overlay without changing the contents.</span></span><br/> <span data-ttu-id="52b64-165">Этот флаг полезен, если окно перемещается, пока видео приостановлено.</span><span class="sxs-lookup"><span data-stu-id="52b64-165">This flag is useful if the window moves while the video is paused.</span></span><br/>                                                                                                                                           |



 

<span data-ttu-id="52b64-166">Приложение должно быть подготовлено к обработке следующих случаев:</span><span class="sxs-lookup"><span data-stu-id="52b64-166">An application should be prepared to handle the following cases:</span></span>

-   <span data-ttu-id="52b64-167">Если перекрытие используется другим приложением, **пресентекс** возвращает **D3DERR \_ NOTAVAILABLE**.</span><span class="sxs-lookup"><span data-stu-id="52b64-167">If another application is using the overlay, **PresentEx** returns **D3DERR\_NOTAVAILABLE**.</span></span>
-   <span data-ttu-id="52b64-168">Если окно перемещается на другой монитор, приложение должно повторно создать цепочку буферов.</span><span class="sxs-lookup"><span data-stu-id="52b64-168">If the window is moved to another monitor, the application must recreate the swap chain.</span></span> <span data-ttu-id="52b64-169">В противном случае, если приложение вызывает **пресентекс** для отображения наложения на другом мониторе, **пресентекс** возвращает **D3DERR \_ инвалиддевице**.</span><span class="sxs-lookup"><span data-stu-id="52b64-169">Otherwise, if the application calls **PresentEx** to display the overlay on a different monitor, **PresentEx** returns **D3DERR\_INVALIDDEVICE**.</span></span>
-   <span data-ttu-id="52b64-170">При изменении режима просмотра Direct3D пытается восстановить наложение.</span><span class="sxs-lookup"><span data-stu-id="52b64-170">If the display mode changes, Direct3D attempts to restore the overlay.</span></span> <span data-ttu-id="52b64-171">Если новый режим не поддерживает наложение, **пресентекс** возвращает **D3DERR \_ унсуппортедоверлай**.</span><span class="sxs-lookup"><span data-stu-id="52b64-171">If the new mode does not support the overlay, **PresentEx** returns **D3DERR\_UNSUPPORTEDOVERLAY**.</span></span>

### <a name="example-code"></a><span data-ttu-id="52b64-172">Пример кода</span><span class="sxs-lookup"><span data-stu-id="52b64-172">Example Code</span></span>

<span data-ttu-id="52b64-173">В следующем примере показано, как создать поверхность наложения.</span><span class="sxs-lookup"><span data-stu-id="52b64-173">The following example shows how to create an overlay surface.</span></span>


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="52b64-174">См. также</span><span class="sxs-lookup"><span data-stu-id="52b64-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52b64-175">API-интерфейсы видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="52b64-175">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 




