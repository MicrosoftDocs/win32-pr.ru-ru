---
description: Метрики пропускной способности для получения помощи в понимании производительности приложения.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Структура D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273737"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a><span data-ttu-id="94800-103">\_Структура D3D9BANDWIDTHTIMINGS D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="94800-103">D3DDEVINFO\_D3D9BANDWIDTHTIMINGS structure</span></span>

<span data-ttu-id="94800-104">Метрики пропускной способности для получения помощи в понимании производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="94800-104">Throughput metrics for help in understanding the performance of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="94800-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94800-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a><span data-ttu-id="94800-106">Члены</span><span class="sxs-lookup"><span data-stu-id="94800-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="94800-107">**максбандвидсутилизед**</span><span class="sxs-lookup"><span data-stu-id="94800-107">**MaxBandwidthUtilized**</span></span>
</dt> <dd>

<span data-ttu-id="94800-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94800-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94800-109">Пропускная способность или максимальная скорость передачи данных с центрального процессора узла на GPU.</span><span class="sxs-lookup"><span data-stu-id="94800-109">The bandwidth or maximum data transfer rate from the host CPU to the GPU.</span></span> <span data-ttu-id="94800-110">Обычно это полоса пропускания шины PCI или AGP, соединяющая ЦП и GPU.</span><span class="sxs-lookup"><span data-stu-id="94800-110">This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="94800-111">**фронтендуплоадмеморютилизедперцент**</span><span class="sxs-lookup"><span data-stu-id="94800-111">**FrontEndUploadMemoryUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="94800-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94800-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94800-113">Процент использования памяти при передаче данных с центрального процессора на графический процессор.</span><span class="sxs-lookup"><span data-stu-id="94800-113">Memory utilized percentage when uploading data from the host CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="94800-114">**вертексратеутилизедперцент**</span><span class="sxs-lookup"><span data-stu-id="94800-114">**VertexRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="94800-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94800-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94800-116">Процент пропускной способности вершин.</span><span class="sxs-lookup"><span data-stu-id="94800-116">Vertex throughput percentage.</span></span> <span data-ttu-id="94800-117">Это количество обработанных вершин по сравнению с теоретической максимальной скоростью обработки вершин.</span><span class="sxs-lookup"><span data-stu-id="94800-117">This is the number of vertices processed compared to the theoretical maximum vertex processing rate.</span></span>

</dd> <dt>

<span data-ttu-id="94800-118">**трианглесетупратеутилизедперцент**</span><span class="sxs-lookup"><span data-stu-id="94800-118">**TriangleSetupRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="94800-119">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94800-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94800-120">Установка треугольника — процент пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="94800-120">Triangle set-up throughput percentage.</span></span> <span data-ttu-id="94800-121">Число треугольников, настроенных для растрирования по сравнению с теоретической максимальной скоростью настройки треугольника.</span><span class="sxs-lookup"><span data-stu-id="94800-121">This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.</span></span>

</dd> <dt>

<span data-ttu-id="94800-122">**филлратеутилизедперцент**</span><span class="sxs-lookup"><span data-stu-id="94800-122">**FillRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="94800-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94800-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="94800-124">Процент пропускной способности заполнения пикселей.</span><span class="sxs-lookup"><span data-stu-id="94800-124">Pixel fill throughput percentage.</span></span> <span data-ttu-id="94800-125">Число пикселей, которые заполняются по сравнению с теоретической заливкой пикселей.</span><span class="sxs-lookup"><span data-stu-id="94800-125">This is the number of pixels that are filled compared to the theoretical pixel fill.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94800-126">Требования</span><span class="sxs-lookup"><span data-stu-id="94800-126">Requirements</span></span>



| <span data-ttu-id="94800-127">Требование</span><span class="sxs-lookup"><span data-stu-id="94800-127">Requirement</span></span> | <span data-ttu-id="94800-128">Значение</span><span class="sxs-lookup"><span data-stu-id="94800-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94800-129">Header</span><span class="sxs-lookup"><span data-stu-id="94800-129">Header</span></span><br/> | <dl> <span data-ttu-id="94800-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="94800-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94800-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94800-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94800-132">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="94800-132">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="94800-133">**GetData**</span><span class="sxs-lookup"><span data-stu-id="94800-133">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
