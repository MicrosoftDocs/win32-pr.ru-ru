---
title: DirectComposition
description: В этом разделе объясняется назначение Microsoft DirectComposition, определяются требования к времени выполнения и описывается, как эффективно использовать Microsoft DirectComposition.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329179"
---
# <a name="directcomposition"></a><span data-ttu-id="b1c62-106">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b1c62-106">DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="b1c62-107">Для приложений в Windows 10 рекомендуется использовать интерфейсы API Windows. UI. компоновки вместо DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b1c62-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="b1c62-108">Дополнительные сведения см. в разделе [модернизировать The классическое приложение с использованием визуального слоя](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="b1c62-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

## <a name="purpose"></a><span data-ttu-id="b1c62-109">Назначение</span><span class="sxs-lookup"><span data-stu-id="b1c62-109">Purpose</span></span>

<span data-ttu-id="b1c62-110">Microsoft DirectComposition — это компонент Windows, который позволяет создавать высокопроизводительные растровые изображения с помощью преобразований, эффектов и анимации.</span><span class="sxs-lookup"><span data-stu-id="b1c62-110">Microsoft DirectComposition is a Windows component that enables high-performance bitmap composition with transforms, effects, and animations.</span></span> <span data-ttu-id="b1c62-111">Разработчики приложений могут использовать API DirectComposition для создания визуально привлекательных пользовательских интерфейсов с плавными анимированными переходами от одного визуального элемента к другому.</span><span class="sxs-lookup"><span data-stu-id="b1c62-111">Application developers can use the DirectComposition API to create visually engaging user interfaces that feature rich and fluid animated transitions from one visual to another.</span></span>

<span data-ttu-id="b1c62-112">DirectComposition обеспечивает широкие и жидкие переходы за счет высокой частоты кадров, использования графического оборудования и работы независимо от потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b1c62-112">DirectComposition enables rich and fluid transitions by achieving a high framerate, using graphics hardware, and operating independently of the UI thread.</span></span> <span data-ttu-id="b1c62-113">DirectComposition может принимать растровое содержимое, рисуемое различными библиотеками отрисовки, включая точечные рисунки Microsoft DirectX, и растровые изображения, отображаемые в окне (точечные рисунки HWND).</span><span class="sxs-lookup"><span data-stu-id="b1c62-113">DirectComposition can accept bitmap content drawn by different rendering libraries, including Microsoft DirectX bitmaps, and bitmaps rendered to a window (HWND bitmaps).</span></span> <span data-ttu-id="b1c62-114">Кроме того, DirectComposition поддерживает разнообразные преобразования, такие как двухмерные преобразования 2D и трехмерные перспективы, а также базовые эффекты, такие как обрезка и непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="b1c62-114">Also, DirectComposition supports a variety of transformations, such as 2D affine transforms and 3D perspective transforms, as well as basic effects such as clipping and opacity.</span></span>

<span data-ttu-id="b1c62-115">DirectComposition предназначен для упрощения процесса составления [*визуальных элементов*](directcomposition-glossary.md) и создания анимированных переходов.</span><span class="sxs-lookup"><span data-stu-id="b1c62-115">DirectComposition is designed to simplify the process of composing [*visuals*](directcomposition-glossary.md) and creating animated transitions.</span></span> <span data-ttu-id="b1c62-116">Если приложение уже содержит код подготовки к просмотру или уже использует рекомендованный API DirectX, достаточно выполнить минимальный объем работы, чтобы эффективно использовать DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b1c62-116">If your application already contains rendering code or already uses the recommended DirectX API, you only need to do a minimal amount of work to use DirectComposition effectively.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b1c62-117">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="b1c62-117">Developer audience</span></span>

<span data-ttu-id="b1c62-118">API DirectComposition предназначен для опытных и высокопроизводительных графических разработчиков, знающих C/C++, имеющих полное представление об объектной модели компонентов (COM) и знакомство с концепциями программирования Windows.</span><span class="sxs-lookup"><span data-stu-id="b1c62-118">The DirectComposition API is intended for experienced and highly-capable graphics developers who know C/C++, have a solid understanding of the Component Object Model (COM), and are familiar with Windows programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b1c62-119">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="b1c62-119">Run-time requirements</span></span>

<span data-ttu-id="b1c62-120">DirectComposition появился в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1c62-120">DirectComposition was introduced in Windows 8.</span></span> <span data-ttu-id="b1c62-121">Он включается в 32-разрядные, 64-битные и процессорные платформы ARM.</span><span class="sxs-lookup"><span data-stu-id="b1c62-121">It is included in 32-bit, 64-bit, and ARM platforms.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b1c62-122">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b1c62-122">In this section</span></span>



| <span data-ttu-id="b1c62-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="b1c62-123">Topic</span></span>                                                                       | <span data-ttu-id="b1c62-124">Описание</span><span class="sxs-lookup"><span data-stu-id="b1c62-124">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1c62-125">Зачем использовать DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="b1c62-125">Why use DirectComposition?</span></span>](why-use-directcomposition-.md)<br/>     | <span data-ttu-id="b1c62-126">В этом разделе описываются возможности и преимущества DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b1c62-126">This topic describes the capabilities and benefits of DirectComposition.</span></span> <br/>                                                                           |
| [<span data-ttu-id="b1c62-127">Как использовать DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b1c62-127">How to Use DirectComposition</span></span>](how-to-use-directcomposition.md)<br/> | <span data-ttu-id="b1c62-128">В этом разделе описываются рекомендации по использованию API DirectComposition и демонстрируется использование API для выполнения нескольких распространенных задач.</span><span class="sxs-lookup"><span data-stu-id="b1c62-128">This section describes best practices for using the DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span> <br/> |
| [<span data-ttu-id="b1c62-129">Основные понятия DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b1c62-129">DirectComposition concepts</span></span>](directcomposition-concepts.md)<br/>     | <span data-ttu-id="b1c62-130">Этот раздел содержит общие сведения о DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b1c62-130">This section provides a conceptual overview of DirectComposition.</span></span><br/>                                                                                   |
| [<span data-ttu-id="b1c62-131">Справочник по DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b1c62-131">DirectComposition reference</span></span>](reference.md)<br/>                     | <span data-ttu-id="b1c62-132">В этом разделе содержатся подробные справочные сведения об элементах, которые составляют API DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b1c62-132">This section provides detailed reference information for the elements that make up the DirectComposition API.</span></span><br/>                                       |
| [<span data-ttu-id="b1c62-133">Примеры DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b1c62-133">DirectComposition samples</span></span>](directcomposition-code-samples.md)<br/>  | <span data-ttu-id="b1c62-134">В следующих примерах приложений показано, как использовать API DirectComposition и продемонстрировать его возможности.</span><span class="sxs-lookup"><span data-stu-id="b1c62-134">The following sample applications show how to use the DirectComposition API and demonstrate its capabilities.</span></span> <br/>                                      |
| [<span data-ttu-id="b1c62-135">Глоссарий DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b1c62-135">DirectComposition glossary</span></span>](directcomposition-glossary.md)<br/>     | <span data-ttu-id="b1c62-136">В этом разделе определяются термины DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b1c62-136">This topic defines DirectComposition terms.</span></span> <br/>                                                                                                        |



 

 

 





