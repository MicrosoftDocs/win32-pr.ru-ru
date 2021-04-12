---
description: Пример Пртдемо и симулятор Прткмдлине, входящие в состав пакета SDK для DirectX, представляют векторы перемещения в вершинах сетки.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Представление PRT с текстурами (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262457"
---
# <a name="representing-prt-with-textures-direct3d-9"></a><span data-ttu-id="a1746-103">Представление PRT с текстурами (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1746-103">Representing PRT With Textures (Direct3D 9)</span></span>

<span data-ttu-id="a1746-104">Пример Пртдемо и симулятор Прткмдлине, входящие в состав пакета SDK для DirectX, представляют векторы перемещения в вершинах сетки.</span><span class="sxs-lookup"><span data-stu-id="a1746-104">The PRTDemo sample and PRTCmdLine simulator included in the DirectX SDK represent transfer vectors at the vertices of a mesh.</span></span> <span data-ttu-id="a1746-105">Чтобы точно представить сигнал PRT, это может потребовать тесселяции, которые могут оказаться непрактичными для текущих игр.</span><span class="sxs-lookup"><span data-stu-id="a1746-105">In order to represent the PRT signal accurately, this can require tessellations that may be impractical for current games.</span></span> <span data-ttu-id="a1746-106">Представление векторов перемещения в текстурных картах — это альтернативный подход, в котором стоимость данных зависит от сложности сетки.</span><span class="sxs-lookup"><span data-stu-id="a1746-106">Representing transfer vectors in texture maps is an alternative approach that has the same data cost independent of mesh complexity.</span></span> <span data-ttu-id="a1746-107">Существует несколько способов создания карт текстуры вектора перемещения с помощью библиотеки D3DX PRT.</span><span class="sxs-lookup"><span data-stu-id="a1746-107">There are several ways to generate transfer vector texture maps using the D3DX PRT Library.</span></span>

## <a name="precomputing-transfer-vectors"></a><span data-ttu-id="a1746-108">Предварительные вычисления векторов перемещения</span><span class="sxs-lookup"><span data-stu-id="a1746-108">Precomputing Transfer Vectors</span></span>

<span data-ttu-id="a1746-109">Один из подходов — изменить примеры Пртдемо и Прткмдлине, чтобы вычислить вектор перемещения для каждого шаг текселя в параметризации поверхности.</span><span class="sxs-lookup"><span data-stu-id="a1746-109">One approach would be to modify the PRTDemo and PRTCmdLine samples to compute a transfer vector at every texel in a parameterization of a surface.</span></span> <span data-ttu-id="a1746-110">Для этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a1746-110">To do this:</span></span>

1.  <span data-ttu-id="a1746-111">Измените вызов [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) , чтобы извлечь координаты текстуры из сетки (екстрактувс должны иметь **значение true**).</span><span class="sxs-lookup"><span data-stu-id="a1746-111">Modify the call to [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to extract texture coordinates from the mesh (ExtractUVs must be **TRUE**)</span></span>
2.  <span data-ttu-id="a1746-112">Замените вызовы [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) на [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) , используя тот же размер текстуры.</span><span class="sxs-lookup"><span data-stu-id="a1746-112">Replace [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) calls with [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) using the same texture size.</span></span>

<span data-ttu-id="a1746-113">Все методы ID3DXPRTEngine работают с имитацией "на шаг текселя", за исключением: Компутебаунцеадаптиве, Компутессадаптиве, COMPUTE и Компутедиректлигхтингшадаптиве.</span><span class="sxs-lookup"><span data-stu-id="a1746-113">All ID3DXPRTEngine methods work with per-texel simulations except for: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS, and ComputeDirectLightingSHAdaptive.</span></span> <span data-ttu-id="a1746-114">В то время как имитация пространства текстуры создает правильный результат, он часто может оказаться довольно длительным, поскольку он, скорее всего, будет рассчитывать векторы перемещения с высокой плотностью.</span><span class="sxs-lookup"><span data-stu-id="a1746-114">While texture-space simulation will generate the correct result, it can often be fairly slow since it will most likely be computing transfer vectors at a high density.</span></span>

<span data-ttu-id="a1746-115">Другой подход заключается в вычислении адаптивного имитации PRTа на вершину (с координатами текстуры, которые будут использоваться для каждого шаг текселя данных) и последующем вызове [**ID3DXPRTEngine:: ресамплебуффер**](id3dxprtengine--resamplebuffer.md) (с помощью выходного буфера, созданного с помощью [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) с соответствующим разрешением).</span><span class="sxs-lookup"><span data-stu-id="a1746-115">Another approach is to compute an adaptive per-vertex PRT simulation (with texture coordinates that will be used for the per-texel data) and then call [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (using an output buffer created using [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) at the appropriate resolution).</span></span> <span data-ttu-id="a1746-116">Это работает со всеми функциями D3DX PRT в пакете SDK и часто может быть гораздо более эффективным, чем прямое вычисление буфера обмена на шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="a1746-116">This works with all D3DX PRT functionality in the SDK and can often be much more efficient than directly computing a per-texel transfer buffer.</span></span>

## <a name="runtime-calculations"></a><span data-ttu-id="a1746-117">Вычисления среды выполнения</span><span class="sxs-lookup"><span data-stu-id="a1746-117">Runtime Calculations</span></span>

<span data-ttu-id="a1746-118">Если используется один кластер, результаты могут быть отфильтрованы и MIP, как и любая другая текстура, и шейдер пикселей идентично коду шейдера вершин, который поставляется с Пртдемо.</span><span class="sxs-lookup"><span data-stu-id="a1746-118">If a single cluster is used the results can be filtered and mip-mapped like any other texture and the pixel shader is identical to the vertex shader code that ships with PRTDemo.</span></span>

<span data-ttu-id="a1746-119">Если сжатие создает несколько кластеров, вы не сможете фильтровать или mipmap данные, поскольку индексы кластеризации не являются непрерывными.</span><span class="sxs-lookup"><span data-stu-id="a1746-119">If compression generates multiple clusters, you cannot filter or mipmap the data because clustering indexes are not continuous.</span></span> <span data-ttu-id="a1746-120">Ниже приведены некоторые альтернативы для обработки нескольких кластерных данных.</span><span class="sxs-lookup"><span data-stu-id="a1746-120">Here are some alternatives for handling multi-clustered data:</span></span>

-   <span data-ttu-id="a1746-121">Выполните все действия по фильтрации в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="a1746-121">Do all of the filtering yourself in the pixel shader.</span></span> <span data-ttu-id="a1746-122">К сожалению, это непрактично для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="a1746-122">Unfortunately, this is generally impractical for performance reasons.</span></span>
-   <span data-ttu-id="a1746-123">Если текстуры являются текстурами с низким разрешением, отличными от MIP, скорее всего, более эффективным будет просто вычислить освещение непосредственно в пространстве текстуры, где не будет выполняться фильтрация, и визуализировать объект с затененной текстурой.</span><span class="sxs-lookup"><span data-stu-id="a1746-123">If the textures are low resolution non mip-mapped textures (ie: light maps), it is most likely more efficient to just compute the lighting directly in texture space - where no filtering will occur, and render the object with a shaded texture.</span></span> <span data-ttu-id="a1746-124">По сути, это динамическая Текстурная схема, которая полностью создана на GPU.</span><span class="sxs-lookup"><span data-stu-id="a1746-124">This is essentially a dynamic light map that is created entirely on the GPU.</span></span>
-   <span data-ttu-id="a1746-125">Если используется текстура Atlas (см. раздел [Использование уватлас (Direct3D 9)](using-uvatlas.md)), можно вручную выполнить кластеризацию сцены, получив все векторы перемещения в подключенном компоненте в пространстве текстуры в том же кластере.</span><span class="sxs-lookup"><span data-stu-id="a1746-125">If a texture atlas is used (see [Using UVAtlas (Direct3D 9)](using-uvatlas.md)), you could manually cluster the scene by having all transfer vectors in a connected component in texture space be in the same cluster.</span></span> <span data-ttu-id="a1746-126">Таким образом можно отфильтровать текстуру, так как все пикселей текстуры, к которым осуществляется доступ, будут находиться в том же кластере, что и конструкция.</span><span class="sxs-lookup"><span data-stu-id="a1746-126">This way you can filter the texture because all texels accessed would be in the same cluster by construction.</span></span> <span data-ttu-id="a1746-127">ИДЕНТИФИКАТОР кластера для данного лица можно распространить из шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="a1746-127">The cluster ID for a given face could be propagated from the vertex shader.</span></span>

<span data-ttu-id="a1746-128">Шейдеры пикселей имеют гораздо меньше постоянных регистров, которые не могут быть проиндексированы, поэтому построитель текстуры немного отличается от шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="a1746-128">Pixel shaders have much fewer constant registers that cannot be indexed, so the pixel shader is somewhat different than the vertex shader.</span></span> <span data-ttu-id="a1746-129">Хранение работы в кластере в динамической текстуре с низким разрешением и использование загрузок текстур является наиболее эффективным способом визуализации при использовании нескольких кластеров.</span><span class="sxs-lookup"><span data-stu-id="a1746-129">Storing the per-cluster work in a low resolution dynamic texture and using texture loads would be the most efficient way to render when using multiple clusters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1746-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a1746-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1746-131">Предварительно вычисленный перенос Радианце</span><span class="sxs-lookup"><span data-stu-id="a1746-131">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> <dt>

<span data-ttu-id="a1746-132">[Демонстрационный пример PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="a1746-132">[PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)</span></span>
</dt> <dt>

<span data-ttu-id="a1746-133">[Симулятор PRT (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="a1746-133">[PRT Simulator (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 



