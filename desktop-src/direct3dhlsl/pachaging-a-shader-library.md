---
title: Упаковка библиотеки шейдеров
description: Здесь мы покажем, как скомпилировать код шейдера, загрузить скомпилированный код в библиотеку шейдеров и привязать ресурсы из исходных слотов к конечным слотам.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb0f16d226357aca63259a9cc014a3c149d84b87d1b9340b1452b802e0df410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906442"
---
# <a name="packaging-a-shader-library"></a>Упаковка библиотеки шейдеров

Здесь мы покажем, как скомпилировать код шейдера, загрузить скомпилированный код в библиотеку шейдеров и привязать ресурсы из исходных слотов к конечным слотам.

**Цель:** Упаковка библиотеки шейдеров для использования при связывании с шейдером.

## <a name="prerequisites"></a>Необходимые компоненты

Предполагается, что вы знакомы с C++. Также вы должны быть знакомы с основными принципами программирования графики.

**Время на выполнение:** 30 минут.

## <a name="instructions"></a>Инструкции

### <a name="1-compiling-your-shader-code"></a>1. Компиляция кода шейдера

Скомпилируйте код шейдера с помощью одной из функций компиляции. Например, в этом фрагменте кода используется [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).

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

Исходная строка содержит некомпилированный код ASCII HLSL.

### <a name="2-load-the-compiled-code-into-a-shader-library"></a>2. Загрузите скомпилированный код в библиотеку шейдера.

Вызовите функцию [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) , чтобы загрузить скомпилированный код ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) в модуль ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)), представляющий библиотеку шейдеров.


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a>3. привяжите ресурсы из исходных слотов к конечным слотам.

Вызовите метод [**ID3D11Module:: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) , чтобы создать экземпляр ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) библиотеки, чтобы затем можно было определить привязки ресурсов для экземпляра.

Вызовите методы BIND класса [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) , чтобы привязать необходимые ресурсы из исходных слотов к конечным слотам. Ресурсами могут быть текстуры, буферы, пробы, буферы констант или Уавс. Как правило, будут использоваться те же слоты, что и в исходной библиотеке.


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



Этот код HLSL показывает, что исходная библиотека использует те же слоты (T0, S0, B0, B1 и B2), что и слоты, используемые в предыдущих методах привязки [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).

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

## <a name="summary-and-next-steps"></a>Сводка и дальнейшие действия

Мы скомпилированы код шейдера, загрузили скомпилированный код в библиотеку шейдеров и привязанные ресурсы из исходных слотов в конечные слоты.

Далее мы создаем функции-Links-Graphs (Флгс) для шейдеров, связываем их с скомпилированным кодом и создаем большие двоичные объекты шейдера, которые может использовать среда выполнения Direct3D.

[Создание графа связывания функций и связывание его с скомпилированным кодом](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование связывания шейдера](using-shader-linking.md)
</dt> </dl>

 

 