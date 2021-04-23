---
description: Флаги возможностей набора элементов драйвера.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423238"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="d766e-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="d766e-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="d766e-104">Флаги возможностей набора элементов драйвера.</span><span class="sxs-lookup"><span data-stu-id="d766e-104">Driver stencil capability flags.</span></span>



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d766e-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="d766e-105">\#define</span></span>                 | <span data-ttu-id="d766e-106">Значение</span><span class="sxs-lookup"><span data-stu-id="d766e-106">Value</span></span>       | <span data-ttu-id="d766e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d766e-107">Description</span></span>                                                                                           |
| <span data-ttu-id="d766e-108">D3DSTENCILCAPS \_</span><span class="sxs-lookup"><span data-stu-id="d766e-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="d766e-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="d766e-109">0x00000001L</span></span> | <span data-ttu-id="d766e-110">Не обновляйте запись в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="d766e-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="d766e-111">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d766e-111">This is the default value.</span></span>                             |
| <span data-ttu-id="d766e-112">D3DSTENCILCAPS \_ 0</span><span class="sxs-lookup"><span data-stu-id="d766e-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="d766e-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="d766e-113">0x00000002L</span></span> | <span data-ttu-id="d766e-114">Задайте для записи в буфере набора элементов значение 0.</span><span class="sxs-lookup"><span data-stu-id="d766e-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="d766e-115">D3DSTENCILCAPS \_ заменить</span><span class="sxs-lookup"><span data-stu-id="d766e-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="d766e-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="d766e-116">0x00000004L</span></span> | <span data-ttu-id="d766e-117">Замените запись в буфере набора элементов значением ссылки.</span><span class="sxs-lookup"><span data-stu-id="d766e-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="d766e-118">D3DSTENCILCAPS \_ инкрсат</span><span class="sxs-lookup"><span data-stu-id="d766e-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="d766e-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="d766e-119">0x00000008L</span></span> | <span data-ttu-id="d766e-120">Увеличение записи буфера набора элементов с фиксацией до максимального значения.</span><span class="sxs-lookup"><span data-stu-id="d766e-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="d766e-121">D3DSTENCILCAPS \_ декрсат</span><span class="sxs-lookup"><span data-stu-id="d766e-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="d766e-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="d766e-122">0x00000010L</span></span> | <span data-ttu-id="d766e-123">Уменьшение записи в буфере набора элементов с фиксацией в ноль.</span><span class="sxs-lookup"><span data-stu-id="d766e-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="d766e-124">D3DSTENCILCAPS \_ инверсия</span><span class="sxs-lookup"><span data-stu-id="d766e-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="d766e-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="d766e-125">0x00000020L</span></span> | <span data-ttu-id="d766e-126">Инвертировать биты в записи в буфере набора элементов.</span><span class="sxs-lookup"><span data-stu-id="d766e-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="d766e-127">D3DSTENCILCAPS \_ INCR</span><span class="sxs-lookup"><span data-stu-id="d766e-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="d766e-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="d766e-128">0x00000040L</span></span> | <span data-ttu-id="d766e-129">Увеличение записи буфера набора элементов с переносом в ноль, если новое значение превышает максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="d766e-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="d766e-130">D3DSTENCILCAPS \_ декр</span><span class="sxs-lookup"><span data-stu-id="d766e-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="d766e-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="d766e-131">0x00000080L</span></span> | <span data-ttu-id="d766e-132">Уменьшите запись в буфере набора элементов, заключив в нее максимальное значение, если новое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="d766e-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="d766e-133">D3DSTENCILCAPS \_ твосидед</span><span class="sxs-lookup"><span data-stu-id="d766e-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="d766e-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="d766e-134">0x00000100L</span></span> | <span data-ttu-id="d766e-135">Устройство поддерживает набор элементов с двумя сторонами.</span><span class="sxs-lookup"><span data-stu-id="d766e-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="d766e-136">Элементы в буфере набора элементов — это целые значения в диапазоне от 0 до 2 ⁿ-1, где n — битовая глубина буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="d766e-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="d766e-137">Эти константы используются членом СтенЦилкапс объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="d766e-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="d766e-138">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="d766e-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d766e-139">Header</span><span class="sxs-lookup"><span data-stu-id="d766e-139">Header</span></span>                   | <span data-ttu-id="d766e-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="d766e-140">d3d9caps.h</span></span> |
| <span data-ttu-id="d766e-141">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="d766e-141">Minimum operating system</span></span> | <span data-ttu-id="d766e-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d766e-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d766e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="d766e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d766e-144">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="d766e-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



