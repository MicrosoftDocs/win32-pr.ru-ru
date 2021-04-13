---
description: 'В этом разделе содержатся сведения о следующих интерфейсах шейдера:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Интерфейсы шейдера (графика Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496302"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a><span data-ttu-id="4c459-103">Интерфейсы шейдера (графика Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4c459-103">Shader Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="4c459-104">В этом разделе содержатся сведения о следующих интерфейсах шейдера:</span><span class="sxs-lookup"><span data-stu-id="4c459-104">This section contains information about the following shader interfaces:</span></span>

<span data-ttu-id="4c459-105">Каждый из этих интерфейсов шейдера управляет скомпилированным шейдером.</span><span class="sxs-lookup"><span data-stu-id="4c459-105">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="4c459-106">Интерфейс создается при компиляции шейдера и передается различным интерфейсам API, которым требуется доступ к скомпилированному шейдеру. Например, при привязке шейдера к этапу конвейера или при получении сигнатуры шейдера.</span><span class="sxs-lookup"><span data-stu-id="4c459-106">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>



| <span data-ttu-id="4c459-107">Интерфейсы Pipeline-Stage</span><span class="sxs-lookup"><span data-stu-id="4c459-107">Pipeline-Stage Interfaces</span></span>                                      | <span data-ttu-id="4c459-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4c459-108">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c459-109">**Интерфейс ID3D10GeometryShader**</span><span class="sxs-lookup"><span data-stu-id="4c459-109">**ID3D10GeometryShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | <span data-ttu-id="4c459-110">Геометрический шейдер реализует обработку на основе примитивов на [этапе Geometry-Shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="4c459-110">A geometry-shader implements per-primitive processing in the [geometry-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> |
| [<span data-ttu-id="4c459-111">**Интерфейс ID3D10PixelShader**</span><span class="sxs-lookup"><span data-stu-id="4c459-111">**ID3D10PixelShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | <span data-ttu-id="4c459-112">Пиксельный шейдер реализует обработку на пиксель на [этапе пиксельного шейдера](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="4c459-112">A pixel-shader implements per-pixel processing in the [pixel-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>           |
| [<span data-ttu-id="4c459-113">**Интерфейс ID3D10VertexShader**</span><span class="sxs-lookup"><span data-stu-id="4c459-113">**ID3D10VertexShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | <span data-ttu-id="4c459-114">Вершинный шейдер реализует обработку на вершину на [этапе вершинного шейдера](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="4c459-114">A vertex-shader implements per-vertex processing in the [vertex-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>        |



 

<span data-ttu-id="4c459-115">Интерфейсы отражения шейдеров позволяют приложению проверять содержимое шейдера во время проектирования или разработки.</span><span class="sxs-lookup"><span data-stu-id="4c459-115">Shader-reflection interfaces allow an application to inspect the contents of a shader at design/author time.</span></span> <span data-ttu-id="4c459-116">Отражение шейдера не полезно для настройки переменных во время выполнения, так как оно является зеркалом данных шейдера и поэтому не поддерживает методы для настройки данных.</span><span class="sxs-lookup"><span data-stu-id="4c459-116">Shader reflection is not useful for setting variables at runtime as it is a mirror of the shader data, and therefore supports no methods for setting data.</span></span>



| <span data-ttu-id="4c459-117">Интерфейсы Shader-Reflection</span><span class="sxs-lookup"><span data-stu-id="4c459-117">Shader-Reflection Interfaces</span></span>                                                                   | <span data-ttu-id="4c459-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4c459-118">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c459-119">**Интерфейс ID3D10ShaderReflection**</span><span class="sxs-lookup"><span data-stu-id="4c459-119">**ID3D10ShaderReflection Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | <span data-ttu-id="4c459-120">COM-интерфейс для чтения информации из скомпилированного шейдера во время создания.</span><span class="sxs-lookup"><span data-stu-id="4c459-120">A COM interface for reading information from a compiled shader at author time.</span></span>     |
| [<span data-ttu-id="4c459-121">**Интерфейс ID3D10ShaderReflectionConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="4c459-121">**ID3D10ShaderReflectionConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | <span data-ttu-id="4c459-122">Вспомогательный интерфейс для получения интерфейса буфера констант с отражением шейдера.</span><span class="sxs-lookup"><span data-stu-id="4c459-122">A helper interface for getting a shader-reflection constant-buffer interface.</span></span>      |
| [<span data-ttu-id="4c459-123">**Интерфейс ID3D10ShaderReflectionType**</span><span class="sxs-lookup"><span data-stu-id="4c459-123">**ID3D10ShaderReflectionType Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | <span data-ttu-id="4c459-124">Вспомогательный интерфейс для получения интерфейса типа шейдера-отражения.</span><span class="sxs-lookup"><span data-stu-id="4c459-124">A helper interface for getting a shader-reflection-type interface.</span></span>                 |
| [<span data-ttu-id="4c459-125">**Интерфейс ID3D10ShaderReflectionVariable**</span><span class="sxs-lookup"><span data-stu-id="4c459-125">**ID3D10ShaderReflectionVariable Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | <span data-ttu-id="4c459-126">Вспомогательный интерфейс для получения интерфейса-переменной шейдера с отражением.</span><span class="sxs-lookup"><span data-stu-id="4c459-126">A helper interface for getting a shader-reflection-variable interface.</span></span>             |
| [<span data-ttu-id="4c459-127">**Интерфейс ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="4c459-127">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | <span data-ttu-id="4c459-128">Интерфейс отражения шейдера для чтения информации из представления "шейдер — ресурс".</span><span class="sxs-lookup"><span data-stu-id="4c459-128">A shader-reflection interface for reading information from a shader-resource view.</span></span> |



 

<span data-ttu-id="4c459-129">Интерфейсы API отражения шейдеров реализуют один интерфейс отражения шейдера COM ([**интерфейс ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) и несколько вспомогательных интерфейсов, отличных от com (остальные интерфейсы).</span><span class="sxs-lookup"><span data-stu-id="4c459-129">Shader reflection APIs implement one COM shader reflection interface ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) and several non-COM helper interfaces (the rest of the interfaces).</span></span> <span data-ttu-id="4c459-130">**Интерфейс ID3D10ShaderReflection** создается при создании объекта отражения шейдера.</span><span class="sxs-lookup"><span data-stu-id="4c459-130">**ID3D10ShaderReflection Interface** is created when a shader reflection object is created.</span></span> <span data-ttu-id="4c459-131">Он соответствует стандартным правилам COM; Создание интерфейса увеличивает число ссылок, и интерфейс должен быть освобожден, если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="4c459-131">It follows standard COM rules; creating the interface increases a reference count and the interface must be released when it is no longer needed.</span></span> <span data-ttu-id="4c459-132">Остальные интерфейсы отражения шейдеров являются вспомогательными интерфейсами, которые не наследуют от IUnknown.</span><span class="sxs-lookup"><span data-stu-id="4c459-132">The remaining shader-reflection interfaces are helper interfaces that do not inherit from IUnknown.</span></span> <span data-ttu-id="4c459-133">Это означает, что они не изменяют счетчик ссылок при их создании, и их не нужно удалять по завершении работы с ними.</span><span class="sxs-lookup"><span data-stu-id="4c459-133">This means that they do not change any reference count when they are created, and they do not need to be destroyed when you are finished with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c459-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4c459-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c459-135">Справочник по шейдерам</span><span class="sxs-lookup"><span data-stu-id="4c459-135">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
