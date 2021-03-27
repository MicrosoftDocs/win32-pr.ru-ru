---
title: Представления порядка программной прорисовки
description: В упорядоченных представлениях средства растеризации (РОВС) разрешается, что код шейдера пикселей помечает привязки UAV с помощью объявления, изменяющего нормальные требования к порядку результатов графического конвейера для Уавс.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134315"
---
# <a name="rasterizer-order-views"></a><span data-ttu-id="1042f-103">Представления порядка программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="1042f-103">Rasterizer Order Views</span></span>

<span data-ttu-id="1042f-104">В упорядоченных представлениях средства растеризации (РОВС) разрешается, что код шейдера пикселей помечает привязки UAV с помощью объявления, изменяющего нормальные требования к порядку результатов графического конвейера для Уавс.</span><span class="sxs-lookup"><span data-stu-id="1042f-104">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="1042f-105">Это позволяет использовать алгоритмы независимой прозрачности заказов (OIT), что дает гораздо более лучшие результаты визуализации, когда несколько прозрачных объектов находятся в разных строках в представлении.</span><span class="sxs-lookup"><span data-stu-id="1042f-105">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span>

-   [<span data-ttu-id="1042f-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="1042f-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="1042f-107">Сведения о реализации</span><span class="sxs-lookup"><span data-stu-id="1042f-107">Implementation details</span></span>](#implementation-details)
-   [<span data-ttu-id="1042f-108">Сводка по API</span><span class="sxs-lookup"><span data-stu-id="1042f-108">API summary</span></span>](#api-summary)
-   [<span data-ttu-id="1042f-109">См. также</span><span class="sxs-lookup"><span data-stu-id="1042f-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="1042f-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="1042f-110">Overview</span></span>

<span data-ttu-id="1042f-111">В стандартных графических конвейерах могут возникнуть проблемы с правильной компоновкой нескольких текстур, содержащих прозрачность.</span><span class="sxs-lookup"><span data-stu-id="1042f-111">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="1042f-112">Для получения желаемого эффекта объекты, такие как провода, растительности и цветные границы, используют прозрачность.</span><span class="sxs-lookup"><span data-stu-id="1042f-112">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="1042f-113">Проблемы возникают, когда несколько текстур, содержащих прозрачность, расположены друг с другом (в качестве примера это повышена ограждение перед созданием стекла, содержащим растительности).</span><span class="sxs-lookup"><span data-stu-id="1042f-113">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="1042f-114">Упорядоченные представления средства растеризации (РОВС) позволяют базовым алгоритмам OIT использовать возможности оборудования для правильного разрешения порядка прозрачности.</span><span class="sxs-lookup"><span data-stu-id="1042f-114">Rasterizer ordered views (ROVs) enable the underlying OIT algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="1042f-115">Прозрачность обрабатывается шейдером пикселей.</span><span class="sxs-lookup"><span data-stu-id="1042f-115">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="1042f-116">В упорядоченных представлениях средства растеризации (РОВС) разрешается, что код шейдера пикселей помечает привязки UAV с помощью объявления, изменяющего нормальные требования к порядку результатов графического конвейера для Уавс.</span><span class="sxs-lookup"><span data-stu-id="1042f-116">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

<span data-ttu-id="1042f-117">РОВС гарантирует порядок доступа к UAV для любой пары перекрывающихся вызовов шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="1042f-117">ROVs guarantee the order of UAV accesses for any pair of overlapping pixel shader invocations.</span></span> <span data-ttu-id="1042f-118">В этом случае "перекрытие" означает, что вызовы создаются одними вызовами Draw и используют одну и ту же пиксельную координату в режиме выполнения с частотой в пикселях, а также один и тот же пиксель и образец координат в режиме выборки частоты.</span><span class="sxs-lookup"><span data-stu-id="1042f-118">In this case “overlapping” means that the invocations are generated by the same draw calls and share the same pixel coordinate when in pixel-frequency execution mode, and the same pixel and sample coordinate in sample-frequency mode.</span></span>

<span data-ttu-id="1042f-119">Порядок, в котором перекрывающиеся РОВы вызовов построителей текстуры, выполняются аналогично порядку отправки геометрии.</span><span class="sxs-lookup"><span data-stu-id="1042f-119">The order in which overlapping ROV accesses of pixel shader invocations are executed is identical to the order in which the geometry is submitted.</span></span> <span data-ttu-id="1042f-120">Это означает, что для перекрывания вызовов шейдера пикселей операции записи ров, выполняемые вызовом шейдера пикселей, должны быть доступны для чтения при последующем вызове и не должны влиять на считывание при предыдущем вызове.</span><span class="sxs-lookup"><span data-stu-id="1042f-120">This means that, for overlapping pixel shader invocations, ROV writes performed by a pixel shader invocation must be available to be read by a subsequent invocation and must not affect reads by a previous invocation.</span></span> <span data-ttu-id="1042f-121">Операции чтения ров, выполняемые вызовом шейдера пикселей, должны отражать операции записи при предыдущем вызове и не должны отражать операции записи при последующем вызове.</span><span class="sxs-lookup"><span data-stu-id="1042f-121">ROV reads performed by a pixel shader invocation must reflect writes by a previous invocation and must not reflect writes by a subsequent invocation.</span></span> <span data-ttu-id="1042f-122">Это важно для Уавс, так как они явно опущены из-за невариации выходных данных, обычно задаются фиксированным порядком результатов графического конвейера.</span><span class="sxs-lookup"><span data-stu-id="1042f-122">This is important for UAVs because they are explicitly omitted from the output-invariance guarantees normally set by the fixed order of graphics pipeline results.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="1042f-123">Сведения о реализации</span><span class="sxs-lookup"><span data-stu-id="1042f-123">Implementation details</span></span>

<span data-ttu-id="1042f-124">Упорядоченные представления средства растеризации (РОВС) объявляются с помощью следующих новых объектов языка шейдеров высокого уровня (HLSL) и доступны только в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="1042f-124">Rasterizer ordered views (ROVs) are declared with the following new High Level Shader Language (HLSL) objects, and are only available to the pixel shader:</span></span>

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

<span data-ttu-id="1042f-125">Используйте эти объекты так же, как другие объекты UAV (например, `RWBuffer` и т. д.).</span><span class="sxs-lookup"><span data-stu-id="1042f-125">Use these objects in the same manner as other UAV objects (such as `RWBuffer` etc.).</span></span>

## <a name="api-summary"></a><span data-ttu-id="1042f-126">Сводные данные API</span><span class="sxs-lookup"><span data-stu-id="1042f-126">API summary</span></span>

<span data-ttu-id="1042f-127">РОВС — это конструкция только для HLSL, которая применяет различную семантику поведения к Уавс.</span><span class="sxs-lookup"><span data-stu-id="1042f-127">ROVs are an HLSL-only construct that applies different behavior semantics to UAVs.</span></span> <span data-ttu-id="1042f-128">Все API-интерфейсы, относящиеся к Уавс, также важны для РОВС.</span><span class="sxs-lookup"><span data-stu-id="1042f-128">All APIs relevant to UAVs are also relevant to ROVs.</span></span> <span data-ttu-id="1042f-129">Обратите внимание, что следующий метод, структуры и вспомогательный класс ссылаются на средство программной прорисовки:</span><span class="sxs-lookup"><span data-stu-id="1042f-129">Note that the following method, structures, and helper class reference the rasterizer:</span></span>

-   <span data-ttu-id="1042f-130">[**D3D11 \_ Средство программной ПРОРИСОВКи \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : структура, содержащая описание средства программной прорисовки, с указанием вспомогательного класса CD3D12 средства программной \_ прорисовки \_ для создания описаний средства растеризации.</span><span class="sxs-lookup"><span data-stu-id="1042f-130">[**D3D11\_RASTERIZER\_DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure holding the rasterizer description, noting the CD3D12\_RASTERIZER\_DESC2 helper class for creating rasterizer descriptions.</span></span>
-   <span data-ttu-id="1042f-131">[**D3D11 \_ FEATURE \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : структура, содержащая логическое значение `ROVsSupported` , обозначающее поддержку.</span><span class="sxs-lookup"><span data-stu-id="1042f-131">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure holding the boolean `ROVsSupported`, indicating the support.</span></span>
-   <span data-ttu-id="1042f-132">[**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : метод для доступа к поддерживаемым функциям.</span><span class="sxs-lookup"><span data-stu-id="1042f-132">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : method to access the supported features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1042f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="1042f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1042f-134">Функции Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="1042f-134">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="1042f-135">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="1042f-135">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 