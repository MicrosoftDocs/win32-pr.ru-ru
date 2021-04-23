---
description: В Direct3D 10 состояние устройства сгруппировано в объекты состояния, что значительно сокращает затраты на изменение состояния.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Объекты состояния (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701165"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="ef3ac-103">Объекты состояния (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ef3ac-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="ef3ac-104">В Direct3D 10 состояние устройства сгруппировано в объекты состояния, что значительно сокращает затраты на изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="ef3ac-105">Есть несколько объектов состояния и каждый из них разработан для инициализации набора состояний определенной стадии конвейера.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="ef3ac-106">Можно создать до 4096 каждого типа объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="ef3ac-107">Входное состояние макета</span><span class="sxs-lookup"><span data-stu-id="ef3ac-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="ef3ac-108">Состояние средства программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="ef3ac-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="ef3ac-109">Состояние шаблона глубины</span><span class="sxs-lookup"><span data-stu-id="ef3ac-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="ef3ac-110">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="ef3ac-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="ef3ac-111">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="ef3ac-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="ef3ac-112">Вопросы производительности</span><span class="sxs-lookup"><span data-stu-id="ef3ac-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="ef3ac-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ef3ac-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="ef3ac-114">Состояние макета входных данных</span><span class="sxs-lookup"><span data-stu-id="ef3ac-114">Input-Layout State</span></span>

<span data-ttu-id="ef3ac-115">Эта группа состояний (см. [**D3D10 \_ input \_ element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) определяет, как на [этапе ввода ассемблера](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) происходит считывание данных из входных буферов и их сборка для использования шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="ef3ac-116">Сюда входит такое состояние, как число элементов в буфера ввода и подпись входных данных.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="ef3ac-117">Этап входного ассемблера — это новый этап в конвейере, задачей которого является потоковая передача примитивов из памяти в конвейер.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="ef3ac-118">Сведения о создании объекта состояния макета ввода см. в разделе [**креатеинпутлайаут**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="ef3ac-119">Состояние средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="ef3ac-119">Rasterizer State</span></span>

<span data-ttu-id="ef3ac-120">Эта группа состояний (см. [**D3D10 средство \_ растеризацииа \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) инициализирует [этап средства прорисовки](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="ef3ac-121">Этот объект содержит такие состояния, как режимы заливки и отбрасывания, включение прямоугольника обрезки и установка параметров множественной дискретизации.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="ef3ac-122">На этой стадии примитивы преобразуются в пиксели с помощью таких операций, как вырезание и сопоставление примитивов с окном просмотра.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="ef3ac-123">Сведения о создании объекта состояния средства растеризации см. в разделе [**креатерастеризерстате**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="ef3ac-124">Состояние трафарета глубины</span><span class="sxs-lookup"><span data-stu-id="ef3ac-124">Depth-Stencil State</span></span>

<span data-ttu-id="ef3ac-125">Эта группа состояний (см. [**D3D10 \_ Depth \_ трафарет \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) инициализирует часть этапа набора элементов глубины на [стадии слияния вывода](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="ef3ac-126">В частности этот объект инициализирует тесты глубины и трафарета.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="ef3ac-127">Сведения о создании объекта состояния глубины-трафарета см. в разделе [**креатедепсстенЦилстате**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="ef3ac-128">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="ef3ac-128">Blend State</span></span>

<span data-ttu-id="ef3ac-129">Эта группа состояний (см. [**D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) инициализирует часть наложения на [стадии слияния вывода](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="ef3ac-130">Сведения о создании объекта состояния Blend см. в разделе [**креатеблендстате**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="ef3ac-131">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="ef3ac-131">Sampler State</span></span>

<span data-ttu-id="ef3ac-132">Эта группа состояний (см. [**D3D10 \_ образец \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) инициализирует объект образца.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="ef3ac-133">Объект дискретизатора используется стадиями шейдера для фильтрации текстур в памяти.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3ac-134">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="ef3ac-134">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="ef3ac-135">В Direct3D 10 объект образца больше не привязан к определенной текстуре — он просто описывает, как выполнять фильтрацию по любому подключенному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-135">In Direct3D 10, the sampler object is no longer bound to a specific texture - it just describes how to do filtering given any attached resource.</span></span> |



 

<span data-ttu-id="ef3ac-136">Сведения о создании объекта состояния образца см. в разделе [**креатесамплерстате**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="ef3ac-137">Вопросы производительности</span><span class="sxs-lookup"><span data-stu-id="ef3ac-137">Performance Considerations</span></span>

<span data-ttu-id="ef3ac-138">Разработка API-интерфейса с применением объектов состояния дает несколько преимуществ в плане производительности.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="ef3ac-139">К ним относятся проверка состояния во время создания объекта, возможность кэширования объектов состояния на аппаратном уровне, значительно сокращает объем состояния, который передается во время вызова API, задающего состояние (путем передачи дескриптора на объект состояния вместо самого состояния).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="ef3ac-140">Для подобного повышения производительности следует создать объекты состояний при запуске приложения, задолго до цикла отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="ef3ac-141">Объекты состояния постоянны, то есть их нельзя изменить после создания.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="ef3ac-142">Вместо этого необходимо их уничтожать и создать заново.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="ef3ac-143">Чтобы справиться с этим ограничением, можно создать до 4096 каждого типа объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="ef3ac-144">Например, можно создать несколько объектов выборки с различными сочетаниями состояния выборки.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="ef3ac-145">Изменение состояния выборки выполняется с помощью вызова соответствующего API набора, который передает в объект маркер (в отличие от состояния образца).</span><span class="sxs-lookup"><span data-stu-id="ef3ac-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="ef3ac-146">Это значительно сокращает издержки во время формирования каждого кадра на изменение состояния, так как число вызовов и объем данных существенно снижается.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="ef3ac-147">Кроме того вы можете использовать систему эффектов, которая будет автоматически управлять эффективным созданием и уничтожением объектов состояния в вашем приложении.</span><span class="sxs-lookup"><span data-stu-id="ef3ac-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef3ac-148">См. также</span><span class="sxs-lookup"><span data-stu-id="ef3ac-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef3ac-149">Функции API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ef3ac-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
