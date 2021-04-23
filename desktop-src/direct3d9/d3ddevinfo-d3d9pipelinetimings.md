---
description: Процент времени обработки данных в конвейере.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: Структура D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674689"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a><span data-ttu-id="e1b64-103">\_Структура D3D9PIPELINETIMINGS D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="e1b64-103">D3DDEVINFO\_D3D9PIPELINETIMINGS structure</span></span>

<span data-ttu-id="e1b64-104">Процент времени обработки данных в конвейере.</span><span class="sxs-lookup"><span data-stu-id="e1b64-104">Percent of time processing data in the pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1b64-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a><span data-ttu-id="e1b64-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e1b64-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1b64-107">**вертекспроцессингтимеперцент**</span><span class="sxs-lookup"><span data-stu-id="e1b64-107">**VertexProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e1b64-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b64-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1b64-109">Процент времени, затраченного на выполнение шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="e1b64-109">Percent of time spent running vertex shaders.</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-110">**пикселпроцессингтимеперцент**</span><span class="sxs-lookup"><span data-stu-id="e1b64-110">**PixelProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e1b64-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b64-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1b64-112">Процент времени, затраченного на выполнение шейдеров пикселей.</span><span class="sxs-lookup"><span data-stu-id="e1b64-112">Percent of time spent running pixel shaders.</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-113">**осергпупроцессингтимеперцент**</span><span class="sxs-lookup"><span data-stu-id="e1b64-113">**OtherGPUProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e1b64-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b64-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1b64-115">Процент времени, затраченного на выполнение другой обработки.</span><span class="sxs-lookup"><span data-stu-id="e1b64-115">Percent of time spent doing other processing.</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-116">**гпуидлетимеперцент**</span><span class="sxs-lookup"><span data-stu-id="e1b64-116">**GPUIdleTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e1b64-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1b64-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e1b64-118">Процент времени, при котором ничего не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="e1b64-118">Percent of time not processing anything.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1b64-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1b64-119">Remarks</span></span>

<span data-ttu-id="e1b64-120">Для оптимальной производительности рекомендуется использовать сбалансированную нагрузку.</span><span class="sxs-lookup"><span data-stu-id="e1b64-120">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b64-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e1b64-121">Requirements</span></span>



| <span data-ttu-id="e1b64-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e1b64-122">Requirement</span></span> | <span data-ttu-id="e1b64-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e1b64-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b64-124">Header</span><span class="sxs-lookup"><span data-stu-id="e1b64-124">Header</span></span><br/> | <dl> <span data-ttu-id="e1b64-125"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b64-125"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b64-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1b64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b64-127">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1b64-127">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="e1b64-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="e1b64-128">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
