---
title: Константы D3DCOMPILE (D3DCompiler. h)
description: Константы D3DCOMPILE указывают, как компилятор компилирует код HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273717"
---
# <a name="d3dcompile-constants"></a>Константы D3DCOMPILE

Константы D3DCOMPILE указывают, как компилятор компилирует код HLSL.

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**\_Отладка D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Направляет компилятору команду на вставку в выходной код отладочного файла, строки, типа или символьной информации.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ пропустить \_ проверку**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Указывает компилятору не проверять созданный код на соответствие известным возможностям и ограничениям. Рекомендуется использовать эту константу только с шейдерами, которые были успешно скомпилированы в прошлом. DirectX всегда проверяет шейдеры перед их назначением устройству.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**\_Оптимизация D3DCOMPILE Skip \_**
</dt> <dd> <dl> <dt>

(1 << 2)
</dt> <dt>



Указывает компилятору пропустить этапы оптимизации во время создания кода. Эту константу рекомендуется устанавливать только в целях отладки.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ Основная строка матрицы D3DCOMPILE Pack \_ \_**
</dt> <dd> <dl> <dt>

(1 << 3)
</dt> <dt>



Направляет компилятору упаковку матриц в построчном порядке для входных и выходных данных шейдера.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_ \_ Столбец матрицы D3DCOMPILE Pack — \_ \_ основной**
</dt> <dd> <dl> <dt>

(1 << 4)
</dt> <dt>



Направляет компилятору упаковку матриц в пошаговом порядке столбцов для ввода и вывода шейдера. Этот тип упаковки, как правило, более эффективен, так как ряд точечных продуктов может выполнять умножение векторных матриц.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Частичная \_ точность D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 5)
</dt> <dt>



Направляет компилятор для выполнения всех вычислений с частичной точностью. Если задать эту константу, скомпилированный код может работать быстрее на определенном оборудовании.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ и \_ программное обеспечение \_ без \_ согласия**
</dt> <dd> <dl> <dt>

(1 << 6)
</dt> <dt>



Направляет компилятору компиляцию вершинного шейдера для следующего более высокого профиля шейдера. Эта константа включает отладку и оптимизацию.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ принудительно использовать \_ \_ программное обеспечение PS \_ без \_ согласия**
</dt> <dd> <dl> <dt>

(1 << 7)
</dt> <dt>



Направляет компилятору компиляцию пиксельного шейдера для следующего более высокого профиля шейдера. Эта константа также включает отладку и оптимизацию.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ без \_ предшейдера**
</dt> <dd> <dl> <dt>

(1 << 8)
</dt> <dt>



Указывает компилятору отключить предшейдеры. Если задать эту константу, компилятор не выберет статическое выражение для вычисления.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ избегать \_ \_ управления потоком**
</dt> <dd> <dl> <dt>

(1 << 9)
</dt> <dt>



Указывает компилятору не использовать конструкции управления потоком там, где это возможно.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ предпочитать \_ \_ Управление потоком**
</dt> <dd> <dl> <dt>

(1 << 10)
</dt> <dt>



Указывает компилятору использовать конструкции управления потоком там, где это возможно.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ включить \_ точность**
</dt> <dd> <dl> <dt>

(1 << 11)
</dt> <dt>



Вызывает принудительную компиляцию, что может привести к невозможности использования устаревшего синтаксиса.

По умолчанию компилятор отключает жесткость в устаревшем синтаксисе.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ включить \_ обратную \_ Совместимость**
</dt> <dd> <dl> <dt>

(1 << 12)
</dt> <dt>



Указывает компилятору включить более старые шейдеры для компиляции до 5 \_ 0 целевых объектов.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_**
</dt> <dd> <dl> <dt>

(1 << 13)
</dt> <dt>



Вызывает принудительную компиляцию IEEE.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**\_LEVEL0 оптимизация \_ D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 14)
</dt> <dt>



Указывает компилятору использовать самый низкий уровень оптимизации. Если задать эту константу, компилятор может создать более медленный код, но быстро создаст код. Установите эту константу при итеративной разработке шейдера.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**\_Level1 оптимизация \_ D3DCOMPILE**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Указывает компилятору использовать второй минимальный уровень оптимизации.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**\_Level2 оптимизация \_ D3DCOMPILE**
</dt> <dd> <dl> <dt>

((1 << 14) \| (1 << 15))
</dt> <dt>



Указывает компилятору использовать второй высший уровень оптимизации.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**\_LEVEL3 оптимизация \_ D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 15)
</dt> <dt>



Указывает компилятору использовать самый высокий уровень оптимизации. Если задать эту константу, компилятор создаст лучший код, но это может занять значительно больше времени. Установите эту константу для окончательных сборок приложения, когда производительность является наиболее важным фактором.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**\_Предупреждения D3DCOMPILE \_ — \_ ошибки**
</dt> <dd> <dl> <dt>

(1 << 18)
</dt> <dt>



Указывает компилятору обрабатывать все предупреждения как ошибки при компиляции кода шейдера. Рекомендуется использовать эту константу для нового кода шейдера, чтобы можно было разрешить все предупреждения и уменьшить число ненужных ошибок в коде.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**\_Ресурсы D3DCOMPILE \_ могут быть \_ псевдонимами**
</dt> <dd> <dl> <dt>

(1 << 19)
</dt> <dt>



Указывает компилятору предположить, что неупорядоченные представления доступа (Уавс) и представления ресурсов шейдера (СРВС) могут быть псевдонимами для CS \_ 5 \_ 0.

> [!Note]  
> Эта константа компилятора является новой, начиная с \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ включить \_ неограниченные \_ таблицы дескрипторов \_**
</dt> <dd> <dl> <dt>

(1 << 20)
</dt> <dt>



Указывает компилятору включить неограниченные таблицы дескрипторов.

> [!Note]  
> Эта константа компилятора является новой, начиная с \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ все \_ ресурсы \_ привязаны**
</dt> <dd> <dl> <dt>

(1 << 21)
</dt> <dt>



Указывает компилятору убедиться, что все ресурсы привязаны.

> [!Note]  
> Эта константа компилятора является новой, начиная с \_47.dll D3dcompiler.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





