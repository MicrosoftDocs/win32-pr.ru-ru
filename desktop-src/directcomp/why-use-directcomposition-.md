---
title: Зачем использовать DirectComposition
description: В этом разделе описываются возможности и преимущества Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Зачем использовать DirectComposition
- причины использования DirectComposition
- Возможности и преимущества DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691624"
---
# <a name="why-use-directcomposition"></a><span data-ttu-id="91f6a-106">Зачем использовать DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="91f6a-106">Why use DirectComposition?</span></span>

> [!NOTE]
> <span data-ttu-id="91f6a-107">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="91f6a-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="91f6a-108">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="91f6a-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="91f6a-109">В этом разделе описываются возможности и преимущества Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="91f6a-109">This topic describes the capabilities and benefits of Microsoft DirectComposition.</span></span> <span data-ttu-id="91f6a-110">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="91f6a-110">It contains the following sections:</span></span>

-   [<span data-ttu-id="91f6a-111">Создание визуально привлекательного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="91f6a-111">Create a visually engaging user interface</span></span>](#create-a-visually-engaging-user-interface)
-   [<span data-ttu-id="91f6a-112">Включение насыщенных и гладких анимаций для приложения</span><span class="sxs-lookup"><span data-stu-id="91f6a-112">Enable rich, smooth animations for your application</span></span>](#enable-rich-smooth-animations-for-your-application)
-   [<span data-ttu-id="91f6a-113">Объединение растровых изображений из различных источников</span><span class="sxs-lookup"><span data-stu-id="91f6a-113">Combine bitmaps from a variety of sources</span></span>](#combine-bitmaps-from-a-variety-of-sources)
-   [<span data-ttu-id="91f6a-114">Экономия памяти при интеграции с DWM</span><span class="sxs-lookup"><span data-stu-id="91f6a-114">Memory savings though integration with DWM</span></span>](#memory-savings-though-integration-with-dwm)
-   [<span data-ttu-id="91f6a-115">Не отключайте уже имеющиеся</span><span class="sxs-lookup"><span data-stu-id="91f6a-115">Keep what you already have</span></span>](#keep-what-you-already-have)
-   [<span data-ttu-id="91f6a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="91f6a-116">Related topics</span></span>](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a><span data-ttu-id="91f6a-117">Создание визуально привлекательного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="91f6a-117">Create a visually engaging user interface</span></span>

<span data-ttu-id="91f6a-118">DirectComposition позволяет объединять и анимировать [*визуальные элементы*](directcomposition-glossary.md) для создания визуально ПРИВЛЕКАТЕЛЬНОГО пользовательского интерфейса для приложений на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="91f6a-118">DirectComposition lets you combine and animate [*visuals*](directcomposition-glossary.md) to create a visually engaging UI for your Windows-based applications.</span></span> <span data-ttu-id="91f6a-119">Это может помочь придать приложению уникальный внешний вид, установив удостоверение, которое будет устанавливаться отдельно от других приложений.</span><span class="sxs-lookup"><span data-stu-id="91f6a-119">It can help give your application a unique look and feel, establishing an identity that sets it apart from other applications.</span></span>

<span data-ttu-id="91f6a-120">DirectComposition также помогает упростить работу с приложениями.</span><span class="sxs-lookup"><span data-stu-id="91f6a-120">DirectComposition can also help make your applications easier to use.</span></span> <span data-ttu-id="91f6a-121">Например, с его помощью можно создавать визуальные подсказки и анимированные переходы, отображающие связи между элементами на экране.</span><span class="sxs-lookup"><span data-stu-id="91f6a-121">For example, you can use it to create visual cues and animated screen transitions that show relationships among items on the screen.</span></span>

## <a name="enable-rich-smooth-animations-for-your-application"></a><span data-ttu-id="91f6a-122">Включение насыщенных и гладких анимаций для приложения</span><span class="sxs-lookup"><span data-stu-id="91f6a-122">Enable rich, smooth animations for your application</span></span>

<span data-ttu-id="91f6a-123">DirectComposition — это высокопроизводительный механизм композиции точечных рисунков, использующий графику с аппаратным ускорением для достижения высокой частоты кадров, что приводит к гладкому и согласованному панорамированию, прокрутке и анимации сложного содержимого.</span><span class="sxs-lookup"><span data-stu-id="91f6a-123">DirectComposition is a high-performance bitmap composition engine that uses hardware-accelerated graphics to achieve high frame rates, resulting in smooth and consistent panning, scrolling, and animations of complex content.</span></span> <span data-ttu-id="91f6a-124">Так как он работает в выделенном потоке, отдельном от потока, который используется для отрисовки пользовательского интерфейса приложения, DirectComposition никогда не может «распрепятствовать» потоку пользовательского интерфейса или помешать приложению рисовать свои элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="91f6a-124">Because it operates on a dedicated thread that is separate from the thread used to render the application UI, DirectComposition can never "starve" the UI thread or interfere with the application's ability to draw its UI elements.</span></span>

## <a name="combine-bitmaps-from-a-variety-of-sources"></a><span data-ttu-id="91f6a-125">Объединение растровых изображений из различных источников</span><span class="sxs-lookup"><span data-stu-id="91f6a-125">Combine bitmaps from a variety of sources</span></span>

<span data-ttu-id="91f6a-126">Многие приложения на базе Windows имеют пользовательский интерфейс, состоящий из элементов, созданных различными графическими платформами.</span><span class="sxs-lookup"><span data-stu-id="91f6a-126">Many Windows-based applications have a UI that consists of elements created by a variety of different graphics frameworks.</span></span> <span data-ttu-id="91f6a-127">Например, приложение может использовать Windows Forms для создания строки состояния, Windows интерфейс графических устройств (GDI) для создания содержимого главного окна, Microsoft DirectX для графического содержимого и т. д.</span><span class="sxs-lookup"><span data-stu-id="91f6a-127">For example, an application might use Windows Forms to create a status bar, Windows Graphics Device Interface (GDI) to create the main window content, Microsoft DirectX for graphics content, and so on.</span></span> <span data-ttu-id="91f6a-128">DirectComposition позволяет объединять содержимое из разнообразных графических платформ и отображать их в одном и том же дочернем окне верхнего уровня без необходимости беспокоиться о том, что происходит, если содержимое разных платформ перекрывается.</span><span class="sxs-lookup"><span data-stu-id="91f6a-128">DirectComposition enables you to combine the content from a variety of graphics frameworks and have it render to the same top-level or child window without needing to worry about what happens if the content from different frameworks overlaps.</span></span>

## <a name="memory-savings-though-integration-with-dwm"></a><span data-ttu-id="91f6a-129">Экономия памяти при интеграции с DWM</span><span class="sxs-lookup"><span data-stu-id="91f6a-129">Memory savings though integration with DWM</span></span>

<span data-ttu-id="91f6a-130">Композиции и анимации, созданные DirectComposition, передаются во встроенный компонент Windows, именуемый [Диспетчер окон рабочего стола (DWM)](/windows/desktop/dwm/dwm-overview) для отрисовки на экране.</span><span class="sxs-lookup"><span data-stu-id="91f6a-130">Compositions and animations created by DirectComposition are passed to a built-in component of Windows called [Desktop Window Manager (DWM)](/windows/desktop/dwm/dwm-overview) for rendering to the screen.</span></span> <span data-ttu-id="91f6a-131">Поэтому на компьютере не требуются специальные компоненты отрисовки или платформы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="91f6a-131">Therefore, no special rendering components or UI frameworks are required on the computer.</span></span>

## <a name="keep-what-you-already-have"></a><span data-ttu-id="91f6a-132">Не отключайте уже имеющиеся</span><span class="sxs-lookup"><span data-stu-id="91f6a-132">Keep what you already have</span></span>

<span data-ttu-id="91f6a-133">Код пользовательского интерфейса в существующем приложении на основе Windows представляет значительные инвестиции.</span><span class="sxs-lookup"><span data-stu-id="91f6a-133">The UI code in an existing Windows-based application represents a significant investment.</span></span> <span data-ttu-id="91f6a-134">В большинстве случаев DirectComposition позволяет создавать и анимировать существующее содержимое пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="91f6a-134">For the most part, DirectComposition lets you compose and animate your existing UI content.</span></span> <span data-ttu-id="91f6a-135">Это означает, что вы можете использовать DirectComposition для внесения значительных изменений в пользовательский интерфейс приложения без необходимости вносить значительные изменения в существующую базу кода пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="91f6a-135">This means you can use DirectComposition to make significant updates and enhancements to your application UI without needing to make extensive changes to your existing UI code base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91f6a-136">См. также</span><span class="sxs-lookup"><span data-stu-id="91f6a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91f6a-137">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="91f6a-137">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 