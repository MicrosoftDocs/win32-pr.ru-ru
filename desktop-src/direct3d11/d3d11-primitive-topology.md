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
# <a name="d3d11_primitive_topology-enumeration"></a>\_Перечисление примитивной \_ топологии D3D11

Способ, с помощью которого конвейер интерпретирует данные вершин, привязанные к этапу ассемблера ввода. Эти значения примитивной топологии определяют, как данные вершин подготавливаются к просмотру на экране.

## <a name="syntax"></a>Синтаксис


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Топология примитива D3D11 не \_ \_ определена**
</dt> <dd>

Этап IA не был инициализирован с помощью простой топологии. Этап IA не будет работать правильно, если не определена топология-примитив.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**\_Поинтлист-примитивная \_ ТОПОЛОГИя D3D11 \_**
</dt> <dd>

Интерпретировать данные вершин как список точек.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**\_Линелист-примитивная \_ ТОПОЛОГИя D3D11 \_**
</dt> <dd>

Интерпретировать данные вершин как список строк.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**\_Линестрип-примитивная \_ ТОПОЛОГИя D3D11 \_**
</dt> <dd>

Интерпретировать данные вершин как линейную полосу.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**\_Трианглелист-примитивная \_ ТОПОЛОГИя D3D11 \_**
</dt> <dd>

Интерпретировать данные вершин как список треугольников.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**\_Трианглестрип-примитивная \_ ТОПОЛОГИя D3D11 \_**
</dt> <dd>

Интерпретировать данные вершин как ленту треугольника.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11- \_ примитивная \_ топология \_ линелист \_**
</dt> <dd>

Интерпретировать данные вершин в виде списка строк с соседными данными.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11- \_ примитивная \_ топология \_ линестрип \_**
</dt> <dd>

Интерпретировать данные вершин как полосу строк с помощью смежных данных.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11- \_ примитивная \_ топология \_ трианглелист \_**
</dt> <dd>

Интерпретировать данные вершин как список треугольников с соседными данными.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11- \_ примитивная \_ топология \_ трианглестрип \_**
</dt> <dd>

Распознавать данные вершин как ленту треугольника с помощью смежных данных.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**\_ \_ \_ \_ \_ Патчлист точка управления \_ D3D11-примитива 1**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 2 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 3 \_ \_ патчлист точка управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 4 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 5 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 6 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 7 \_ \_ патчлист точка управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 8 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 9 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 10 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 11 — \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 12 \_ \_ патчлист точка управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 13 \_ \_ патчлист точка управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 14 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 15 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 16 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 17 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 18 \_ \_ патчлист точки управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 19 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 20 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 21 \_ \_ патчлист точка управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 22 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 23 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 24 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 25 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 26 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 27. \_ \_ патчлист точка управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 28 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 29 \_ \_ патчлист точка управления \_**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 30 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 31 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11- \_ примитивная \_ топология \_ 32 \_ \_ точка управления \_ патчлист**
</dt> <dd>

Интерпретировать данные вершин как список исправлений.

</dd> </dl>

## <a name="remarks"></a>Примечания

Перечисление **\_ примитивной \_ топологии D3D11** является типом, определенным в файле заголовка D3D11. h как перечисление [**\_ примитивов \_ D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , которое полностью определено в файле заголовка D3DCommon. h.
