---
title: texreg2gb-PS
description: Интерпретирует зеленый и синий цветовые компоненты регистра источника как данные адреса текстуры для выборки текстуры на этапе, соответствующей номеру регистра назначения.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984005"
---
# <a name="texreg2gb---ps"></a><span data-ttu-id="5dbea-103">texreg2gb-PS</span><span class="sxs-lookup"><span data-stu-id="5dbea-103">texreg2gb - ps</span></span>

<span data-ttu-id="5dbea-104">Интерпретирует зеленый и синий цветовые компоненты регистра источника как данные адреса текстуры для выборки текстуры на этапе, соответствующей номеру регистра назначения.</span><span class="sxs-lookup"><span data-stu-id="5dbea-104">Interprets the green and blue color components of the source register as texture address data to sample the texture at the stage corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dbea-105">Syntax</span></span>



| <span data-ttu-id="5dbea-106">texreg2gb DST, src</span><span class="sxs-lookup"><span data-stu-id="5dbea-106">texreg2gb dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="5dbea-107">где</span><span class="sxs-lookup"><span data-stu-id="5dbea-107">where</span></span>

-   <span data-ttu-id="5dbea-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="5dbea-108">dst is the destination register.</span></span>
-   <span data-ttu-id="5dbea-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="5dbea-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dbea-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dbea-110">Remarks</span></span>



| <span data-ttu-id="5dbea-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="5dbea-111">Pixel shader versions</span></span> | <span data-ttu-id="5dbea-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="5dbea-112">1\_1</span></span> | <span data-ttu-id="5dbea-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="5dbea-113">1\_2</span></span> | <span data-ttu-id="5dbea-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5dbea-114">1\_3</span></span> | <span data-ttu-id="5dbea-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="5dbea-115">1\_4</span></span> | <span data-ttu-id="5dbea-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5dbea-116">2\_0</span></span> | <span data-ttu-id="5dbea-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5dbea-117">2\_x</span></span> | <span data-ttu-id="5dbea-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5dbea-118">2\_sw</span></span> | <span data-ttu-id="5dbea-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5dbea-119">3\_0</span></span> | <span data-ttu-id="5dbea-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5dbea-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5dbea-121">texreg2gb</span><span class="sxs-lookup"><span data-stu-id="5dbea-121">texreg2gb</span></span>             |      | <span data-ttu-id="5dbea-122">x</span><span class="sxs-lookup"><span data-stu-id="5dbea-122">x</span></span>    | <span data-ttu-id="5dbea-123">x</span><span class="sxs-lookup"><span data-stu-id="5dbea-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="5dbea-124">Эта инструкция полезна для операций повторного сопоставления цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="5dbea-124">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="5dbea-125">Ниже приведен пример последовательности, в которой приведена инструкция.</span><span class="sxs-lookup"><span data-stu-id="5dbea-125">Here is an example of the sequence the instruction follows.</span></span>

<dl> <span data-ttu-id="5dbea-126">Да t (n)</span><span class="sxs-lookup"><span data-stu-id="5dbea-126">tex t(n)</span></span>  
<span data-ttu-id="5dbea-127">texreg2gb t (m), t (n), где m > n</span><span class="sxs-lookup"><span data-stu-id="5dbea-127">texreg2gb t(m), t(n) where m > n</span></span>  
<span data-ttu-id="5dbea-128">Первая инструкция загружает цвет текстуры (RGBA)</span><span class="sxs-lookup"><span data-stu-id="5dbea-128">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="5dbea-129">регистрация тн</span><span class="sxs-lookup"><span data-stu-id="5dbea-129">// into register tn</span></span>  
<span data-ttu-id="5dbea-130">Да тн</span><span class="sxs-lookup"><span data-stu-id="5dbea-130">tex tn</span></span>  
<span data-ttu-id="5dbea-131">Вторая инструкция повторно сопоставляет цвет.</span><span class="sxs-lookup"><span data-stu-id="5dbea-131">// The second instruction remaps the color</span></span>  
<span data-ttu-id="5dbea-132">t (m)<sub>RGBA</sub> = текстуресампле (этап m)<sub>RGBA</sub> с использованием t (n)<sub>ГБ</sub> в качестве координат</span><span class="sxs-lookup"><span data-stu-id="5dbea-132">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="5dbea-133">\_bx2 не может использоваться для реестра src в инструкциях [texreg2ar-PS](texreg2ar---ps.md) или texreg2gb.</span><span class="sxs-lookup"><span data-stu-id="5dbea-133">\_bx2 cannot be used on the src register for [texreg2ar - ps](texreg2ar---ps.md) or texreg2gb instructions.</span></span>

<span data-ttu-id="5dbea-134">Для этой инструкции исходный регистр должен использовать неподписанные данные.</span><span class="sxs-lookup"><span data-stu-id="5dbea-134">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="5dbea-135">Использование подписанных или смешанных данных в исходном регистре приведет к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="5dbea-135">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="5dbea-136">Дополнительные сведения см. в разделе [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="5dbea-136">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dbea-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5dbea-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dbea-138">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="5dbea-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 