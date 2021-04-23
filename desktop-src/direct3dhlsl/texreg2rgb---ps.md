---
title: texreg2rgb-PS
description: Интерпретирует цветовые компоненты красного, зеленого и синего (RGB) исходного регистра как данные адреса текстуры для выборки текстуры на этапе, соответствующей номеру регистра назначения. Результат сохраняется в реестре назначения.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532879"
---
# <a name="texreg2rgb---ps"></a><span data-ttu-id="3c383-104">texreg2rgb-PS</span><span class="sxs-lookup"><span data-stu-id="3c383-104">texreg2rgb - ps</span></span>

<span data-ttu-id="3c383-105">Интерпретирует цветовые компоненты красного, зеленого и синего (RGB) исходного регистра как данные адреса текстуры для выборки текстуры на этапе, соответствующей номеру регистра назначения.</span><span class="sxs-lookup"><span data-stu-id="3c383-105">Interprets the red, green, and blue (RGB) color components of the source register as texture address data in order to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="3c383-106">Результат сохраняется в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="3c383-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c383-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c383-107">Syntax</span></span>



| <span data-ttu-id="3c383-108">texreg2rgb DST, src</span><span class="sxs-lookup"><span data-stu-id="3c383-108">texreg2rgb dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="3c383-109">где</span><span class="sxs-lookup"><span data-stu-id="3c383-109">where</span></span>

-   <span data-ttu-id="3c383-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="3c383-110">dst is the destination register.</span></span>
-   <span data-ttu-id="3c383-111">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="3c383-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c383-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c383-112">Remarks</span></span>



| <span data-ttu-id="3c383-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="3c383-113">Pixel shader versions</span></span> | <span data-ttu-id="3c383-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3c383-114">1\_1</span></span> | <span data-ttu-id="3c383-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="3c383-115">1\_2</span></span> | <span data-ttu-id="3c383-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3c383-116">1\_3</span></span> | <span data-ttu-id="3c383-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="3c383-117">1\_4</span></span> | <span data-ttu-id="3c383-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c383-118">2\_0</span></span> | <span data-ttu-id="3c383-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3c383-119">2\_x</span></span> | <span data-ttu-id="3c383-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c383-120">2\_sw</span></span> | <span data-ttu-id="3c383-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c383-121">3\_0</span></span> | <span data-ttu-id="3c383-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c383-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3c383-123">texreg2rgb</span><span class="sxs-lookup"><span data-stu-id="3c383-123">texreg2rgb</span></span>            |      | <span data-ttu-id="3c383-124">x</span><span class="sxs-lookup"><span data-stu-id="3c383-124">x</span></span>    | <span data-ttu-id="3c383-125">x</span><span class="sxs-lookup"><span data-stu-id="3c383-125">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="3c383-126">Эта инструкция полезна для операций повторного сопоставления цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="3c383-126">This instruction is useful for color-space remapping operations.</span></span> <span data-ttu-id="3c383-127">Он поддерживает двухмерные (двумерные) и трехмерные (трехмерные) координаты.</span><span class="sxs-lookup"><span data-stu-id="3c383-127">It supports two-dimensional (2D) and three-dimensional (3D) coordinates.</span></span> <span data-ttu-id="3c383-128">Его можно использовать так же, как [texreg2ar-PS](texreg2ar---ps.md) или [texreg2gb-PS](texreg2gb---ps.md) , для сопоставления 2D-данных.</span><span class="sxs-lookup"><span data-stu-id="3c383-128">It can be used just like the [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md) to remap 2D data.</span></span> <span data-ttu-id="3c383-129">Однако эта инструкция также поддерживает трехмерные данные, чтобы их можно было использовать с картами кубов и трехмерными текстурами объемов.</span><span class="sxs-lookup"><span data-stu-id="3c383-129">However, this instruction also supports 3D data so it can be used with cube maps and 3D volume textures.</span></span>

<span data-ttu-id="3c383-130">Ниже приведен пример последовательности, в которой приведена инструкция.</span><span class="sxs-lookup"><span data-stu-id="3c383-130">Here is an example of the sequence the instruction follows.</span></span>


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



<span data-ttu-id="3c383-131">Ниже приведены более подробные сведения о том, как выполняется повторное сопоставление.</span><span class="sxs-lookup"><span data-stu-id="3c383-131">Here is more detail about how the remapping is accomplished.</span></span>

<dl> <span data-ttu-id="3c383-132">Первая инструкция загружает цвет текстуры (RGBA) в регистр тн.</span><span class="sxs-lookup"><span data-stu-id="3c383-132">// The first instruction loads the texture color (RGBA) into register tn</span></span>  
<span data-ttu-id="3c383-133">Да тн</span><span class="sxs-lookup"><span data-stu-id="3c383-133">tex tn</span></span>  
<span data-ttu-id="3c383-134">Вторая инструкция повторно сопоставляет цвет.</span><span class="sxs-lookup"><span data-stu-id="3c383-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="3c383-135">t (m)<sub>RGBA</sub> = текстуресампле (этап m)<sub>RGBA</sub> с использованием t (n)<sub>RGB</sub> в качестве координат</span><span class="sxs-lookup"><span data-stu-id="3c383-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>RGB</sub> as coordinates</span></span>
</dl>

## <a name="related-topics"></a><span data-ttu-id="3c383-136">См. также</span><span class="sxs-lookup"><span data-stu-id="3c383-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c383-137">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="3c383-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




