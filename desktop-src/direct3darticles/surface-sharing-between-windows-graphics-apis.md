---
title: Совместное использование поверхности API графических интерфейсов Windows
description: В этом разделе представлен технический обзор взаимодействия с использованием поверхности API графических интерфейсов Windows, включая Direct3D 11, Direct2D, DirectWrite, Direct3D 10 и Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1032cb1cf9b16280088f00e79e7e59bb7f1510b1
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343619"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="30cbd-103">Совместное использование поверхности API графических интерфейсов Windows</span><span class="sxs-lookup"><span data-stu-id="30cbd-103">Surface sharing between Windows graphics APIs</span></span>

<span data-ttu-id="30cbd-104">В этом разделе представлен технический обзор взаимодействия с использованием поверхности API графических интерфейсов Windows, включая Direct3D 11, Direct2D, DirectWrite, Direct3D 10 и Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="30cbd-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="30cbd-105">Если у вас уже есть опыт работы с этими API, этот документ поможет вам использовать несколько интерфейсов API для визуализации на одной и той же поверхности приложения, предназначенной для операционных систем Windows 7 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="30cbd-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="30cbd-106">В этом разделе также приводятся рекомендации и ссылки на дополнительные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="30cbd-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="30cbd-107">Для обеспечения взаимодействия Direct2D и DirectWrite в среде выполнения DirectX 11,1 можно использовать [устройства Direct2D и контексты устройств](/windows/desktop/Direct2D/devices-and-device-contexts) для непосредственного отображения на устройствах Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="30cbd-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="30cbd-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="30cbd-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="30cbd-109">Введение</span><span class="sxs-lookup"><span data-stu-id="30cbd-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="30cbd-110">Общие сведения о взаимодействии API</span><span class="sxs-lookup"><span data-stu-id="30cbd-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="30cbd-111">Сценарии взаимодействия</span><span class="sxs-lookup"><span data-stu-id="30cbd-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="30cbd-112">Общий доступ к устройствам Direct3D 10,1 с помощью Direct2D</span><span class="sxs-lookup"><span data-stu-id="30cbd-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="30cbd-113">Синхронизированные общие поверхности DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="30cbd-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="30cbd-114">Взаимодействие между интерфейсами API на основе Direct3D 9Ex и DXGI</span><span class="sxs-lookup"><span data-stu-id="30cbd-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="30cbd-115">Заключение</span><span class="sxs-lookup"><span data-stu-id="30cbd-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="30cbd-116">Введение</span><span class="sxs-lookup"><span data-stu-id="30cbd-116">Introduction</span></span>

<span data-ttu-id="30cbd-117">В этом документе взаимодействие API графических интерфейсов Windows относится к совместному использованию одной и той же области отрисовки различными интерфейсами API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="30cbd-118">Такой тип взаимодействия позволяет приложениям создавать привлекательные экраны, используя несколько API графических интерфейсов Windows, а также упростить миграцию на новые технологии, обеспечивая совместимость с существующими интерфейсами API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="30cbd-119">В Windows 7 (и Windows Vista SP2 с пакетом взаимодействия Windows 7, Vista 7IP) API графической отрисовки — это Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9C и более ранние API Direct3D, а также GDI и GDI+.</span><span class="sxs-lookup"><span data-stu-id="30cbd-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="30cbd-120">Компонент Windows Imaging Component (WIC) и DirectWrite — это связанные технологии для обработки изображений, и Direct2D выполняет отрисовку текста.</span><span class="sxs-lookup"><span data-stu-id="30cbd-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="30cbd-121">API ускорения видео DirectX (ДКСВА), основанный на Direct3D 9C и Direct3D 9Ex, используется для обработки видео.</span><span class="sxs-lookup"><span data-stu-id="30cbd-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="30cbd-122">Так как API графических интерфейсов Windows развиваются в сторону, основанной на Direct3D, корпорация Майкрософт придает больше усилий для обеспечения взаимодействия между API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="30cbd-123">Новые API-интерфейсы Direct3D и интерфейсы API более высокого уровня, основанные на интерфейсах API Direct3D, также обеспечивают поддержку, необходимую для обеспечения совместимости с более старыми API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="30cbd-124">Чтобы продемонстрировать, Direct2D приложения могут использовать Direct3D 10,1, совместно используя устройство Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="30cbd-125">Кроме того, интерфейсы API Direct3D 11, Direct2D и Direct3D 10,1 могут использовать преимущества графической инфраструктуры DirectX (DXGI) 1,1, которая обеспечивает синхронизированные общие поверхности, полностью поддерживающие взаимодействие между этими API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="30cbd-126">API-интерфейсы DXGI 1,1 взаимодействуют с GDI, а с GDI+ по ассоциации, получая контекст устройства GDI из поверхности DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="30cbd-127">Дополнительные сведения см. в документации по взаимодействию с DXGI и GDI, доступной на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="30cbd-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="30cbd-128">Несинхронизированный общий доступ к поверхности поддерживается средой выполнения Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="30cbd-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="30cbd-129">Видеоприложения на основе ДКСВА могут использовать вспомогательную функцию взаимодействия 9Ex и DXGI Direct3D для совместимости с Direct3D 9Ex на основе ДКСВА с Direct3D 11 для Compute Shader или могут взаимодействовать с Direct2D для двумерных элементов управления или отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="30cbd-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="30cbd-130">WIC и DirectWrite также взаимодействуют с GDI, Direct2D и ассоциациями, другими API-интерфейсами Direct3D.</span><span class="sxs-lookup"><span data-stu-id="30cbd-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="30cbd-131">Direct3D 10,0, Direct3D 9C и более ранние среды выполнения Direct3D не поддерживают общие поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="30cbd-132">Копии памяти системы будут по-прежнему использоваться для взаимодействия с интерфейсами API на основе GDI или DXGI.</span><span class="sxs-lookup"><span data-stu-id="30cbd-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="30cbd-133">Обратите внимание, что сценарии взаимодействия в этом документе относятся к отрисовке нескольких графических интерфейсов API в общей области отрисовки, а не в одном окне приложения.</span><span class="sxs-lookup"><span data-stu-id="30cbd-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="30cbd-134">Синхронизация для отдельных интерфейсов API, предназначенных для разных поверхностей, которые затем объединяются в одно окно, выходит за рамки данного документа.</span><span class="sxs-lookup"><span data-stu-id="30cbd-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="30cbd-135">Общие сведения о взаимодействии API</span><span class="sxs-lookup"><span data-stu-id="30cbd-135">API Interoperability Overview</span></span>

<span data-ttu-id="30cbd-136">Совместный доступ к поверхности API графических интерфейсов Windows можно описать с помощью сценариев API и API и соответствующих функций взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="30cbd-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="30cbd-137">В Windows 7 и начиная с Windows Vista с пакетом обновления 2 (SP2) с 7IP новые API и связанные среды выполнения включают Direct2D и связанные технологии: Direct3D 11 и DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="30cbd-138">Производительность GDI была также улучшена в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30cbd-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="30cbd-139">В пакет обновления 1 (SP1) для Windows Vista появился Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="30cbd-140">На следующей схеме показана поддержка взаимодействия между API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-140">The following diagram shows the interoperability support between APIs.</span></span>

![Схема поддержки взаимодействия между API графических интерфейсов Windows](images/surface-sharing-interoperability.png)

<span data-ttu-id="30cbd-142">На этой диаграмме стрелки показывают сценарии взаимодействия, в которых одна и та же поверхность может быть доступна для подключенных API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="30cbd-143">Синие стрелки указывают механизмы взаимодействия, появившиеся в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="30cbd-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="30cbd-144">Зеленые стрелки указывают поддержку взаимодействия для новых API или усовершенствований, которые помогают старым API взаимодействовать с более новыми API.</span><span class="sxs-lookup"><span data-stu-id="30cbd-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="30cbd-145">Например, зеленые стрелки представляют общий доступ к устройствам, поддержку синхронизированной общей поверхности, вспомогательный модуль синхронизации Direct3D 9Ex/DXGI и получение контекста устройства GDI из совместимой области.</span><span class="sxs-lookup"><span data-stu-id="30cbd-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="30cbd-146">Сценарии взаимодействия</span><span class="sxs-lookup"><span data-stu-id="30cbd-146">Interoperability Scenarios</span></span>

<span data-ttu-id="30cbd-147">Начиная с Windows 7 и Windows Vista 7IP, основные предложения от API графических интерфейсов Windows поддерживают поддержку нескольких интерфейсов API для одной и той же поверхности DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="30cbd-148">**Direct3D 11, Direct3D 10,1, Direct2D — взаимодействие друг с другом**</span><span class="sxs-lookup"><span data-stu-id="30cbd-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="30cbd-149">API Direct3D 11, Direct3D 10,1 и Direct2D (и связанные с ним API, такие как DirectWrite и WIC) могут взаимодействовать друг с другом с помощью устройства Direct3D 10,1 или синхронизированных общих поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="30cbd-150">Общий доступ к устройствам Direct3D 10,1 с помощью Direct2D</span><span class="sxs-lookup"><span data-stu-id="30cbd-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="30cbd-151">Совместное использование устройств между Direct2D и Direct3D 10,1 позволяет приложению использовать оба API для беспрепятственного и эффективного отображения на одной поверхности DXGI 1,1, используя один и тот же базовый объект устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="30cbd-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="30cbd-152">Direct2D предоставляет возможность вызывать API-интерфейсы Direct2D с помощью существующего устройства Direct3D 10,1, используя тот факт, что Direct2D построен на основе среды выполнения Direct3D 10,1 и DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="30cbd-153">В следующих фрагментах кода показано, как Direct2D получает целевой объект отрисовки устройства Direct3D 10,1 из поверхности DXGI 1,1, связанной с устройством.</span><span class="sxs-lookup"><span data-stu-id="30cbd-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="30cbd-154">Целевой объект отрисовки устройства Direct3D 10,1 может выполнять вызовы рисования Direct2D между API Бегиндрав и EndDraw.</span><span class="sxs-lookup"><span data-stu-id="30cbd-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



<span data-ttu-id="30cbd-155">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="30cbd-155">**Remarks**</span></span>

-   <span data-ttu-id="30cbd-156">Связанное устройство Direct3D 10,1 должно поддерживать формат BGRA.</span><span class="sxs-lookup"><span data-stu-id="30cbd-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="30cbd-157">Это устройство было создано путем вызова D3D10CreateDevice1 с параметром D3D10 \_ Create \_ Device \_ BGRA \_ support.</span><span class="sxs-lookup"><span data-stu-id="30cbd-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="30cbd-158">Формат BGRA поддерживается начиная с Direct3D 10 на уровне компонентов 9,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="30cbd-159">Приложение не должно создавать несколько ID2D1RenderTargets, сопоставленных с одним и тем же устройством Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="30cbd-160">Для оптимальной производительности следует постоянно размещать по крайней мере один ресурс, например текстуры или поверхности, связанные с устройством.</span><span class="sxs-lookup"><span data-stu-id="30cbd-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="30cbd-161">Совместное использование устройств подходит для внутрипроцессного, однопотокового использования одного устройства отрисовки, совместно используемого как интерфейсами API отрисовки Direct3D 10,1, так и Direct2D.</span><span class="sxs-lookup"><span data-stu-id="30cbd-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="30cbd-162">Синхронизированные общие поверхности позволяют использовать многопоточные, внутрипроцессный и необработанное использование нескольких устройств отрисовки, используемых интерфейсами API Direct3D 10,1, Direct2D и Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="30cbd-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="30cbd-163">Другой способ взаимодействия Direct3D 10,1 и Direct2D заключается в использовании ID3D1RenderTarget:: Креатешаредбитмап, который создает объект ID2D1Bitmap из Идксгисурфаце.</span><span class="sxs-lookup"><span data-stu-id="30cbd-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="30cbd-164">Вы можете записать сцену Direct3D 10.1 в растровое изображение и визуализировать ее с помощью Direct2D.</span><span class="sxs-lookup"><span data-stu-id="30cbd-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="30cbd-165">Дополнительные сведения см. в разделе [метод ID2D1RenderTarget:: креатешаредбитмап](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span><span class="sxs-lookup"><span data-stu-id="30cbd-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="30cbd-166">Direct2Dное растрирование программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="30cbd-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="30cbd-167">Совместное использование устройств с помощью Direct3D 10,1 не поддерживается при использовании модуля подготовки программного обеспечения Direct2D, например путем указания D2D1 рендеринга \_ \_ \_ использования целевого \_ \_ программного обеспечения \_ в D2D1 \_ прорисовка целевого \_ объекта \_ при создании целевого объекта прорисовки Direct2D.</span><span class="sxs-lookup"><span data-stu-id="30cbd-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="30cbd-168">Direct2D может использовать средство программной прорисовки WARP10 для совместного использования устройства с Direct3D 10 или Direct3D 11, но производительность значительно снижается.</span><span class="sxs-lookup"><span data-stu-id="30cbd-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="30cbd-169">Синхронизированные общие поверхности DXGI 1,1</span><span class="sxs-lookup"><span data-stu-id="30cbd-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="30cbd-170">Все интерфейсы API Direct3D 11, Direct3D 10,1 и Direct2D используют DXGI 1,1, который предоставляет функции для синхронизации чтения и записи в одну и ту же поверхность видеопамяти (DXGISurface1) двумя или более устройствами Direct3D.</span><span class="sxs-lookup"><span data-stu-id="30cbd-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="30cbd-171">Устройства отрисовки, использующие синхронизированные общие поверхности, могут быть устройствами Direct3D 10,1 или Direct3D 11, работающими в одном процессе или между процессами.</span><span class="sxs-lookup"><span data-stu-id="30cbd-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="30cbd-172">Приложения могут использовать синхронизированные общие поверхности для взаимодействия любых устройств на базе DXGI 1,1, таких как Direct3D 11 и Direct3D 10,1, или между Direct3D 11 и Direct2D, получая устройство Direct3D 10,1 из Direct2D целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="30cbd-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="30cbd-173">В API-интерфейсах Direct3D 10,1 и более поздних версий для использования DXGI 1,1 Убедитесь, что устройство Direct3D создано с помощью объекта адаптера DXGI 1,1, который перечисляются из объекта фабрики DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="30cbd-174">Вызовите CreateDXGIFactory1, чтобы создать объект IDXGIFactory1, и EnumAdapters1, чтобы перечислить объект IDXGIAdapter1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="30cbd-175">Объект IDXGIAdapter1 необходимо передать в рамках вызова D3D10CreateDevice или D3D10CreateDeviceAndSwapChain.</span><span class="sxs-lookup"><span data-stu-id="30cbd-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="30cbd-176">Дополнительные сведения об API-интерфейсах DXGI 1,1 см. в [руководстве по программированию для DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="30cbd-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="30cbd-177">API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="30cbd-177">APIs</span></span>

<span data-ttu-id="30cbd-178">**\_ \_ \_ Общие \_ кэйедмутекс ресурсов D3D10**</span><span class="sxs-lookup"><span data-stu-id="30cbd-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="30cbd-179">При создании синхронизированного общего ресурса Установите флаг D3D10 \_ ресурсов \_ \_ Общие \_ кэйедмутекс в D3D10 \_ ресурс \_ Прочие \_ .</span><span class="sxs-lookup"><span data-stu-id="30cbd-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="30cbd-180">**\_ \_ \_ Общие \_ кэйедмутекс ресурсов D3D10**</span><span class="sxs-lookup"><span data-stu-id="30cbd-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="30cbd-181">Позволяет синхронизировать созданный ресурс с помощью API-интерфейсов Идксгикэйедмутекс:: Аккуиресинк и Релеасесинк.</span><span class="sxs-lookup"><span data-stu-id="30cbd-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="30cbd-182">Следующие API-интерфейсы Direct3D 10,1 для создания ресурсов, которые принимают \_ параметр флага D3D10 ресурса, были \_ \_ расширены для поддержки нового флага.</span><span class="sxs-lookup"><span data-stu-id="30cbd-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="30cbd-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="30cbd-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="30cbd-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="30cbd-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="30cbd-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="30cbd-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="30cbd-186">ID3D10Device1:: CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="30cbd-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="30cbd-187">Если какая-либо из перечисленных функций вызывается с \_ \_ \_ \_ УСТАНОВЛЕНным флагом D3D10 reshared кэйедмутекс, то возвращаемый интерфейс может быть запрошен для интерфейса Идксгикэйедмутекс, который реализует интерфейсы API аккуиресинк и релеасесинк для синхронизации доступа к поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="30cbd-188">Устройство, создающее поверхность и любое другое устройство, открывающее поверхность (с помощью Опеншаредресаурце), требуется для вызова Идксгикэйедмутекс:: Аккуиресинк перед всеми командами отрисовки на поверхность, и Идксгикэйедмутекс:: Релеасесинк при завершении подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="30cbd-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="30cbd-189">Устройства деформации и ссылки не поддерживают общие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="30cbd-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="30cbd-190">Попытка создать ресурс с этим флагом на устройстве деформации или на устройство ссылки приведет к тому, что метод Create вернет \_ код ошибки E OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="30cbd-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="30cbd-191">**ИНТЕРФЕЙС ИДКСГИКЭЙЕДМУТЕКС**</span><span class="sxs-lookup"><span data-stu-id="30cbd-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="30cbd-192">Новый интерфейс в DXGI 1,1, Идксгикэйедмутекс представляет ключ мьютекса, который обеспечивает эксклюзивный доступ к общему ресурсу, используемому несколькими устройствами.</span><span class="sxs-lookup"><span data-stu-id="30cbd-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="30cbd-193">Справочную документацию об этом интерфейсе и его двух методах, Аккуиресинк и Релеасесинк, см. в разделе [идксгикэйедмутекс](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="30cbd-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="30cbd-194">Пример: синхронизированный общий доступ к поверхности между двумя устройствами Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="30cbd-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="30cbd-195">В приведенном ниже примере показан общий доступ к поверхности между двумя устройствами Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="30cbd-196">Синхронизированная Общая поверхность создается устройством Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



<span data-ttu-id="30cbd-197">Одно устройство Direct3D 10.1 может получить синхронизированную общую область для отрисовки путем вызова Аккуиресинк, а затем освободить поверхность для отрисовки другого устройства путем вызова Релеасесинк.</span><span class="sxs-lookup"><span data-stu-id="30cbd-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="30cbd-198">При отсутствии совместного использования синхронизированной общей поверхности с любым другим устройством Direct3D создатель может получить и освободить синхронизированную общую поверхность (для запуска и завершения подготовки к просмотру), добавив и выполнив одно и то же значение ключа.</span><span class="sxs-lookup"><span data-stu-id="30cbd-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



<span data-ttu-id="30cbd-199">Второе устройство Direct3D 10.1 может получить синхронизированную общую область для отрисовки путем вызова Аккуиресинк, а затем освобождает поверхность для отрисовки первого устройства путем вызова Релеасесинк.</span><span class="sxs-lookup"><span data-stu-id="30cbd-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="30cbd-200">Обратите внимание, что устройство 2 может получить синхронизированную общую поверхность, используя то же значение ключа, которое указано в вызове Релеасесинк устройством 1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



<span data-ttu-id="30cbd-201">Дополнительные устройства, совместно использующие одну и ту же поверхность, могут принять и освободить поверхность с помощью дополнительных ключей, как показано в следующих вызовах.</span><span class="sxs-lookup"><span data-stu-id="30cbd-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



<span data-ttu-id="30cbd-202">Обратите внимание, что реальное приложение может всегда отображаться на промежуточной поверхности, которая затем копируется в общую область, чтобы предотвратить любое устройство, ожидающее другого устройства, которое использует эту поверхность.</span><span class="sxs-lookup"><span data-stu-id="30cbd-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="30cbd-203">Использование синхронизированных общих поверхностей с Direct2D и Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="30cbd-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="30cbd-204">Аналогично, для совместного использования интерфейсов API Direct3D 11 и Direct3D 10,1 можно создать синхронизированную общую область на любом устройстве API и предоставить общий доступ другим устройствам API в или из процесса.</span><span class="sxs-lookup"><span data-stu-id="30cbd-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="30cbd-205">Приложения, использующие Direct2D, могут использовать устройство Direct3D 10,1 и использовать синхронизированную общую поверхность для взаимодействия с Direct3D 11 или другими устройствами Direct3D 10,1, независимо от того, принадлежат ли они одному и тому же процессу или разным процессам.</span><span class="sxs-lookup"><span data-stu-id="30cbd-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="30cbd-206">Однако для однопроцессных приложений с одним потоком совместное использование устройств является самым высокопроизводительным и эффективным способом взаимодействия между Direct2D и Direct3D 10 или Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="30cbd-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="30cbd-207">Средство программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="30cbd-207">Software Rasterizer</span></span>

<span data-ttu-id="30cbd-208">Синхронизированные общие поверхности не поддерживаются, если приложения используют средства программной прорисовки Direct3D или Direct2D, в том числе средство средства прорисовки и деформацию, вместо использования аппаратного ускорения графики.</span><span class="sxs-lookup"><span data-stu-id="30cbd-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="30cbd-209">Взаимодействие между интерфейсами API на основе Direct3D 9Ex и DXGI</span><span class="sxs-lookup"><span data-stu-id="30cbd-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="30cbd-210">API-интерфейсы 9Ex Direct3D включали понятие общего доступа к поверхности, позволяющее другим API-интерфейсам считывать из общей поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="30cbd-211">Чтобы предоставить общий доступ к чтению и записи на общую поверхность Direct3D 9Ex, необходимо добавить вручную синхронизацию с самим приложением.</span><span class="sxs-lookup"><span data-stu-id="30cbd-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="30cbd-212">Общие поверхности Direct3D 9Ex и вспомогательное приложение синхронизации вручную</span><span class="sxs-lookup"><span data-stu-id="30cbd-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="30cbd-213">Самая фундаментальная задача в области взаимодействия Direct3D 9Ex и Direct3D 10 или 11 заключается в передаче одной поверхности с первого устройства (устройства A) второму (устройство б), таким образом, когда устройство б получает маркер на поверхности, подготовка к просмотру устройства A гарантированно завершена.</span><span class="sxs-lookup"><span data-stu-id="30cbd-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="30cbd-214">Таким образом, устройство б может использовать эту область без беспокойства.</span><span class="sxs-lookup"><span data-stu-id="30cbd-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="30cbd-215">Это очень похоже на проблему классической модели "производитель-получатель", и в этом обсуждении моделируется проблема.</span><span class="sxs-lookup"><span data-stu-id="30cbd-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="30cbd-216">Первое устройство, использующее поверхность, а затем использующая ее, — это производитель (устройство а), а устройство, которое изначально ожидает, является потребителем (устройство б).</span><span class="sxs-lookup"><span data-stu-id="30cbd-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="30cbd-217">Любое реальное приложение является более сложным, чем оно, и будет объединять несколько стандартных блоков "производитель-получатель" для создания требуемой функциональности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="30cbd-218">Стандартные блоки "производитель-получатель" реализуются в вспомогательном модуле с помощью очереди поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="30cbd-219">Поверхности помещаются в очередь производителем и выводятся из очереди потребителем.</span><span class="sxs-lookup"><span data-stu-id="30cbd-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="30cbd-220">В вспомогательном модуле представлены три интерфейса COM: Исурфацекуеуе, Исурфацепродуцер и Исурфацеконсумер.</span><span class="sxs-lookup"><span data-stu-id="30cbd-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="30cbd-221">High-Level обзор вспомогательной функции</span><span class="sxs-lookup"><span data-stu-id="30cbd-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="30cbd-222">Объект Исурфацекуеуе является стандартным блоком для использования общих поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="30cbd-223">Он создается с инициализированным устройством Direct3D и описанием для создания фиксированного количества общих поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="30cbd-224">Объект Queue управляет созданием ресурсов и открытием кода.</span><span class="sxs-lookup"><span data-stu-id="30cbd-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="30cbd-225">Число и тип поверхностей фиксированы; После создания поверхностей приложение не сможет добавлять или удалять их.</span><span class="sxs-lookup"><span data-stu-id="30cbd-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="30cbd-226">Каждый экземпляр объекта Исурфацекуеуе обеспечивает сортировку односторонней улицы, которую можно использовать для отправки поверхностей с устройства, производящего работу, на устройство.</span><span class="sxs-lookup"><span data-stu-id="30cbd-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="30cbd-227">Для включения общего доступа к контактам между устройствами конкретных приложений можно использовать несколько таких односторонних улиц.</span><span class="sxs-lookup"><span data-stu-id="30cbd-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="30cbd-228">**Создание или время существования объекта**</span><span class="sxs-lookup"><span data-stu-id="30cbd-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="30cbd-229">Существует два способа создания объекта очереди: с помощью Креатесурфацекуеуе или метода Clone объекта Исурфацекуеуе.</span><span class="sxs-lookup"><span data-stu-id="30cbd-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="30cbd-230">Поскольку интерфейсы являются COM-объектами, применяется стандартное управление жизненным циклом COM.</span><span class="sxs-lookup"><span data-stu-id="30cbd-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="30cbd-231">**Модель "производитель-получатель"**</span><span class="sxs-lookup"><span data-stu-id="30cbd-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="30cbd-232">Постановка в очередь (): производитель вызывает эту функцию, чтобы указать, что она выполняется с поверхностью, которая теперь может быть доступна для другого устройства.</span><span class="sxs-lookup"><span data-stu-id="30cbd-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="30cbd-233">После возврата этой функции устройство производителя больше не имеет прав на поверхность, и его использование будет незащищенным.</span><span class="sxs-lookup"><span data-stu-id="30cbd-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="30cbd-234">Вывод из очереди (). устройство, вызывающее потребление, вызывает эту функцию для получения общей поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="30cbd-235">API гарантирует, что все выходящие из очереди поверхности будут готовы к использованию.</span><span class="sxs-lookup"><span data-stu-id="30cbd-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="30cbd-236">**Метаданные**</span><span class="sxs-lookup"><span data-stu-id="30cbd-236">**Metadata**</span></span>  
<span data-ttu-id="30cbd-237">API поддерживает связывание метаданных с общими областями.</span><span class="sxs-lookup"><span data-stu-id="30cbd-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="30cbd-238">В постановке в очередь () можно указать дополнительные метаданные, которые будут переданы устройству, используемому для использования.</span><span class="sxs-lookup"><span data-stu-id="30cbd-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="30cbd-239">Метаданные должны быть меньше, чем максимальное значение, известное во время создания.</span><span class="sxs-lookup"><span data-stu-id="30cbd-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="30cbd-240">Функция requeue () при необходимости может передавать буфер и указатель на размер буфера.</span><span class="sxs-lookup"><span data-stu-id="30cbd-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="30cbd-241">Очередь заполняет буфер метаданными из соответствующего вызова очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="30cbd-242">**клонирования**</span><span class="sxs-lookup"><span data-stu-id="30cbd-242">**Cloning**</span></span>  
<span data-ttu-id="30cbd-243">Каждый объект Исурфацекуеуе разрешает одностороннюю синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="30cbd-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="30cbd-244">Предполагается, что подавляющее большинство приложений, использующих этот API, будет использовать закрытую систему.</span><span class="sxs-lookup"><span data-stu-id="30cbd-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="30cbd-245">Простейшая закрытая система с двумя устройствами, отправляющим поверхности, должна иметь две очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="30cbd-246">Объект Исурфацекуеуе содержит метод Clone (), позволяющий создать несколько очередей, которые являются частью одного и того же крупного конвейера.</span><span class="sxs-lookup"><span data-stu-id="30cbd-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="30cbd-247">Clone создает новый объект Исурфацекуеуе из существующего объекта и разделяет все открытые ресурсы между ними.</span><span class="sxs-lookup"><span data-stu-id="30cbd-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="30cbd-248">Полученный объект имеет точно те же поверхности, что и исходная очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="30cbd-249">Клонированные очереди могут иметь разные размеры метаданных друг от друга.</span><span class="sxs-lookup"><span data-stu-id="30cbd-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="30cbd-250">**Surfaces**</span><span class="sxs-lookup"><span data-stu-id="30cbd-250">**Surfaces**</span></span>  
<span data-ttu-id="30cbd-251">Исурфацекуеуе отвечает за создание поверхностей и управление ими.</span><span class="sxs-lookup"><span data-stu-id="30cbd-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="30cbd-252">Не допускается ставить в очередь произвольные поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="30cbd-253">Кроме того, поверхность должна иметь только один активный "владелец".</span><span class="sxs-lookup"><span data-stu-id="30cbd-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="30cbd-254">Он должен находиться в определенной очереди или использоваться конкретным устройством.</span><span class="sxs-lookup"><span data-stu-id="30cbd-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="30cbd-255">Его нельзя использовать в нескольких очередях или для того, чтобы устройства продолжали использовать область после ее постановки в очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="30cbd-256">Сведения об API</span><span class="sxs-lookup"><span data-stu-id="30cbd-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="30cbd-257">исурфацекуеуе</span><span class="sxs-lookup"><span data-stu-id="30cbd-257">IsurfaceQueue</span></span>

<span data-ttu-id="30cbd-258">Очередь отвечает за создание и обслуживание общих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30cbd-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="30cbd-259">Он также предоставляет функции для сцепления нескольких очередей с помощью клонирования.</span><span class="sxs-lookup"><span data-stu-id="30cbd-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="30cbd-260">В очереди есть методы, которые открывают устройство, производящее создание, и устройство.</span><span class="sxs-lookup"><span data-stu-id="30cbd-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="30cbd-261">В любое время можно открыть только один из них.</span><span class="sxs-lookup"><span data-stu-id="30cbd-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="30cbd-262">Очередь предоставляет следующие интерфейсы API:</span><span class="sxs-lookup"><span data-stu-id="30cbd-262">The queue exposes the following APIs:</span></span>



| <span data-ttu-id="30cbd-263">API</span><span class="sxs-lookup"><span data-stu-id="30cbd-263">API</span></span>                            | <span data-ttu-id="30cbd-264">Описание</span><span class="sxs-lookup"><span data-stu-id="30cbd-264">Description</span></span>                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="30cbd-265">креатесурфацекуеуе</span><span class="sxs-lookup"><span data-stu-id="30cbd-265">CreateSurfaceQueue</span></span>          | <span data-ttu-id="30cbd-266">Создает объект Исурфацекуеуе ("корневую" очередь).</span><span class="sxs-lookup"><span data-stu-id="30cbd-266">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="30cbd-267">Исурфацекуеуе:: Опенконсумер</span><span class="sxs-lookup"><span data-stu-id="30cbd-267">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="30cbd-268">Возвращает интерфейс для использования устройством для вывода из очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-268">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="30cbd-269">Исурфацекуеуе:: Опенпродуцер</span><span class="sxs-lookup"><span data-stu-id="30cbd-269">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="30cbd-270">Возвращает интерфейс для устройства, создающего постановку в очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-270">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="30cbd-271">Исурфацекуеуе:: Clone</span><span class="sxs-lookup"><span data-stu-id="30cbd-271">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="30cbd-272">Создает объект Исурфацекуеуе, который совместно использует поверхности с объектом корневой очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-272">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="30cbd-273">**креатесурфацекуеуе**</span><span class="sxs-lookup"><span data-stu-id="30cbd-273">**CreateSurfaceQueue**</span></span>  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



<span data-ttu-id="30cbd-274">**Члены**</span><span class="sxs-lookup"><span data-stu-id="30cbd-274">**Members**</span></span>  

<span data-ttu-id="30cbd-275">**Ширина**. **Высота**  измерений общих поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-275">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="30cbd-276">Все общие поверхности должны иметь одинаковые размеры.</span><span class="sxs-lookup"><span data-stu-id="30cbd-276">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="30cbd-277">**Формат** Формат общих поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-277">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="30cbd-278">Все общие поверхности должны иметь одинаковый формат.</span><span class="sxs-lookup"><span data-stu-id="30cbd-278">All shared surfaces must have the same format.</span></span> <span data-ttu-id="30cbd-279">Допустимые форматы зависят от устройств, которые будут использоваться, так как разные пары устройств могут совместно использовать различные типы форматов.</span><span class="sxs-lookup"><span data-stu-id="30cbd-279">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="30cbd-280">**Нумсурфацес**  Количество поверхностей, входящих в очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-280">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="30cbd-281">Это фиксированное число.</span><span class="sxs-lookup"><span data-stu-id="30cbd-281">This is a fixed number.</span></span>  
 <span data-ttu-id="30cbd-282">**Метадатасизе**  Максимальный размер буфера метаданных.</span><span class="sxs-lookup"><span data-stu-id="30cbd-282">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="30cbd-283">**Флаги**  Флаги для управления поведением очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-283">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="30cbd-284">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="30cbd-284">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="30cbd-285">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="30cbd-285">**Parameters**</span></span>

 <span data-ttu-id="30cbd-286">*пдеск* \[ в \]  описание создаваемой очереди общей поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-286">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="30cbd-287">*пдевице* \[ на \]  устройстве, которое следует использовать для создания общих поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-287">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="30cbd-288">Это явный параметр из-за возможности Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="30cbd-288">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="30cbd-289">Для поверхностей, совместно используемых Direct3D 9 и Direct3D 10, поверхности должны создаваться с помощью Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="30cbd-289">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="30cbd-290">*ппкуеуе* \[ out \]  при возврате содержит указатель на объект исурфацекуеуе.</span><span class="sxs-lookup"><span data-stu-id="30cbd-290">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="30cbd-291">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="30cbd-291">**Return Values**</span></span>

<span data-ttu-id="30cbd-292">Если *пдевице* не поддерживает совместное использование ресурсов, эта функция ВОЗВРАЩАЕТ ошибку DXGI, \_ \_ Недопустимый \_ вызов.</span><span class="sxs-lookup"><span data-stu-id="30cbd-292">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="30cbd-293">Эта функция создает ресурсы.</span><span class="sxs-lookup"><span data-stu-id="30cbd-293">This function creates the resources.</span></span> <span data-ttu-id="30cbd-294">В случае сбоя он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="30cbd-294">If it fails, it returns an error.</span></span> <span data-ttu-id="30cbd-295">Если оно завершается успешно, то возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="30cbd-295">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="30cbd-296">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="30cbd-296">**Remarks**</span></span>

<span data-ttu-id="30cbd-297">При создании объекта Queue также создаются все поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-297">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="30cbd-298">Предполагается, что все поверхности являются целевыми объектами рендеринга, и они будут созданы с помощью \_ \_ целевого объекта рендеринга привязки D3D10 \_ и \_ \_ \_ установленных флагов ресурсов шейдера D3D10 BIND (или эквивалентных флагов для разных сред выполнения).</span><span class="sxs-lookup"><span data-stu-id="30cbd-298">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="30cbd-299">Разработчик может указать флаг, указывающий, будет ли доступ к очереди выполняться несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="30cbd-299">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="30cbd-300">Если флаги не заданы (**flags** = = 0), очередь будет использоваться несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="30cbd-300">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="30cbd-301">Разработчик может указать единый потоковый доступ, который отключает код синхронизации и обеспечивает повышение производительности в этих случаях.</span><span class="sxs-lookup"><span data-stu-id="30cbd-301">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="30cbd-302">Каждая клонированная очередь имеет собственный флаг, поэтому различные очереди в системе могут иметь разные элементы управления синхронизации.</span><span class="sxs-lookup"><span data-stu-id="30cbd-302">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="30cbd-303">**Открытие производителя**</span><span class="sxs-lookup"><span data-stu-id="30cbd-303">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="30cbd-304">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="30cbd-304">**Parameters**</span></span>  

<span data-ttu-id="30cbd-305">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="30cbd-305">*pDevice* \[in\]</span></span>  

<span data-ttu-id="30cbd-306">Устройство производителя, которое ставит в очередь поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-306">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="30cbd-307">*пппродуцер* \[ out \] возвращает объект интерфейсу Producer.</span><span class="sxs-lookup"><span data-stu-id="30cbd-307">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="30cbd-308">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="30cbd-308">**Return Values**</span></span>

<span data-ttu-id="30cbd-309">Если устройство не поддерживает совместное использование поверхностей, возвращает ошибку DXGI \_ , \_ Недопустимый \_ вызов.</span><span class="sxs-lookup"><span data-stu-id="30cbd-309">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="30cbd-310">**Открытие объекта-получателя**</span><span class="sxs-lookup"><span data-stu-id="30cbd-310">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="30cbd-311">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="30cbd-311">**Parameters**</span></span>  
 <span data-ttu-id="30cbd-312">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="30cbd-312">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="30cbd-313">Устройство-потребитель, которое вымещает поверхности из очереди поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-313">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="30cbd-314">*ппконсумер* \[ \]  метод out возвращает объект для интерфейса потребителя.</span><span class="sxs-lookup"><span data-stu-id="30cbd-314">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="30cbd-315">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="30cbd-315">**Return Values**</span></span>

<span data-ttu-id="30cbd-316">Если устройство не поддерживает совместное использование поверхностей, возвращает ошибку DXGI \_ , \_ Недопустимый \_ вызов.</span><span class="sxs-lookup"><span data-stu-id="30cbd-316">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="30cbd-317">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="30cbd-317">**Remarks**</span></span>

<span data-ttu-id="30cbd-318">Эта функция открывает все поверхности в очереди для устройства ввода и кэширует их.</span><span class="sxs-lookup"><span data-stu-id="30cbd-318">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="30cbd-319">Последующие вызовы для вывода из очереди будут просто переходить в кэш и не должны повторно открывать поверхности каждый раз.</span><span class="sxs-lookup"><span data-stu-id="30cbd-319">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="30cbd-320">Клонирование Идксгикссурфацекуеуе</span><span class="sxs-lookup"><span data-stu-id="30cbd-320">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="30cbd-321">**Члены** **метадатасизе** и **flags** имеют то же поведение, что и для креатесурфацекуеуе.</span><span class="sxs-lookup"><span data-stu-id="30cbd-321">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="30cbd-322">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="30cbd-322">**Parameters**</span></span>

<span data-ttu-id="30cbd-323">*пдеск* \[ в \] структуре, которая предоставляет описание создаваемого объекта Clone.</span><span class="sxs-lookup"><span data-stu-id="30cbd-323">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="30cbd-324">Этот параметр должен быть инициализирован.</span><span class="sxs-lookup"><span data-stu-id="30cbd-324">This parameter should be initialized.</span></span>  
<span data-ttu-id="30cbd-325">*ппкуеуе* \[ out \] возвращает инициализированный объект.</span><span class="sxs-lookup"><span data-stu-id="30cbd-325">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="30cbd-326">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="30cbd-326">**Remarks**</span></span>

<span data-ttu-id="30cbd-327">Можно клонировать из любого существующего объекта очереди, даже если он не является корневым.</span><span class="sxs-lookup"><span data-stu-id="30cbd-327">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="30cbd-328">идксгикссурфацеконсумер</span><span class="sxs-lookup"><span data-stu-id="30cbd-328">IDXGIXSurfaceConsumer</span></span>

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



<span data-ttu-id="30cbd-329">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="30cbd-329">**Parameters**</span></span>  
<span data-ttu-id="30cbd-330">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="30cbd-330">*id* \[in\]</span></span>  
<span data-ttu-id="30cbd-331">РЕФИИД двухмерной поверхности устройства.</span><span class="sxs-lookup"><span data-stu-id="30cbd-331">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="30cbd-332">Для IDirect3DDevice9 РЕФИИД должен быть \_ \_ Ууидоф (IDirect3DTexture9).</span><span class="sxs-lookup"><span data-stu-id="30cbd-332">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="30cbd-333">Для ID3D10Device РЕФИИД должен быть \_ \_ Ууидоф (ID3D10Texture2D).</span><span class="sxs-lookup"><span data-stu-id="30cbd-333">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="30cbd-334">Для ID3D11Device РЕФИИД должен быть \_ \_ Ууидоф (ID3D11Texture2D).</span><span class="sxs-lookup"><span data-stu-id="30cbd-334">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="30cbd-335">*ппсурфаце* \[ out \] возвращает указатель на поверхность.</span><span class="sxs-lookup"><span data-stu-id="30cbd-335">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="30cbd-336">*pBuffer* \[ в, out \] необязательный параметр и, если Not **null**, при возврате содержит метаданные, переданные в соответствующий вызов очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-336">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="30cbd-337">*пбуфферсизе* \[ в \] *выpBuffer* размер в байтах.</span><span class="sxs-lookup"><span data-stu-id="30cbd-337">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="30cbd-338">Возвращает число байтов, возвращенных в *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="30cbd-338">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="30cbd-339">Если в вызове очереди не предоставлены метаданные, *pBuffer* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="30cbd-339">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="30cbd-340">*двтимеаут* \[ в \] задает значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="30cbd-340">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="30cbd-341">Дополнительные сведения см. в комментариях.</span><span class="sxs-lookup"><span data-stu-id="30cbd-341">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="30cbd-342">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="30cbd-342">**Return Values**</span></span>

<span data-ttu-id="30cbd-343">Эта функция может возвращать \_ время ожидания, если задано значение времени ожидания и функция не возвращает значение до истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="30cbd-343">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="30cbd-344">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="30cbd-344">See Remarks.</span></span> <span data-ttu-id="30cbd-345">Если нет доступных поверхностей, функция возвращает параметру WITH *ппсурфаце* значение **null**, *пбуфферсизе* значение 0, а возвращаемое значение — 0x80070120 (для Win32 \_ — \_ HRESULT ( \_ время ожидания ожидания)).</span><span class="sxs-lookup"><span data-stu-id="30cbd-345">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="30cbd-346">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="30cbd-346">**Remarks**</span></span>

<span data-ttu-id="30cbd-347">Этот API может блокироваться, если очередь пуста.</span><span class="sxs-lookup"><span data-stu-id="30cbd-347">This API can block if the queue is empty.</span></span> <span data-ttu-id="30cbd-348">Параметр *двтимеаут* работает идентично API-интерфейсам синхронизации Windows, таким как WaitForSingleObject.</span><span class="sxs-lookup"><span data-stu-id="30cbd-348">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="30cbd-349">Для поведения без блокировки используйте значение времени ожидания 0.</span><span class="sxs-lookup"><span data-stu-id="30cbd-349">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="30cbd-350">исурфацепродуцер</span><span class="sxs-lookup"><span data-stu-id="30cbd-350">ISurfaceProducer</span></span>

<span data-ttu-id="30cbd-351">Этот интерфейс предоставляет два метода, которые позволяют приложению ставить в очередь поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-351">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="30cbd-352">После того как поверхность помещается в очередь, указатель поверхности становится недействительным и ненадежным для использования.</span><span class="sxs-lookup"><span data-stu-id="30cbd-352">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="30cbd-353">Единственным действием, которое приложение должно выполнить с помощью указателя, является его освобождение.</span><span class="sxs-lookup"><span data-stu-id="30cbd-353">The only action that the application should perform with the pointer is to release it.</span></span>



| <span data-ttu-id="30cbd-354">Метод</span><span class="sxs-lookup"><span data-stu-id="30cbd-354">Method</span></span>                          | <span data-ttu-id="30cbd-355">Описание</span><span class="sxs-lookup"><span data-stu-id="30cbd-355">Description</span></span>                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30cbd-356">Исурфацепродуцер:: поставить в очередь</span><span class="sxs-lookup"><span data-stu-id="30cbd-356">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="30cbd-357">Помещает поверхность в очередь для объекта очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-357">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="30cbd-358">По завершении этого вызова Производитель выполняет действия с поверхностью, а поверхность — готовой для другого устройства.</span><span class="sxs-lookup"><span data-stu-id="30cbd-358">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="30cbd-359">Исурфацепродуцер:: Flush</span><span class="sxs-lookup"><span data-stu-id="30cbd-359">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="30cbd-360">Используется, если приложения должны иметь поведение без блокировки.</span><span class="sxs-lookup"><span data-stu-id="30cbd-360">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="30cbd-361">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="30cbd-361">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="30cbd-362">**Постановка в очередь**</span><span class="sxs-lookup"><span data-stu-id="30cbd-362">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="30cbd-363">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="30cbd-363">**Parameters**</span></span>  
<span data-ttu-id="30cbd-364">*псурфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="30cbd-364">*pSurface* \[in\]</span></span>  
<span data-ttu-id="30cbd-365">Поверхность создающего устройства, которая должна быть поставлена в очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-365">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="30cbd-366">Эта Рабочая область должна быть выведена из очереди из той же сети очередей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-366">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="30cbd-367">*pBuffer* \[ в \] необязательном параметре, который используется для передачи метаданных.</span><span class="sxs-lookup"><span data-stu-id="30cbd-367">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="30cbd-368">Он должен указывать на данные, которые будут переданы в вызов вывода из очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-368">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="30cbd-369">*BufferSize* \[ \] размер *pBuffer* в байтах.</span><span class="sxs-lookup"><span data-stu-id="30cbd-369">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="30cbd-370">*Флаги* \[ в \] необязательном параметре, который управляет поведением этой функции.</span><span class="sxs-lookup"><span data-stu-id="30cbd-370">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="30cbd-371">Единственный флаг — \_ флаг очереди поверхности \_ — \_ \_ не \_ ждать.</span><span class="sxs-lookup"><span data-stu-id="30cbd-371">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="30cbd-372">Дополнительные сведения см. в примечаниях к диску.</span><span class="sxs-lookup"><span data-stu-id="30cbd-372">See the Remarks for Flush.</span></span> <span data-ttu-id="30cbd-373">Если флаг не передается (*flags* = = 0), используется поведение блокировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30cbd-373">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="30cbd-374">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="30cbd-374">**Return Values**</span></span>

<span data-ttu-id="30cbd-375">Эта функция может возвращать \_ ошибку \_ DXGI \_ , если не используется флаг " \_ флаг" \_ очереди поверхности \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="30cbd-375">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="30cbd-376">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="30cbd-376">**Remarks**</span></span>

-   <span data-ttu-id="30cbd-377">Эта функция помещает поверхность в очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-377">This function puts the surface on the queue.</span></span> <span data-ttu-id="30cbd-378">Если в приложении не указан \_ флаг очереди поверхности \_ \_ , то \_ \_ Эта функция блокируется и ВЫПОЛНЯЕТ синхронизацию GPU-ЦП, чтобы гарантировать, что вся отрисовка на поверхности в очереди завершена.</span><span class="sxs-lookup"><span data-stu-id="30cbd-378">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="30cbd-379">Если эта функция выполнена, поверхность будет доступна для вывода из очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-379">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="30cbd-380">Если требуется Неблокирующее поведение, используйте флаг "не \_ \_ ожидать".</span><span class="sxs-lookup"><span data-stu-id="30cbd-380">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="30cbd-381">Дополнительные сведения см. в разделе Flush ().</span><span class="sxs-lookup"><span data-stu-id="30cbd-381">See Flush() for details.</span></span>
-   <span data-ttu-id="30cbd-382">Согласно правилам подсчета ссылок COM, поверхность, возвращаемая функцией вывода из очереди, будет иметь AddRef (), поэтому приложению не нужно делать это.</span><span class="sxs-lookup"><span data-stu-id="30cbd-382">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="30cbd-383">После вызова очереди приложение должно освободить поверхность, так как она больше не используется.</span><span class="sxs-lookup"><span data-stu-id="30cbd-383">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="30cbd-384">**Очистка**</span><span class="sxs-lookup"><span data-stu-id="30cbd-384">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="30cbd-385">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="30cbd-385">**Parameters**</span></span>  
<span data-ttu-id="30cbd-386">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="30cbd-386">*Flags* \[in\]</span></span>  
<span data-ttu-id="30cbd-387">Единственный флаг — \_ флаг очереди поверхности \_ — \_ \_ не \_ ждать.</span><span class="sxs-lookup"><span data-stu-id="30cbd-387">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="30cbd-388">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="30cbd-388">See Remarks.</span></span> <span data-ttu-id="30cbd-389">*нсурфацес* \[ out \] возвращает количество поверхностей, которые все еще находятся в состоянии ожидания и не сбрасываются.</span><span class="sxs-lookup"><span data-stu-id="30cbd-389">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="30cbd-390">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="30cbd-390">**Return Values**</span></span>

<span data-ttu-id="30cbd-391">Эта функция может возвращать \_ ошибку \_ DXGI \_ \_ , если не используется флаг \_ флага очереди поверхности " \_ \_ \_ не ожидать" \_ .</span><span class="sxs-lookup"><span data-stu-id="30cbd-391">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="30cbd-392">Эта функция возвращает значение \_ ОК, если все поверхности были успешно сброшены.</span><span class="sxs-lookup"><span data-stu-id="30cbd-392">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="30cbd-393">Эта функция возвращает \_ ошибку DXGI \_ \_ , пока \_ не была очищена ни одна из поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-393">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="30cbd-394">Вместе возвращаемое значение и *нсурфацес* указывают приложению, какая работа была выполнена, и если какая-то работа остается действительной.</span><span class="sxs-lookup"><span data-stu-id="30cbd-394">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="30cbd-395">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="30cbd-395">**Remarks**</span></span>

<span data-ttu-id="30cbd-396">Flush имеет смысл только в том случае, если предыдущий вызов в очередь использовал флаг "не ожидать". \_ \_ в противном случае он будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="30cbd-396">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="30cbd-397">Если при вызове в очередь использовался \_ флаг "не \_ ожидать", постановка в очередь выполняется немедленно и синхронизация GPU-CPU не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="30cbd-397">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="30cbd-398">Поверхность по-прежнему считается поставленной в очередь. устройство, производящее работу, не может продолжать его использовать, но недоступно для вывода из очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-398">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="30cbd-399">Чтобы попытаться зафиксировать поверхность для вывода из очереди, необходимо вызвать Flush.</span><span class="sxs-lookup"><span data-stu-id="30cbd-399">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="30cbd-400">Сброс пытается зафиксировать все поверхности, которые в настоящий момент поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-400">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="30cbd-401">Если в параметре Flush не передается флаг, он блокирует и очищает всю очередь, подготавливая все поверхности в ней для вывода из очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-401">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="30cbd-402">Если \_ \_ используется флаг «не ожидать ожидания», то очередь будет проверять поверхности, чтобы узнать, готовы ли они к работе; этот шаг не блокируется.</span><span class="sxs-lookup"><span data-stu-id="30cbd-402">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="30cbd-403">Поверхности, для которых завершена синхронизация GPU и ЦП, будут готовы для устройства потребителя.</span><span class="sxs-lookup"><span data-stu-id="30cbd-403">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="30cbd-404">Поверхности, которые все еще ожидают обработки, не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="30cbd-404">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="30cbd-405">Функция возвращает количество поверхностей, которые все еще необходимо сбросить.</span><span class="sxs-lookup"><span data-stu-id="30cbd-405">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="30cbd-406">Сброс не нарушает семантику очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-406">Flush will not break the queue semantics.</span></span> <span data-ttu-id="30cbd-407">API гарантирует, что поверхности, поставленные в очередь первыми, будут зафиксированы до последующей постановки поверхностей, независимо от того, когда происходит синхронизация GPU и ЦП.</span><span class="sxs-lookup"><span data-stu-id="30cbd-407">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="30cbd-408">Помощник по взаимодействию Direct3D 9Ex и DXGI: как использовать</span><span class="sxs-lookup"><span data-stu-id="30cbd-408">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="30cbd-409">Мы планируем использовать в большинстве случаев использование двух устройств, совместно использующих несколько поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-409">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="30cbd-410">Поскольку это также является простейшим сценарием, в этом документе подробно описывается использование API-интерфейсов для достижения этой цели, обсуждается неблокирующесть вариации и заканчивается краткий раздел об инициализации для трех устройств.</span><span class="sxs-lookup"><span data-stu-id="30cbd-410">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="30cbd-411">Два устройства</span><span class="sxs-lookup"><span data-stu-id="30cbd-411">Two Devices</span></span>

<span data-ttu-id="30cbd-412">Пример приложения, использующего этот вспомогательный метод, может одновременно использовать Direct3D 9Ex и Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="30cbd-412">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="30cbd-413">Приложение может обрабатывать содержимое на обоих устройствах и представлять содержимое с помощью Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="30cbd-413">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="30cbd-414">Обработка может означать визуализацию содержимого, декодирование видео, запуск шейдеров вычислений и т. д.</span><span class="sxs-lookup"><span data-stu-id="30cbd-414">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="30cbd-415">Для каждого кадра приложение сначала будет работать с Direct3D 11, затем обрабатываться с помощью Direct3D 9 и, наконец, с Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="30cbd-415">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="30cbd-416">Более того, при обработке с помощью Direct3D 11 будут получены некоторые метаданные, которые необходимо будет использовать в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="30cbd-416">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="30cbd-417">В этом разделе рассматривается использование вспомогательного метода в трех компонентах, соответствующих этой последовательности: инициализация, главный цикл и очистка.</span><span class="sxs-lookup"><span data-stu-id="30cbd-417">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="30cbd-418">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="30cbd-418">**Initialization**</span></span>  
<span data-ttu-id="30cbd-419">Инициализация включает следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="30cbd-419">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="30cbd-420">Инициализируйте оба устройства.</span><span class="sxs-lookup"><span data-stu-id="30cbd-420">Initialize both devices.</span></span>
2.  <span data-ttu-id="30cbd-421">Создайте корневую очередь: m \_ 11to9Queue.</span><span class="sxs-lookup"><span data-stu-id="30cbd-421">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="30cbd-422">Клонировать из корневой очереди: m \_ 9to11Queue.</span><span class="sxs-lookup"><span data-stu-id="30cbd-422">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="30cbd-423">Вызовите Опенпродуцер/Опенконсумер в обеих очередях.</span><span class="sxs-lookup"><span data-stu-id="30cbd-423">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="30cbd-424">В именах очередей используются цифры от 9 до 11, чтобы указать, какой API _является производителем_, а что является потребителем: **\_ m\*\*\*_в_**_очередь_\* потребителя.</span><span class="sxs-lookup"><span data-stu-id="30cbd-424">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_**_producer_*_to_*_consumer_*_Queue_*.</span></span> <span data-ttu-id="30cbd-425">Соответственно, m \_ 11to9Queue указывает очередь, для которой устройство Direct3D 11 создает поверхности, используемые устройством Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="30cbd-425">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="30cbd-426">Аналогичным образом, m \_ 9to11Queue указывает очередь, для которой Direct3D 9 создает поверхности, потребляемые Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="30cbd-426">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="30cbd-427">Корневая очередь изначально заполнена, а все клонированные очереди изначально пусты.</span><span class="sxs-lookup"><span data-stu-id="30cbd-427">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="30cbd-428">Это не должно быть проблемой для приложения, за исключением первого цикла постановки в очередь и вывода из очереди и доступности метаданных.</span><span class="sxs-lookup"><span data-stu-id="30cbd-428">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="30cbd-429">Если при выводе запроса на получение метаданных из очереди не было задано ни одного из них (так как ничего не произошло или если очередь не установила ничего), вывод из очереди не получит никаких метаданных.</span><span class="sxs-lookup"><span data-stu-id="30cbd-429">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="30cbd-430">**Инициализируйте оба устройства.**</span><span class="sxs-lookup"><span data-stu-id="30cbd-430">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="30cbd-431">**Создайте корневую очередь.**</span><span class="sxs-lookup"><span data-stu-id="30cbd-431">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="30cbd-432">На этом шаге также создаются поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-432">This step also creates the surfaces.</span></span> <span data-ttu-id="30cbd-433">Ограничения размера и формата идентичны созданию общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="30cbd-433">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="30cbd-434">Размер буфера метаданных фиксируется во время создания, и в этом случае мы просто передаем UINT.</span><span class="sxs-lookup"><span data-stu-id="30cbd-434">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="30cbd-435">Очередь должна быть создана с фиксированным числом поверхностей.</span><span class="sxs-lookup"><span data-stu-id="30cbd-435">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="30cbd-436">Производительность будет зависеть от сценария.</span><span class="sxs-lookup"><span data-stu-id="30cbd-436">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="30cbd-437">Наличие нескольких поверхностей увеличивает вероятность того, что устройства заняты.</span><span class="sxs-lookup"><span data-stu-id="30cbd-437">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="30cbd-438">Например, если имеется только одна поверхность, то не будет параллелизации между двумя устройствами.</span><span class="sxs-lookup"><span data-stu-id="30cbd-438">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="30cbd-439">С другой стороны, увеличение количества поверхностей увеличивает объем памяти, что может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="30cbd-439">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="30cbd-440">В этом примере используются две поверхности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-440">This example uses two surfaces.</span></span>  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  <span data-ttu-id="30cbd-441">**Клонировать корневую очередь.**</span><span class="sxs-lookup"><span data-stu-id="30cbd-441">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="30cbd-442">Каждая клонированная очередь должна использовать одни и те же поверхности, но может иметь разные размеры буфера метаданных и другие флаги.</span><span class="sxs-lookup"><span data-stu-id="30cbd-442">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="30cbd-443">В этом случае нет метаданных от Direct3D 9 до Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="30cbd-443">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="30cbd-444">**Откройте устройство Producer и потребитель.**</span><span class="sxs-lookup"><span data-stu-id="30cbd-444">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="30cbd-445">Приложение должно выполнить этот шаг перед вызовом постановки в очередь и вывода из очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-445">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="30cbd-446">При открытии производителя и потребителя возвращаются интерфейсы, которые содержат API постановки в очередь или из очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-446">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="30cbd-447">**Главный цикл**</span><span class="sxs-lookup"><span data-stu-id="30cbd-447">**Main Loop**</span></span>  
<span data-ttu-id="30cbd-448">Использование очереди моделируется после классической проблемы с производителем или потребителем.</span><span class="sxs-lookup"><span data-stu-id="30cbd-448">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="30cbd-449">Это следует рассматривать с точки зрения каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="30cbd-449">Think of this from a per-device perspective.</span></span> <span data-ttu-id="30cbd-450">Каждое устройство должно выполнить следующие действия: вывести из очереди, чтобы получить поверхность из очереди использования, обработать на поверхности, а затем поставить в очередь на ее создание.</span><span class="sxs-lookup"><span data-stu-id="30cbd-450">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="30cbd-451">Для устройства Direct3D 11 использование Direct3D 9 почти идентично.</span><span class="sxs-lookup"><span data-stu-id="30cbd-451">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



<span data-ttu-id="30cbd-452">**Очистка**</span><span class="sxs-lookup"><span data-stu-id="30cbd-452">**Cleaning Up**</span></span>  
<span data-ttu-id="30cbd-453">Этот шаг очень прост.</span><span class="sxs-lookup"><span data-stu-id="30cbd-453">This step is very straightforward.</span></span> <span data-ttu-id="30cbd-454">В дополнение к обычным действиям по очистке интерфейсов API Direct3D приложение должно освободить COM-интерфейсы возврата.</span><span class="sxs-lookup"><span data-stu-id="30cbd-454">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="30cbd-455">Использование без блокировки</span><span class="sxs-lookup"><span data-stu-id="30cbd-455">Non-Blocking Use</span></span>

<span data-ttu-id="30cbd-456">Предыдущий пример имеет смысл для многопоточных случаев использования, в которых каждое устройство имеет собственный поток.</span><span class="sxs-lookup"><span data-stu-id="30cbd-456">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="30cbd-457">В примере используются блокирующие версии API-интерфейсов: бесконечно для времени ожидания и флаги для постановки в очередь.</span><span class="sxs-lookup"><span data-stu-id="30cbd-457">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="30cbd-458">Если вы хотите использовать вспомогательную функцию без блокировки, необходимо внести несколько изменений.</span><span class="sxs-lookup"><span data-stu-id="30cbd-458">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="30cbd-459">В этом разделе показано Неблокирующее использование с обоими устройствами в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="30cbd-459">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="30cbd-460">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="30cbd-460">**Initialization**</span></span>  
<span data-ttu-id="30cbd-461">Инициализация идентична за исключением флагов.</span><span class="sxs-lookup"><span data-stu-id="30cbd-461">Initialization is identical except for the flags.</span></span> <span data-ttu-id="30cbd-462">Так как приложение является однопотоковым, используйте этот флаг для создания.</span><span class="sxs-lookup"><span data-stu-id="30cbd-462">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="30cbd-463">Это выключает часть кода синхронизации, что может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="30cbd-463">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



<span data-ttu-id="30cbd-464">Открытие устройств производителя и потребителя аналогично тому, как показано в примере блокировки.</span><span class="sxs-lookup"><span data-stu-id="30cbd-464">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="30cbd-465">**Использование очереди**</span><span class="sxs-lookup"><span data-stu-id="30cbd-465">**Using the Queue**</span></span>  
<span data-ttu-id="30cbd-466">Существует множество способов использования очереди в неблокирующем режиме с различными характеристиками производительности.</span><span class="sxs-lookup"><span data-stu-id="30cbd-466">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="30cbd-467">Следующий пример прост, но имеет низкую производительность из-за чрезмерного цикла и опроса.</span><span class="sxs-lookup"><span data-stu-id="30cbd-467">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="30cbd-468">Несмотря на эти проблемы, в примере показано, как использовать вспомогательную функцию.</span><span class="sxs-lookup"><span data-stu-id="30cbd-468">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="30cbd-469">Подход состоит в том, чтобы постоянно находиться в цикле и выставить в очередь, процесс, поставить в очередь и очистить.</span><span class="sxs-lookup"><span data-stu-id="30cbd-469">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="30cbd-470">Если какие-либо из шагов завершаются неудачей, так как ресурс недоступен, приложение просто пытается снова выполнить следующий цикл.</span><span class="sxs-lookup"><span data-stu-id="30cbd-470">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



<span data-ttu-id="30cbd-471">Более сложное решение может проверять возвращаемое значение из постановки в очередь и с записи на диск, чтобы определить, требуется ли очистка.</span><span class="sxs-lookup"><span data-stu-id="30cbd-471">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="30cbd-472">Три устройства</span><span class="sxs-lookup"><span data-stu-id="30cbd-472">Three Devices</span></span>

<span data-ttu-id="30cbd-473">Расширение предыдущих примеров для охвата нескольких устройств — это просто.</span><span class="sxs-lookup"><span data-stu-id="30cbd-473">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="30cbd-474">Следующий код выполняет инициализацию.</span><span class="sxs-lookup"><span data-stu-id="30cbd-474">The following code performs the initialization.</span></span> <span data-ttu-id="30cbd-475">После создания объектов producer/consumer код для их использования будет одинаковым.</span><span class="sxs-lookup"><span data-stu-id="30cbd-475">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="30cbd-476">В этом примере есть три устройства, и, следовательно, три очереди.</span><span class="sxs-lookup"><span data-stu-id="30cbd-476">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="30cbd-477">Передает поток с Direct3D 9 на Direct3D 10 на Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="30cbd-477">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



<span data-ttu-id="30cbd-478">Как упоминалось ранее, клонирование работает так же, независимо от того, какая очередь клонируется.</span><span class="sxs-lookup"><span data-stu-id="30cbd-478">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="30cbd-479">Например, второй вызов клонирования мог быть отключен от \_ объекта 9to10Queue m.</span><span class="sxs-lookup"><span data-stu-id="30cbd-479">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a><span data-ttu-id="30cbd-480">Заключение</span><span class="sxs-lookup"><span data-stu-id="30cbd-480">Conclusion</span></span>

<span data-ttu-id="30cbd-481">Вы можете создавать решения, использующие взаимодействие, чтобы использовать возможности нескольких API DirectX.</span><span class="sxs-lookup"><span data-stu-id="30cbd-481">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="30cbd-482">Взаимодействие API графических интерфейсов Windows теперь предлагает стандартную среду выполнения для управления поверхностью 1,1.</span><span class="sxs-lookup"><span data-stu-id="30cbd-482">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="30cbd-483">Эта среда выполнения позволяет использовать синхронизированную поддержку общего доступа к поверхности в новых интерфейсах API, таких как Direct3D 11, Direct3D 10,1 и Direct2D.</span><span class="sxs-lookup"><span data-stu-id="30cbd-483">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="30cbd-484">Улучшения взаимодействия между новыми API-интерфейсами и существующими API-интерфейсами упрощают перенос приложений и обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="30cbd-484">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="30cbd-485">Интерфейсы API потребителя 9Ex и DXGI 1,1 могут взаимодействовать, как показано в механизме синхронизации, предоставленном с помощью примера вспомогательного кода в коллекции кода MSDN.</span><span class="sxs-lookup"><span data-stu-id="30cbd-485">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 