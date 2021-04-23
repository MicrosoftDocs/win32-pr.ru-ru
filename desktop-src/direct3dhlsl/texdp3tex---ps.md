---
title: texdp3tex-PS
description: Выполняет программный продукт с тремя компонентами и использует результат для поиска по одномерной текстуре.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996855"
---
# <a name="texdp3tex---ps"></a><span data-ttu-id="0079c-103">texdp3tex-PS</span><span class="sxs-lookup"><span data-stu-id="0079c-103">texdp3tex - ps</span></span>

<span data-ttu-id="0079c-104">Выполняет программный продукт с тремя компонентами и использует результат для поиска по одномерной текстуре.</span><span class="sxs-lookup"><span data-stu-id="0079c-104">Performs a three-component dot product and uses the result to do a 1D texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="0079c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0079c-105">Syntax</span></span>



| <span data-ttu-id="0079c-106">texdp3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="0079c-106">texdp3tex dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="0079c-107">где</span><span class="sxs-lookup"><span data-stu-id="0079c-107">where</span></span>

-   <span data-ttu-id="0079c-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="0079c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="0079c-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="0079c-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0079c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="0079c-110">Remarks</span></span>



| <span data-ttu-id="0079c-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="0079c-111">Pixel shader versions</span></span> | <span data-ttu-id="0079c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="0079c-112">1\_1</span></span> | <span data-ttu-id="0079c-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="0079c-113">1\_2</span></span> | <span data-ttu-id="0079c-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0079c-114">1\_3</span></span> | <span data-ttu-id="0079c-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="0079c-115">1\_4</span></span> | <span data-ttu-id="0079c-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0079c-116">2\_0</span></span> | <span data-ttu-id="0079c-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0079c-117">2\_x</span></span> | <span data-ttu-id="0079c-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0079c-118">2\_sw</span></span> | <span data-ttu-id="0079c-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0079c-119">3\_0</span></span> | <span data-ttu-id="0079c-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0079c-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0079c-121">texdp3tex</span><span class="sxs-lookup"><span data-stu-id="0079c-121">texdp3tex</span></span>             |      | <span data-ttu-id="0079c-122">x</span><span class="sxs-lookup"><span data-stu-id="0079c-122">x</span></span>    | <span data-ttu-id="0079c-123">x</span><span class="sxs-lookup"><span data-stu-id="0079c-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0079c-124">Регистры текстур должны использовать следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="0079c-124">Texture registers must use the following sequence.</span></span>


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



<span data-ttu-id="0079c-125">Ниже приведены более подробные сведения о том, как выполняется поиск с помощью точки и текстуры.</span><span class="sxs-lookup"><span data-stu-id="0079c-125">Here is more detail about how the dot product and texture lookup are done.</span></span>

<span data-ttu-id="0079c-126">Инструкция texdp3tex выполняет 3-компонентный продукт.</span><span class="sxs-lookup"><span data-stu-id="0079c-126">The texdp3tex instruction performs a three-component dot product.</span></span>

<span data-ttu-id="0079c-127">u "= TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0079c-127">u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0079c-128">Результат используется для выборки текстуры на этапе текстуры m с помощью одномерного поиска.</span><span class="sxs-lookup"><span data-stu-id="0079c-128">The result is used to sample the texture at texture stage m by performing a 1D lookup.</span></span>

<span data-ttu-id="0079c-129">t (m)<sub>RGBA</sub> = текстуресампле (этап m)<sub>RGBA</sub> с использованием (u, 0, 0) в качестве координат</span><span class="sxs-lookup"><span data-stu-id="0079c-129">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates</span></span>

## <a name="related-topics"></a><span data-ttu-id="0079c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0079c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0079c-131">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0079c-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




