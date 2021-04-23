---
title: texreg2ar-PS
description: Интерпретирует компоненты альфа-и красного цвета исходной регистрации как данные адреса текстуры (u, v) для выборки текстуры на этапе, соответствующей номеру регистра назначения. Результат сохраняется в реестре назначения.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487889"
---
# <a name="texreg2ar---ps"></a><span data-ttu-id="76cf0-104">texreg2ar-PS</span><span class="sxs-lookup"><span data-stu-id="76cf0-104">texreg2ar - ps</span></span>

<span data-ttu-id="76cf0-105">Интерпретирует компоненты альфа-и красного цвета исходной регистрации как данные адреса текстуры (u, v) для выборки текстуры на этапе, соответствующей номеру регистра назначения.</span><span class="sxs-lookup"><span data-stu-id="76cf0-105">Interprets the alpha and red color components of the source register as texture address data (u,v) to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="76cf0-106">Результат сохраняется в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="76cf0-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="76cf0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76cf0-107">Syntax</span></span>



| <span data-ttu-id="76cf0-108">texreg2ar DST, src</span><span class="sxs-lookup"><span data-stu-id="76cf0-108">texreg2ar dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="76cf0-109">где</span><span class="sxs-lookup"><span data-stu-id="76cf0-109">where</span></span>

-   <span data-ttu-id="76cf0-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="76cf0-110">dst is the destination register.</span></span>
-   <span data-ttu-id="76cf0-111">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="76cf0-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="76cf0-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="76cf0-112">Remarks</span></span>



| <span data-ttu-id="76cf0-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="76cf0-113">Pixel shader versions</span></span> | <span data-ttu-id="76cf0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="76cf0-114">1\_1</span></span> | <span data-ttu-id="76cf0-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="76cf0-115">1\_2</span></span> | <span data-ttu-id="76cf0-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="76cf0-116">1\_3</span></span> | <span data-ttu-id="76cf0-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="76cf0-117">1\_4</span></span> | <span data-ttu-id="76cf0-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76cf0-118">2\_0</span></span> | <span data-ttu-id="76cf0-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="76cf0-119">2\_x</span></span> | <span data-ttu-id="76cf0-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76cf0-120">2\_sw</span></span> | <span data-ttu-id="76cf0-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76cf0-121">3\_0</span></span> | <span data-ttu-id="76cf0-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="76cf0-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="76cf0-123">texreg2ar</span><span class="sxs-lookup"><span data-stu-id="76cf0-123">texreg2ar</span></span>             | <span data-ttu-id="76cf0-124">x</span><span class="sxs-lookup"><span data-stu-id="76cf0-124">x</span></span>    | <span data-ttu-id="76cf0-125">x</span><span class="sxs-lookup"><span data-stu-id="76cf0-125">x</span></span>    | <span data-ttu-id="76cf0-126">x</span><span class="sxs-lookup"><span data-stu-id="76cf0-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="76cf0-127">Эта инструкция полезна для операций повторного сопоставления цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="76cf0-127">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="76cf0-128">Ниже приведен пример последовательности, в которой приведена инструкция:</span><span class="sxs-lookup"><span data-stu-id="76cf0-128">Here is an example of the sequence the instruction follows:</span></span>

<dl> <span data-ttu-id="76cf0-129">Да t (n)</span><span class="sxs-lookup"><span data-stu-id="76cf0-129">tex t(n)</span></span>  
<span data-ttu-id="76cf0-130">texreg2ar t (m), t (n), где m > n</span><span class="sxs-lookup"><span data-stu-id="76cf0-130">texreg2ar t(m), t(n) where m > n</span></span>  
<span data-ttu-id="76cf0-131">Первая инструкция загружает цвет текстуры (RGBA)</span><span class="sxs-lookup"><span data-stu-id="76cf0-131">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="76cf0-132">регистрация тн</span><span class="sxs-lookup"><span data-stu-id="76cf0-132">// into register tn</span></span>  
<span data-ttu-id="76cf0-133">Да тн</span><span class="sxs-lookup"><span data-stu-id="76cf0-133">tex tn</span></span>  
<span data-ttu-id="76cf0-134">Вторая инструкция повторно сопоставляет цвет.</span><span class="sxs-lookup"><span data-stu-id="76cf0-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="76cf0-135">t (m)<sub>RGBA</sub> = текстуресампле (этап m)<sub>RGBA</sub> с использованием t (n)<sub>AR</sub> в качестве координат</span><span class="sxs-lookup"><span data-stu-id="76cf0-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="76cf0-136">\_bx2 нельзя использовать для инструкций src Register для texreg2ar или [texreg2gb-PS](texreg2gb---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="76cf0-136">\_bx2 cannot be used on the src register for texreg2ar or [texreg2gb - ps](texreg2gb---ps.md) instructions.</span></span>

<span data-ttu-id="76cf0-137">Для этой инструкции исходный регистр должен использовать неподписанные данные.</span><span class="sxs-lookup"><span data-stu-id="76cf0-137">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="76cf0-138">Использование подписанных или смешанных данных в исходном регистре приведет к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="76cf0-138">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="76cf0-139">Дополнительные сведения см. в разделе [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="76cf0-139">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76cf0-140">См. также</span><span class="sxs-lookup"><span data-stu-id="76cf0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76cf0-141">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="76cf0-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 