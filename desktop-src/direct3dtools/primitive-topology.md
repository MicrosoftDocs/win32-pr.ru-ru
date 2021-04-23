---
description: Перечисление, используемое для обозначения топологии сетки. См. Мешдатаверткаллбакк.
MS-HAID: vspixengine.PRIMITIVE\_TOPOLOGY
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление PRIMITIVE_TOPOLOGY
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A845DD10-C735-4EA1-82D3-07F3B26508E7
api_name:
- PRIMITIVE_TOPOLOGY
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e448fcaaeaa2b1b50bd77b18ac4b3ac3f5e122a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072312"
---
# <a name="span-idvspixengineprimitive_topologyspanprimitive_topology-enumeration"></a><span data-ttu-id="b0a26-104"><span id="vspixengine.primitive_topology"></span>Перечисление ПРИМИТИВных \_ топологий</span><span class="sxs-lookup"><span data-stu-id="b0a26-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="b0a26-105">Перечисление, используемое для обозначения топологии сетки.</span><span class="sxs-lookup"><span data-stu-id="b0a26-105">An enum used to indicate the topology of a mesh.</span></span> <span data-ttu-id="b0a26-106">См. Мешдатаверткаллбакк.</span><span class="sxs-lookup"><span data-stu-id="b0a26-106">See MeshDataVertCallback.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a26-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0a26-107">Syntax</span></span>


```C++
} PRIMITIVE_TOPOLOGY;
```

## <a name="constants"></a><span data-ttu-id="b0a26-108">Константы</span><span class="sxs-lookup"><span data-stu-id="b0a26-108">Constants</span></span>

<span data-ttu-id="b0a26-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**Топология ПРИМИТИВа не \_ \_ определена**</span><span class="sxs-lookup"><span data-stu-id="b0a26-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>  
<span data-ttu-id="b0a26-110">Топология сетки не определена.</span><span class="sxs-lookup"><span data-stu-id="b0a26-110">The topology of the mesh is undefined.</span></span>

<span data-ttu-id="b0a26-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**\_поинтлист ТОПОЛОГИИ примитивов \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>  
<span data-ttu-id="b0a26-112">Топология сетки — это список точек.</span><span class="sxs-lookup"><span data-stu-id="b0a26-112">The topology of the mesh is a point list.</span></span>

<span data-ttu-id="b0a26-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**\_линелист ТОПОЛОГИИ примитивов \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>  
<span data-ttu-id="b0a26-114">Топология сетки — это список линий.</span><span class="sxs-lookup"><span data-stu-id="b0a26-114">The topology of the mesh is a line list.</span></span>

<span data-ttu-id="b0a26-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**\_линестрип ТОПОЛОГИИ примитивов \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>  
<span data-ttu-id="b0a26-116">Топология сетки является линейной полосой.</span><span class="sxs-lookup"><span data-stu-id="b0a26-116">The topology of the mesh is a line strip.</span></span>

<span data-ttu-id="b0a26-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**\_трианглелист ТОПОЛОГИИ примитивов \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>  
<span data-ttu-id="b0a26-118">Топология сетки — это список треугольников.</span><span class="sxs-lookup"><span data-stu-id="b0a26-118">The topology of the mesh is a triangle list.</span></span>

<span data-ttu-id="b0a26-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**\_трианглестрип ТОПОЛОГИИ примитивов \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>  
<span data-ttu-id="b0a26-120">Топология сетки представляет собой треугольную ленту.</span><span class="sxs-lookup"><span data-stu-id="b0a26-120">The topology of the mesh is a triangle strip.</span></span>

<span data-ttu-id="b0a26-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**\_трианглефан ТОПОЛОГИИ примитивов \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLEFAN**</span></span>  
<span data-ttu-id="b0a26-122">Топология сетки — это вентилятор с треугольником.</span><span class="sxs-lookup"><span data-stu-id="b0a26-122">The topology of the mesh is a triangle fan.</span></span>

<span data-ttu-id="b0a26-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**\_линелистная топология-примитивная \_ \_ разница**</span><span class="sxs-lookup"><span data-stu-id="b0a26-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>  
<span data-ttu-id="b0a26-124">Топология сетки — это список линий с соседкой.</span><span class="sxs-lookup"><span data-stu-id="b0a26-124">The topology of the mesh is a line list with adjacency.</span></span>

<span data-ttu-id="b0a26-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**\_линестрипная топология-примитивная \_ \_ разница**</span><span class="sxs-lookup"><span data-stu-id="b0a26-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>  
<span data-ttu-id="b0a26-126">Топология сетки является линейной полосой с соседкой.</span><span class="sxs-lookup"><span data-stu-id="b0a26-126">The topology of the mesh is a line strip with adjacency.</span></span>

<span data-ttu-id="b0a26-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**\_трианглелистная топология-примитивная \_ \_ разница**</span><span class="sxs-lookup"><span data-stu-id="b0a26-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>  
<span data-ttu-id="b0a26-128">Топология сетки — это список треугольников с соседкой.</span><span class="sxs-lookup"><span data-stu-id="b0a26-128">The topology of the mesh is a triangle list with adjacency.</span></span>

<span data-ttu-id="b0a26-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**\_трианглестрипная топология-примитивная \_ \_ разница**</span><span class="sxs-lookup"><span data-stu-id="b0a26-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>  
<span data-ttu-id="b0a26-130">Топология сетки представляет собой треугольную полоску с соседкой.</span><span class="sxs-lookup"><span data-stu-id="b0a26-130">The topology of the mesh is a triangle strip with adjacency.</span></span>

<span data-ttu-id="b0a26-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**\_ \_ \_ \_ Патчлист точка управления примитивной топологии 1 \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-132">Топология сетки — это список исправлений с 1 контрольной точкой.</span><span class="sxs-lookup"><span data-stu-id="b0a26-132">The topology of the mesh is a patch list with 1 control point.</span></span>

<span data-ttu-id="b0a26-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**\_Точка управления примитивной топологии \_ 2 \_ \_ \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-134">Топология сети — это список исправлений с двумя контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-134">The topology of the mesh is a patch list with 2 control points.</span></span>

<span data-ttu-id="b0a26-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**Точка управления-ПРИМИТИВная \_ топология \_ 3 \_ \_ \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-136">Топология сетки — это список исправлений с тремя контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-136">The topology of the mesh is a patch list with 3 control points.</span></span>

<span data-ttu-id="b0a26-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**Точка управления-ПРИМИТИВная \_ топология \_ 4 \_ \_ \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-138">Топология сетки — это список исправлений с 4 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-138">The topology of the mesh is a patch list with 4 control points.</span></span>

<span data-ttu-id="b0a26-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 5 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-140">Топология сетки — это список исправлений с 5 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-140">The topology of the mesh is a patch list with 5 control points.</span></span>

<span data-ttu-id="b0a26-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 6 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-142">Топология сети — это список исправлений с 6 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-142">The topology of the mesh is a patch list with 6 control points.</span></span>

<span data-ttu-id="b0a26-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**\_Точка управления примитивной топологии \_ 7 \_ \_ \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-144">Топология сетки — это список исправлений с 7 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-144">The topology of the mesh is a patch list with 7 control points.</span></span>

<span data-ttu-id="b0a26-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 8 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-146">Топология сетки — это список исправлений с 8 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-146">The topology of the mesh is a patch list with 8 control points.</span></span>

<span data-ttu-id="b0a26-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 9 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-148">Топология сети — это список исправлений с 9 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-148">The topology of the mesh is a patch list with 9 control points.</span></span>

<span data-ttu-id="b0a26-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 10 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-150">Топология сетки — это список исправлений с 10 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-150">The topology of the mesh is a patch list with 10 control points.</span></span>

<span data-ttu-id="b0a26-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 11 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-152">Топология сетки — это список исправлений с 11 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-152">The topology of the mesh is a patch list with 11 control points.</span></span>

<span data-ttu-id="b0a26-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 12 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-154">Топология сетки — это список исправлений с 12 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-154">The topology of the mesh is a patch list with 12 control points.</span></span>

<span data-ttu-id="b0a26-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 13 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-156">Топология сетки — это список исправлений с 13 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-156">The topology of the mesh is a patch list with 13 control points.</span></span>

<span data-ttu-id="b0a26-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**ПРИМИТИВная \_ топология \_ 14 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-158">Топология сетки — это список исправлений с 14 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-158">The topology of the mesh is a patch list with 14 control points.</span></span>

<span data-ttu-id="b0a26-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 15 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-160">Топология сети — это список исправлений с 15 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-160">The topology of the mesh is a patch list with 15 control points.</span></span>

<span data-ttu-id="b0a26-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**\_Топология примитива \_ 16 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-162">Топология сети — это список исправлений с 16 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-162">The topology of the mesh is a patch list with 16 control points.</span></span>

<span data-ttu-id="b0a26-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**\_Топология примитива \_ 17 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-164">Топология сетки — это список исправлений с 17 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-164">The topology of the mesh is a patch list with 17 control points.</span></span>

<span data-ttu-id="b0a26-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**\_Топология примитивов \_ 18 \_ \_ патчлист точки управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-166">Топология сетки — это список исправлений 18 контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="b0a26-166">The topology of the mesh is a patch list with 18 control points.</span></span>

<span data-ttu-id="b0a26-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**\_Топология примитива \_ 19 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-168">Топология сетки — это список исправлений с 19 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-168">The topology of the mesh is a patch list with 19 control points.</span></span>

<span data-ttu-id="b0a26-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**\_Топология примитива \_ 20 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-170">Топология сети — это список исправлений с 20 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-170">The topology of the mesh is a patch list with 20 control points.</span></span>

<span data-ttu-id="b0a26-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**\_Топология примитивов \_ 21 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-172">Топология сети — это список исправлений с 21 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-172">The topology of the mesh is a patch list with 21 control points.</span></span>

<span data-ttu-id="b0a26-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**\_Топология примитивов \_ 22 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-174">Топология сетки — это список исправлений с 22 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-174">The topology of the mesh is a patch list with 22 control points.</span></span>

<span data-ttu-id="b0a26-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**\_Топология примитивов \_ 23 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-176">Топология сетки — это список исправлений с 23 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-176">The topology of the mesh is a patch list with 23 control points.</span></span>

<span data-ttu-id="b0a26-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**\_Топология-примитив \_ 24 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-178">Топология сети — это список исправлений с 24 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-178">The topology of the mesh is a patch list with 24 control points.</span></span>

<span data-ttu-id="b0a26-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**\_Топология примитива \_ 25 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-180">Топология сетки — это список исправлений с 25 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-180">The topology of the mesh is a patch list with 25 control points.</span></span>

<span data-ttu-id="b0a26-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 26 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-182">Топология сети — это список исправлений с 26 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-182">The topology of the mesh is a patch list with 26 control points.</span></span>

<span data-ttu-id="b0a26-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 27 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-184">Топология сети — это список исправлений с 27 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-184">The topology of the mesh is a patch list with 27 control points.</span></span>

<span data-ttu-id="b0a26-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**\_Топология примитивов \_ 28 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-186">Топология сетки — это список исправлений с 28 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-186">The topology of the mesh is a patch list with 28 control points.</span></span>

<span data-ttu-id="b0a26-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**\_Топология примитивов \_ 29 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-188">Топология сетки — это список исправлений с 29 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-188">The topology of the mesh is a patch list with 29 control points.</span></span>

<span data-ttu-id="b0a26-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**Патчлист-ПРИМИТИВная \_ топология \_ 30 \_ \_ точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-190">Топология сетки — это список исправлений с 30 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-190">The topology of the mesh is a patch list with 30 control points.</span></span>

<span data-ttu-id="b0a26-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**\_Топология-примитив \_ 31 \_ \_ патчлист точка управления \_**</span><span class="sxs-lookup"><span data-stu-id="b0a26-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-192">Топология сетки — это список исправлений с 31 контрольными точками.</span><span class="sxs-lookup"><span data-stu-id="b0a26-192">The topology of the mesh is a patch list with 31 control points.</span></span>

<span data-ttu-id="b0a26-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**ПРИМИТИВная \_ топология \_ 32 \_ \_ точка управления \_ патчлист**</span><span class="sxs-lookup"><span data-stu-id="b0a26-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="b0a26-194">Топология сети — это список исправлений с контрольными точками 32.</span><span class="sxs-lookup"><span data-stu-id="b0a26-194">The topology of the mesh is a patch list with 32 control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a26-195">Требования</span><span class="sxs-lookup"><span data-stu-id="b0a26-195">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b0a26-196">Header</span><span class="sxs-lookup"><span data-stu-id="b0a26-196">Header</span></span></p></td><td><span data-ttu-id="b0a26-197">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="b0a26-197">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



