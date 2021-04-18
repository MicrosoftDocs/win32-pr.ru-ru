---
title: Базовые перечисления
description: Следующие перечисления объявляются в d3d12. h.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 7f34266e4afdec14e97caa81f393733f1c1ec684
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "105700979"
---
# <a name="core-enumerations"></a>Базовые перечисления

Следующие перечисления объявляются в d3d12. h.

## <a name="in-this-section"></a>Содержание раздела

| Раздел и описание |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Указывает версию макета корневой подписи. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Указывает модель шейдера. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Определяет константы, задающих операции GPU для отрисовки и вычислений. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Определяет константы, указывающие уровень динамической оптимизации, применяемый к работам GPU, которые впоследствии передаются. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Задает Коэффициенты смешения, которые модуляции значений для шейдера пикселей и целевого объекта прорисовки. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Указывает операции смешения RGB или Alpha. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Определяет способ просмотра ресурса буфера. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Определяет параметры представления неупорядоченного доступа для буферного ресурса. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Указывает, что следует очистить в представлении трафарета глубины. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Определяет, какие компоненты каждого пикселя целевого объекта отрисовки доступны для записи во время смешения. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Используется для определения типов списков команд, поддерживающих различные операции. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Указывает тип списка команд. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Задает флаги, используемые при создании очереди команд. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Определяет уровни приоритета для очереди команд. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Задает параметры сравнения. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Определяет, включено ли консервативное растрирование. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Определяет уровень уровня консервативной растеризации. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Задает свойства страницы ЦП для кучи. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Задает уровень общего доступа между узлами адаптера, например "уровень 1", "Эмуляция", "уровень 1" или "уровень 2".  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Указывает, что треугольники, направленные в определенное направление, не рисуются. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Указывает тип данных памяти, на который указывает параметр *pData* для [**ID3D12DebugDevice1:: сетдебугпараметер**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) и [**ID3D12DebugDevice1:: жетдебугпараметер**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter). |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Определяет часть буфера шаблона глубины для записи данных глубины. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Задает параметры для кучи. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Указывает тип кучи дескрипторов.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Указывает изменчивости для дескрипторов и данных, на которые они ссылаются в описании корневой сигнатуры 1,1, что может включить некоторые оптимизации драйверов. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Указывает диапазон, так что, например, если часть таблицы дескрипторов имеет 100 представлений ресурсов шейдера (СРВС), этот диапазон можно объявить в одной записи, а не в 100.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Определяет константы, задающих операции GPU для отрисовки и вычислений. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Определяет константы (используемые [интерфейсом ID3D12DeviceRemovedExtendedDataSettings](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)), которые определяют, как отдельные устройства удаляют функции расширенных данных (направлять). |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Определяет константы, используемые в [структуре D3D12_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) для указания контрольных флагов для среды выполнения Direct3D. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Определяет константы, указывающие версию удаленных расширенных данных устройства (НАПРАВЛЯТЬ), используемую [структурой D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Указывает, как получить доступ к ресурсу, используемому в представлении трафарета глубины. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Задает параметры представления шаблона глубины. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Параметры функции Direct3D 12, поддерживаемые текущим графическим драйвером.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Задает параметры ограждения.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Задает режим заполнения, используемый при отрисовке треугольников. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Задает параметры фильтрации во время выборки текстур. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Указывает тип сокращения фильтра.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Задает тип фильтров "увеличение" или "минификации".  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Указывает ресурсы, которые поддерживаются для указанного формата. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Указывает, какие неупорядоченные ресурсы поддерживаются для указанного формата. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Определяет флаги, указывающие состояния, связанные со списком команд графики. Значения могут быть побитовыми или объединенными. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Задает параметры кучи, например, может ли куча содержать текстуры, а также общие ресурсы для разных адаптеров.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Определяет константы, которые задают поддержку сериализации кучи. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Указывает тип кучи. Если резидентные, кучи находятся в определенном пуле физической памяти с определенными свойствами кэша ЦП.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). При использовании топологии примитивов треугольной линии позиции вершин обрабатываются как вершины непрерывной треугольной полосы. Существует специальное значение индекса, представляющее потребность в ненепрерывности полосы, значение индекса Cut. В этом перечислении перечислены поддерживаемые вырезанные значения.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Указывает тип косвенного параметра.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Определяет тип данных, содержащихся во входном слоте. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Определяет константы, указывающие состояние времени существования объекта, отслеживающего время существования. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Указывает логические операции, которые необходимо настроить для целевого объекта прорисовки. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Определяет константы, которые указывают, что следует делать с результатами профилирования более ранней рабочей нагрузки. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Указывает пул памяти для кучи. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Определяет константы, указывающие флаги для параметра meta-команде. Значения могут быть побитовыми или объединенными. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Определяет константы, которые указывают этап параметра для команды meta. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Определяет константы, указывающие тип данных параметра для команды meta. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Задает несколько флагов ожидания для нескольких ограждений. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Задает параметры для определения уровней качества.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Флаги для управления состоянием конвейера.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Указывает тип подобъекта в описании потока состояния конвейера. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Указывает операцию затенения для применения.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Указывает, как конвейер интерпретирует геометрические или поверхностиные примитивы ввода шейдера. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Задает уровень поддержки программируемых положений, предлагаемых адаптером. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Определяет константы, указывающие флаги сеанса защищенных ресурсов. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Определяет константы, определяющие поддержку сеанса защищенных ресурсов. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Определяет константы, указывающие состояние защищенного сеанса. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Указывает тип создаваемой кучи запроса. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Указывает тип запроса. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Флаги, передаваемые функции [**трацерай**](./traceray-function.md) для переопределения прозрачности, отбора и поведения при начальном выходе. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Задает флаги для сборки структуры ускорения райтраЦинг. Используйте значение из этого перечисления в структуре [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) , которая предоставляет входные данные для операции построения структуры ускорения. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Указывает тип операции копирования, выполняемой при вызове [**копирайтраЦингакцелератионструктуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Указывает тип структуры ускорения, данные после сборки, которые можно получить с помощью вызовов [**емитрайтраЦингакцелератионструктурепостбуилдинфо**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) и [**буилдрайтраЦингакцелератионструктуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Указывает тип структуры ускорения райтраЦинг. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Задает флаги для райтраЦинг Geometry в структуре [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) . |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Указывает тип геометрии, используемый для райтраЦинг. Используйте значение из этого перечисления, чтобы указать тип геометрии в [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Флаги для экземпляра структуры ускорения райтраЦинг. Эти флаги можно использовать для переопределения [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) для отдельных экземпляров. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Задает уровень поддержки трассировки лучей на графическом устройстве. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Указывает тип доступа, присваиваемый приложению указанным ресурсам при переходе в проход визуализации. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Указывает тип доступа, присваиваемый приложению указанным ресурсам при переходе с этапа прорисовки. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Указывает природу этапа подготовки к просмотру; Например, является ли он приостановкой или возобновлением прохода визуализации. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Используется с функцией Енкуеуемакересидент для выбора способа продолжения операций местонахождение при превышении бюджета памяти. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Указывает обширные сегменты приоритета местонахождение, которые полезны для быстрой установки схемы приоритета приложения. |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Указывает операцию разрешения. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Флаги для настройки барьеров разделения ресурсов.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Указывает тип описания барьера ресурсов (переход на использование ресурсов). |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Определяет уровень используемой привязки ресурса.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Определяет тип используемого ресурса. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Указывает параметры для работы с ресурсами.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Указывает, какой уровень кучи ресурсов поддерживает оборудование и драйверы.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Указывает состояние ресурса, относящегося к использованию ресурса.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Указывает изменчивости данных, на которые ссылаются дескрипторы в корневом описании сигнатуры 1,1, что может включить некоторые оптимизации драйверов. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Указывает тип корневого слота подписи.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Задает параметры для макета корневой подписи.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Определяет тип ресурса для просмотра в качестве целевого объекта отрисовки. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Описывает уровень поддержки кэширования шейдеров в текущем графическом драйвере. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Указывает, как направляется память с помощью представления ресурсов шейдера (SRV).  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Описывает параметры минимальной точности для шейдеров в текущем графическом драйвере.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Задает шейдеры, которые могут получать доступ к содержимому заданного корневого слота подписи. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Определяет константы, указывающие уровень поддержки совместного использования API. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Определяет тип ресурса, который будет просматриваться как ресурс шейдера. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Задает цвет границы для статического образца.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Определяет операции с наборами элементов, которые могут быть выполнены во время тестирования шаблона глубины. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Определяет метод разрешения координат текстуры, находящихся за пределами границ текстуры.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Указывает, какой тип копирования текстур должен выполняться. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Задает параметры макета текстуры.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Задает способ копирования плитки.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Указывает, как выполнить операцию сопоставления плиток.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Задает диапазон сопоставлений плиток.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Определяет уровень уровня, на котором поддерживаются мозаичные ресурсы.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Определяет параметры неупорядоченного представления доступа. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Задает параметры для создания экземпляров представления. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Указывает уровень уровня, на котором поддерживается создание экземпляров представлений. |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Указывает режим, используемый операцией **вритебуффериммедиате** . |

## <a name="related-topics"></a>См. также

* [Справочник по коду](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)