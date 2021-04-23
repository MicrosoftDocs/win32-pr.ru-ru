---
title: Упаковка библиотеки шейдеров
description: Здесь мы покажем, как скомпилировать код шейдера, загрузить скомпилированный код в библиотеку шейдеров и привязать ресурсы из исходных слотов к конечным слотам.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997146"
---
# <a name="packaging-a-shader-library"></a><span data-ttu-id="8ea28-103">Упаковка библиотеки шейдеров</span><span class="sxs-lookup"><span data-stu-id="8ea28-103">Packaging a shader library</span></span>

<span data-ttu-id="8ea28-104">Здесь мы покажем, как скомпилировать код шейдера, загрузить скомпилированный код в библиотеку шейдеров и привязать ресурсы из исходных слотов к конечным слотам.</span><span class="sxs-lookup"><span data-stu-id="8ea28-104">Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="8ea28-105">**Цель:** Упаковка библиотеки шейдеров для использования при связывании с шейдером.</span><span class="sxs-lookup"><span data-stu-id="8ea28-105">**Objective:** To package a shader library to use for shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8ea28-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="8ea28-106">Prerequisites</span></span>

<span data-ttu-id="8ea28-107">Предполагается, что вы знакомы с C++.</span><span class="sxs-lookup"><span data-stu-id="8ea28-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="8ea28-108">Также вы должны быть знакомы с основными принципами программирования графики.</span><span class="sxs-lookup"><span data-stu-id="8ea28-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="8ea28-109">**Время на выполнение:** 30 минут.</span><span class="sxs-lookup"><span data-stu-id="8ea28-109">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="8ea28-110">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8ea28-110">Instructions</span></span>

### <a name="1-compiling-your-shader-code"></a><span data-ttu-id="8ea28-111">1. Компиляция кода шейдера</span><span class="sxs-lookup"><span data-stu-id="8ea28-111">1. Compiling your shader code</span></span>

<span data-ttu-id="8ea28-112">Скомпилируйте код шейдера с помощью одной из функций компиляции.</span><span class="sxs-lookup"><span data-stu-id="8ea28-112">Compile your shader code with one of the compile functions.</span></span> <span data-ttu-id="8ea28-113">Например, в этом фрагменте кода используется [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="8ea28-113">For example, this code snippet uses [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span></span>

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

<span data-ttu-id="8ea28-114">Исходная строка содержит некомпилированный код ASCII HLSL.</span><span class="sxs-lookup"><span data-stu-id="8ea28-114">The source string contains the uncompiled ASCII HLSL code.</span></span>

### <a name="2-load-the-compiled-code-into-a-shader-library"></a><span data-ttu-id="8ea28-115">2. Загрузите скомпилированный код в библиотеку шейдера.</span><span class="sxs-lookup"><span data-stu-id="8ea28-115">2. Load the compiled code into a shader library.</span></span>

<span data-ttu-id="8ea28-116">Вызовите функцию [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) , чтобы загрузить скомпилированный код ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) в модуль ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)), представляющий библиотеку шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8ea28-116">Call the [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) function to load the compiled code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) into a module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) that represents a shader library.</span></span>


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a><span data-ttu-id="8ea28-117">3. привяжите ресурсы из исходных слотов к конечным слотам.</span><span class="sxs-lookup"><span data-stu-id="8ea28-117">3. Bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="8ea28-118">Вызовите метод [**ID3D11Module:: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) , чтобы создать экземпляр ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) библиотеки, чтобы затем можно было определить привязки ресурсов для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8ea28-118">Call the [**ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) method to create an instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) of the library so you can then define resource bindings for the instance.</span></span>

<span data-ttu-id="8ea28-119">Вызовите методы BIND класса [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) , чтобы привязать необходимые ресурсы из исходных слотов к конечным слотам.</span><span class="sxs-lookup"><span data-stu-id="8ea28-119">Call the bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) to bind the resources you need from source slots to destination slots.</span></span> <span data-ttu-id="8ea28-120">Ресурсами могут быть текстуры, буферы, пробы, буферы констант или Уавс.</span><span class="sxs-lookup"><span data-stu-id="8ea28-120">The resources can be textures, buffers, samplers, constant buffers, or UAVs.</span></span> <span data-ttu-id="8ea28-121">Как правило, будут использоваться те же слоты, что и в исходной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="8ea28-121">Typically, you will use the same slots as the source library.</span></span>


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



<span data-ttu-id="8ea28-122">Этот код HLSL показывает, что исходная библиотека использует те же слоты (T0, S0, B0, B1 и B2), что и слоты, используемые в предыдущих методах привязки [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span><span class="sxs-lookup"><span data-stu-id="8ea28-122">This HLSL code shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span></span>

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a><span data-ttu-id="8ea28-123">Сводка и дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="8ea28-123">Summary and next steps</span></span>

<span data-ttu-id="8ea28-124">Мы скомпилированы код шейдера, загрузили скомпилированный код в библиотеку шейдеров и привязанные ресурсы из исходных слотов в конечные слоты.</span><span class="sxs-lookup"><span data-stu-id="8ea28-124">We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.</span></span>

<span data-ttu-id="8ea28-125">Далее мы создаем функции-Links-Graphs (Флгс) для шейдеров, связываем их с скомпилированным кодом и создаем большие двоичные объекты шейдера, которые может использовать среда выполнения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8ea28-125">Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.</span></span>

[<span data-ttu-id="8ea28-126">Создание графа связывания функций и связывание его с скомпилированным кодом</span><span class="sxs-lookup"><span data-stu-id="8ea28-126">Constructing a function-linking-graph and linking it to compiled code</span></span>](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a><span data-ttu-id="8ea28-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8ea28-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea28-128">Использование связывания шейдера</span><span class="sxs-lookup"><span data-stu-id="8ea28-128">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 