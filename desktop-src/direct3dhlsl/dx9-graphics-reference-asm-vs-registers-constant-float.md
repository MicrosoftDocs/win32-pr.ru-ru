---
title: Регистр постоянного float (Справочник по HLSL VS)
description: Входной регистр шейдера вершин для четырех компонентов с плавающей запятой. Установите регистр константы с помощью DEF-VS или Сетвертексшадерконстантф.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413111"
---
# <a name="constant-float-register-hlsl-vs-reference"></a><span data-ttu-id="0323b-104">Регистр постоянного float (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="0323b-104">Constant float register (HLSL VS reference)</span></span>

<span data-ttu-id="0323b-105">Входной регистр шейдера вершин для четырех компонентов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0323b-105">Vertex shader input register for a four component floating-point constant.</span></span> <span data-ttu-id="0323b-106">Установите регистр константы с помощью [DEF-VS](def---vs.md) или [**сетвертексшадерконстантф**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="0323b-106">Set a constant register with either [def - vs](def---vs.md) or [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span></span>

<span data-ttu-id="0323b-107">Файл регистра константы доступен только для чтения с точки шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="0323b-107">The constant register file is read-only from the perspective of the vertex shader.</span></span> <span data-ttu-id="0323b-108">Любая одна инструкция может обращаться только к одному регистру констант.</span><span class="sxs-lookup"><span data-stu-id="0323b-108">Any single instruction may access only one constant register.</span></span> <span data-ttu-id="0323b-109">Однако каждый источник в этой инструкции может независимо свиззле и инвертировать этот вектор по мере считывания.</span><span class="sxs-lookup"><span data-stu-id="0323b-109">However, each source in that instruction may independently swizzle and negate that vector as it is read.</span></span>

<span data-ttu-id="0323b-110">Поведение констант шейдера изменилось между Direct3D 8 и Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0323b-110">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="0323b-111">Для Direct3D 9 константы, заданные с помощью дефкс, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="0323b-111">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="0323b-112">Время существования константы, объявленной с помощью дефкс, ограничено выполнением только этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="0323b-112">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="0323b-113">И наоборот, константы, заданные с помощью API-интерфейсов, Сетксксксшадерконстанткс инициализировать константы в глобальном пространстве.</span><span class="sxs-lookup"><span data-stu-id="0323b-113">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="0323b-114">Константы в глобальном пространстве не копируются в локальное пространство (видимую шейдеру) до тех пор, пока не будет вызван Сетксксксшадерконстантс.</span><span class="sxs-lookup"><span data-stu-id="0323b-114">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="0323b-115">Для Direct3D 8 константы, заданные с помощью дефкс или API, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="0323b-115">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="0323b-116">При каждом выполнении шейдера все константы используются текущим шейдером независимо от метода, используемого для их установки.</span><span class="sxs-lookup"><span data-stu-id="0323b-116">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

<span data-ttu-id="0323b-117">Регистр константы обозначается как абсолютный или относительный:</span><span class="sxs-lookup"><span data-stu-id="0323b-117">A constant register is designated as either absolute or relative:</span></span>


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



<span data-ttu-id="0323b-118">Регистр констант может быть считан, поэтому либо с помощью абсолютного индекса, либо с относительным индексом от регистра адресов.</span><span class="sxs-lookup"><span data-stu-id="0323b-118">The constant register can be read, therefore, either by using an absolute index or with a relative index from an address register.</span></span> <span data-ttu-id="0323b-119">Операции чтения из недопустимых регистров возвращают (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="0323b-119">Reads from out-of-range registers return (0.0, 0.0, 0.0, 0.0).</span></span>

## <a name="examples"></a><span data-ttu-id="0323b-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="0323b-120">Examples</span></span>

<span data-ttu-id="0323b-121">Ниже приведен пример объявления двух констант с плавающей запятой в шейдере.</span><span class="sxs-lookup"><span data-stu-id="0323b-121">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="0323b-122">Эти константы загружаются каждый раз при вызове [**сетвертексшадер**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="0323b-122">These constants are loaded every time [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) is called.</span></span>

<span data-ttu-id="0323b-123">Ниже приведен пример использования API.</span><span class="sxs-lookup"><span data-stu-id="0323b-123">Here is an example using the API.</span></span>


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



<span data-ttu-id="0323b-124">Если вы устанавливаете постоянные значения с помощью API, то объявление шейдера не требуется.</span><span class="sxs-lookup"><span data-stu-id="0323b-124">If you are setting constant values with the API, there is no shader declaration required.</span></span>



| <span data-ttu-id="0323b-125">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="0323b-125">Vertex shader versions</span></span> | <span data-ttu-id="0323b-126">1\_1</span><span class="sxs-lookup"><span data-stu-id="0323b-126">1\_1</span></span> | <span data-ttu-id="0323b-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0323b-127">2\_0</span></span> | <span data-ttu-id="0323b-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0323b-128">2\_sw</span></span> | <span data-ttu-id="0323b-129">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0323b-129">2\_x</span></span> | <span data-ttu-id="0323b-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0323b-130">3\_0</span></span> | <span data-ttu-id="0323b-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0323b-131">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="0323b-132">Регистр констант</span><span class="sxs-lookup"><span data-stu-id="0323b-132">Constant Register</span></span>      | <span data-ttu-id="0323b-133">x</span><span class="sxs-lookup"><span data-stu-id="0323b-133">x</span></span>    | <span data-ttu-id="0323b-134">x</span><span class="sxs-lookup"><span data-stu-id="0323b-134">x</span></span>    | <span data-ttu-id="0323b-135">x</span><span class="sxs-lookup"><span data-stu-id="0323b-135">x</span></span>     | <span data-ttu-id="0323b-136">x</span><span class="sxs-lookup"><span data-stu-id="0323b-136">x</span></span>    | <span data-ttu-id="0323b-137">x</span><span class="sxs-lookup"><span data-stu-id="0323b-137">x</span></span>    | <span data-ttu-id="0323b-138">x</span><span class="sxs-lookup"><span data-stu-id="0323b-138">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="0323b-139">См. также</span><span class="sxs-lookup"><span data-stu-id="0323b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0323b-140">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="0323b-140">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 