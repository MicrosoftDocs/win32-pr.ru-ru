---
title: dcl_samplerType (SM3-VS ASM)
description: Объявите образец шейдера вершин.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996970"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="a08bc-103">дкл \_ самплертипе (SM3-VS ASM)</span><span class="sxs-lookup"><span data-stu-id="a08bc-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="a08bc-104">Объявите образец шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="a08bc-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a08bc-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="a08bc-106">дкл \_ самплертипе s\#</span><span class="sxs-lookup"><span data-stu-id="a08bc-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="a08bc-107">где:</span><span class="sxs-lookup"><span data-stu-id="a08bc-107">where:</span></span>

-   <span data-ttu-id="a08bc-108">\_Самплертипе определяет тип данных образца.</span><span class="sxs-lookup"><span data-stu-id="a08bc-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="a08bc-109">Определяет, сколько координат требуется для каждой координаты текстуры при выборки.</span><span class="sxs-lookup"><span data-stu-id="a08bc-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="a08bc-110">Определены следующие измерения координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="a08bc-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="a08bc-111">\_двухмерном</span><span class="sxs-lookup"><span data-stu-id="a08bc-111">\_2d</span></span>
    -   <span data-ttu-id="a08bc-112">\_Куба</span><span class="sxs-lookup"><span data-stu-id="a08bc-112">\_cube</span></span>
    -   <span data-ttu-id="a08bc-113">\_тома</span><span class="sxs-lookup"><span data-stu-id="a08bc-113">\_volume</span></span>
-   <span data-ttu-id="a08bc-114">s \# определяет образец, где s — это аббревиатура для образца, а \# — номер образца.</span><span class="sxs-lookup"><span data-stu-id="a08bc-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="a08bc-115">[Образцы (Direct3D 9 ASM-VS)](dx9-graphics-reference-asm-vs-registers-sampler.md)s являются псевдо, так как вы не можете напрямую читать их или записывать.</span><span class="sxs-lookup"><span data-stu-id="a08bc-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08bc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a08bc-116">Remarks</span></span>



| <span data-ttu-id="a08bc-117">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="a08bc-117">Vertex shader versions</span></span> | <span data-ttu-id="a08bc-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="a08bc-118">1\_1</span></span> | <span data-ttu-id="a08bc-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a08bc-119">2\_0</span></span> | <span data-ttu-id="a08bc-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a08bc-120">2\_x</span></span> | <span data-ttu-id="a08bc-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a08bc-121">2\_sw</span></span> | <span data-ttu-id="a08bc-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a08bc-122">3\_0</span></span> | <span data-ttu-id="a08bc-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a08bc-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a08bc-124">дкл \_ самплертипе</span><span class="sxs-lookup"><span data-stu-id="a08bc-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="a08bc-125">x</span><span class="sxs-lookup"><span data-stu-id="a08bc-125">x</span></span>    | <span data-ttu-id="a08bc-126">x</span><span class="sxs-lookup"><span data-stu-id="a08bc-126">x</span></span>     |



 

<span data-ttu-id="a08bc-127">Все \_ инструкции самплертипе дкл должны располагаться перед первой исполняемой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="a08bc-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a08bc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a08bc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a08bc-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="a08bc-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




