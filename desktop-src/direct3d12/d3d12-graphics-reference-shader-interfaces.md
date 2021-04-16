---
title: Интерфейсы шейдера (графика Direct3D 12)
description: D3d12shader. h объявляет следующие интерфейсы.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- интерфейсы, шейдер Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105719184"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a><span data-ttu-id="3ed4f-104">Интерфейсы шейдера (графика Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="3ed4f-104">Shader Interfaces (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="3ed4f-105">d3d12shader. h объявляет следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-105">d3d12shader.h declares the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ed4f-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="3ed4f-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ed4f-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="3ed4f-107">Topic</span></span></th>
<th><span data-ttu-id="3ed4f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3ed4f-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ed4f-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed4f-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="3ed4f-110">Интерфейс отражения параметров функции обращается к сведениям о параметрах функции.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-110">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3ed4f-111">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-111">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed4f-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed4f-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="3ed4f-113">Интерфейс отражения функции обращается к сведениям о функции.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-113">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3ed4f-114">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-114">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ed4f-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed4f-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="3ed4f-116">Интерфейс отражения библиотеки обращается к сведениям о библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-116">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3ed4f-117">Этот интерфейс является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 12 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-117">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed4f-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed4f-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="3ed4f-119">Интерфейс отражения шейдеров получает доступ к сведениям шейдера.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-119">A shader-reflection interface accesses shader information.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ed4f-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed4f-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="3ed4f-121">Этот интерфейс отражения шейдеров предоставляет доступ к буферу констант.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-121">This shader-reflection interface provides access to a constant buffer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ed4f-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed4f-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="3ed4f-123">Этот интерфейс отражения шейдеров предоставляет доступ к типу переменной.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-123">This shader-reflection interface provides access to variable type.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ed4f-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ed4f-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="3ed4f-125">Этот интерфейс отражения шейдеров предоставляет доступ к переменной.</span><span class="sxs-lookup"><span data-stu-id="3ed4f-125">This shader-reflection interface provides access to a variable.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3ed4f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3ed4f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ed4f-127">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3ed4f-127">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="3ed4f-128">Справочник по шейдерам</span><span class="sxs-lookup"><span data-stu-id="3ed4f-128">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





