---
title: Создание графа связывания функций и связывание его с скомпилированным кодом
description: В этой статье мы покажем, как создавать графы связывания функций (Флгс) для шейдеров и как связать эти шейдеры с библиотекой шейдеров для создания больших двоичных объектов шейдера, которые может использовать среда выполнения Direct3D.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890913"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a><span data-ttu-id="fdcb5-103">Создание графа связывания функций и связывание его с скомпилированным кодом</span><span class="sxs-lookup"><span data-stu-id="fdcb5-103">Constructing a function-linking-graph and linking it to compiled code</span></span>

<span data-ttu-id="fdcb5-104">В этой статье мы покажем, как создавать графы связывания функций (Флгс) для шейдеров и как связать эти шейдеры с библиотекой шейдеров для создания больших двоичных объектов шейдера, которые может использовать среда выполнения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-104">Here we show you how to construct function-linking-graphs (FLGs) for shaders and how to link those shaders with a shader library to produce shader blobs that the Direct3D runtime can use.</span></span>

<span data-ttu-id="fdcb5-105">**Цель:** Для создания графа связывания функций и связывания его с скомпилированным кодом.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-105">**Objective:** To construct a function-linking-graph and link it to compiled code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fdcb5-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="fdcb5-106">Prerequisites</span></span>

<span data-ttu-id="fdcb5-107">Предполагается, что вы знакомы с C++.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="fdcb5-108">Также вы должны быть знакомы с основными принципами программирования графики.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="fdcb5-109">Также предполагается, что вы выполнили [упаковку библиотеки шейдеров](pachaging-a-shader-library.md).</span><span class="sxs-lookup"><span data-stu-id="fdcb5-109">We also assume that you went through [Packaging a shader library](pachaging-a-shader-library.md).</span></span>

<span data-ttu-id="fdcb5-110">**Время на выполнение:** 30 минут.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-110">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="fdcb5-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="fdcb5-111">Instructions</span></span>

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a><span data-ttu-id="fdcb5-112">1. создайте граф связывания функций для шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-112">1. Construct a function-linking-graph for the vertex shader.</span></span>

<span data-ttu-id="fdcb5-113">Вызовите функцию [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) , чтобы создать диаграмму Function-Linking ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) для представления шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-113">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the vertex shader.</span></span>

<span data-ttu-id="fdcb5-114">Чтобы определить входные параметры для шейдера вершин, используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) Structures.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-114">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the vertex shader.</span></span> <span data-ttu-id="fdcb5-115">[Этап входного ассемблера](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) передает входные параметры в шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-115">The [Input-Assembler Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) feeds the input parameters to the vertex shader.</span></span> <span data-ttu-id="fdcb5-116">Макет входных параметров шейдера вершин соответствует макету шейдера вершин в скомпилированном коде.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-116">The layout of the vertex shader’s input parameters matches the layout of the vertex shader in the compiled code.</span></span> <span data-ttu-id="fdcb5-117">После определения входных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетинпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) , чтобы определить входной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-117">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> vertexShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &vertexShaderGraph));

            // Define the main input node which will be fed by the Input Assembler pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderInputParameters[] =
            {
                {"inputPos",  "POSITION0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputTex",  "TEXCOORD0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderInputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetInputSignature(vertexShaderInputParameters, ARRAYSIZE(vertexShaderInputParameters), 
                &vertexShaderInputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="fdcb5-118">Вызовите метод [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) , чтобы создать узел для основной функции шейдера вершин и вызвать [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из входного узла в узел для основной функции шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-118">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main vertex shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main vertex shader function.</span></span>


```C++
            // Create a node for the main VertexFunction call using the output of the helper functions.
            ComPtr<ID3D11LinkingNode> vertexFunctionCallNode;
            LinkingThrowIfFailed(vertexShaderGraph->CallFunction("", shaderLibrary.Get(), "VertexFunction", &vertexFunctionCallNode), 
                vertexShaderGraph.Get());

            // Define the graph edges from the input node and helper function nodes.
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForPos.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 0), vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexShaderInputNode.Get(), 1, vertexFunctionCallNode.Get(), 1), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForNorm.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 2), vertexShaderGraph.Get());
```



<span data-ttu-id="fdcb5-119">Используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) Structures, чтобы определить выходные параметры для шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-119">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the vertex shader.</span></span> <span data-ttu-id="fdcb5-120">Шейдер вершин передает выходные параметры в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-120">The vertex shader feeds its output parameters to the pixel shader.</span></span> <span data-ttu-id="fdcb5-121">Макет выходных параметров шейдера вершин соответствует макету шейдера пикселей в скомпилированном коде.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-121">The layout of the vertex shader’s output parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="fdcb5-122">После определения выходных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетаутпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) , чтобы определить выходной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-122">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            // Define the main output node which will feed the Pixel Shader pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderOutputParameters[] =
            {
                {"outputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderOutputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetOutputSignature(vertexShaderOutputParameters, ARRAYSIZE(vertexShaderOutputParameters), 
                &vertexShaderOutputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="fdcb5-123">Выполните вызовы [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из узла для основной функции шейдера вершин в выходной узел.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-123">Make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the node for the main vertex shader function to the output node.</span></span>


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



<span data-ttu-id="fdcb5-124">Вызовите метод [**ID3D11FunctionLinkingGraph:: креатемодулеинстанце**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) , чтобы завершить граф шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-124">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the vertex shader graph.</span></span>


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a><span data-ttu-id="fdcb5-125">2. Связывание шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="fdcb5-125">2. Link the vertex shader</span></span>

<span data-ttu-id="fdcb5-126">Вызовите функцию [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) , чтобы создать компоновщик ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)), который можно использовать для связывания экземпляра библиотеки шейдеров, созданной в [упаковке библиотеки шейдеров](pachaging-a-shader-library.md) , с экземпляром графа вершинного шейдера, созданного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-126">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the vertex shader graph that you created in the preceding step.</span></span> <span data-ttu-id="fdcb5-127">Вызовите метод [**ID3D11Linker:: уселибрари**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) , чтобы указать библиотеку шейдеров, используемую для компоновки.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-127">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="fdcb5-128">Вызовите метод [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) , чтобы связать библиотеку шейдеров с графом шейдера вершин и создать указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к скомпилированному коду шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-128">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the vertex shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled vertex shader code.</span></span> <span data-ttu-id="fdcb5-129">Затем можно передать этот скомпилированный код шейдера вершин в метод [**ID3D11Device:: креатевертексшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) , чтобы создать объект шейдера вершин и метод [**ID3D11Device:: креатеинпутлайаут**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) для создания объекта макета ввода.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-129">You can then pass this compiled vertex shader code to the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method to create the vertex shader object and to the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) method to create the input-layout object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the vertex shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(vertexShaderGraphInstance.Get(), "main", ("vs" + m_shaderModelSuffix).c_str(), 0, &vertexShaderBlob, 
                &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11VertexShader> vertexShader;
    DX::ThrowIfFailed(
        device->CreateVertexShader(
            vertexShaderBlob->GetBufferPointer(),
            vertexShaderBlob->GetBufferSize(),
            nullptr,
            &vertexShader
            )
        );
    context->VSSetShader(vertexShader.Get(), nullptr, 0);
    D3D11_INPUT_ELEMENT_DESC inputLayoutDesc[] =
    {
        { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0,  D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT,    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "NORMAL",   0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, D3D11_INPUT_PER_VERTEX_DATA, 0 }
    };
    ComPtr<ID3D11InputLayout> inputLayout;
    DX::ThrowIfFailed(device->CreateInputLayout(inputLayoutDesc, ARRAYSIZE(inputLayoutDesc), vertexShaderBlob->GetBufferPointer(), vertexShaderBlob->GetBufferSize(), &inputLayout));
    context->IASetInputLayout(inputLayout.Get());
```



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a><span data-ttu-id="fdcb5-130">3. Создание графа связывания функций для шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-130">3. Construct a function-linking-graph for the pixel shader.</span></span>

<span data-ttu-id="fdcb5-131">Вызовите функцию [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) , чтобы создать диаграмму Function-Linking ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) для представления шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-131">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the pixel shader.</span></span>

<span data-ttu-id="fdcb5-132">Используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) для определения входных параметров шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-132">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the pixel shader.</span></span> <span data-ttu-id="fdcb5-133">Этап шейдера вершин передает входные параметры в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-133">The vertex shader stage feeds the input parameters to the pixel shader.</span></span> <span data-ttu-id="fdcb5-134">Макет входных параметров шейдера пикселей соответствует макету шейдера пикселей в скомпилированном коде.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-134">The layout of the pixel shader’s input parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="fdcb5-135">После определения входных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетинпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) , чтобы определить входной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-135">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> pixelShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &pixelShaderGraph));

            // Define the main input node which will be fed by the vertex shader pipeline stage.
            static const D3D11_PARAMETER_DESC pixelShaderInputParameters[] =
            {
                {"inputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderInputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetInputSignature(pixelShaderInputParameters, ARRAYSIZE(pixelShaderInputParameters), 
                &pixelShaderInputNode), pixelShaderGraph.Get());
```



<span data-ttu-id="fdcb5-136">Вызовите метод [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) , чтобы создать узел для основной функции шейдера пикселей и вызвать [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из входного узла в узел для основной функции шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-136">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main pixel shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main pixel shader function.</span></span>


```C++
            // Create a node for the main ColorFunction call and connect it to the pixel shader inputs.
            ComPtr<ID3D11LinkingNode> colorValueNode;
            LinkingThrowIfFailed(pixelShaderGraph->CallFunction("", shaderLibrary.Get(), "ColorFunction", &colorValueNode), 
                pixelShaderGraph.Get());

            // Define the graph edges from the input node.
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 0, colorValueNode.Get(), 0), 
                pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 1, colorValueNode.Get(), 1), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="fdcb5-137">Используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) Structures, чтобы определить выходные параметры для шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-137">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the pixel shader.</span></span> <span data-ttu-id="fdcb5-138">Шейдер пикселей передает выходные параметры на [этап слияния вывода](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span><span class="sxs-lookup"><span data-stu-id="fdcb5-138">The pixel shader feeds its output parameters to the [Output-Merger Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span></span> <span data-ttu-id="fdcb5-139">После определения выходных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетаутпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) , чтобы определить выходной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера пикселей и выполнить вызовы [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из узла функции шейдера пикселей в выходной узел.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-139">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from a pixel shader function node to the output node.</span></span>


```C++
            // Define the main output node which will feed the Output Merger pipeline stage.
            D3D11_PARAMETER_DESC pixelShaderOutputParameters[] =
            {
                {"outputColor", "SV_TARGET", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderOutputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetOutputSignature(pixelShaderOutputParameters, ARRAYSIZE(pixelShaderOutputParameters), 
                &pixelShaderOutputNode), pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(fillAlphaCallNode.Get(), D3D_RETURN_PARAMETER_INDEX, pixelShaderOutputNode.Get(), 0), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="fdcb5-140">Вызовите метод [**ID3D11FunctionLinkingGraph:: креатемодулеинстанце**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) , чтобы завершить граф шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-140">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the pixel shader graph.</span></span>


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a><span data-ttu-id="fdcb5-141">4. Связывание шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="fdcb5-141">4. Link the pixel shader</span></span>

<span data-ttu-id="fdcb5-142">Вызовите функцию [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) , чтобы создать компоновщик ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)), который можно использовать для связи экземпляра библиотеки шейдеров, созданной при [упаковке библиотеки шейдеров](pachaging-a-shader-library.md) , с экземпляром графа построителя текстуры, созданного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-142">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the pixel shader graph that you created in the preceding step.</span></span> <span data-ttu-id="fdcb5-143">Вызовите метод [**ID3D11Linker:: уселибрари**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) , чтобы указать библиотеку шейдеров, используемую для компоновки.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-143">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="fdcb5-144">Вызовите метод [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) , чтобы связать библиотеку шейдеров с графом шейдера пикселей и создать указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к скомпилированному коду шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-144">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the pixel shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled pixel shader code.</span></span> <span data-ttu-id="fdcb5-145">Затем можно передать этот скомпилированный код построителя текстуры в метод [**ID3D11Device:: креатепикселшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) , чтобы создать объект шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-145">You can then pass this compiled pixel shader code to the [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) method to create the pixel shader object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the pixel shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(pixelShaderGraphInstance.Get(), "main", ("ps" + m_shaderModelSuffix).c_str(), 0, &pixelShaderBlob, &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11PixelShader> pixelShader;
    DX::ThrowIfFailed(
        device->CreatePixelShader(
            pixelShaderBlob->GetBufferPointer(),
            pixelShaderBlob->GetBufferSize(),
            nullptr,
            &pixelShader
            )
        );
    context->PSSetShader(pixelShader.Get(), nullptr, 0);
```



## <a name="summary"></a><span data-ttu-id="fdcb5-146">Итоги</span><span class="sxs-lookup"><span data-stu-id="fdcb5-146">Summary</span></span>

<span data-ttu-id="fdcb5-147">Мы использовали методы [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) для создания графиков шейдеров вершин и текстур, а также для задания структуры шейдера программным способом.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-147">We used the [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) methods to construct the vertex and pixel shader graphs and to specify the shader structure programmatically.</span></span>

<span data-ttu-id="fdcb5-148">Эти конструкции графа состоят из последовательностей вызовов предварительно скомпилированных функций, которые передают значения друг другу.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-148">These graph constructions consist of sequences of precompiled function calls that pass values to each other.</span></span> <span data-ttu-id="fdcb5-149">Узлы ФЛГ ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) представляют узлы шейдера входных и выходных данных и вызовы функций предкомпилированных библиотек.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-149">FLG nodes ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) represent input and output shader nodes and invocations of precompiled library functions.</span></span> <span data-ttu-id="fdcb5-150">Порядок, в котором регистрируются узлы вызова функции, определяет последовательность вызовов.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-150">The order in which you register the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="fdcb5-151">Сначала необходимо указать входной узел ([**ID3D11FunctionLinkingGraph:: сетинпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) и выходной узел Last ([**ID3D11FunctionLinkingGraph:: сетаутпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span><span class="sxs-lookup"><span data-stu-id="fdcb5-151">You must specify the input node ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first and the output node last ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span></span> <span data-ttu-id="fdcb5-152">ФЛГ края определяют, как передаются значения из одного узла в другой.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-152">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="fdcb5-153">Типы данных передаваемых значений должны быть одинаковыми. неявное преобразование типа отсутствует.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-153">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="fdcb5-154">Правила Shape и группирующие соответствуют поведению HLSL.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-154">Shape and swizzling rules follow the HLSL behavior.</span></span> <span data-ttu-id="fdcb5-155">В этой последовательности значения могут передаваться только вперед.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-155">Values can only be passed forward in this sequence.</span></span>

<span data-ttu-id="fdcb5-156">Мы также использовали [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) методы для связывания библиотеки шейдеров с графами шейдеров и создания больших двоичных объектов шейдера для использования в среде выполнения Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-156">We also used [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) methods to link the shader library with the shader graphs and to produce shader blobs for the Direct3D runtime to use.</span></span>

<span data-ttu-id="fdcb5-157">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="fdcb5-157">Congratulations!</span></span> <span data-ttu-id="fdcb5-158">Теперь вы можете использовать связывание шейдеров в своих приложениях.</span><span class="sxs-lookup"><span data-stu-id="fdcb5-158">You are now ready to use shader linking in your own apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdcb5-159">См. также</span><span class="sxs-lookup"><span data-stu-id="fdcb5-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdcb5-160">Использование связывания шейдера</span><span class="sxs-lookup"><span data-stu-id="fdcb5-160">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 