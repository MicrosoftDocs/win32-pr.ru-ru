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
# <a name="how-to-create-a-constant-buffer"></a><span data-ttu-id="128f2-104">Как создать буфер константы</span><span class="sxs-lookup"><span data-stu-id="128f2-104">How to: Create a Constant Buffer</span></span>

<span data-ttu-id="128f2-105">[Буферы констант](overviews-direct3d-11-resources-buffers-intro.md) содержат константные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="128f2-105">[Constant buffers](overviews-direct3d-11-resources-buffers-intro.md) contain shader constant data.</span></span> <span data-ttu-id="128f2-106">В этом разделе показано, как инициализировать [Константный буфер](overviews-direct3d-11-resources-buffers-intro.md) при подготовке к подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="128f2-106">This topic shows how to initialize a [constant buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="128f2-107">**Инициализация буфера констант**</span><span class="sxs-lookup"><span data-stu-id="128f2-107">**To initialize a constant buffer**</span></span>

1.  <span data-ttu-id="128f2-108">Определите структуру, описывающую постоянные данные шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="128f2-108">Define a structure that describes the vertex shader constant data.</span></span>
2.  <span data-ttu-id="128f2-109">Выделите память для структуры, определенной на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="128f2-109">Allocate memory for the structure that you defined in step one.</span></span> <span data-ttu-id="128f2-110">Заполните этот буфер с постоянными данными шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="128f2-110">Fill this buffer with vertex shader constant data.</span></span> <span data-ttu-id="128f2-111">Можно использовать функцию **malloc** или **New** для выделения памяти, или можно выделить память для структуры из стека.</span><span class="sxs-lookup"><span data-stu-id="128f2-111">You can use **malloc** or **new** to allocate the memory, or you can allocate memory for the structure from the stack.</span></span>
3.  <span data-ttu-id="128f2-112">Создайте описание буфера, заполнив структуру [**D3D11 \_ буфера \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="128f2-112">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="128f2-113">Передайте \_ флаг D3D11 привязки \_ константного \_ буфера в элемент **биндфлагс** и передайте размер структуры описания буфера констант в байтах в элемент **битевидс** .</span><span class="sxs-lookup"><span data-stu-id="128f2-113">Pass the D3D11\_BIND\_CONSTANT\_BUFFER flag to the **BindFlags** member and pass the size of the constant buffer description structure in bytes to the **ByteWidth** member.</span></span>

    > [!Note]  
    > <span data-ttu-id="128f2-114">\_ \_ Флаг буфера константы привязки D3D11 \_ не может сочетаться с другими флагами.</span><span class="sxs-lookup"><span data-stu-id="128f2-114">The D3D11\_BIND\_CONSTANT\_BUFFER flag cannot be combined with any other flags.</span></span>

     

4.  <span data-ttu-id="128f2-115">Создайте описание данных о подресурсе, заполнив [**структуру \_ \_ данных подресурсов D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="128f2-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="128f2-116">Элемент **псисмем** структуры **\_ \_ данных подресурса D3D11** должен указывать непосредственно на постоянные данные шейдера вершин, созданные на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="128f2-116">The **pSysMem** member of the **D3D11\_SUBRESOURCE\_DATA** structure must point directly to the vertex shader constant data that you created in step two.</span></span>
5.  <span data-ttu-id="128f2-117">Вызовите метод [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) при передаче структуры [**\_ буфера \_ DESC D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , [**структуры \_ \_ данных подресурса D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) и адреса указателя на интерфейс [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) для инициализации.</span><span class="sxs-lookup"><span data-stu-id="128f2-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="128f2-118">В этих примерах кода показано, как создать буфер констант.</span><span class="sxs-lookup"><span data-stu-id="128f2-118">These code examples demonstrate how to create a constant buffer.</span></span>

<span data-ttu-id="128f2-119">В этом примере предполагается, что **g \_ pd3dDevice** является допустимым объектом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , а **g \_ pd3dContext** — допустимым объектом [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="128f2-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that **g\_pd3dContext** is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


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



<span data-ttu-id="128f2-120">В этом примере показано связанное определение HLSL кбуффер.</span><span class="sxs-lookup"><span data-stu-id="128f2-120">This example shows the associated HLSL cbuffer definition.</span></span>

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
> <span data-ttu-id="128f2-121">Не забудьте сопоставить \_ \_ Макет памяти буфера VS с разметкой HLSL в C++.</span><span class="sxs-lookup"><span data-stu-id="128f2-121">Make sure to match the VS\_CONSTANT\_BUFFER memory layout in C++ with the HLSL layout.</span></span> <span data-ttu-id="128f2-122">Сведения о том, как HLSL обрабатывает макет в памяти, см. в разделе [правила упаковки для константных переменных](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="128f2-122">For info about how HLSL handles layout in memory, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="128f2-123">См. также</span><span class="sxs-lookup"><span data-stu-id="128f2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="128f2-124">Buffers</span><span class="sxs-lookup"><span data-stu-id="128f2-124">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="128f2-125">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="128f2-125">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 