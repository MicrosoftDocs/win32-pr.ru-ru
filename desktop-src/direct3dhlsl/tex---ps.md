---
title: Да-PS
description: Загружает регистр назначения с использованием данных цвета (RGBA) из текстуры. Текстура должна быть привязана к определенной стадии текстуры (n) с помощью Сеттекстуре. Выбор текстуры управляется Сетсамплерстате.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987665"
---
# <a name="tex---ps"></a><span data-ttu-id="b3b88-105">Да-PS</span><span class="sxs-lookup"><span data-stu-id="b3b88-105">tex - ps</span></span>

<span data-ttu-id="b3b88-106">Загружает регистр назначения с использованием данных цвета (RGBA) из текстуры.</span><span class="sxs-lookup"><span data-stu-id="b3b88-106">Loads the destination register with color data (RGBA) sampled from a texture.</span></span> <span data-ttu-id="b3b88-107">Текстура должна быть привязана к определенной стадии текстуры (n) с помощью [**сеттекстуре**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="b3b88-107">The texture must be bound to a particular texture stage (n) using [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="b3b88-108">Выбор текстуры управляется [**сетсамплерстате**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="b3b88-108">Texture sampling is controlled by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b88-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3b88-109">Syntax</span></span>



| <span data-ttu-id="b3b88-110">Да DST</span><span class="sxs-lookup"><span data-stu-id="b3b88-110">tex dst</span></span> |
|---------|



 

<span data-ttu-id="b3b88-111">где</span><span class="sxs-lookup"><span data-stu-id="b3b88-111">where</span></span>

-   <span data-ttu-id="b3b88-112">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="b3b88-112">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b88-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3b88-113">Remarks</span></span>



| <span data-ttu-id="b3b88-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="b3b88-114">Pixel shader versions</span></span> | <span data-ttu-id="b3b88-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="b3b88-115">1\_1</span></span> | <span data-ttu-id="b3b88-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="b3b88-116">1\_2</span></span> | <span data-ttu-id="b3b88-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b3b88-117">1\_3</span></span> | <span data-ttu-id="b3b88-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="b3b88-118">1\_4</span></span> | <span data-ttu-id="b3b88-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3b88-119">2\_0</span></span> | <span data-ttu-id="b3b88-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b3b88-120">2\_x</span></span> | <span data-ttu-id="b3b88-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3b88-121">2\_sw</span></span> | <span data-ttu-id="b3b88-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3b88-122">3\_0</span></span> | <span data-ttu-id="b3b88-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3b88-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b3b88-124">Да</span><span class="sxs-lookup"><span data-stu-id="b3b88-124">tex</span></span>                   | <span data-ttu-id="b3b88-125">x</span><span class="sxs-lookup"><span data-stu-id="b3b88-125">x</span></span>    | <span data-ttu-id="b3b88-126">x</span><span class="sxs-lookup"><span data-stu-id="b3b88-126">x</span></span>    | <span data-ttu-id="b3b88-127">x</span><span class="sxs-lookup"><span data-stu-id="b3b88-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="b3b88-128">Номер целевой регистрации указывает номер стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="b3b88-128">The destination register number specifies the texture stage number.</span></span>

<span data-ttu-id="b3b88-129">Выборка текстур использует координаты текстуры для поиска или выборки значений цвета в заданных координатах (u, v, w, q), принимая во внимание атрибуты состояния стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="b3b88-129">Texture sampling uses texture coordinates to look up, or sample, a color value at the specified (u,v,w,q) coordinates while taking into account the texture stage state attributes.</span></span>

<span data-ttu-id="b3b88-130">Данные координат текстуры интерполируются на основе данных координат текстурной текстуры и связаны с определенной стадией текстуры.</span><span class="sxs-lookup"><span data-stu-id="b3b88-130">The texture coordinate data is interpolated from the vertex texture coordinate data and is associated with a specific texture stage.</span></span> <span data-ttu-id="b3b88-131">Ассоциация по умолчанию является сопоставлением "один к одному" между номером стадии текстуры и порядком объявления координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="b3b88-131">The default association is a one-to-one mapping between texture stage number and texture coordinate declaration order.</span></span> <span data-ttu-id="b3b88-132">Это означает, что первый набор координат текстуры, определенный в формате вершины, по умолчанию связан с этапом текстуры 0.</span><span class="sxs-lookup"><span data-stu-id="b3b88-132">This means that the first set of texture coordinates defined in the vertex format are by default associated with texture stage 0.</span></span>

<span data-ttu-id="b3b88-133">Координаты текстуры могут быть связаны с любым этапом с помощью двух методов.</span><span class="sxs-lookup"><span data-stu-id="b3b88-133">Texture coordinates may be associated with any stage using two techniques.</span></span> <span data-ttu-id="b3b88-134">При использовании шейдера вершин с фиксированной функцией или конвейера фиксированной функции флаг состояния стадии текстуры Тсс \_ текскурдиндекс можно использовать в [**сеттекстурестажестате**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) для связывания координат с стадией.</span><span class="sxs-lookup"><span data-stu-id="b3b88-134">When using a fixed function vertex shader or the fixed function pipeline, the texture stage state flag TSS\_TEXCOORDINDEX can be used in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) to associate coordinates to a stage.</span></span> <span data-ttu-id="b3b88-135">В противном случае координаты текстуры выводятся с помощью Отна вершин шейдера при использовании программируемого шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="b3b88-135">Otherwise, the texture coordinates are output by the vertex shader oTₙ registers when using a programmable vertex shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3b88-136">См. также</span><span class="sxs-lookup"><span data-stu-id="b3b88-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3b88-137">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="b3b88-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 