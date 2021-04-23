---
description: Способ, с помощью которого конвейер интерпретирует данные вершин, привязанные к этапу ассемблера ввода. Эти значения примитивной топологии определяют, как данные вершин подготавливаются к просмотру на экране.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: '\_Перечисление примитивной \_ топологии D3D11'
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998002"
---
# <a name="d3d11_primitive_topology-enumeration"></a><span data-ttu-id="cf800-104">\_Перечисление примитивной \_ топологии D3D11</span><span class="sxs-lookup"><span data-stu-id="cf800-104">D3D11\_PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="cf800-105">Способ, с помощью которого конвейер интерпретирует данные вершин, привязанные к этапу ассемблера ввода.</span><span class="sxs-lookup"><span data-stu-id="cf800-105">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="cf800-106">Эти значения примитивной топологии определяют, как данные вершин подготавливаются к просмотру на экране.</span><span class="sxs-lookup"><span data-stu-id="cf800-106">These primitive topology values determine how the vertex data is rendered on screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf800-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf800-107">Syntax</span></span>


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a><span data-ttu-id="cf800-108">Константы</span><span class="sxs-lookup"><span data-stu-id="cf800-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf800-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Топология примитива D3D11 не \_ \_ определена**</span><span class="sxs-lookup"><span data-stu-id="cf800-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-110">Этап IA не был инициализирован с помощью простой топологии.</span><span class="sxs-lookup"><span data-stu-id="cf800-110">The IA stage has not been initialized with a primitive topology.</span></span> <span data-ttu-id="cf800-111">Этап IA не будет работать правильно, если не определена топология-примитив.</span><span class="sxs-lookup"><span data-stu-id="cf800-111">The IA stage will not function properly unless a primitive topology is defined.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**\_Поинтлист-примитивная \_ ТОПОЛОГИя D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-113">Интерпретировать данные вершин как список точек.</span><span class="sxs-lookup"><span data-stu-id="cf800-113">Interpret the vertex data as a list of points.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**\_Линелист-примитивная \_ ТОПОЛОГИя D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-115">Интерпретировать данные вершин как список строк.</span><span class="sxs-lookup"><span data-stu-id="cf800-115">Interpret the vertex data as a list of lines.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**\_Линестрип-примитивная \_ ТОПОЛОГИя D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-117">Интерпретировать данные вершин как линейную полосу.</span><span class="sxs-lookup"><span data-stu-id="cf800-117">Interpret the vertex data as a line strip.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**\_Трианглелист-примитивная \_ ТОПОЛОГИя D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-119">Интерпретировать данные вершин как список треугольников.</span><span class="sxs-lookup"><span data-stu-id="cf800-119">Interpret the vertex data as a list of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**\_Трианглестрип-примитивная \_ ТОПОЛОГИя D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-121">Интерпретировать данные вершин как ленту треугольника.</span><span class="sxs-lookup"><span data-stu-id="cf800-121">Interpret the vertex data as a triangle strip.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11- \_ примитивная \_ топология \_ линелист \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-123">Интерпретировать данные вершин в виде списка строк с соседными данными.</span><span class="sxs-lookup"><span data-stu-id="cf800-123">Interpret the vertex data as list of lines with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11- \_ примитивная \_ топология \_ линестрип \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-125">Интерпретировать данные вершин как полосу строк с помощью смежных данных.</span><span class="sxs-lookup"><span data-stu-id="cf800-125">Interpret the vertex data as line strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11- \_ примитивная \_ топология \_ трианглелист \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-127">Интерпретировать данные вершин как список треугольников с соседными данными.</span><span class="sxs-lookup"><span data-stu-id="cf800-127">Interpret the vertex data as list of triangles with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11- \_ примитивная \_ топология \_ трианглестрип \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-129">Распознавать данные вершин как ленту треугольника с помощью смежных данных.</span><span class="sxs-lookup"><span data-stu-id="cf800-129">Interpret the vertex data as triangle strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**\_ \_ \_ \_ \_ Патчлист точка управления \_ D3D11-примитива 1**</span><span class="sxs-lookup"><span data-stu-id="cf800-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-131">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-131">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 2 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-133">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-133">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 3 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-135">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-135">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 4 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-137">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-137">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 5 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-139">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-139">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 6 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-141">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-141">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 7 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-143">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-143">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 8 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-145">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-145">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 9 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-147">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-147">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 10 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-149">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-149">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 11 — \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-151">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-151">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 12 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-153">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-153">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 13 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-155">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-155">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 14 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-157">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-157">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 15 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-159">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-159">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 16 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-161">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-161">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 17 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-163">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-163">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 18 \_ \_ патчлист точки управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-165">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-165">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 19 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-167">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-167">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 20 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-169">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-169">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 21 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-171">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-171">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 22 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-173">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-173">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 23 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-175">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-175">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 24 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-177">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-177">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 25 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-179">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-179">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 26 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-181">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-181">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 27. \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-183">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-183">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 28 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-185">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-185">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 29 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="cf800-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-187">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-187">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 30 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-189">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-189">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 31 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-191">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-191">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="cf800-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 32 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="cf800-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="cf800-193">Интерпретировать данные вершин как список исправлений.</span><span class="sxs-lookup"><span data-stu-id="cf800-193">Interpret the vertex data as a patch list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf800-194">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf800-194">Remarks</span></span>

<span data-ttu-id="cf800-195">Перечисление **\_ примитивной \_ топологии D3D11** является типом, определенным в файле заголовка D3D11. h как перечисление [**\_ примитивов \_ D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , которое полностью определено в файле заголовка D3DCommon. h.</span><span class="sxs-lookup"><span data-stu-id="cf800-195">The **D3D11\_PRIMITIVE\_TOPOLOGY** enumeration is type defined in the D3D11.h header file as a [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) enumeration, which is fully defined in the D3DCommon.h header file.</span></span>
