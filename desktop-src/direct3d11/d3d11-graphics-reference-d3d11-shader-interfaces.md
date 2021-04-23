---
title: 'Интерфейсы шейдеров (графика Direct3D 11) '
description: В этом разделе содержатся сведения об интерфейсах шейдера.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- интерфейсы, шейдер Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55e591d56442b641482a76a4ec93c0055029fc0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414524"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a><span data-ttu-id="06e17-104">Интерфейсы шейдеров (графика Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="06e17-104">Shader Interfaces (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="06e17-105">В этом разделе содержатся сведения об интерфейсах шейдера.</span><span class="sxs-lookup"><span data-stu-id="06e17-105">This section contains information about the shader interfaces.</span></span>

<span data-ttu-id="06e17-106">Каждый из этих интерфейсов шейдера управляет скомпилированным шейдером.</span><span class="sxs-lookup"><span data-stu-id="06e17-106">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="06e17-107">Интерфейс создается при компиляции шейдера и передается различным интерфейсам API, которым требуется доступ к скомпилированному шейдеру. Например, при привязке шейдера к этапу конвейера или при получении сигнатуры шейдера.</span><span class="sxs-lookup"><span data-stu-id="06e17-107">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="06e17-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="06e17-108">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06e17-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="06e17-109">Topic</span></span></th>
<th><span data-ttu-id="06e17-110">Описание</span><span class="sxs-lookup"><span data-stu-id="06e17-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06e17-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-112">Этот интерфейс инкапсулирует класс HLSL.</span><span class="sxs-lookup"><span data-stu-id="06e17-112">This interface encapsulates an HLSL class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-114">Этот интерфейс инкапсулирует динамическую компоновку HLSL.</span><span class="sxs-lookup"><span data-stu-id="06e17-114">This interface encapsulates an HLSL dynamic linkage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-116">Интерфейс шейдера вычислений управляет исполняемой программой (шейдером вычислений), которая управляет этапом COMPUTE-Shader.</span><span class="sxs-lookup"><span data-stu-id="06e17-116">A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-118">Интерфейс шейдера домена управляет исполняемой программой (шейдером доменов), которая управляет стадией шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="06e17-118">A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-120">Интерфейс графа с функциями компоновки используется для создания шейдеров, состоящих из последовательности вызовов предкомпилированных функций, которые передают значения друг другу.</span><span class="sxs-lookup"><span data-stu-id="06e17-120">A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-121">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-121">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-123">Интерфейс отражения функции обращается к сведениям о функции.</span><span class="sxs-lookup"><span data-stu-id="06e17-123">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-124">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-124">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-126">Интерфейс отражения параметров функции обращается к сведениям о параметрах функции.</span><span class="sxs-lookup"><span data-stu-id="06e17-126">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-127">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-127">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-129">Интерфейс шейдера Geometry управляет исполняемой программой (шейдером Geometry), которая управляет стадией шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="06e17-129">A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-131">Интерфейс шейдера поверхности управляет исполняемой программой (шейдером поверхности), которая управляет стадией поверхности-Shader.</span><span class="sxs-lookup"><span data-stu-id="06e17-131">A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-133">Интерфейс отражения библиотеки обращается к сведениям о библиотеке.</span><span class="sxs-lookup"><span data-stu-id="06e17-133">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-134">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-134">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-136">Интерфейс компоновщика используется для связи модуля шейдера.</span><span class="sxs-lookup"><span data-stu-id="06e17-136">A linker interface is used to link a shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-137">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-137">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-139">Для связывания с шейдером используется интерфейс связывания и узлов.</span><span class="sxs-lookup"><span data-stu-id="06e17-139">A linking-node interface is used for shader linking.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-140">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-140">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-142">Интерфейс модуля создает экземпляр модуля, который используется для повторной привязки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06e17-142">A module interface creates an instance of a module that is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-143">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-143">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-145">Интерфейс экземпляра модуля используется для повторной привязки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06e17-145">A module-instance interface is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06e17-146">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="06e17-146">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-148">Интерфейс построителя текстуры управляет исполняемой программой (построитель текстуры), которая управляет стадией построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="06e17-148">A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-150">Интерфейс отражения шейдеров получает доступ к сведениям шейдера.</span><span class="sxs-lookup"><span data-stu-id="06e17-150">A shader-reflection interface accesses shader information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-152">Этот интерфейс отражения шейдеров предоставляет доступ к буферу констант.</span><span class="sxs-lookup"><span data-stu-id="06e17-152">This shader-reflection interface provides access to a constant buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-154">Этот интерфейс отражения шейдеров предоставляет доступ к типу переменной.</span><span class="sxs-lookup"><span data-stu-id="06e17-154">This shader-reflection interface provides access to variable type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-156">Этот интерфейс отражения шейдеров предоставляет доступ к переменной.</span><span class="sxs-lookup"><span data-stu-id="06e17-156">This shader-reflection interface provides access to a variable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-158">Интерфейс <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> реализует методы для получения трассировок выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="06e17-158">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> interface implements methods for obtaining traces of shader executions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06e17-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-160">Интерфейс <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> реализует метод для создания объектов сведений о трассировке шейдера.</span><span class="sxs-lookup"><span data-stu-id="06e17-160">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> interface implements a method for generating shader trace information objects.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e17-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e17-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="06e17-162">Интерфейс шейдера вершин управляет исполняемой программой (вершинным шейдером), которая управляет стадией шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="06e17-162">A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="06e17-163">См. также</span><span class="sxs-lookup"><span data-stu-id="06e17-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06e17-164">Справочник по шейдерам</span><span class="sxs-lookup"><span data-stu-id="06e17-164">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

