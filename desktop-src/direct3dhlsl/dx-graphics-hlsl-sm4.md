---
title: Модель шейдера 4
description: Shader Model 4 является надмножеством возможностей в модели шейдера 3, за исключением того, что модель шейдеров 4 не поддерживает функции в модели шейдера 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412423"
---
# <a name="shader-model-4"></a><span data-ttu-id="f3fc8-103">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f3fc8-103">Shader Model 4</span></span>

<span data-ttu-id="f3fc8-104">Shader Model 4 является надмножеством возможностей в [модели шейдера 3](dx-graphics-hlsl-sm3.md), за исключением того, что модель шейдеров 4 не поддерживает функции в модели шейдера 1.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-104">Shader Model 4 is a superset of the capabilities in [Shader Model 3](dx-graphics-hlsl-sm3.md), except that Shader Model 4 doesn't support the features in Shader Model 1.</span></span> <span data-ttu-id="f3fc8-105">Она была разработана с помощью стандартного шейдера, предоставляющего общий набор функций для всех программируемых шейдеров, которые можно программировать только с помощью HLSL.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-105">It has been designed using a common-shader core that gives a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3fc8-106">Компонент</span><span class="sxs-lookup"><span data-stu-id="f3fc8-106">Feature</span></span></th>
<th><span data-ttu-id="f3fc8-107">Возможностями.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-107">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3fc8-108">Набор инструкций</span><span class="sxs-lookup"><span data-stu-id="f3fc8-108">Instruction Set</span></span></td>
<td><span data-ttu-id="f3fc8-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Функции HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3fc8-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fc8-110">Набор регистров</span><span class="sxs-lookup"><span data-stu-id="f3fc8-110">Register Set</span></span></td>
<td><span data-ttu-id="f3fc8-111">Набор регистров доступен через члены в постоянных и текстурных буферах с использованием семантики HLSL для таких операций, как упаковка компонентов.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-111">The register set is accessible through members in constant and texture buffers using HLSL semantics for things like component packing.</span></span>
<ul>
<li><span data-ttu-id="f3fc8-112">Регистры шейдеров пикселей (см. раздел <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">регистры-ps_4_0</a> и <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">регистры-ps_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="f3fc8-112">Pixel shader registers (see <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers - ps_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Registers - ps_4_1</a>)</span></span></li>
<li><span data-ttu-id="f3fc8-113">Регистры шейдеров вершин (см. раздел <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">регистры-vs_4_0</a> и <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">регистры-vs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="f3fc8-113">Vertex shader registers (see <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers - vs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Registers - vs_4_1</a>)</span></span></li>
<li><span data-ttu-id="f3fc8-114">Регистры шейдеров Geometry (см. раздел <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">регистры-gs_4_0</a> и <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">регистры-gs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="f3fc8-114">Geometry shader registers (see <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers - gs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Registers - gs_4_1</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fc8-115">Максимум вершинного шейдера</span><span class="sxs-lookup"><span data-stu-id="f3fc8-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="f3fc8-116">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="f3fc8-116">No restriction</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fc8-117">Максимальный размер шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="f3fc8-117">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="f3fc8-118">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="f3fc8-118">No restriction</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3fc8-119">Добавлены новые профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="f3fc8-119">New Shader Profiles Added</span></span></td>
<td><span data-ttu-id="f3fc8-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="f3fc8-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1\*</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3fc8-121">Добавлен новый профиль Effect-Framework</span><span class="sxs-lookup"><span data-stu-id="f3fc8-121">New Effect-Framework Profile Added</span></span></td>
<td><span data-ttu-id="f3fc8-122">fx_4_0, fx_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="f3fc8-122">fx_4_0, fx_4_1\*</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f3fc8-123">\* -GS \_ 4 \_ 1, PS \_ 4 1 \_ , VS \_ 4 \_ 1 и FX \_ 4 1 \_ поддерживаются в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-123">\* - gs\_4\_1, ps\_4\_1, vs\_4\_1 and fx\_4\_1 are supported on Direct3D 10.1 or higher.</span></span>

<span data-ttu-id="f3fc8-124">Модель шейдеров 4 поддерживает новый этап конвейера — этап шейдера Geometry, который можно использовать для создания или изменения существующей геометрии.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-124">Shader Model 4 supports a new pipeline stage—the geometry-shader stage—which can be used to create or modify existing geometry.</span></span> <span data-ttu-id="f3fc8-125">Он также включает два новых типа объектов: объект потокового вывода, предназначенный для потоковой передачи данных из этапа геометрии, и объект текстуры шаблона, реализующий функции выборки текстур.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-125">It also includes two new object types: a stream-output object designed for streaming data out of the geometry stage, and a templated texture object that implements texture sampling functions.</span></span>

-   [<span data-ttu-id="f3fc8-126">Основные компоненты шейдера</span><span class="sxs-lookup"><span data-stu-id="f3fc8-126">Common-Shader Core</span></span>](dx-graphics-hlsl-common-core.md)
-   [<span data-ttu-id="f3fc8-127">Константы</span><span class="sxs-lookup"><span data-stu-id="f3fc8-127">Constants</span></span>](dx-graphics-hlsl-constants.md)
-   [<span data-ttu-id="f3fc8-128">Объект Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="f3fc8-128">Geometry-Shader Object</span></span>](dx-graphics-hlsl-geometry-shader.md)
-   [<span data-ttu-id="f3fc8-129">Потоковый выходной объект</span><span class="sxs-lookup"><span data-stu-id="f3fc8-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
-   [<span data-ttu-id="f3fc8-130">Объект текстуры</span><span class="sxs-lookup"><span data-stu-id="f3fc8-130">Texture Object</span></span>](dx-graphics-hlsl-to-type.md)

<span data-ttu-id="f3fc8-131">Модель шейдеров 4 поддерживает правила упаковки, определяющие, насколько тесно данные могут быть упорядочены при хранении.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-131">Shader Model 4 supports packing rules that dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="f3fc8-132">Эти правила описаны в разделе [правила упаковки для константных переменных](dx-graphics-hlsl-packing-rules.md) .</span><span class="sxs-lookup"><span data-stu-id="f3fc8-132">These rules are described in [Packing Rules for Constant Variables](dx-graphics-hlsl-packing-rules.md)</span></span>

<span data-ttu-id="f3fc8-133">В разделе [Assembly Shader Model 4](dx-graphics-hlsl-sm4-asm.md) описаны инструкции ассемблера, поддерживаемые шейдером Model 4 и shader Model 4,1.</span><span class="sxs-lookup"><span data-stu-id="f3fc8-133">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) section describes the assembly instructions that the Shader Model 4 and Shader Model 4.1 support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3fc8-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f3fc8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3fc8-135">Модели шейдеров и профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="f3fc8-135">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




