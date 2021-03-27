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
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a>Создание графа связывания функций и связывание его с скомпилированным кодом

В этой статье мы покажем, как создавать графы связывания функций (Флгс) для шейдеров и как связать эти шейдеры с библиотекой шейдеров для создания больших двоичных объектов шейдера, которые может использовать среда выполнения Direct3D.

**Цель:** Для создания графа связывания функций и связывания его с скомпилированным кодом.

## <a name="prerequisites"></a>Предварительные условия

Предполагается, что вы знакомы с C++. Также вы должны быть знакомы с основными принципами программирования графики.

Также предполагается, что вы выполнили [упаковку библиотеки шейдеров](pachaging-a-shader-library.md).

**Время на выполнение:** 30 минут.

## <a name="instructions"></a>Инструкции

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a>1. создайте граф связывания функций для шейдера вершин.

Вызовите функцию [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) , чтобы создать диаграмму Function-Linking ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) для представления шейдера вершин.

Чтобы определить входные параметры для шейдера вершин, используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) Structures. [Этап входного ассемблера](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) передает входные параметры в шейдер вершин. Макет входных параметров шейдера вершин соответствует макету шейдера вершин в скомпилированном коде. После определения входных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетинпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) , чтобы определить входной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера вершин.


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



Вызовите метод [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) , чтобы создать узел для основной функции шейдера вершин и вызвать [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из входного узла в узел для основной функции шейдера вершин.


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



Используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) Structures, чтобы определить выходные параметры для шейдера вершин. Шейдер вершин передает выходные параметры в шейдер пикселей. Макет выходных параметров шейдера вершин соответствует макету шейдера пикселей в скомпилированном коде. После определения выходных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетаутпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) , чтобы определить выходной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера вершин.


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



Выполните вызовы [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из узла для основной функции шейдера вершин в выходной узел.


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



Вызовите метод [**ID3D11FunctionLinkingGraph:: креатемодулеинстанце**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) , чтобы завершить граф шейдера вершин.


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a>2. Связывание шейдера вершин

Вызовите функцию [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) , чтобы создать компоновщик ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)), который можно использовать для связывания экземпляра библиотеки шейдеров, созданной в [упаковке библиотеки шейдеров](pachaging-a-shader-library.md) , с экземпляром графа вершинного шейдера, созданного на предыдущем шаге. Вызовите метод [**ID3D11Linker:: уселибрари**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) , чтобы указать библиотеку шейдеров, используемую для компоновки. Вызовите метод [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) , чтобы связать библиотеку шейдеров с графом шейдера вершин и создать указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к скомпилированному коду шейдера вершин. Затем можно передать этот скомпилированный код шейдера вершин в метод [**ID3D11Device:: креатевертексшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) , чтобы создать объект шейдера вершин и метод [**ID3D11Device:: креатеинпутлайаут**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) для создания объекта макета ввода.


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



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a>3. Создание графа связывания функций для шейдера пикселей.

Вызовите функцию [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) , чтобы создать диаграмму Function-Linking ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) для представления шейдера пикселей.

Используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) для определения входных параметров шейдера пикселей. Этап шейдера вершин передает входные параметры в шейдер пикселей. Макет входных параметров шейдера пикселей соответствует макету шейдера пикселей в скомпилированном коде. После определения входных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетинпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) , чтобы определить входной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера пикселей.


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



Вызовите метод [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) , чтобы создать узел для основной функции шейдера пикселей и вызвать [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из входного узла в узел для основной функции шейдера пикселей.


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



Используйте массив [**D3D11 \_ параметра \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) Structures, чтобы определить выходные параметры для шейдера пикселей. Шейдер пикселей передает выходные параметры на [этап слияния вывода](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage). После определения выходных параметров вызовите метод [**ID3D11FunctionLinkingGraph:: сетаутпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) , чтобы определить выходной узел ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) для шейдера пикселей и выполнить вызовы [**ID3D11FunctionLinkingGraph::P ассвалуе**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) , чтобы передать значения из узла функции шейдера пикселей в выходной узел.


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



Вызовите метод [**ID3D11FunctionLinkingGraph:: креатемодулеинстанце**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) , чтобы завершить граф шейдера пикселей.


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a>4. Связывание шейдера пикселей

Вызовите функцию [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) , чтобы создать компоновщик ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)), который можно использовать для связи экземпляра библиотеки шейдеров, созданной при [упаковке библиотеки шейдеров](pachaging-a-shader-library.md) , с экземпляром графа построителя текстуры, созданного на предыдущем шаге. Вызовите метод [**ID3D11Linker:: уселибрари**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) , чтобы указать библиотеку шейдеров, используемую для компоновки. Вызовите метод [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) , чтобы связать библиотеку шейдеров с графом шейдера пикселей и создать указатель на интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) , который можно использовать для доступа к скомпилированному коду шейдера пикселей. Затем можно передать этот скомпилированный код построителя текстуры в метод [**ID3D11Device:: креатепикселшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) , чтобы создать объект шейдера пикселей.


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



## <a name="summary"></a>Итоги

Мы использовали методы [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) для создания графиков шейдеров вершин и текстур, а также для задания структуры шейдера программным способом.

Эти конструкции графа состоят из последовательностей вызовов предварительно скомпилированных функций, которые передают значения друг другу. Узлы ФЛГ ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) представляют узлы шейдера входных и выходных данных и вызовы функций предкомпилированных библиотек. Порядок, в котором регистрируются узлы вызова функции, определяет последовательность вызовов. Сначала необходимо указать входной узел ([**ID3D11FunctionLinkingGraph:: сетинпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) и выходной узел Last ([**ID3D11FunctionLinkingGraph:: сетаутпутсигнатуре**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)). ФЛГ края определяют, как передаются значения из одного узла в другой. Типы данных передаваемых значений должны быть одинаковыми. неявное преобразование типа отсутствует. Правила Shape и группирующие соответствуют поведению HLSL. В этой последовательности значения могут передаваться только вперед.

Мы также использовали [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) методы для связывания библиотеки шейдеров с графами шейдеров и создания больших двоичных объектов шейдера для использования в среде выполнения Direct3D.

Поздравляем! Теперь вы можете использовать связывание шейдеров в своих приложениях.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование связывания шейдера](using-shader-linking.md)
</dt> </dl>

 

 