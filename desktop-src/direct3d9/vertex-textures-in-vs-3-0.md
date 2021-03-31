---
description: Модель вершинного шейдера 3,0 поддерживает поиск текстур в шейдере вершин с помощью инструкции текслдл-VS текстуры Load.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Текстуры вершин в vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806520"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a><span data-ttu-id="a6f46-103">Текстуры вершин в VS \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a6f46-103">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>

<span data-ttu-id="a6f46-104">Модель вершинного шейдера 3,0 поддерживает поиск текстур в шейдере вершин с помощью инструкции [текслдл-VS](../direct3dhlsl/texldl---vs.md) текстуры Load.</span><span class="sxs-lookup"><span data-stu-id="a6f46-104">The vertex shader 3.0 model supports texture lookup in the vertex shader using the [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load statement.</span></span> <span data-ttu-id="a6f46-105">Ядро вершин содержит четыре этапа образца текстуры, именуемые [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 и D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="a6f46-105">The vertex engine contains four texture sampler stages, named [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2, and D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="a6f46-106">Они отличаются от образца карт смещения и выборки текстур в ядре пикселей.</span><span class="sxs-lookup"><span data-stu-id="a6f46-106">These are distinct from the displacement map sampler and texture samplers in the pixel engine.</span></span>

<span data-ttu-id="a6f46-107">Чтобы выбрать текстуры на этих четырех стадиях, можно использовать ядро вершин и программировать этапы с помощью метода [**чеккдевицеформат**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a6f46-107">To sample textures set at those four stages, you can use the vertex engine and program the stages with the [**CheckDeviceFormat**](/windows/desktop/api) method.</span></span> <span data-ttu-id="a6f46-108">Задайте текстуры на этих этапах с помощью [**сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), указав индекс промежуточного [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) через D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="a6f46-108">Set textures at those stages using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), with the stage index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) through D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="a6f46-109">Новый регистр появился в шейдере вершин, регистр образцов (как в PS \_ 2 \_ 0), который представляет собой образец текстуры вершин.</span><span class="sxs-lookup"><span data-stu-id="a6f46-109">A new register has been introduced in the vertex shader, the sampler register (like in ps\_2\_0), which represents the vertex texture sampler.</span></span> <span data-ttu-id="a6f46-110">Этот регистр необходимо определить в шейдере перед его использованием.</span><span class="sxs-lookup"><span data-stu-id="a6f46-110">This register needs to be defined in the shader before using it.</span></span>

<span data-ttu-id="a6f46-111">Приложение может запросить, поддерживается ли формат в качестве текстуры вершин, вызвав [**чеккдевицеформат**](/windows/desktop/api) с [D3DUSAGE \_ Query \_ вертекстекстуре](d3dusage-query.md).</span><span class="sxs-lookup"><span data-stu-id="a6f46-111">An application can query if a format is supported as a vertex texture by calling [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE](d3dusage-query.md).</span></span>

> [!Note]  
> <span data-ttu-id="a6f46-112">Это флаг запроса, поэтому он не принимается ни в одной функции Креатекскскс.</span><span class="sxs-lookup"><span data-stu-id="a6f46-112">This is a query flag so it is not accepted in any Createxxx function.</span></span> <span data-ttu-id="a6f46-113">Текстуру вершин, созданную в пуле по умолчанию, можно задать как текстуру пикселей и наоборот.</span><span class="sxs-lookup"><span data-stu-id="a6f46-113">A vertex texture created in the default pool can be set as a pixel texture and vice versa.</span></span> <span data-ttu-id="a6f46-114">Однако, чтобы использовать обработку вершин программного обеспечения, текстуру вершин необходимо создать в вспомогательном пуле (независимо от того, является ли это устройство смешанного режима или устройством обработки вершин).</span><span class="sxs-lookup"><span data-stu-id="a6f46-114">However, to use the software vertex processing, the vertex texture must be created in the scratch pool (no matter if it is a mixed-mode device or a software vertex processing device).</span></span>

 

<span data-ttu-id="a6f46-115">Функциональные возможности идентичны текстурам в пикселях, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="a6f46-115">The functionality is identical to the pixel textures, except for the following:</span></span>

-   <span data-ttu-id="a6f46-116">Фильтрация по анизотропной текстуре не поддерживается, поэтому D3DSAMP \_ максанисотропи игнорируется, а D3DTEXF \_ анизотропию нельзя установить для увеличения или уменьшение для этих этапов.</span><span class="sxs-lookup"><span data-stu-id="a6f46-116">Anisotropic texture filtering is not supported, hence D3DSAMP\_MAXANISOTROPY is ignored and D3DTEXF\_ANISOTROPIC cannot be set for magnify, or minify for these stages.</span></span>
-   <span data-ttu-id="a6f46-117">Интенсивность сведений об изменениях недоступна, поэтому приложение должно вычислять уровень детализации и предоставлять эту информацию в качестве параметра для [текслдл-VS](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="a6f46-117">Rate of change information is not available, hence the application has to compute the level of detail and provide that information as a parameter to [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="a6f46-118">К ним относятся указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="a6f46-118">Restrictions include:</span></span>

-   <span data-ttu-id="a6f46-119">Как и в шейдерах пикселей, если поддерживаются многоэлементные текстуры, D3DSAMP \_ елементиндекс используется для выяснения того, из какого элемента нужно выполнить выборку.</span><span class="sxs-lookup"><span data-stu-id="a6f46-119">As in pixel shaders, if multielement textures are supported, D3DSAMP\_ELEMENTINDEX is used to figure out which element to sample from.</span></span>
-   <span data-ttu-id="a6f46-120">Состояние D3DSAMP \_ дмапоффсет игнорируется для этих этапов.</span><span class="sxs-lookup"><span data-stu-id="a6f46-120">The state D3DSAMP\_DMAPOFFSET is ignored for these stages.</span></span>
-   <span data-ttu-id="a6f46-121">Используйте [**чеккдевицеформат**](/windows/desktop/api) с [D3DUSAGE \_ Query \_ вертекстекстуре "](d3dusage-query.md) , чтобы запросить текстуру, чтобы узнать, можно ли ее использовать в качестве текстуры вершин.</span><span class="sxs-lookup"><span data-stu-id="a6f46-121">Use [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE"](d3dusage-query.md) to query a texture to see if it can be used as a vertex texture.</span></span>
-   <span data-ttu-id="a6f46-122">Вертекстекстурефилтеркапс указывает, какие виды фильтров разрешены для образцов текстур вершин.</span><span class="sxs-lookup"><span data-stu-id="a6f46-122">VertexTextureFilterCaps indicates what kind of filters are allowed at the vertex texture samplers.</span></span> <span data-ttu-id="a6f46-123">[D3DPTFILTERCAPS \_ МИНФАНИСОТРОПИК](d3dptfiltercaps.md) и D3DPTFILTERCAPS \_ магфанисотропик запрещены.</span><span class="sxs-lookup"><span data-stu-id="a6f46-123">[D3DPTFILTERCAPS\_MINFANISOTROPIC](d3dptfiltercaps.md) and D3DPTFILTERCAPS\_MAGFANISOTROPIC are disallowed.</span></span>

## <a name="sampling-stage-registers"></a><span data-ttu-id="a6f46-124">Регистры этапа выборки</span><span class="sxs-lookup"><span data-stu-id="a6f46-124">Sampling Stage Registers</span></span>

<span data-ttu-id="a6f46-125">Регистр этапа выборки определяет единицу выборки, которую можно использовать в операторах загрузки текстур.</span><span class="sxs-lookup"><span data-stu-id="a6f46-125">A sampling stage register identifies a sampling unit that can be used in texture load statements.</span></span> <span data-ttu-id="a6f46-126">Единица выборки соответствует этапу выборки текстуры, в котором инкапсулировано состояние выборки, заданное в [**сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="a6f46-126">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span>

<span data-ttu-id="a6f46-127">Каждая выборка уникально определяет одну поверхность текстуры, для которой задан соответствующий образец с помощью [**сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="a6f46-127">Each sampler uniquely identifies a single texture surface that is set to the corresponding sampler using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="a6f46-128">Однако одну и ту же поверхность текстуры можно задать в нескольких пробах.</span><span class="sxs-lookup"><span data-stu-id="a6f46-128">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="a6f46-129">Во время рисования текстуру нельзя одновременно задать как цель рендеринга и текстуру на этапе.</span><span class="sxs-lookup"><span data-stu-id="a6f46-129">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="a6f46-130">Поскольку VS \_ 3 \_ 0 поддерживает четыре пробы, можно считывать до четырех поверхностей текстуры из одного прохода шейдера.</span><span class="sxs-lookup"><span data-stu-id="a6f46-130">Because vs\_3\_0 supports four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="a6f46-131">Регистр образца может отображаться только в качестве аргумента в операторе загрузки текстуры: [текслдл-VS](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="a6f46-131">A sampler register might appear only as an argument in the texture load statement: [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="a6f46-132">В VS \_ 3 \_ 0, если используется образец, он должен быть объявлен в начале программы шейдера с помощью [дкл \_ самплертипе (SM3-VS ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (как в PS \_ 2 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="a6f46-132">In vs\_3\_0, if you use a sampler, it must be declared at the beginning of the shader program, using the [dcl\_samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (as in ps\_2\_0).</span></span>

## <a name="software-processing"></a><span data-ttu-id="a6f46-133">Обработка программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="a6f46-133">Software Processing</span></span>

<span data-ttu-id="a6f46-134">Эта функция будет поддерживаться в процессе обработки вершин программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a6f46-134">This feature will be supported in software vertex processing.</span></span> <span data-ttu-id="a6f46-135">Поддерживаемые типы фильтров можно проверить путем вызова [**жетдевицекапс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) и проверки вертекстекстурефилтеркапс.</span><span class="sxs-lookup"><span data-stu-id="a6f46-135">The specific filter types supported can be checked by calling [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) and checking VertexTextureFilterCaps.</span></span> <span data-ttu-id="a6f46-136">Все опубликованные форматы текстур будут поддерживаться в качестве текстур вершин в обработке вершин программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a6f46-136">All published texture formats will be supported as vertex textures in software vertex processing.</span></span>

<span data-ttu-id="a6f46-137">Приложения могут проверить, поддерживается ли формат текстуры в режиме обработки вершин программного обеспечения, вызвав [**чеккдевицеформат**](/windows/desktop/api) и ПРЕДОСТАВИВ (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ софтварепроцессинг**](d3dusage.md)) в качестве использования.</span><span class="sxs-lookup"><span data-stu-id="a6f46-137">Applications can check if a particular texture format is supported in the software vertex processing mode by calling [**CheckDeviceFormat**](/windows/desktop/api) and providing (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md)) as usage.</span></span> <span data-ttu-id="a6f46-138">Для обработки вершин программного обеспечения поддерживаются все форматы.</span><span class="sxs-lookup"><span data-stu-id="a6f46-138">All formats are supported for software vertex processing.</span></span> <span data-ttu-id="a6f46-139">Для обработки вершин программного обеспечения требуется вспомогательный пул.</span><span class="sxs-lookup"><span data-stu-id="a6f46-139">The scratch pool is required for software vertex processing.</span></span>

## <a name="api-changes"></a><span data-ttu-id="a6f46-140">Изменения API</span><span class="sxs-lookup"><span data-stu-id="a6f46-140">API Changes</span></span>


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a><span data-ttu-id="a6f46-141">См. также</span><span class="sxs-lookup"><span data-stu-id="a6f46-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6f46-142">Конвейер вершин</span><span class="sxs-lookup"><span data-stu-id="a6f46-142">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
