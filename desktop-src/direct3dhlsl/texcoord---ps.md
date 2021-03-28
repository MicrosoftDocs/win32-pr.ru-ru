---
title: текскурд-PS
description: Интерпретирует данные координаты текстуры (UVW1) как данные цвета (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792193"
---
# <a name="texcoord---ps"></a><span data-ttu-id="3d0a1-103">текскурд-PS</span><span class="sxs-lookup"><span data-stu-id="3d0a1-103">texcoord - ps</span></span>

<span data-ttu-id="3d0a1-104">Интерпретирует данные координаты текстуры (UVW1) как данные цвета (RGBA).</span><span class="sxs-lookup"><span data-stu-id="3d0a1-104">Interprets texture coordinate data (UVW1) as color data (RGBA).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d0a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d0a1-105">Syntax</span></span>



| <span data-ttu-id="3d0a1-106">текскурд DST</span><span class="sxs-lookup"><span data-stu-id="3d0a1-106">texcoord dst</span></span> |
|--------------|



 

<span data-ttu-id="3d0a1-107">где</span><span class="sxs-lookup"><span data-stu-id="3d0a1-107">where</span></span>

-   <span data-ttu-id="3d0a1-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d0a1-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d0a1-109">Remarks</span></span>



| <span data-ttu-id="3d0a1-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="3d0a1-110">Pixel shader versions</span></span> | <span data-ttu-id="3d0a1-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="3d0a1-111">1\_1</span></span> | <span data-ttu-id="3d0a1-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="3d0a1-112">1\_2</span></span> | <span data-ttu-id="3d0a1-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3d0a1-113">1\_3</span></span> | <span data-ttu-id="3d0a1-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="3d0a1-114">1\_4</span></span> | <span data-ttu-id="3d0a1-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d0a1-115">2\_0</span></span> | <span data-ttu-id="3d0a1-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3d0a1-116">2\_x</span></span> | <span data-ttu-id="3d0a1-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3d0a1-117">2\_sw</span></span> | <span data-ttu-id="3d0a1-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d0a1-118">3\_0</span></span> | <span data-ttu-id="3d0a1-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3d0a1-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3d0a1-120">текскурд</span><span class="sxs-lookup"><span data-stu-id="3d0a1-120">texcoord</span></span>              | <span data-ttu-id="3d0a1-121">x</span><span class="sxs-lookup"><span data-stu-id="3d0a1-121">x</span></span>    | <span data-ttu-id="3d0a1-122">x</span><span class="sxs-lookup"><span data-stu-id="3d0a1-122">x</span></span>    | <span data-ttu-id="3d0a1-123">x</span><span class="sxs-lookup"><span data-stu-id="3d0a1-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="3d0a1-124">Эта инструкция интерпретирует набор координат текстуры (UVW1), соответствующий номеру регистра назначения, как данные цвета (RGBA).</span><span class="sxs-lookup"><span data-stu-id="3d0a1-124">This instruction interprets the texture coordinate set (UVW1) corresponding to the destination register number as color data (RGBA).</span></span> <span data-ttu-id="3d0a1-125">Если набор координат текстуры содержит менее трех компонентов, отсутствующие компоненты имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-125">If the texture coordinate set contains fewer than three components, the missing components are set to 0.</span></span> <span data-ttu-id="3d0a1-126">Четвертый компонент всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-126">The fourth component is always set to 1.</span></span> <span data-ttu-id="3d0a1-127">Все значения отправляются между 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-127">All values are clamped between 0 and 1.</span></span>

<span data-ttu-id="3d0a1-128">Преимущество текскурд заключается в том, что он предоставляет способ передачи данных вершин с высокой точностью непосредственно в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-128">The advantage of texcoord is that it provides a way to pass vertex data interpolated at high precision directly into the pixel shader.</span></span> <span data-ttu-id="3d0a1-129">Однако если данные записываются в регистр назначения, то в зависимости от количества бит, используемых оборудованием для регистров, будет потеряна какая-либо точность.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-129">However, when the data is written into the destination register, some precision will be lost, depending on the number of bits used by the hardware for registers.</span></span>

<span data-ttu-id="3d0a1-130">Эта инструкция не демонстрирует выборку текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-130">No texture is sampled by this instruction.</span></span> <span data-ttu-id="3d0a1-131">Только координаты текстуры, заданные на этом этапе текстуры, являются релевантными.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-131">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="3d0a1-132">Любые данные текстуры (такие как положение, нормальное и светлое направление источника) могут быть сопоставлены шейдером вершин в координатах текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-132">Any texture data (such as position, normal, and light source direction) can be mapped by a vertex shader into a texture coordinate.</span></span> <span data-ttu-id="3d0a1-133">Для этого необходимо связать текстуру с регистром текстуры с помощью [**сеттекстуре**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) и указать, как выборка текстур выполняется с помощью [**сеттекстурестажестате**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="3d0a1-133">This is done by associating a texture with a texture register using [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) and by specifying how the texture sampling is done using [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span> <span data-ttu-id="3d0a1-134">Если используется фиксированный конвейер функции, обязательно укажите \_ флаг Тсс текскурдиндекс.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-134">If the fixed function pipeline is used, be sure to supply the TSS\_TEXCOORDINDEX flag.</span></span>

<span data-ttu-id="3d0a1-135">Эта инструкция используется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3d0a1-135">This instruction is used as follows:</span></span>


```
texcoord tn
```



<span data-ttu-id="3d0a1-136">[Регистр координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (тн) содержит четыре значения цвета (RGBA).</span><span class="sxs-lookup"><span data-stu-id="3d0a1-136">An [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contains four color values (RGBA).</span></span> <span data-ttu-id="3d0a1-137">Данные также можно рассматривать как векторные данные (ксизв).</span><span class="sxs-lookup"><span data-stu-id="3d0a1-137">The data can also be thought of as vector data (xyzw).</span></span> <span data-ttu-id="3d0a1-138">текскурд получит три из этих значений (XYZ) из набора координат текстуры x, а четвертый компонент (w) имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-138">texcoord will retrieve three of these values (xyz) from texture coordinate set x, and the fourth component (w) is set to 1.</span></span> <span data-ttu-id="3d0a1-139">Адрес текстуры копируется из набора координат текстуры n.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-139">The texture address is copied from the texture coordinate set n.</span></span> <span data-ttu-id="3d0a1-140">Результат находится в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-140">The result is clamped between 0 and 1.</span></span>

<span data-ttu-id="3d0a1-141">Данный пример служит только для демонстрационных целей.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-141">This example is for illustration only.</span></span> <span data-ttu-id="3d0a1-142">Код C, сопровождающий шейдер, не оптимизирован для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-142">The C code accompanying the shader has not been optimized for performance.</span></span>

<span data-ttu-id="3d0a1-143">Ниже приведен пример шейдера с использованием текскурд.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-143">Here is an example shader using texcoord.</span></span>


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



<span data-ttu-id="3d0a1-144">Отображаемые выходные данные шейдера пикселей показаны на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-144">The rendered output from the pixel shader is shown in the following illustration.</span></span> <span data-ttu-id="3d0a1-145">Значения координат (u, v, w, 1) сопоставляются с каналами (RGB).</span><span class="sxs-lookup"><span data-stu-id="3d0a1-145">The (u,v,w,1) coordinate values map to the (rgb) channels.</span></span> <span data-ttu-id="3d0a1-146">Для альфа-канала задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-146">The alpha channel is set to 1.</span></span> <span data-ttu-id="3d0a1-147">На углах иллюстрации координаты (0,0, 0, 0, 1) интерпретируется как черный; (1, 0, 0, 1) — красный; (0, 1, 0, 1) является зеленым; и (1, 1, 0, 1) содержит зеленый и красный цвета, выдавая желтый цвет.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-147">At the corners of the illustration, coordinate (0,0,0,1) is interpreted as black; (1,0,0,1) is red; (0,1,0,1) is green; and (1,1,0,1) contains green and red, producing yellow.</span></span>

![Иллюстрация отображаемых выходных данных примера шейдера пикселей](images/pstexcoord.jpg)

<span data-ttu-id="3d0a1-149">Для использования шейдера требуется дополнительный код, а пример сценария показан ниже.</span><span class="sxs-lookup"><span data-stu-id="3d0a1-149">Additional code is required to use this shader and an example scenario is shown below.</span></span>


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a><span data-ttu-id="3d0a1-150">См. также</span><span class="sxs-lookup"><span data-stu-id="3d0a1-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d0a1-151">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="3d0a1-151">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 