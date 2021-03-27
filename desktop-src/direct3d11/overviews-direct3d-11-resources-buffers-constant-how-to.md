---
title: Создание буфера констант
description: В этом разделе показано, как инициализировать константный буфер при подготовке к подготовке к просмотру.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- буфер констант, создание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793321"
---
# <a name="how-to-create-a-constant-buffer"></a>Как создать буфер константы

[Буферы констант](overviews-direct3d-11-resources-buffers-intro.md) содержат константные данные шейдера. В этом разделе показано, как инициализировать [Константный буфер](overviews-direct3d-11-resources-buffers-intro.md) при подготовке к подготовке к просмотру.

**Инициализация буфера констант**

1.  Определите структуру, описывающую постоянные данные шейдера вершин.
2.  Выделите память для структуры, определенной на шаге 1. Заполните этот буфер с постоянными данными шейдера вершин. Можно использовать функцию **malloc** или **New** для выделения памяти, или можно выделить память для структуры из стека.
3.  Создайте описание буфера, заполнив структуру [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Передайте \_ флаг D3D11 привязки \_ константного \_ буфера в элемент **биндфлагс** и передайте размер структуры описания буфера констант в байтах в элемент **битевидс** .

    > [!Note]  
    > \_ \_ Флаг буфера константы привязки D3D11 \_ не может сочетаться с другими флагами.

     

4.  Создайте описание данных о подресурсе, заполнив [**структуру \_ \_ данных подресурсов D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . Элемент **псисмем** структуры **\_ \_ данных подресурса D3D11** должен указывать непосредственно на постоянные данные шейдера вершин, созданные на шаге 2.
5.  Вызовите метод [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) при передаче структуры [**\_ буфера \_ DESC D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , [**структуры \_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) и адреса указателя на интерфейс [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) для инициализации.

В этих примерах кода показано, как создать буфер констант.

В этом примере предполагается, что **g \_ pd3dDevice** является допустимым объектом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , а **g \_ pd3dContext** — допустимым объектом [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



В этом примере показано связанное определение HLSL кбуффер.

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> Не забудьте сопоставить \_ \_ Макет памяти буфера VS с разметкой HLSL в C++. Сведения о том, как HLSL обрабатывает макет в памяти, см. в разделе [правила упаковки для константных переменных](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Buffers](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 