---
title: Перелистывание моделей, "грязных" прямоугольников, прокручиваемых областей
description: DXGI 1,2 поддерживает новую цепочку перелистывания моделей, "грязных" прямоугольников и областей с прокруткой. Мы расскажем о преимуществах использования новой цепочки перелистывания моделей и оптимизации представления, указав «грязные» прямоугольники и области с прокруткой.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "104555035"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a><span data-ttu-id="0513c-104">Перелистывание моделей, "грязных" прямоугольников, прокручиваемых областей</span><span class="sxs-lookup"><span data-stu-id="0513c-104">Flip model, dirty rectangles, scrolled areas</span></span>

<span data-ttu-id="0513c-105">DXGI 1,2 поддерживает новую цепочку перелистывания моделей, "грязных" прямоугольников и областей с прокруткой.</span><span class="sxs-lookup"><span data-stu-id="0513c-105">DXGI 1.2 supports a new flip-model swap chain, dirty rectangles, and scrolled areas.</span></span> <span data-ttu-id="0513c-106">Мы расскажем о преимуществах использования новой цепочки перелистывания моделей и оптимизации представления, указав «грязные» прямоугольники и области с прокруткой.</span><span class="sxs-lookup"><span data-stu-id="0513c-106">We explain the benefits of using the new flip-model swap chain and of optimizing presentation by specifying dirty rectangles and scrolled areas.</span></span>

## <a name="dxgi-flip-model-presentation"></a><span data-ttu-id="0513c-107">Представление "Зеркальная презентация" в виде модели</span><span class="sxs-lookup"><span data-stu-id="0513c-107">DXGI flip-model presentation</span></span>

<span data-ttu-id="0513c-108">В DXGI 1,2 добавлена поддержка модели эргономичного представления для API-интерфейсов Direct3D 10 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="0513c-108">DXGI 1.2 adds support for the flip presentation model for Direct3D 10 and later APIs.</span></span> <span data-ttu-id="0513c-109">В Windows 7 технология Direct3D 9EX сначала предприняла [представление "переворот-модель](../direct3darticles/direct3d-9ex-improvements.md) ", чтобы избежать ненужного копирования буфера цепочки подкачки.</span><span class="sxs-lookup"><span data-stu-id="0513c-109">In Windows 7, Direct3D 9EX first adopted [flip-model presentation](../direct3darticles/direct3d-9ex-improvements.md) to avoid unnecessarily copying the swap-chain buffer.</span></span> <span data-ttu-id="0513c-110">При использовании модели перелистывания задние буферы переносятся между средой выполнения и диспетчер окон рабочего стола (DWM), поэтому DWM всегда объединяется непосредственно из заднего буфера, а не копирует содержимое заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="0513c-110">By using flip model, back buffers are flipped between the runtime and Desktop Window Manager (DWM), so DWM always composes directly from the back buffer instead of copying the back buffer content.</span></span>

<span data-ttu-id="0513c-111">API-интерфейсы DXGI 1,2 включают пересмотренный интерфейс цепочки замены DXGI, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="0513c-111">DXGI 1.2 APIs include a revised DXGI swap-chain interface, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="0513c-112">Можно использовать несколько методов интерфейса [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) , чтобы создать соответствующий объект **IDXGISwapChain1** для использования с дескриптором [**HWND**](../winprog/windows-data-types.md) , объектом [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , [DirectComposition](../directcomp/directcomposition-portal.md)или платформой [**Windows. UI. XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="0513c-112">You can use multiple [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) interface methods to create the appropriate **IDXGISwapChain1** object to use with an [**HWND**](../winprog/windows-data-types.md) handle, a [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) object, [DirectComposition](../directcomp/directcomposition-portal.md), or the [**Windows.UI.Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) framework.</span></span>

<span data-ttu-id="0513c-113">Можно выбрать модель зеркального отображения, указав значение [**\_ \_ \_ \_ последовательного перечисления эффекты подкачки для перелистывания**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) в элементе **SwapEffect** структуры [**\_ \_ \_ DESC1 в цепочке**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) , а также установив элемент **BufferCount** **\_ цепочки подкачки DXGI \_ \_ DESC1** в значение минимум 2.</span><span class="sxs-lookup"><span data-stu-id="0513c-113">You select the flip presentation model by specifying the [**DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) enumeration value in the **SwapEffect** member of the [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and by setting the **BufferCount** member of **DXGI\_SWAP\_CHAIN\_DESC1** to a minimum of 2.</span></span> <span data-ttu-id="0513c-114">Дополнительные сведения об использовании модели перелистывания DXGI см. в разделе [модель перелистывания DXGI](dxgi-flip-model.md).</span><span class="sxs-lookup"><span data-stu-id="0513c-114">For more info about how to use DXGI flip model, see [DXGI flip model](dxgi-flip-model.md).</span></span> <span data-ttu-id="0513c-115">Из-за более плавной презентации модели представления и других новых функций рекомендуется использовать функцию отражать модель представления для всех новых приложений, написанных с помощью API Direct3D 10 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="0513c-115">Because of the flip presentation model's smoother presentation and other new functionality, we recommend that you use flip presentation model for all new apps that you write with Direct3D 10 and later APIs.</span></span>

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a><span data-ttu-id="0513c-116">Использование «грязных» прямоугольников и прямоугольника прокрутки в представлении цепочки буферов</span><span class="sxs-lookup"><span data-stu-id="0513c-116">Using dirty rectangles and the scroll rectangle in swap chain presentation</span></span>

<span data-ttu-id="0513c-117">Используя «грязные» прямоугольники и прямоугольник прокрутки в представлении цепочки буферов, вы экономите использование пропускной способности памяти и связанного использования системы, поскольку объем данных в пикселях, который операционная система должна нарисовать, уменьшается, если операционной системе не нужно рисовать весь фрейм.</span><span class="sxs-lookup"><span data-stu-id="0513c-117">By using dirty rectangles and the scroll rectangle in swap chain presentation, you save on the usage of memory bandwidth and the related usage of system power because the amount of pixel data that the operating system needs to draw the next presented frame is reduced if the operating system doesn't need to draw the entire frame.</span></span> <span data-ttu-id="0513c-118">Для приложений, которые часто отображаются с помощью подключение к удаленному рабочему столу и других технологий удаленного доступа, экономия особенно заметна в соответствии с качеством отображения, так как эти технологии используют «грязные» прямоугольники и метаданные прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0513c-118">For apps that are often displayed via Remote Desktop Connection and other remote-accessing technologies, the savings are particularly noticeable in the display quality because these technologies use dirty rectangles and scroll metadata.</span></span>

<span data-ttu-id="0513c-119">Можно использовать только прокрутку с цепочками переключения DXGI, выполняемыми в с параметром отразить модель представления.</span><span class="sxs-lookup"><span data-stu-id="0513c-119">You can use scroll only with DXGI swap chains that run in flip presentation model.</span></span> <span data-ttu-id="0513c-120">Вы можете использовать "грязные" прямоугольники с цепочками переключения DXGI, которые выполняются как в модели отражения, так и в модели BitBlt (задаются с [**\_ \_ \_ последовательностью переключения DXGI**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="0513c-120">You can use dirty rectangles with DXGI swap chains that run in both flip model and bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span>

<span data-ttu-id="0513c-121">В этом сценарии и иллюстрации показаны функциональные возможности использования «грязных» прямоугольников и прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0513c-121">In this scenario and illustration we show the functionality of using dirty rectangles and scroll.</span></span> <span data-ttu-id="0513c-122">Здесь прокручиваемое приложение содержит текст и анимацию видео.</span><span class="sxs-lookup"><span data-stu-id="0513c-122">Here, a scrollable app contains text and animating video.</span></span> <span data-ttu-id="0513c-123">Приложение использует «грязные» прямоугольники, чтобы просто обновить анимацию видео и новую строку для окна, а не обновлять окно целиком.</span><span class="sxs-lookup"><span data-stu-id="0513c-123">The app uses dirty rectangles to just update the animating video and new line for the window, instead of updating the entire window.</span></span> <span data-ttu-id="0513c-124">Прямоугольник прокрутки позволяет операционной системе копировать и переводить ранее визуализированное содержимое в новом фрейме и отображать только новую строку в новом фрейме.</span><span class="sxs-lookup"><span data-stu-id="0513c-124">The scroll rectangle allows the operating system to copy and translate the previously rendered content on the new frame and to render only the new line on the new frame.</span></span>

<span data-ttu-id="0513c-125">Приложение выполняет презентацию, вызывая метод [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) .</span><span class="sxs-lookup"><span data-stu-id="0513c-125">The app performs presentation by calling the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method.</span></span> <span data-ttu-id="0513c-126">В этом вызове приложение передает указатель на структуру [**\_ \_ параметров DXGI**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) , содержащую "грязные" прямоугольники и число "грязных" прямоугольников, а также прямоугольник прокрутки и соответствующее смещение прокрутки, либо как "грязные" прямоугольники, так и прямоугольник прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0513c-126">In this call, the app passes a pointer to a [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) structure that includes dirty rectangles and the number of dirty rectangles, or the scroll rectangle and the associated scroll offset, or both dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="0513c-127">Наше приложение передает 2 "грязных" прямоугольников и прямоугольник прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0513c-127">Our app passes 2 dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="0513c-128">Прямоугольник прокрутки — это область предыдущего кадра, которую операционная система должна скопировать в текущий кадр перед отрисовкой текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="0513c-128">The scroll rectangle is the area of the previous frame that the operating system needs to copy to the current frame before it renders the current frame.</span></span> <span data-ttu-id="0513c-129">Приложение задает анимацию видео и новую строку в качестве «грязных» прямоугольников, а операционная система отображает их в текущем кадре.</span><span class="sxs-lookup"><span data-stu-id="0513c-129">The app specifies the animating video and new line as dirty rectangles, and the operating system renders them on the current frame.</span></span>

![Иллюстрация перекрывающихся прямоугольников прокрутки и "грязных"](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

<span data-ttu-id="0513c-131">Пунктирный прямоугольник показывает прямоугольник прокрутки в текущем кадре.</span><span class="sxs-lookup"><span data-stu-id="0513c-131">The dashed rectangle shows the scroll rectangle in the current frame.</span></span> <span data-ttu-id="0513c-132">Прямоугольник прокрутки задается  членом пскроллрект [**в \_ \_ параметрах DXGI Present**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span><span class="sxs-lookup"><span data-stu-id="0513c-132">The scroll rectangle is specified by the **pScrollRect** member of [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span></span> <span data-ttu-id="0513c-133">Стрелка показывает смещение прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0513c-133">The arrow shows the scroll offset.</span></span> <span data-ttu-id="0513c-134">Смещение прокрутки задается  членом пскроллоффсет **в \_ \_ параметрах DXGI Present**.</span><span class="sxs-lookup"><span data-stu-id="0513c-134">The scroll offset is specified by the **pScrollOffset** member of **DXGI\_PRESENT\_PARAMETERS**.</span></span> <span data-ttu-id="0513c-135">В заполненных прямоугольниках отображаются "грязные" прямоугольники, которые приложение обновило с новым содержимым.</span><span class="sxs-lookup"><span data-stu-id="0513c-135">Filled rectangles show dirty rectangles that the app updated with new content.</span></span> <span data-ttu-id="0513c-136">Закрашенные прямоугольники задаются членами **диртиректскаунт** и **пдиртиректс** в **\_ \_ параметрах DXGI Present**.</span><span class="sxs-lookup"><span data-stu-id="0513c-136">The filled rectangles are specified by the **DirtyRectsCount** and **pDirtyRects** members of **DXGI\_PRESENT\_PARAMETERS**.</span></span>

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a><span data-ttu-id="0513c-137">Пример 2. цепочка перелистывания моделей с "грязными" прямоугольниками и прямоугольником прокрутки</span><span class="sxs-lookup"><span data-stu-id="0513c-137">Sample 2-buffer flip-model swap chain with dirty rectangles and scroll rectangle</span></span>

<span data-ttu-id="0513c-138">На следующем рисунке и последовательности показан пример операции представления "перелистывание DXGI", в которой используются «грязные» прямоугольники и прямоугольник прокрутки.</span><span class="sxs-lookup"><span data-stu-id="0513c-138">The next illustration and sequence shows an example of a DXGI flip-model presentation operation that uses dirty rectangles and a scroll rectangle.</span></span> <span data-ttu-id="0513c-139">В этом примере мы используем минимальное количество буферов для представления "Зеркальная модель", которое представляет собой число буферов, равное двум, одному интерфейсному буферу, содержащему отображаемое содержимое приложения, и одному обратному буферу, содержащему текущий кадр, который приложение хочет подготовить.</span><span class="sxs-lookup"><span data-stu-id="0513c-139">In this example we use the minimum number of buffers for flip-model presentation, which is a buffer count of two, one front buffer that contains the app display content and one back buffer that contains the current frame that the app wants to render.</span></span>

1.  <span data-ttu-id="0513c-140">Как показано в интерфейсе спереди в начале кадра, прокручиваемое приложение изначально отображает рамку с текстом и анимацией видео.</span><span class="sxs-lookup"><span data-stu-id="0513c-140">As shown in the front buffer at the beginning of the frame, the scrollable app initially shows a frame with some text and animating video.</span></span>
2.  <span data-ttu-id="0513c-141">Чтобы отобразить следующий кадр, приложение визуализирует в обратном буфере "грязные" прямоугольники, которые обновляют видео в анимации и новую строку для окна.</span><span class="sxs-lookup"><span data-stu-id="0513c-141">To render the next frame, the app renders onto the back buffer the dirty rectangles that update the animating video and the new line for the window.</span></span>
3.  <span data-ttu-id="0513c-142">Когда приложение вызывает [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), оно указывает «грязные» прямоугольники, прямоугольник прокрутки и смещение.</span><span class="sxs-lookup"><span data-stu-id="0513c-142">When the app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), it specifies the dirty rectangles and the scroll rectangle and offset.</span></span> <span data-ttu-id="0513c-143">Затем среда выполнения копирует прямоугольник прокрутки из предыдущего кадра за вычетом обновленных «грязных» прямоугольников в текущий задний буфер.</span><span class="sxs-lookup"><span data-stu-id="0513c-143">The runtime next copies the scroll rectangle from the previous frame minus the updated dirty rectangles onto the current back buffer.</span></span>
4.  <span data-ttu-id="0513c-144">Среда выполнения наконец меняет местами передний и задний буферы.</span><span class="sxs-lookup"><span data-stu-id="0513c-144">The runtime finally swaps the front and back buffers.</span></span>

![Пример цепочки перелистывания моделей с прямоугольниками прокрутки и "грязными"](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a><span data-ttu-id="0513c-146">Отслеживание «грязных» прямоугольников и прямоугольников прокрутки в нескольких кадрах</span><span class="sxs-lookup"><span data-stu-id="0513c-146">Tracking dirty rectangles and scroll rectangles across multiple frames</span></span>

<span data-ttu-id="0513c-147">При использовании «грязных» прямоугольников в приложении необходимо отслеживанию «грязных» прямоугольников для поддержки добавочной визуализации.</span><span class="sxs-lookup"><span data-stu-id="0513c-147">When you use dirty rectangles in your app, you must track the dirty rectangles to support incremental rendering.</span></span> <span data-ttu-id="0513c-148">Когда приложение вызывает [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) с "грязными" прямоугольниками, необходимо обеспечить актуальность каждого пикселя в "грязных" прямоугольниках.</span><span class="sxs-lookup"><span data-stu-id="0513c-148">When your app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) with dirty rectangles, you must ensure that every pixel within the dirty rectangles is up to date.</span></span> <span data-ttu-id="0513c-149">Если вы не полностью переготовите всю область "грязного" прямоугольника или не можете понять, какие области изменялся, необходимо скопировать некоторые данные из предыдущего полностью согласованного заднего буфера в текущий устаревший задний буфер до начала подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0513c-149">If you aren't completely re-rendering the whole area of the dirty rectangle or if you can’t know for certain the areas that are dirtied, you must copy some data from the previous fully coherent back buffer to the current, stale back buffer before you start rendering.</span></span>

<span data-ttu-id="0513c-150">Среда выполнения копирует только различия между обновленными областями предыдущего кадра и обновленными областями текущего кадра на текущий задний буфер.</span><span class="sxs-lookup"><span data-stu-id="0513c-150">The runtime copies only the differences between updated areas of the previous frame and updated areas of the current frame onto the current back buffer.</span></span> <span data-ttu-id="0513c-151">Если эти области пересекаются, среда выполнения копирует только разницу между ними.</span><span class="sxs-lookup"><span data-stu-id="0513c-151">If these areas intersect, the runtime copies only the difference between them.</span></span> <span data-ttu-id="0513c-152">Как видно на следующей схеме и последовательности, необходимо скопировать пересечение между «грязным» прямоугольником из кадра 1 и «грязным» прямоугольником из фрейма 2 в «грязный» прямоугольник фрейма 2.</span><span class="sxs-lookup"><span data-stu-id="0513c-152">As you can see in the following diagram and sequence, you must copy the intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>

1.  <span data-ttu-id="0513c-153">Показать "грязный" прямоугольник в кадре 1.</span><span class="sxs-lookup"><span data-stu-id="0513c-153">Present dirty rectangle in frame 1.</span></span>
2.  <span data-ttu-id="0513c-154">Скопируйте пересечение между «грязным» прямоугольником из фрейма 1 и «грязным» прямоугольником из фрейма 2 в «грязный» прямоугольник фрейма 2.</span><span class="sxs-lookup"><span data-stu-id="0513c-154">Copy intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>
3.  <span data-ttu-id="0513c-155">Представление "грязных" прямоугольника в кадре 2.</span><span class="sxs-lookup"><span data-stu-id="0513c-155">Present dirty rectangle in frame 2.</span></span>

![Отслеживание прямоугольников прокрутки и «грязных» рамок в нескольких кадрах](images/track-dirty-rects-scroll-rects.png)

<span data-ttu-id="0513c-157">Чтобы обобщить, для цепочки подкачки с N буферами область, которую среда выполнения копирует из последнего кадра в текущий кадр в текущем фрейме, — это:</span><span class="sxs-lookup"><span data-stu-id="0513c-157">To generalize, for a swap chain with N buffers, the area that the runtime copies from the last frame to the current frame on the current frame’s present is:</span></span>

![Уравнение для вычисления области, которую копирует среда выполнения](images/runtime-copy-equation.png)

<span data-ttu-id="0513c-159">где buffer указывает индекс буфера в цепочке буферов, начиная с текущего индекса буфера, равным нулю.</span><span class="sxs-lookup"><span data-stu-id="0513c-159">where buffer indicates the buffer index in a swap chain, starting with current buffer index at zero.</span></span>

<span data-ttu-id="0513c-160">Вы можете отслеживать любые пересечения между предыдущим и грязными прямоугольниками текущего кадра, сохранив копию «грязных» прямоугольников предыдущего кадра или повторно выполнив визуализацию «грязных» прямоугольников нового кадра с соответствующим содержимым из предыдущего кадра.</span><span class="sxs-lookup"><span data-stu-id="0513c-160">You can keep track of any intersections between the previous frame and the current frame’s dirty rectangles by keeping a copy of the previous frame’s dirty rectangles or by re-rendering the new frame’s dirty rectangles with the appropriate content from the previous frame.</span></span>

<span data-ttu-id="0513c-161">Аналогично, в случаях, когда цепочка подкачки имеет более 2 задних буферов, необходимо обеспечить копирование и повторное отображение перекрывающихся областей между «грязными» прямоугольниками текущего буфера и «грязными» прямоугольниками всех предыдущих кадров.</span><span class="sxs-lookup"><span data-stu-id="0513c-161">Similarly, in the cases where the swap chain has more than 2 back buffers, you must ensure that overlapping areas between the current buffer’s dirty rectangles and the dirty rectangles of all previous frame’s are copied or re-rendered.</span></span>

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a><span data-ttu-id="0513c-162">Отслеживание одного пересечения между 2 "грязными" прямоугольниками</span><span class="sxs-lookup"><span data-stu-id="0513c-162">Tracking a single intersection between 2 dirty rectangles</span></span>

<span data-ttu-id="0513c-163">В самом простом случае при обновлении одного «грязного» прямоугольника на кадр, «Грязные» прямоугольники в двух кадрах могут пересекаться.</span><span class="sxs-lookup"><span data-stu-id="0513c-163">In the simplest case, when you update a single dirty rectangle per frame, the dirty rectangles across two frames might intersect.</span></span> <span data-ttu-id="0513c-164">Чтобы узнать, перекрывается ли «грязный» прямоугольник предыдущего кадра и «грязный» прямоугольник текущего фрейма, необходимо проверить, пересекаются ли «грязный» прямоугольник предыдущего кадра с «грязным» прямоугольником текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="0513c-164">To find out whether the dirty rectangle of the previous frame and the dirty rectangle of the current frame overlap, you need to verify whether the dirty rectangle of the previous frame intersects with the dirty rectangle of the current frame.</span></span> <span data-ttu-id="0513c-165">Чтобы определить, пересекаются ли две структуры [**Rect**](/previous-versions//dd162897(v=vs.85)) , представляющие два «грязных» прямоугольников, можно вызвать функцию GDI [**интерсектрект**](/windows/win32/api/winuser/nf-winuser-intersectrect) .</span><span class="sxs-lookup"><span data-stu-id="0513c-165">You can call the GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) function to determine whether two [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that represent the two dirty rectangles intersect.</span></span>

<span data-ttu-id="0513c-166">В этом фрагменте кода вызов [**интерсектрект**](/windows/win32/api/winuser/nf-winuser-intersectrect) возвращает пересечение двух «грязных» прямоугольников в другом [**Rect**](/previous-versions//dd162897(v=vs.85)) , именуемом диртиректкопи.</span><span class="sxs-lookup"><span data-stu-id="0513c-166">In this code snippet, a call to [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) returns the intersection of two dirty rectangles in another [**RECT**](/previous-versions//dd162897(v=vs.85)) called dirtyRectCopy.</span></span> <span data-ttu-id="0513c-167">После того как фрагмент кода определит, что два "грязных" прямоугольников пересекаются, он вызывает метод [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) , чтобы скопировать область пересечения в текущий кадр.</span><span class="sxs-lookup"><span data-stu-id="0513c-167">After the code snippet determines that the two dirty rectangles intersect, it calls the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy the region of intersection into the current frame.</span></span>

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

<span data-ttu-id="0513c-168">Если вы используете этот фрагмент кода в приложении, приложение будет готово вызвать [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , чтобы обновить текущий кадр с текущим «грязным» прямоугольником.</span><span class="sxs-lookup"><span data-stu-id="0513c-168">If you use this code snippet in your application, the app will then be ready to call [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) to update the current frame with the current dirty rectangle.</span></span>

### <a name="tracking-intersections-between-n-dirty-rectangles"></a><span data-ttu-id="0513c-169">Отслеживание пересечения между N грязными прямоугольниками</span><span class="sxs-lookup"><span data-stu-id="0513c-169">Tracking intersections between N dirty rectangles</span></span>

<span data-ttu-id="0513c-170">Если указать несколько «грязных» прямоугольников, которые могут включать «грязный» прямоугольник для вновь обнаруженной прокрутки на кадр, необходимо проверить и отнести перекрытия, которые могут произойти между всеми «грязными» прямоугольниками предыдущего кадра, и всеми «грязными» прямоугольниками текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="0513c-170">If you specify multiple dirty rectangles, which can include a dirty rectangle for the newly revealed scroll line, per frame, you need to verify and track any overlaps that might occur between all the dirty rectangles of the previous frame and all the dirty rectangles of the current frame.</span></span> <span data-ttu-id="0513c-171">Чтобы вычислить пересечения между «грязными» прямоугольниками предыдущего фрейма и «грязными» прямоугольниками текущего фрейма, можно сгруппировать «грязные» прямоугольники в регионы.</span><span class="sxs-lookup"><span data-stu-id="0513c-171">To calculate the intersections between the dirty rectangles of the previous frame and the dirty rectangles of the current frame, you can group the dirty rectangles into regions.</span></span>

<span data-ttu-id="0513c-172">В этом фрагменте кода мы вызываем функцию GDI [**сетректргн**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) для преобразования каждого "грязного" прямоугольника в прямоугольную область, а затем ВЫЗЫВАЕМ функцию GDI [**комбинергн**](/windows/win32/api/wingdi/nf-wingdi-combinergn) , чтобы объединить все изменившиеся прямоугольные области в группу.</span><span class="sxs-lookup"><span data-stu-id="0513c-172">In this code snippet, we call the GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) function to convert each dirty rectangle into a rectangular region and then we call the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to combine all the dirty rectangular regions into a group.</span></span>

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

<span data-ttu-id="0513c-173">Теперь можно использовать функцию GDI [**комбинергн**](/windows/win32/api/wingdi/nf-wingdi-combinergn) для определения пересечения между «грязной» областью предыдущего кадра и «грязной» областью текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="0513c-173">You can now use the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to determine the intersection between the dirty region of the previous frame and the dirty region of the current frame.</span></span> <span data-ttu-id="0513c-174">После получения пересекающейся области вызовите функцию GDI [**жетрегиондата**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) , чтобы получить каждый отдельный прямоугольник из пересекающейся области, а затем вызовите метод [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) , чтобы скопировать каждый пересекающийся прямоугольник в текущий задний буфер.</span><span class="sxs-lookup"><span data-stu-id="0513c-174">After you obtain the intersecting region, call the GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) function to obtain each individual rectangle from the intersecting region and then call the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy each intersecting rectangle into the current back buffer.</span></span> <span data-ttu-id="0513c-175">В следующем фрагменте кода показано, как использовать эти функции GDI и Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0513c-175">The next code snippet shows how to use these GDI and Direct3D functions.</span></span>

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a><span data-ttu-id="0513c-176">Цепочка перекачки модели BitBlt с "грязными" прямоугольниками</span><span class="sxs-lookup"><span data-stu-id="0513c-176">Bitblt model swap chain with dirty rectangles</span></span>

<span data-ttu-id="0513c-177">Вы можете использовать "грязные" прямоугольники с цепочками переключения DXGI, которые выполняются в модели BitBlt (задаются с [**\_ \_ \_ последовательностью переключения DXGI**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="0513c-177">You can use dirty rectangles with DXGI swap chains that run in bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span> <span data-ttu-id="0513c-178">Цепочки переключения моделей BitBlt, использующие более одного буфера, также должны отслеживать перекрывающиеся "грязные" прямоугольники в кадрах таким же образом, как описано в разделе [Отслеживание грязных прямоугольников и прямоугольники прокрутки в нескольких кадрах](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) для отражения цепочек перестановки моделей.</span><span class="sxs-lookup"><span data-stu-id="0513c-178">Bitblt model swap chains that use more than one buffer must also track overlapping dirty rectangles across frames in the same way as described in [Tracking dirty rectangles and scroll rectangles across multiple frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) for flip model swap chains.</span></span> <span data-ttu-id="0513c-179">Цепочки переключения моделей BitBlt только с одним буфером не должны откладывать перекрывающиеся "грязные" прямоугольники, так как весь буфер перерисовывается в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="0513c-179">Bitblt model swap chains with just one buffer need not track overlapping dirty rectangles because the entire buffer is redrawn every frame.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0513c-180">См. также</span><span class="sxs-lookup"><span data-stu-id="0513c-180">Related topics</span></span>

[<span data-ttu-id="0513c-181">Усовершенствования DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="0513c-181">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
