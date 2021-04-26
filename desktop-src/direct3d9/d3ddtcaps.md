---
description: Константы, описывающие типы данных вершин, поддерживаемые устройством.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 094ca568554722f4da2606233f4ad2c1e59e892f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999451"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="a0767-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="a0767-103">D3DDTCAPS</span></span>

<span data-ttu-id="a0767-104">Константы, описывающие типы данных вершин, поддерживаемые устройством.</span><span class="sxs-lookup"><span data-stu-id="a0767-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="a0767-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="a0767-105">\#define</span></span>              | <span data-ttu-id="a0767-106">Значение</span><span class="sxs-lookup"><span data-stu-id="a0767-106">Value</span></span>       | <span data-ttu-id="a0767-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a0767-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0767-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="a0767-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="a0767-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="a0767-109">0x00000001L</span></span> | <span data-ttu-id="a0767-110">байт без знака 4D.</span><span class="sxs-lookup"><span data-stu-id="a0767-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="a0767-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="a0767-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="a0767-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="a0767-112">0x00000002L</span></span> | <span data-ttu-id="a0767-113">Нормализованный байт без знака 4D.</span><span class="sxs-lookup"><span data-stu-id="a0767-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="a0767-114">Каждый из четырех байтов нормализован путем деления на 255,0.</span><span class="sxs-lookup"><span data-stu-id="a0767-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="a0767-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="a0767-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="a0767-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="a0767-116">0x00000004L</span></span> | <span data-ttu-id="a0767-117">Нормализованная, коротко знакомая с двухмерной подписью, расширенная до (первый байт/32767.0, второй байт/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="a0767-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="a0767-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="a0767-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="a0767-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="a0767-119">0x00000008L</span></span> | <span data-ttu-id="a0767-120">Нормализовано, короткое время со знаком, расширено до (первый байт/32767.0, второй байт/32767.0, третий байт/32767.0, четвертый байт/32767.0).</span><span class="sxs-lookup"><span data-stu-id="a0767-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="a0767-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="a0767-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="a0767-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="a0767-122">0x00000010L</span></span> | <span data-ttu-id="a0767-123">Нормализованная, двухмерная без знака, расширенная до (первый байт/65535.0, второй байт/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="a0767-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="a0767-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="a0767-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="a0767-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="a0767-125">0x00000020L</span></span> | <span data-ttu-id="a0767-126">Нормализованное значение неподписанного формата 4D без знака, расширено до (первый байт/65535.0, второй байт/65535.0, третий байт/65535.0, четвертый байт/65535.0).</span><span class="sxs-lookup"><span data-stu-id="a0767-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="a0767-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="a0767-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="a0767-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="a0767-128">0x00000040L</span></span> | <span data-ttu-id="a0767-129">Трехмерный формат без знака 10 10 10, развернутый до (значение, значение, значение, 1).</span><span class="sxs-lookup"><span data-stu-id="a0767-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="a0767-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="a0767-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="a0767-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="a0767-131">0x00000080L</span></span> | <span data-ttu-id="a0767-132">формат трехмерной подписи 10 10 10 нормализован и расширен до (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="a0767-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="a0767-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a0767-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="a0767-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="a0767-134">0x00000100L</span></span> | <span data-ttu-id="a0767-135">Двумерные 16-битные числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a0767-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="a0767-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a0767-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="a0767-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="a0767-137">0x00000200L</span></span> | <span data-ttu-id="a0767-138">4D 16-разрядные числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a0767-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="a0767-139">Эти константы используются членом Деклтипес объекта [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="a0767-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a0767-140">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="a0767-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a0767-141">Header</span><span class="sxs-lookup"><span data-stu-id="a0767-141">Header</span></span>                   | <span data-ttu-id="a0767-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a0767-142">d3d9caps.h</span></span> |
| <span data-ttu-id="a0767-143">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="a0767-143">Minimum operating system</span></span> | <span data-ttu-id="a0767-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a0767-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a0767-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a0767-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0767-146">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="a0767-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



