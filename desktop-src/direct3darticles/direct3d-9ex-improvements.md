---
title: Улучшения в Direct3D 9Ex
description: В этом разделе описывается добавлена поддержка режима перелистывания в Windows 7 и связанная с ней статистика в Direct3D 9Ex и диспетчер окон рабочего стола.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413419"
---
# <a name="direct3d-9ex-improvements"></a><span data-ttu-id="e24aa-103">Улучшения в Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="e24aa-103">Direct3D 9Ex improvements</span></span>

<span data-ttu-id="e24aa-104">В этом разделе описывается добавлена поддержка режима перелистывания в Windows 7 и связанная с ней статистика в Direct3D 9Ex и диспетчер окон рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e24aa-104">This topic describes Windows 7's added support for Flip Mode Present and its associated present statistics in Direct3D 9Ex and Desktop Window Manager.</span></span> <span data-ttu-id="e24aa-105">Целевые приложения включают приложения для показа видео или частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="e24aa-105">Target applications include video or frame rate-based presentation applications.</span></span> <span data-ttu-id="e24aa-106">Приложения, использующие режим отражения Direct3D 9Ex, предоставляют возможность снизить нагрузку на системные ресурсы при включенном DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-106">Applications that use Direct3D 9Ex Flip Mode Present reduce the system resource load when DWM is enabled.</span></span> <span data-ttu-id="e24aa-107">Предоставление улучшений статистики, связанных с режимом отражения, позволяет приложениям Direct3D 9Ex лучше управлять скоростью презентации, предоставляя механизмы обратной связи и исправления в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="e24aa-107">Present statistics enhancements associated with Flip Mode Present enable Direct3D 9Ex applications to better control the rate of presentation by providing real-time feedback and correction mechanisms.</span></span> <span data-ttu-id="e24aa-108">Включены подробные пояснения и указатели на примеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e24aa-108">Detailed explanations and pointers to sample resources are included.</span></span>

<span data-ttu-id="e24aa-109">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="e24aa-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e24aa-110">Улучшены возможности Direct3D 9Ex для Windows 7</span><span class="sxs-lookup"><span data-stu-id="e24aa-110">What's Improved about Direct3D 9Ex for Windows 7</span></span>](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [<span data-ttu-id="e24aa-111">Представление режима отражения Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="e24aa-111">Direct3D 9EX Flip Mode Presentation</span></span>](#direct3d-9ex-flip-mode-presentation)
-   [<span data-ttu-id="e24aa-112">Модель программирования и API</span><span class="sxs-lookup"><span data-stu-id="e24aa-112">Programming Model and APIs</span></span>](#programming-model-and-apis)
    -   [<span data-ttu-id="e24aa-113">Как принять участие в модели отражения Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="e24aa-113">How to Opt Into the Direct3D 9Ex Flip Model</span></span>](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [<span data-ttu-id="e24aa-114">Рекомендации по проектированию для приложений модели 9Ex для отражения Direct3D</span><span class="sxs-lookup"><span data-stu-id="e24aa-114">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="e24aa-115">Синхронизация кадров для приложений модели перелистывания Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="e24aa-115">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="e24aa-116">Синхронизация кадров для оконных приложений при отключенном DWM</span><span class="sxs-lookup"><span data-stu-id="e24aa-116">Frame Synchronization for Windowed Applications When DWM is Off</span></span>](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [<span data-ttu-id="e24aa-117">Пошаговое руководство по модели перелистывания Direct3D 9Ex и представлению статистики</span><span class="sxs-lookup"><span data-stu-id="e24aa-117">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [<span data-ttu-id="e24aa-118">Сводка рекомендаций по программированию для синхронизации кадров</span><span class="sxs-lookup"><span data-stu-id="e24aa-118">Summary of Programming Recommendations for Frame Synchronization</span></span>](#summary-of-programming-recommendations-for-frame-synchronization)
-   [<span data-ttu-id="e24aa-119">Заключение об улучшениях Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="e24aa-119">Conclusion about Direct3D 9Ex Improvements</span></span>](#conclusion-about-direct3d-9ex-improvements)
-   [<span data-ttu-id="e24aa-120">Вызов действия</span><span class="sxs-lookup"><span data-stu-id="e24aa-120">Call to Action</span></span>](#call-to-action)
-   [<span data-ttu-id="e24aa-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e24aa-121">Related topics</span></span>](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a><span data-ttu-id="e24aa-122">Улучшены возможности Direct3D 9Ex для Windows 7</span><span class="sxs-lookup"><span data-stu-id="e24aa-122">What's Improved about Direct3D 9Ex for Windows 7</span></span>

<span data-ttu-id="e24aa-123">Режим отражения представления Direct3D 9Ex — это улучшенный режим показа образов в Direct3D 9Ex, который эффективно передает готовые изображения в Windows 7 диспетчер окон рабочего стола (DWM) для компоновки.</span><span class="sxs-lookup"><span data-stu-id="e24aa-123">Flip Mode Presentation of Direct3D 9Ex is an improved mode of presenting images in Direct3D 9Ex that efficiently hands off rendered images to Windows 7 Desktop Window Manager (DWM) for composition.</span></span> <span data-ttu-id="e24aa-124">Начиная с Windows Vista DWM формирует весь Настольный компьютер.</span><span class="sxs-lookup"><span data-stu-id="e24aa-124">Beginning in Windows Vista, DWM composes the entire Desktop.</span></span> <span data-ttu-id="e24aa-125">Когда DWM включен, приложения с оконным режимом представляют свое содержимое на рабочем столе с помощью метода с именем БЛТ Mode, представленного DWM (или БЛТ Model).</span><span class="sxs-lookup"><span data-stu-id="e24aa-125">When DWM is enabled, windowed mode applications present their contents on the Desktop by using a method called Blt Mode Present to DWM (or Blt Model).</span></span> <span data-ttu-id="e24aa-126">При использовании модели БЛТ DWM сохраняет копию поверхности визуализации Direct3D 9Ex для композиции рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e24aa-126">With Blt Model, DWM maintains a copy of the Direct3D 9Ex rendered surface for Desktop composition.</span></span> <span data-ttu-id="e24aa-127">При обновлении приложения новое содержимое копируется на поверхность DWM через БЛТ.</span><span class="sxs-lookup"><span data-stu-id="e24aa-127">When the application updates, the new content is copied to the DWM surface through a blt.</span></span> <span data-ttu-id="e24aa-128">Для приложений, содержащих Direct3D и GDI, данные GDI также копируются на поверхность DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-128">For applications that contain Direct3D and GDI content, the GDI data is also copied onto the DWM surface.</span></span>

<span data-ttu-id="e24aa-129">В Windows 7 режим отражения, представленный в DWM (или отражение модели), — это новый метод представления, который, по сути, позволяет передавать дескрипторы областей приложений между приложениями оконного режима и DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-129">Available in Windows 7, Flip Mode Present to DWM (or Flip Model) is a new presentation method that essentially enables passing handles of application surfaces between windowed mode applications and DWM.</span></span> <span data-ttu-id="e24aa-130">Помимо сохранения ресурсов, модель отражения поддерживает улучшенную текущую статистику.</span><span class="sxs-lookup"><span data-stu-id="e24aa-130">In addition to saving resources, Flip Model supports enhanced present statistics.</span></span>

<span data-ttu-id="e24aa-131">Эта статистика представляет собой сведения о времени кадров, которые приложения могут использовать для синхронизации видеопотоков и звуковых потоков, а также для восстановления после сбоев воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="e24aa-131">Present statistics are frame-timing information that applications can use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="e24aa-132">Сведения о времени кадров в представленной статистике позволяют приложениям настраивать скорость показа видеокадров для более гладких презентаций.</span><span class="sxs-lookup"><span data-stu-id="e24aa-132">The frame-timing information in present statistics allows applications to adjust the presentation rate of their video frames for smoother presentation.</span></span> <span data-ttu-id="e24aa-133">В Windows Vista, где DWM поддерживает соответствующую копию области кадров для композиции рабочего стола, приложения могут использовать представленную статистику, предоставляемую DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-133">In Windows Vista, where DWM maintains a corresponding copy of the frame surface for Desktop composition, applications can use present statistics provided by DWM.</span></span> <span data-ttu-id="e24aa-134">Этот метод получения текущей статистики будет по-прежнему доступен в Windows 7 для существующих приложений.</span><span class="sxs-lookup"><span data-stu-id="e24aa-134">This method of obtaining present statistics will still be available in Windows 7 for existing applications.</span></span>

<span data-ttu-id="e24aa-135">В Windows 7 приложения на основе Direct3D 9Ex, использующие модель отражения, должны использовать интерфейсы API D3D9Ex для получения текущей статистики.</span><span class="sxs-lookup"><span data-stu-id="e24aa-135">In Windows 7, Direct3D 9Ex-based applications that adopt Flip Model should use D3D9Ex APIs to obtain present statistics.</span></span> <span data-ttu-id="e24aa-136">Когда DWM включен, в оконном режиме и полноэкранном режиме монопольного режима Direct3D 9Ex приложения могут рассчитывать на одни и те же данные статистики при использовании модели перелистывания.</span><span class="sxs-lookup"><span data-stu-id="e24aa-136">When DWM is enabled, windowed mode and full-screen exclusive mode Direct3D 9Ex applications can expect the same present statistics information when using Flip Model.</span></span> <span data-ttu-id="e24aa-137">Модель перелистывания Direct3D 9Ex, имеющая статистику. позволяет приложениям запрашивать статистические данные в режиме реального времени, а не после отображения кадра на экране; одни и те же данные статистики доступны для приложений с оконным режимом Flip-Model с поддержкой приложений в полноэкранном режиме. добавленный флаг в интерфейсах API D3D9Ex позволяет приложениям-шаблонам эффективно удалять последние кадры во время презентации.</span><span class="sxs-lookup"><span data-stu-id="e24aa-137">Direct3D 9Ex Flip Model present statistics enable applications to query for present statistics in real time, rather than after the frame has been shown on screen; the same present statistics information is available for windowed-mode Flip-Model enabled applications as full-screen applications; an added flag in D3D9Ex APIs allows Flip Model applications to effectively discard late frames at presentation time.</span></span>

<span data-ttu-id="e24aa-138">Модель перелистывания Direct3D 9Ex должна использоваться новыми приложениями для показа видео или кадров, которые предназначены для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e24aa-138">Direct3D 9Ex Flip Model should be used by new video or frame rate-based presentation applications that target Windows 7.</span></span> <span data-ttu-id="e24aa-139">Из-за синхронизации между DWM и средой выполнения Direct3D 9Ex в приложениях, использующих модель перелистывания, необходимо указать от 2 до 4 обратных буферов, чтобы обеспечить плавную презентацию.</span><span class="sxs-lookup"><span data-stu-id="e24aa-139">Because of the synchronization between DWM and the Direct3D 9Ex runtime, applications that use Flip Model should specify between 2 to 4 backbuffers to ensure smooth presentation.</span></span> <span data-ttu-id="e24aa-140">Для приложений, использующих данные о статистике, будет выгодно использовать улучшенную статистику.</span><span class="sxs-lookup"><span data-stu-id="e24aa-140">Those applications that use present statistics information will benefit from using Flip Model enabled present statistics enhancements.</span></span>

## <a name="direct3d-9ex-flip-mode-presentation"></a><span data-ttu-id="e24aa-141">Представление режима отражения Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="e24aa-141">Direct3D 9EX Flip Mode Presentation</span></span>

<span data-ttu-id="e24aa-142">Повышение производительности в режиме зеркального отражения Direct3D 9Ex имеет большое значение в системе, когда DWM включен и приложение находится в оконном режиме, а не в полноэкранном режиме монопольного доступа.</span><span class="sxs-lookup"><span data-stu-id="e24aa-142">Performance improvements of Direct3D 9Ex Flip Mode Present are significant on the system when DWM is on and when the application is in windowed mode, rather than in full screen exclusive mode.</span></span> <span data-ttu-id="e24aa-143">В следующей таблице и иллюстрации показано упрощенное Сравнение использования пропускной способности памяти и операций чтения и записи в приложениях с окнами, которые выбирают отразить модель относительно модели использования по умолчанию БЛТ.</span><span class="sxs-lookup"><span data-stu-id="e24aa-143">The following table and illustration show a simplified comparison of memory bandwidth usages and system reads and writes of windowed applications that choose Flip Model versus the default usage Blt Model.</span></span>



| <span data-ttu-id="e24aa-144">Режим БЛТ, представленный в DWM</span><span class="sxs-lookup"><span data-stu-id="e24aa-144">Blt mode present to DWM</span></span>                                                                                                 | <span data-ttu-id="e24aa-145">Режим перелистывания D3D9Ex, представленный в DWM</span><span class="sxs-lookup"><span data-stu-id="e24aa-145">D3D9Ex Flip Mode Present to DWM</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="e24aa-146">1. приложение обновляет свой кадр (Write).</span><span class="sxs-lookup"><span data-stu-id="e24aa-146">1. The application updates its frame (Write)</span></span><br/>                                                                 | <span data-ttu-id="e24aa-147">1. приложение обновляет свой кадр (Write).</span><span class="sxs-lookup"><span data-stu-id="e24aa-147">1. The application updates its frame (Write)</span></span><br/>                     |
| <span data-ttu-id="e24aa-148">2. Среда выполнения Direct3D копирует содержимое поверхности в поверхность перенаправления DWM (чтение, запись).</span><span class="sxs-lookup"><span data-stu-id="e24aa-148">2. Direct3D runtime copies surface contents to a DWM redirection surface (Read, Write)</span></span><br/>                       | <span data-ttu-id="e24aa-149">2. Среда выполнения Direct3D передает поверхность приложения в DWM</span><span class="sxs-lookup"><span data-stu-id="e24aa-149">2. Direct3D runtime passes the application surface to DWM</span></span><br/>        |
| <span data-ttu-id="e24aa-150">3. После завершения копирования в общей области DWM отображает на экране область приложения (чтение, запись).</span><span class="sxs-lookup"><span data-stu-id="e24aa-150">3. After the shared surface copy is completed, DWM renders the application surface onto screen (Read, Write)</span></span><br/> | <span data-ttu-id="e24aa-151">3. DWM отображает поверхность приложения на экране (чтение, запись).</span><span class="sxs-lookup"><span data-stu-id="e24aa-151">3. DWM renders the application surface onto screen (Read, Write)</span></span><br/> |



 

![Иллюстрация сравнения модели БЛТ и модели перелистывания](images/blt-flip-mode-present.png)

<span data-ttu-id="e24aa-153">Режим перелистывания представляет собой сокращение использования системной памяти за счет сокращения числа операций чтения и записи средой выполнения Direct3D для композиции оконных кадров с помощью DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-153">Flip Mode Present reduces system memory usage by reducing the number of reads and writes by the Direct3D runtime for the windowed frame composition by DWM.</span></span> <span data-ttu-id="e24aa-154">Это снижает энергопотребление системы и общее использование памяти.</span><span class="sxs-lookup"><span data-stu-id="e24aa-154">This reduces the system power consumption and overall memory usage.</span></span>

<span data-ttu-id="e24aa-155">Приложения могут воспользоваться преимуществами режима перелистывания Direct3D 9Ex, который предоставляет расширенные статистические данные, когда DWM включен, независимо от того, находится ли приложение в оконном режиме или в полноэкранном режиме монопольного доступа.</span><span class="sxs-lookup"><span data-stu-id="e24aa-155">Applications can take advantage of Direct3D 9Ex Flip Mode present statistics enhancements when DWM is on, regardless of whether the application is in windowed mode or in full screen exclusive mode.</span></span>

## <a name="programming-model-and-apis"></a><span data-ttu-id="e24aa-156">Модель программирования и API</span><span class="sxs-lookup"><span data-stu-id="e24aa-156">Programming Model and APIs</span></span>

<span data-ttu-id="e24aa-157">Новая частота видео или кадров — определении приложения, использующие API Direct3D 9Ex в Windows 7, могут использовать преимущества памяти и энергосбережения и улучшенную презентацию, предлагаемую режимом перелистывания при работе в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e24aa-157">New video or frame rate-gauging applications that use Direct3D 9Ex APIs on Windows 7 can take advantage of the memory and power savings and of the improved presentation offered by Flip Mode Present when running on Windows 7.</span></span> <span data-ttu-id="e24aa-158">(При запуске в предыдущих версиях Windows среда выполнения Direct3D по умолчанию использует приложение в режиме БЛТ.)</span><span class="sxs-lookup"><span data-stu-id="e24aa-158">(When running on previous Windows versions, the Direct3D runtime defaults the application to Blt Mode Present.)</span></span>

<span data-ttu-id="e24aa-159">Режим отражения подразумевает, что приложение может воспользоваться преимуществами отзывов и исправлений статистики в реальном времени, когда DWM включен.</span><span class="sxs-lookup"><span data-stu-id="e24aa-159">Flip Mode Present entails that the application can take advantage of real-time present statistics feedback and correction mechanisms when DWM is on.</span></span> <span data-ttu-id="e24aa-160">Однако приложения, использующие режим перелистывания, должны иметь представление об ограничениях при использовании параллельной отрисовки API GDI.</span><span class="sxs-lookup"><span data-stu-id="e24aa-160">However, applications that use Flip Mode Present should be aware of limitations when they use concurrent GDI API rendering.</span></span>

<span data-ttu-id="e24aa-161">Можно изменить существующие приложения, чтобы воспользоваться преимуществами режима перелистывания, с теми же преимуществами и предостережениями, что и у вновь разработанных приложений.</span><span class="sxs-lookup"><span data-stu-id="e24aa-161">You can modify existing applications to take advantage of Flip Mode Present, with the same benefits and caveats as the newly developed applications.</span></span>

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a><span data-ttu-id="e24aa-162">Как принять участие в модели отражения Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="e24aa-162">How to Opt Into the Direct3D 9Ex Flip Model</span></span>

<span data-ttu-id="e24aa-163">Приложения Direct3D 9Ex, предназначенные для Windows 7, могут выбрать модель перелистывания, создав цепочку буферов со значением перечисления [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="e24aa-163">Direct3D 9Ex applications that target Windows 7 can opt into the Flip Model by creating the swap chain with the [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) enumeration value.</span></span> <span data-ttu-id="e24aa-164">Чтобы принять участие в переворачивании модели, приложения определяют структуру [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) , а затем передают указатель на эту структуру при вызове API [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .</span><span class="sxs-lookup"><span data-stu-id="e24aa-164">To opt into the Flip Model, applications specify the [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) structure, and then pass a pointer to this structure when they call the [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API.</span></span> <span data-ttu-id="e24aa-165">В этом разделе описывается, как приложения, предназначенные для Windows 7, используют **IDirect3D9Ex:: креатедевицеекс** для выбора модели перелистывания.</span><span class="sxs-lookup"><span data-stu-id="e24aa-165">This section describes how applications that target Windows 7 use **IDirect3D9Ex::CreateDeviceEx** to opt into the Flip Model.</span></span> <span data-ttu-id="e24aa-166">Дополнительные сведения об API **IDirect3D9Ex:: креатедевицеекс** см. в разделе **IDirect3D9Ex:: креатедевицеекс на сайте MSDN**.</span><span class="sxs-lookup"><span data-stu-id="e24aa-166">For more information about the **IDirect3D9Ex::CreateDeviceEx** API, see **IDirect3D9Ex::CreateDeviceEx on MSDN**.</span></span>

<span data-ttu-id="e24aa-167">Для удобства синтаксис [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) и [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) повторяется здесь.</span><span class="sxs-lookup"><span data-stu-id="e24aa-167">For convenience, the syntax of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) and [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

<span data-ttu-id="e24aa-168">При изменении приложений Direct3D 9Ex для Windows 7 для выбора модели перелистывания следует учитывать следующие элементы об указанных членах [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):</span><span class="sxs-lookup"><span data-stu-id="e24aa-168">When you modify Direct3D 9Ex applications for Windows 7 to opt into the Flip Model, you should consider the following items about the specified members of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):</span></span>

<dl> <dt>

<span data-ttu-id="e24aa-169">**баккбуфферкаунт**</span><span class="sxs-lookup"><span data-stu-id="e24aa-169">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="e24aa-170">(Только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e24aa-170">(Windows 7 Only)</span></span>

<span data-ttu-id="e24aa-171">Если для **SwapEffect** задан новый \_ тип эффектов цепочки замены D3DSWAPEFFECT флипекс, то число задних буферов должно быть больше или равно 2, чтобы предотвратить снижение производительности приложения в результате ожидания освобождения предыдущего текущего буфера диспетчером DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-171">When **SwapEffect** is set to the new D3DSWAPEFFECT\_FLIPEX swap chain effect type, the back buffer count should be equal or greater than 2, to prevent an application performance penalty as a result of waiting on the previous Present buffer to be released by DWM.</span></span>

<span data-ttu-id="e24aa-172">Если приложение также использует представленную статистику, связанную с D3DSWAPEFFECT \_ флипекс, рекомендуется установить для счетчика задних буферов значение от 2 до 4.</span><span class="sxs-lookup"><span data-stu-id="e24aa-172">When the application also uses present statistics associated with D3DSWAPEFFECT\_FLIPEX, we recommend that you set the back buffer count to from 2 to 4.</span></span>

<span data-ttu-id="e24aa-173">Использование D3DSWAPEFFECT \_ флипекс в Windows Vista или предыдущих версиях операционной системы вернет ошибку [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="e24aa-173">Using D3DSWAPEFFECT\_FLIPEX on Windows Vista or previous operating system versions will return fail from [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

<span data-ttu-id="e24aa-174">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="e24aa-174">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="e24aa-175">(Только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e24aa-175">(Windows 7 Only)</span></span>

<span data-ttu-id="e24aa-176">Новый \_ тип эффектов цепочки D3DSWAPEFFECT флипекс swap определяет, когда приложение использует режим перелистывания, представленный в DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-176">The new D3DSWAPEFFECT\_FLIPEX swap chain effect type designates when an application is adopting Flip Mode Present to DWM.</span></span> <span data-ttu-id="e24aa-177">Это позволяет приложению более эффективно использовать память и мощь, а также позволяет приложению воспользоваться преимуществами полноэкранного представления статистики в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="e24aa-177">It allows the application more efficient usage of memory and power, and also enables the application to take advantage of full-screen present statistics in windowed mode.</span></span> <span data-ttu-id="e24aa-178">Поведение полноэкранного приложения не затрагивается.</span><span class="sxs-lookup"><span data-stu-id="e24aa-178">Full-screen application behavior is not affected.</span></span> <span data-ttu-id="e24aa-179">Если для параметра windowd задано значение **true** , а для **SwapEffect** задано значение D3DSWAPEFFECT \_ флипекс, среда выполнения создает один лишний обратный буфер и поворачивает каждый из них в буфер, который становится передним буфером во время презентации.</span><span class="sxs-lookup"><span data-stu-id="e24aa-179">If Windowed is set to **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIPEX, the runtime creates one extra back buffer and rotates whichever handle belongs to the buffer that becomes the front buffer at presentation time.</span></span>

</dd> <dt>

<span data-ttu-id="e24aa-180">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="e24aa-180">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="e24aa-181">(Только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e24aa-181">(Windows 7 Only)</span></span>

<span data-ttu-id="e24aa-182">Не удается установить флаг [D3DPRESENTFLAG \_ БЛОКИРУЕМого \_ буфера](/windows/desktop/direct3d9/d3dpresentflag) обмена, если для **SwapEffect** задан новый тип воздействия на цепочку замены [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="e24aa-182">The [D3DPRESENTFLAG\_LOCKABLE\_BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) flag cannot be set if **SwapEffect** is set to the new [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chain effect type.</span></span>

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="e24aa-183">Рекомендации по проектированию для приложений модели 9Ex для отражения Direct3D</span><span class="sxs-lookup"><span data-stu-id="e24aa-183">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="e24aa-184">Используйте рекомендации, приведенные в следующих разделах, чтобы разработать приложения модели отражения 9Ex Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e24aa-184">Use the guidelines in the following sections to design your Direct3D 9Ex Flip Model applications.</span></span>

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a><span data-ttu-id="e24aa-185">Использование режима отражения в отдельном HWND из режима БЛТ</span><span class="sxs-lookup"><span data-stu-id="e24aa-185">Use Flip Mode Present in a Separate HWND from Blt Mode Present</span></span>

<span data-ttu-id="e24aa-186">Приложения должны использовать режим перелистывания Direct3D 9Ex, имеющийся в HWND, который не предназначен для других API, включая режим БЛТ, который представляет Direct3D 9Ex, другие версии Direct3D или GDI.</span><span class="sxs-lookup"><span data-stu-id="e24aa-186">Applications should use Direct3D 9Ex Flip Mode Present in an HWND that is not also targeted by other APIs, including Blt Mode Present Direct3D 9Ex, other versions of Direct3D, or GDI.</span></span> <span data-ttu-id="e24aa-187">Режим отражения может использоваться для представления дочерним окнам; Таким образом, приложения могут использовать модель перелистывания, если она не смешана с моделью БЛТ в том же HWND, как показано на следующих иллюстрациях.</span><span class="sxs-lookup"><span data-stu-id="e24aa-187">Flip Mode Present can be used to present to child windows; that is, applications can use Flip Model when it is not mixed with Blt Model in the same HWND, as shown in the following illustrations.</span></span>

![Иллюстрация родительского окна Direct3D и дочернего окна GDI, каждый из которых имеет собственный HWND](images/parent-d3d.png)

![Иллюстрация родительского окна GDI и дочернего окна Direct3D, каждый из которых имеет собственный HWND](images/parent-gdi.png)

<span data-ttu-id="e24aa-190">Так как модель БЛТ поддерживает дополнительную копию поверхности, GDI и другие содержимое Direct3D можно добавить в один и тот же HWND через поэтапные обновления из Direct3D и GDI.</span><span class="sxs-lookup"><span data-stu-id="e24aa-190">Because Blt Model maintains an additional copy of the surface, GDI and other Direct3D contents can be added to the same HWND through piecemeal updates from Direct3D and GDI.</span></span> <span data-ttu-id="e24aa-191">С помощью модели перелистывания можно увидеть только содержимое Direct3D 9Ex в цепочках подкачки [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) , которые передаются в DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-191">Using the Flip Model, only Direct3D 9Ex content in [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chains that are passed to DWM will be visible.</span></span> <span data-ttu-id="e24aa-192">Все остальные обновления БЛТ модели Direct3D или GDI будут игнорироваться, как показано на следующих иллюстрациях.</span><span class="sxs-lookup"><span data-stu-id="e24aa-192">All other Blt Model Direct3D or GDI content updates will be ignored, as shown in the following illustrations.</span></span>

![Иллюстрация текста GDI, который может не отображаться, если используется модель перелистывания, а содержимое Direct3D и GDI находятся в одном HWND](images/d3d-gdi-same-hwnd.png)

![Иллюстрация содержимого Direct3D и GDI, в котором включены DWM и приложение находится в режиме с окнами](images/d3d-gdinotext-same-hwnd.png)

<span data-ttu-id="e24aa-195">Поэтому модель отражения должна быть включена для буферов цепочки подкачки, где только модель перелистывания Direct3D 9Ex отрисовывается во весь HWND.</span><span class="sxs-lookup"><span data-stu-id="e24aa-195">Therefore, Flip Model should be enabled for swap chain buffers surfaces where the Direct3D 9Ex Flip Model alone renders to the entire HWND.</span></span>

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a><span data-ttu-id="e24aa-196">Не используйте модель перелистывания с Скроллвиндов или Скроллвиндовекс GDI</span><span class="sxs-lookup"><span data-stu-id="e24aa-196">Do Not Use Flip Model with GDI's ScrollWindow or ScrollWindowEx</span></span>

<span data-ttu-id="e24aa-197">Некоторые приложения Direct3D 9Ex используют функции Скроллвиндов или Скроллвиндовекс GDI для обновления содержимого окна при активации события прокрутки пользователем.</span><span class="sxs-lookup"><span data-stu-id="e24aa-197">Some Direct3D 9Ex applications use GDI's ScrollWindow or ScrollWindowEx functions to update window contents when a user scroll event is triggered.</span></span> <span data-ttu-id="e24aa-198">Скроллвиндов и Скроллвиндовекс выполняют блтс содержимое окна на экране при прокрутке окна.</span><span class="sxs-lookup"><span data-stu-id="e24aa-198">ScrollWindow and ScrollWindowEx perform blts of window contents on screen as a window is scrolled.</span></span> <span data-ttu-id="e24aa-199">Эти функции также нуждаются в обновлениях модели БЛТ для содержимого GDI и Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="e24aa-199">These functions also require Blt Model updates for GDI and Direct3D 9Ex content.</span></span> <span data-ttu-id="e24aa-200">Приложения, использующие какую-либо функцию, не обязательно будут отображать видимое содержимое окна при прокрутке экрана, когда приложение находится в оконном режиме, а DWM включен.</span><span class="sxs-lookup"><span data-stu-id="e24aa-200">Applications that use either function will not necessarily display visible window contents scrolling on screen when the application is in windowed mode and DWM is enabled.</span></span> <span data-ttu-id="e24aa-201">Мы не рекомендуем использовать интерфейсы API Скроллвиндов и Скроллвиндовекс GDI в приложениях, а затем перерисовывать их содержимое на экране в ответ на прокрутку.</span><span class="sxs-lookup"><span data-stu-id="e24aa-201">We recommend that you not use GDI's ScrollWindow and ScrollWindowEx APIs in your applications, and instead redraw their contents on screen in response to scrolling.</span></span>

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a><span data-ttu-id="e24aa-202">Использовать одну \_ цепь перекачки D3DSWAPEFFECT флипекс на HWND</span><span class="sxs-lookup"><span data-stu-id="e24aa-202">Use One D3DSWAPEFFECT\_FLIPEX Swap Chain per HWND</span></span>

<span data-ttu-id="e24aa-203">Приложения, использующие модель перелистывания, не должны использовать несколько цепочек переключения моделей перелистывания, предназначенных для одного и того же HWND.</span><span class="sxs-lookup"><span data-stu-id="e24aa-203">Applications that use Flip Model should not use multiple Flip Model swap chains targeting the same HWND.</span></span>

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="e24aa-204">Синхронизация кадров для приложений модели перелистывания Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="e24aa-204">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="e24aa-205">Текущая статистика — это сведения о времени кадров, которые используются приложениями мультимедиа для синхронизации видео и звуковых потоков, а затем восстанавливаются после сбоев воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="e24aa-205">Present statistics are frame timing information that media applications use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="e24aa-206">Чтобы обеспечить доступность статистики, приложение Direct3D 9Ex должно гарантировать, что параметр *бехавиорфлагс* , который приложение передает в [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) , содержит флаг поведения устройства [D3DCREATE \_ включить \_ пресентстатс](/windows/desktop/direct3d9/d3dcreate).</span><span class="sxs-lookup"><span data-stu-id="e24aa-206">To enable present statistics availability, the Direct3D 9Ex application must ensure that the *BehaviorFlags* parameter that the application passes to [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contains the device behavior flag [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span></span>

<span data-ttu-id="e24aa-207">Для удобства синтаксис [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) повторяется здесь.</span><span class="sxs-lookup"><span data-stu-id="e24aa-207">For convenience, the syntax of [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

<span data-ttu-id="e24aa-208">Модель перелистывания Direct3D 9Ex добавляет флаг презентации [ \_ форцеиммедиате D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) , обеспечивающий [ \_ \_ мгновенное](/windows/desktop/direct3d9/d3dpresent) поведение флага D3DPRESENT.</span><span class="sxs-lookup"><span data-stu-id="e24aa-208">Direct3D 9Ex Flip Model adds the [D3DPRESENT\_FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation flag that enforces the [D3DPRESENT\_INTERVAL\_IMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation-flag behavior.</span></span> <span data-ttu-id="e24aa-209">Приложение Direct3D 9Ex указывает эти флаги презентации в параметре *dwFlags* , который приложение передает в [**IDirect3DDevice9Ex::P ресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e24aa-209">The Direct3D 9Ex application specifies these presentation flags in the *dwFlags* parameter that the application passes to [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), as shown here.</span></span>

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

<span data-ttu-id="e24aa-210">При изменении приложения Direct3D 9Ex для Windows 7 следует учитывать следующие сведения об указанных флагах презентации [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) :</span><span class="sxs-lookup"><span data-stu-id="e24aa-210">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the specified [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) presentation flags:</span></span>

<dl> <dt>

[<span data-ttu-id="e24aa-211">D3DPRESENT \_ донотфлип</span><span class="sxs-lookup"><span data-stu-id="e24aa-211">D3DPRESENT\_DONOTFLIP</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="e24aa-212">Этот флаг доступен только в полноэкранном режиме или</span><span class="sxs-lookup"><span data-stu-id="e24aa-212">This flag is available only in full-screen mode or</span></span>

<span data-ttu-id="e24aa-213">(Только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e24aa-213">(Windows 7 Only)</span></span>

<span data-ttu-id="e24aa-214">Когда приложение задает член **SwapEffect** [**\_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) в [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) в вызове [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="e24aa-214">when the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

[<span data-ttu-id="e24aa-215">D3DPRESENT \_ форцеиммедиате</span><span class="sxs-lookup"><span data-stu-id="e24aa-215">D3DPRESENT\_FORCEIMMEDIATE</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="e24aa-216">(Только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e24aa-216">(Windows 7 Only)</span></span>

<span data-ttu-id="e24aa-217">Этот флаг можно указать только в том случае, если приложение  задает для члена [**SwapEffect \_ параметров D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) значение [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) в вызове [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="e24aa-217">This flag can be specified only if the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span> <span data-ttu-id="e24aa-218">Приложение может использовать этот флаг, чтобы немедленно обновить поверхность с несколькими кадрами позже в очереди DWM Present, по сути пропуская промежуточные кадры.</span><span class="sxs-lookup"><span data-stu-id="e24aa-218">The application can use this flag to immediately update a surface with several frames later in the DWM Present queue, essentially skipping intermediate frames.</span></span>

<span data-ttu-id="e24aa-219">Оконные приложения с поддержкой Флипекс могут использовать этот флаг для немедленного обновления поверхности с кадром, который позже находится в очереди DWM, пропуская промежуточные кадры.</span><span class="sxs-lookup"><span data-stu-id="e24aa-219">Windowed FlipEx-enabled applications can use this flag to immediately update a surface with a frame that is later in the DWM Present queue, skipping intermediate frames.</span></span> <span data-ttu-id="e24aa-220">Это особенно полезно для мультимедийных приложений, которые хотят отбросить фреймы, которые были обнаружены как последние и представлять последующие кадры во время составления.</span><span class="sxs-lookup"><span data-stu-id="e24aa-220">This is especially useful for media applications that want to discard frames that have been detected as late and present subsequent frames at composition time.</span></span> <span data-ttu-id="e24aa-221">[**IDirect3DDevice9Ex::P ресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) возвращает ошибку недопустимого параметра, если этот флаг указан неправильно.</span><span class="sxs-lookup"><span data-stu-id="e24aa-221">[**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) returns invalid parameter error if this flag is improperly specified.</span></span>

</dd> </dl>

<span data-ttu-id="e24aa-222">Чтобы получить данные статистики, приложение получает структуру [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) , вызывая API [**IDirect3DSwapChain9Ex:: жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e24aa-222">To obtain present statistics information, the application obtains the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure by calling the [**IDirect3DSwapChain9Ex::GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API.</span></span>

<span data-ttu-id="e24aa-223">Структура [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) содержит статистику о вызовах [**IDirect3DDevice9Ex::P ресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="e24aa-223">The [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure contains statistics about [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span> <span data-ttu-id="e24aa-224">Устройство должно быть создано с помощью вызова [**IDirect3D9Ex:: креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) с флагом [D3DCREATE \_ Enable \_ пресентстатс](/windows/desktop/direct3d9/d3dcreate) .</span><span class="sxs-lookup"><span data-stu-id="e24aa-224">The device must be created by using a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) call with the [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) flag.</span></span> <span data-ttu-id="e24aa-225">В противном случае данные, возвращаемые функцией [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , не определены.</span><span class="sxs-lookup"><span data-stu-id="e24aa-225">Otherwise, the data returned by [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is undefined.</span></span> <span data-ttu-id="e24aa-226">Цепочка подкачки Direct3D 9Ex с поддержкой отражения предоставляет данные статистики в оконном и полноэкранном режимах.</span><span class="sxs-lookup"><span data-stu-id="e24aa-226">A Flip-Model-enabled Direct3D 9Ex swap chain provides present statistics information in both windowed and full-screen modes.</span></span>

<span data-ttu-id="e24aa-227">Для цепочек переключения БЛТ 9Ex Direct3D с поддержкой моделей в оконном режиме все значения структуры [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) будут обнулены.</span><span class="sxs-lookup"><span data-stu-id="e24aa-227">For Blt-Model-enabled Direct3D 9Ex swap chains in windowed mode, all [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure values will be zeroes.</span></span>

<span data-ttu-id="e24aa-228">Для Флипекс представлена статистика [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) возвращает D3DERR представления о несвязанной \_ \_ статистике \_ в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="e24aa-228">For FlipEx present statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) returns D3DERR\_PRESENT\_STATISTICS\_DISJOINT in the following situations:</span></span>

-   <span data-ttu-id="e24aa-229">Первый вызов [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) когда-либо, что означает начало последовательности</span><span class="sxs-lookup"><span data-stu-id="e24aa-229">First call to [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, which indicates the beginning of a sequence</span></span>
-   <span data-ttu-id="e24aa-230">Выход из рабочего стола из состояния "вкл."</span><span class="sxs-lookup"><span data-stu-id="e24aa-230">DWM transition from on to off</span></span>
-   <span data-ttu-id="e24aa-231">Изменение режима: в оконном режиме на весь экран или из полноэкранного режима до полноэкранных переходов</span><span class="sxs-lookup"><span data-stu-id="e24aa-231">Mode change: either windowed mode to or from full screen or full screen to full screen transitions</span></span>

<span data-ttu-id="e24aa-232">Для удобства синтаксис [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) повторяется здесь.</span><span class="sxs-lookup"><span data-stu-id="e24aa-232">For convenience, the syntax of [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is repeated here.</span></span>

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

<span data-ttu-id="e24aa-233">Метод [**IDirect3DSwapChain9Ex:: жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) возвращает последнюю пресенткаунт, то есть текущий идентификатор последнего успешного вызова, который был создан устройством отображения, связанным с цепочкой буферов обмена.</span><span class="sxs-lookup"><span data-stu-id="e24aa-233">The [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) method returns the last PresentCount, that is, the Present ID of the last successful Present call that was made by a display device that is associated with the swap chain.</span></span> <span data-ttu-id="e24aa-234">Этот идентификатор представляет собой значение элемента **пресенткаунт** структуры [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) .</span><span class="sxs-lookup"><span data-stu-id="e24aa-234">This Present ID is the value of the **PresentCount** member of the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure.</span></span> <span data-ttu-id="e24aa-235">Для цепочек переключения БЛТ 9Ex Direct3D с поддержкой модели в оконном режиме все значения структуры **D3DPRESENTSTATS** будут обнулены.</span><span class="sxs-lookup"><span data-stu-id="e24aa-235">For Blt-Model-enabled Direct3D 9Ex swap chains, while in windowed mode, all **D3DPRESENTSTATS** structure values will be zeroes.</span></span>

<span data-ttu-id="e24aa-236">Для удобства синтаксис [**IDirect3DSwapChain9Ex:: жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) повторяется здесь.</span><span class="sxs-lookup"><span data-stu-id="e24aa-236">For convenience, the syntax of [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) is repeated here.</span></span>

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

<span data-ttu-id="e24aa-237">При изменении приложения Direct3D 9Ex для Windows 7 следует учитывать следующие сведения о структуре [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :</span><span class="sxs-lookup"><span data-stu-id="e24aa-237">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure:</span></span>

-   <span data-ttu-id="e24aa-238">Значение Пресенткаунт, возвращаемое [**жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) , не обновляется, когда вызов [**пресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) с D3DPRESENT \_ донотваит, указанным в параметре *dwFlags* , возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e24aa-238">The PresentCount value that [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) returns does not update when a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) call with D3DPRESENT\_DONOTWAIT specified in the *dwFlags* parameter returns failure.</span></span>
-   <span data-ttu-id="e24aa-239">Когда [**пресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) вызывается с помощью D3DPRESENT \_ Донотфлип, вызов [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) выполняется, но не возвращает обновленную структуру [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) , когда приложение находится в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="e24aa-239">When [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) is called with D3DPRESENT\_DONOTFLIP, a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>
-   <span data-ttu-id="e24aa-240">**Пресентрефрешкаунт** и **синкрефрешкаунт** в [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span><span class="sxs-lookup"><span data-stu-id="e24aa-240">**PresentRefreshCount** versus **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span></span>
    -   <span data-ttu-id="e24aa-241">**Пресентрефрешкаунт** равно **синкрефрешкаунт** , когда приложение представлено на каждом вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e24aa-241">**PresentRefreshCount** is equal to **SyncRefreshCount** when the application presents on every vsync.</span></span>
    -   <span data-ttu-id="e24aa-242">**Синкрефрешкаунт** получается в интервале вертикальной синхронизации, когда предпринята передача, **синккпктиме** приблизительно соответствует времени, связанному с интервалом вертикальной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e24aa-242">**SyncRefreshCount** is obtained on the vsync interval when the present was submitted, **SyncQPCTime** is approximately the time associated with the vsync interval.</span></span>

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a><span data-ttu-id="e24aa-243">Синхронизация кадров для оконных приложений при отключенном DWM</span><span class="sxs-lookup"><span data-stu-id="e24aa-243">Frame Synchronization for Windowed Applications When DWM is Off</span></span>

<span data-ttu-id="e24aa-244">Когда DWM отключается, оконные приложения отображаются непосредственно на экране монитора, не пробегая цепочки зеркального отражения.</span><span class="sxs-lookup"><span data-stu-id="e24aa-244">When DWM is off, windowed applications display directly to the monitor screen without going through a flip chain.</span></span> <span data-ttu-id="e24aa-245">В Windows Vista не поддерживается получение статистических данных о кадрах для оконных приложений, когда DWM выключен.</span><span class="sxs-lookup"><span data-stu-id="e24aa-245">In Windows Vista, there is no support for obtaining frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="e24aa-246">Для поддержки API, где приложениям не требуется использовать DWM, Windows 7 возвращает статистику кадров для оконных приложений, когда DWM выключен.</span><span class="sxs-lookup"><span data-stu-id="e24aa-246">To maintain an API where applications need not be DWM- aware, Windows 7 will return frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="e24aa-247">Статистика кадра, возвращаемая при отключенном DWM, является только оценкой.</span><span class="sxs-lookup"><span data-stu-id="e24aa-247">The frame statistics returned when DWM is off are estimations only.</span></span>

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a><span data-ttu-id="e24aa-248">Walk-Through модели отражения Direct3D 9Ex и представление статистики — пример</span><span class="sxs-lookup"><span data-stu-id="e24aa-248">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>

<span data-ttu-id="e24aa-249">**Чтобы принять участие в презентации Флипекс для примера Direct3D 9Ex**</span><span class="sxs-lookup"><span data-stu-id="e24aa-249">**To opt into FlipEx presentation for Direct3D 9Ex sample**</span></span>

1.  <span data-ttu-id="e24aa-250">Убедитесь, что пример приложения работает в операционной системе Windows 7 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e24aa-250">Ensure the sample application is running on Windows 7 or later operating system version.</span></span>
2.  <span data-ttu-id="e24aa-251">Задайте для элемента **SwapEffect** в [**\_ параметрах D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) значение [**D3DSWAPEFFECT \_ флипекс**](/windows/desktop/direct3d9/d3dswapeffect) в вызове [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="e24aa-251">Set the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



<span data-ttu-id="e24aa-252">**Чтобы выбрать Флипекс, связанную с этой статистикой для примера 9Ex Direct3D**</span><span class="sxs-lookup"><span data-stu-id="e24aa-252">**To also opt into FlipEx associated Present Statistics for Direct3D 9Ex sample**</span></span>

-   <span data-ttu-id="e24aa-253">Задайте [D3DCREATE \_ Enable \_ пресентстатс](/windows/desktop/direct3d9/d3dcreate) в параметре *бехавиорфлагс* [**креатедевицеекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="e24aa-253">Set [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in the *BehaviorFlags* parameter of [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



<span data-ttu-id="e24aa-254">**Чтобы избежать проблем, выявление и восстановление после сбоев**</span><span class="sxs-lookup"><span data-stu-id="e24aa-254">**To avoid, detect and recover from glitches**</span></span>

1.  <span data-ttu-id="e24aa-255">Вызовы, представленные в очереди: Рекомендуемое число буферов в диапазоне от 2 до 4.</span><span class="sxs-lookup"><span data-stu-id="e24aa-255">Queue Present calls: recommended backbuffer count is from 2 to 4.</span></span>
2.  <span data-ttu-id="e24aa-256">В примере Direct3D 9Ex добавляется неявный Недопустимый буфер, фактически Текущая длина очереди — число незаполненных буферов + 1.</span><span class="sxs-lookup"><span data-stu-id="e24aa-256">Direct3D 9Ex sample adds an implicit backbuffer, actual Present queue length is backbuffer count + 1.</span></span>
3.  <span data-ttu-id="e24aa-257">Класс Helper предоставляет структуру очереди для хранения всех успешно отправленных ИДЕНТИФИКАТОРов представления (Пресенткаунт) и связанных, вычисляемых или ожидаемых Пресентрефрешкаунт.</span><span class="sxs-lookup"><span data-stu-id="e24aa-257">Create helper Present queue structure to store all successfully submitted Present's Present ID (PresentCount) and associated, calculated/expected PresentRefreshCount.</span></span>
4.  <span data-ttu-id="e24aa-258">Чтобы обнаружить возникновение сбоя, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e24aa-258">To detect glitch occurrence:</span></span>

    -   <span data-ttu-id="e24aa-259">Вызовите [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e24aa-259">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span></span>
    -   <span data-ttu-id="e24aa-260">Получите текущий идентификатор (Пресенткаунт) и число вертикальной синхронизации, где отображается кадр (Пресентрефрешкаунт) кадра, для которого получена статистика.</span><span class="sxs-lookup"><span data-stu-id="e24aa-260">Get the Present ID (PresentCount) and vsync count where the frame is shown (PresentRefreshCount) of the frame whose present statistics is obtained.</span></span>
    -   <span data-ttu-id="e24aa-261">Извлеките ожидаемый Пресентрефрешкаунт (Таржетрефреш в образце кода), связанный с текущим ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="e24aa-261">Retrieve the expected PresentRefreshCount (TargetRefresh in sample code) associated with the Present ID.</span></span>
    -   <span data-ttu-id="e24aa-262">Если фактический Пресентрефрешкаунт позже, чем ожидалось, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="e24aa-262">If actual PresentRefreshCount is later than expected, a glitch has occurred.</span></span>

5.  <span data-ttu-id="e24aa-263">Для восстановления после сбоя выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e24aa-263">To recover from glitch:</span></span>

    -   <span data-ttu-id="e24aa-264">Вычислите количество пропускаемых кадров (g \_ ииммедиатес Variable в образце кода).</span><span class="sxs-lookup"><span data-stu-id="e24aa-264">Calculate how many frames to skip (g\_ iImmediates variable in sample code).</span></span>
    -   <span data-ttu-id="e24aa-265">Представьте пропущенные кадры с интервалом D3DPRESENT \_ форцеиммедиате.</span><span class="sxs-lookup"><span data-stu-id="e24aa-265">Present the skipped frames with interval D3DPRESENT\_FORCEIMMEDIATE.</span></span>

<span data-ttu-id="e24aa-266">**Рекомендации по обнаружению и восстановлению сбоев**</span><span class="sxs-lookup"><span data-stu-id="e24aa-266">**Considerations for glitch detection and recovery**</span></span>

1.  <span data-ttu-id="e24aa-267">Восстановление после сбоя принимает N (g \_ икуеуеделай Variable в образце кода) число существующих вызовов, где N (g \_ икуеуеделай) равно g \_ Ииммедиатес плюс длина текущей очереди, то есть:</span><span class="sxs-lookup"><span data-stu-id="e24aa-267">Glitch recovery takes N (g\_iQueueDelay variable in sample code) number of Present calls where N (g\_iQueueDelay) equals g\_iImmediates plus length of the Present queue, that is:</span></span>

    -   <span data-ttu-id="e24aa-268">Пропуск кадров с текущим интервалом D3DPRESENT \_ форцеиммедиате, плюс</span><span class="sxs-lookup"><span data-stu-id="e24aa-268">Skipping frames with Present interval D3DPRESENT\_FORCEIMMEDIATE, plus</span></span>
    -   <span data-ttu-id="e24aa-269">В поставленных в очередь представление, которое необходимо обработать</span><span class="sxs-lookup"><span data-stu-id="e24aa-269">Queued Presents that need to be processed</span></span>

2.  <span data-ttu-id="e24aa-270">Установите ограничение на длину сбоя ( \_ \_ в примере — предельное число аварийных восстановлений).</span><span class="sxs-lookup"><span data-stu-id="e24aa-270">Set a limit to the glitch length (GLITCH\_RECOVERY\_LIMIT in sample).</span></span> <span data-ttu-id="e24aa-271">Если пример приложения не может выполнить восстановление после слишком длинного сбоя (например, 1 секунда или 60 всинкс для монитора 60 Гц), можно переключиться на временную анимацию и сбросить текущую вспомогательную очередь.</span><span class="sxs-lookup"><span data-stu-id="e24aa-271">If the sample application cannot recover from a glitch that is too long (that is say, 1 second, or 60 vsyncs on 60Hz monitor), jump over the intermittent animation and reset the Present helper queue.</span></span>


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



<span data-ttu-id="e24aa-272">**Пример сценария**</span><span class="sxs-lookup"><span data-stu-id="e24aa-272">**Sample scenario**</span></span>

-   <span data-ttu-id="e24aa-273">На следующем рисунке показано приложение с количеством буферов в 4.</span><span class="sxs-lookup"><span data-stu-id="e24aa-273">The following illustration shows an application with backbuffer count of 4.</span></span> <span data-ttu-id="e24aa-274">Фактически Текущая длина очереди равна 5.</span><span class="sxs-lookup"><span data-stu-id="e24aa-274">The actual Present queue length is therefore 5.</span></span>

    ![Иллюстрация отображаемых кадров аппликас и представление очереди](images/sample-scenario.png)

    <span data-ttu-id="e24aa-276">Кадр а предназначен для перехода на экран с числом интервалов синхронизации, равным 1, но было обнаружено, что оно отображается в интервале синхронизации, равном 4.</span><span class="sxs-lookup"><span data-stu-id="e24aa-276">Frame A is targeted to go on screen on sync interval count of 1 but was detected that it was shown on sync interval count of 4.</span></span> <span data-ttu-id="e24aa-277">Поэтому произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="e24aa-277">Therefore a glitch has occurred.</span></span> <span data-ttu-id="e24aa-278">Последующие 3 кадра представлены с D3DPRESENT \_ интервалом \_ форцеиммедиате.</span><span class="sxs-lookup"><span data-stu-id="e24aa-278">Subsequent 3 frames are presented with D3DPRESENT\_INTERVAL\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="e24aa-279">Сбой должен занять до 8 вызовов до восстановления. следующий кадр будет отображаться в соответствии со значением интервала синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e24aa-279">The glitch should take a total of 8 Present calls before it is recovered - the next frame will be shown as per its targeted sync interval count.</span></span>

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a><span data-ttu-id="e24aa-280">Сводка рекомендаций по программированию для синхронизации кадров</span><span class="sxs-lookup"><span data-stu-id="e24aa-280">Summary of Programming Recommendations for Frame Synchronization</span></span>

-   <span data-ttu-id="e24aa-281">Создайте резервный список всех идентификаторов Ластпресенткаунт (полученных через [**жетластпресенткаунт**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) и связанных с ними оценочных пресентрефрешкаунт всех предоставленных данных.</span><span class="sxs-lookup"><span data-stu-id="e24aa-281">Create a backup list of all the LastPresentCount IDs (obtained via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) and associated estimated PresentRefreshCount of all the Presents submitted.</span></span>
    > [!Note]  
    > <span data-ttu-id="e24aa-282">Когда приложение вызывает [**пресентекс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) с помощью D3DPRESENT \_ Донотфлип, вызов [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) выполняется, но не возвращает обновленную структуру [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) , когда приложение находится в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="e24aa-282">When the application calls [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) with D3DPRESENT\_DONOTFLIP, the [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>

     

-   <span data-ttu-id="e24aa-283">Вызовите [**жетпресентстатистикс**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) , чтобы получить фактический пресентрефрешкаунт, связанный с каждым ПРЕДСТАВЛЕНным идентификатором отображаемых кадров, чтобы убедиться, что приложение обрабатывает ошибку, возвращенную из вызова.</span><span class="sxs-lookup"><span data-stu-id="e24aa-283">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) to obtain the actual PresentRefreshCount associated with each Present ID of frames shown, to make sure that the application handles failure returns from the call.</span></span>
-   <span data-ttu-id="e24aa-284">Если фактический Пресентрефрешкаунт является более поздней, чем оценка Пресентрефрешкаунт, обнаруживается сбой.</span><span class="sxs-lookup"><span data-stu-id="e24aa-284">If actual PresentRefreshCount is later than estimated PresentRefreshCount, a glitch is detected.</span></span> <span data-ttu-id="e24aa-285">Компенсация за счет отправки кадров задержкойа, имеющихся в D3DPRESENT \_ форцеиммедиате.</span><span class="sxs-lookup"><span data-stu-id="e24aa-285">Compensate by submitting lagging frames' Present with D3DPRESENT\_FORCEIMMEDIATE.</span></span>
-   <span data-ttu-id="e24aa-286">Когда один кадр отображается в текущей очереди в конце, все последующие кадры в очереди будут представлены позднее.</span><span class="sxs-lookup"><span data-stu-id="e24aa-286">When one frame is presented late in the Present queue, all subsequent queued frames will be presented late.</span></span> <span data-ttu-id="e24aa-287">D3DPRESENT \_ форцеиммедиате будет исправлять только следующий кадр, который будет представлен после всех кадров в очереди.</span><span class="sxs-lookup"><span data-stu-id="e24aa-287">D3DPRESENT\_FORCEIMMEDIATE will correct only the next frame to be presented after all the queued frames.</span></span> <span data-ttu-id="e24aa-288">Таким образом, Текущая очередь или число буферов небольшого размера не должны быть слишком длинными, так что при этом возникает меньше сбоев кадров.</span><span class="sxs-lookup"><span data-stu-id="e24aa-288">Therefore, the Present queue or backbuffer count should not be too long -- so there are less frame glitches to catch up with.</span></span> <span data-ttu-id="e24aa-289">Оптимальное число походящих буферов в диапазоне от 2 до 4.</span><span class="sxs-lookup"><span data-stu-id="e24aa-289">The optimal backbuffer count is 2 to 4.</span></span>
-   <span data-ttu-id="e24aa-290">Если предполагаемый Пресентрефрешкаунт позже, чем фактический Пресентрефрешкаунт, может произойти регулирование DWM.</span><span class="sxs-lookup"><span data-stu-id="e24aa-290">If estimated PresentRefreshCount is later than the actual PresentRefreshCount, DWM throttling might have occurred.</span></span> <span data-ttu-id="e24aa-291">Возможны следующие решения.</span><span class="sxs-lookup"><span data-stu-id="e24aa-291">The following solutions are possible:</span></span>

    -   <span data-ttu-id="e24aa-292">сокращение длины текущей очереди</span><span class="sxs-lookup"><span data-stu-id="e24aa-292">reducing Present queue length</span></span>
    -   <span data-ttu-id="e24aa-293">уменьшение требований к памяти GPU с помощью других средств, помимо уменьшения числа существующих очередей (т. е. снижения качества, удаления эффектов и т. д.)</span><span class="sxs-lookup"><span data-stu-id="e24aa-293">reducing GPU memory requirements with any other means besides reducing Present Queue length (that is, decreasing quality, removing effects, and so on)</span></span>
    -   <span data-ttu-id="e24aa-294">Указание [**двменаблеммксс**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) для предотвращения регулирования DWM в целом</span><span class="sxs-lookup"><span data-stu-id="e24aa-294">specifying [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) to prevent DWM throttling in general</span></span>

-   <span data-ttu-id="e24aa-295">Проверьте работоспособность представления приложения и производительность статистики кадров в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="e24aa-295">Verify application display functionality and frame statistics performance in the following scenarios:</span></span>

    -   <span data-ttu-id="e24aa-296">Включение и отключение DWM</span><span class="sxs-lookup"><span data-stu-id="e24aa-296">with DWM on and off</span></span>
    -   <span data-ttu-id="e24aa-297">полноэкранные и оконные режимы</span><span class="sxs-lookup"><span data-stu-id="e24aa-297">fullscreen exclusive and windowed modes</span></span>
    -   <span data-ttu-id="e24aa-298">оборудование с более низким уровнем возможностей</span><span class="sxs-lookup"><span data-stu-id="e24aa-298">lower capability hardware</span></span>

-   <span data-ttu-id="e24aa-299">Когда приложения не могут восстановиться из большого числа кадров с ошибкой с D3DPRESENT \_ форцеиммедиате, они потенциально могут выполнять следующие операции:</span><span class="sxs-lookup"><span data-stu-id="e24aa-299">When applications cannot recover from large numbers of glitched frames with D3DPRESENT\_FORCEIMMEDIATE Present, they can potentially perform the following operations:</span></span>

    -   <span data-ttu-id="e24aa-300">Сократите использование ЦП и GPU, выполнив визуализацию с меньшей рабочей нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="e24aa-300">reduce CPU and GPU usage by rendering with less workload.</span></span>
    -   <span data-ttu-id="e24aa-301">в случае кодирования видео ускоряет декодирование, уменьшая качество и, следовательно, использование ЦП и GPU.</span><span class="sxs-lookup"><span data-stu-id="e24aa-301">in the case of video decode, decode faster by reducing quality and, therefore, CPU and GPU usage.</span></span>

## <a name="conclusion-about-direct3d-9ex-improvements"></a><span data-ttu-id="e24aa-302">Заключение об улучшениях Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="e24aa-302">Conclusion about Direct3D 9Ex Improvements</span></span>

<span data-ttu-id="e24aa-303">В Windows 7 приложения, отображающие частоту кадров видео или датчика во время презентации, могут отражать модель перелистывания.</span><span class="sxs-lookup"><span data-stu-id="e24aa-303">On Windows 7, applications that display video or gauge frame rate during presentation can opt into Flip Model.</span></span> <span data-ttu-id="e24aa-304">Представленные в статистике усовершенствования, связанные с отражением модели Direct3D 9Ex, могут использовать приложения, которые синхронизируют презентацию на частоту кадров, а также отзывы в реальном времени для обнаружения и восстановления сбоев.</span><span class="sxs-lookup"><span data-stu-id="e24aa-304">The present statistics improvements that are associated with Flip Model Direct3D 9Ex can benefit applications that synchronize presentation per frame rate, with real time feedback for glitch detection and recovery.</span></span> <span data-ttu-id="e24aa-305">Разработчикам, использующим модель перелистывания Direct3D 9Ex, следует ориентироваться на отдельный HWND из содержимого GDI и синхронизацию частот кадров в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e24aa-305">Developers that adopt the Direct3D 9Ex Flip Model should take targeting a separate HWND from GDI content and frame rate synchronization into account.</span></span> <span data-ttu-id="e24aa-306">Дополнительные сведения см. в этой статье и в документации MSDN.</span><span class="sxs-lookup"><span data-stu-id="e24aa-306">Refer to details in this topic, and MSDN documentation.</span></span> <span data-ttu-id="e24aa-307">Дополнительную документацию см. [в центре разработчиков DirectX на сайте MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="e24aa-307">For additional documentation, see [DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span></span>

## <a name="call-to-action"></a><span data-ttu-id="e24aa-308">Призыв к действию</span><span class="sxs-lookup"><span data-stu-id="e24aa-308">Call to Action</span></span>

<span data-ttu-id="e24aa-309">Мы рекомендуем использовать модель перелистывания Direct3D 9Ex и ее текущую статистику в Windows 7 при создании приложений, которые пытаются синхронизировать частоту кадров презентации или восстановить после сбоев отображения.</span><span class="sxs-lookup"><span data-stu-id="e24aa-309">We encourage you to use Direct3D 9Ex Flip Model and its present statistics on Windows 7 when you create applications that attempt to synchronize presentation frame rate or recover from display glitches.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e24aa-310">См. также</span><span class="sxs-lookup"><span data-stu-id="e24aa-310">Related topics</span></span>

<span data-ttu-id="e24aa-311">[Центр разработчиков DirectX на MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="e24aa-311">[DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> </dl>