---
title: Основные структуры (графика Direct3D 12)
description: Следующие структуры объявляются в d3d12. h.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5dd546055c22711ecd9a3796e520ad034e9e46c6
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812691"
---
# <a name="core-structures"></a>Базовые структуры

Следующие структуры объявляются в d3d12. h.

## <a name="in-this-section"></a>Содержание раздела

| Раздел и описание |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Представляет удаленные данные (НАПРАВЛЯТЬ) в виде узла в связанном списке устройства. |
| [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc). Описывает состояние смешения. |
| [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box). Описывает трехмерное поле. |
| [**D3D12_BUFFER_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Описывает элементы в буферном ресурсе для использования в представлении целевого объекта визуализации. |
| [**D3D12_BUFFER_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_srv). Описывает элементы в буферном ресурсе для использования в представлении ресурсов шейдера. |
| [**D3D12_BUFFER_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_buffer_uav). Описывает элементы в буфере для использования в представлении неупорядоченного доступа. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Сохраняет состояние конвейера. |
| [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value). Описывает значение, используемое для оптимизации операций очистки для определенного ресурса. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Описывает очередь команд. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Описывает аргументы (параметры) сигнатуры команды. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Описывает объект состояния "вычисление конвейера". |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Описывает буфер константы для просмотра. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Описывает дескриптор дескриптора ЦП. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Описывает состояние трафарета глубины. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Описывает состояние трафарета глубины. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Задает глубину и значение трафарета. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Описывает подресурсы текстуры, доступные из представления трафарета глубины. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Описывает операции с наборами элементов, которые могут быть выполнены на основе результатов теста набора элементов. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Описывает кучу дескрипторов. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range). Описывает диапазон дескрипторов. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Описывает диапазон дескрипторов с флагами для определения их изменчивости. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Представляет данные о том, что устройство удалило Расширенные данные (НАПРАВЛЯТЬ) версии 1,0. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Представляет данные удаления устройства с расширенными данными (НАПРАВЛЯТЬ) версии 1,1, чтобы отладчики и расширения отладчика могли получать доступ к данным НАПРАВЛЯТЬ. |
| [**D3D12_DISCARD_REGION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_discard_region). Содержит сведения о операции отмены ресурса. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Описывает параметры диспетчеризации для использования в шейдере вычислений. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_arguments). Описывает параметры для экземпляров рисования. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Описывает параметры для рисования индексированных экземпляров. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Описывает, как узел в связанном списке, данные о выделении, записанные устройством, удалили Расширенные данные (НАПРАВЛЯТЬ). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Содержит указатель на заголовок связанного списка объектов [D3D12_AUTO_BREADCRUMB_NODE](/windows/win32/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) . Список представляет состояние автоматической иерархии до удаления устройства. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Описывает данные выделения, связанные с ошибкой страницы GPU по заданному виртуальному адресу (ва). |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Предоставьте подробные сведения об архитектуре адаптера, помогая приложениям оптимизировать работу с определенными свойствами адаптера. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Предоставьте подробные сведения об архитектуре адаптера, помогая приложениям оптимизировать работу с определенными свойствами адаптера. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Сведения о поддержке адаптера для определения приоритетов различных типов очередей команд. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Указывает уровень поддержки совместного использования ресурсов разными адаптерами. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Описание параметров функции Direct3D 12 в текущем графическом драйвере. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Описывает уровень поддержки для операций Wave HLSL 6,0. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Сведения о поддержке адаптером некоторых дополнительных функций Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Используется для указания уровня поддержки, предоставляемого адаптером для дополнительных функций Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Указывает уровень поддержки для текстур MSAA с выравниванием по 64 КБ, совместного использования через API и встроенных 16-разрядных операций шейдера. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Указывает уровень поддержки, предоставляемый адаптером для проходов отрисовки, трассировки лучей и шейдера, мозаичного представления ресурсов уровня 3. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Указывает уровень поддержки, предоставляемый адаптером для заливки переменной скорости (ВРС), и указывает, поддерживается ли фоновая обработка. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS7**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options7). Указывает уровень поддержки, предоставляемый адаптером для сетки и шейдеров усиления, а также для отзывов образцов. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS8**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options8). Указывает, поддерживаются ли текстуры с несогласованным блочным сжатием. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS9**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options9). Указывает, существует ли поддержка шейдеров сетки, значений *SV_RenderTargetArrayIndex* с 8 или более, типизированным ресурсом 64-разрядное целое число атомарных, производных и производных от него операций выборки, а также уровень поддержки для операций вавемма (wave_matrix). |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS10**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options10). Указывает, можно ли использовать объединение SUM, а также следует ли задавать *SV_ShadingRate* из шейдера сетки. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS11**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options11). Указывает, поддерживается ли 64-разрядное целое число, атомарное для ресурсов в куче дескрипторов. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Используется, чтобы детерминине, поддерживает ли адаптер создание куч из существующей системной памяти. Такие кучи не предназначены для общего использования, но они чрезвычайно полезны для диагностики, так как они гарантированно сохраняются даже после сбоя адаптера или при возникновении события удаления устройства. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Содержит сведения о [уровнях функций](/windows/win32/direct3d11/overviews-direct3d-11-devices-downlevel-intro) , поддерживаемых текущим графическим драйвером. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Описывает формат данных DXGI. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Описывает, какие ресурсы поддерживаются текущим драйвером графики для заданного формата. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Сведения об ограничениях виртуального адресного пространства GPU адаптера, включая максимальное число битов на ресурс и на процесс. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Описывает уровни качества изображения для заданного формата и количества выборок. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Указывает уровень поддержки для сеансов защищенных ресурсов. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPE_COUNT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_type_count). Указывает число типов сеансов защищенных ресурсов. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_TYPES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_types). Указывает список типов сеансов защищенных ресурсов. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Указывает уровень поддержки, предоставляемый адаптером для метакоммандс. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Передайте эту структуру в [**чеккфеатуресуппорт**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) для проверки поддержки версии корневой сигнатуры. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Указывает уровень поддержки сериализации кучи. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Описывает уровень кэширования шейдера, поддерживаемый в текущем графическом драйвере. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Содержит поддерживаемую модель шейдера. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Описывает дескриптор GPU. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Описывает объект состояния графического конвейера. |
| [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc). Описывает кучу. |
| [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties). Описывает свойства кучи. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Описывает буфер индексов для просмотра. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Описывает косвенный аргумент (косвенный параметр) для использования с сигнатурой команды. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc). Описывает один элемент для этапа входного ассемблера графического конвейера. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Описывает данные входного буфера для этапа ассемблера ввода. |
| [**D3D12_MEMCPY_DEST**](/windows/win32/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Описывает назначение операции копирования в памяти. |
| [**D3D12_META_COMMAND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Описывает команду meta. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Описывает параметр для команды meta. |
| [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Описывает мозаичную структуру мозаичного ресурса с помощью MIP-карты. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Описывает поток состояния конвейера. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Описывает объем размещенного подресурса, включая смещение и D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Описание флагов для сеанса защищенного ресурса на адаптер. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Запрос сведений о графических операциях конвейера между вызовами [**бегинкуери**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) и [**ендкуери**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery). |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Описывает данные запроса для выходного потока. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Описывает назначение кучи запросов. Куча запроса содержит массив отдельных запросов. |
| [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range). Описывает диапазон памяти. |
| [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64). Описывает диапазон памяти в 64-битном адресном пространстве. |
| [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Описывает состояние средства отображения программной прорисовки. |
| [**D3D12_RAYTRACING_AABB**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Представляет ограничивающий прямоугольник с согласованием по осям (ААББ), используемый в качестве геометрического объекта райтраЦинг. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Описывает требования к пространству для структуры ускорения после сжатия. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Описывает пространство, используемое в данный момент структурой ускорения. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Описание данных после сборки, создаваемых из структуры ускорения. Используйте эту структуру в вызовах [**емитрайтраЦингакцелератионструктурепостбуилдинфо**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) и [**буилдрайтраЦингакцелератионструктуре**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Описывает размер и расположение сериализованной структуры ускорения и заголовка |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Описывает требования к пространству для декодирования структуры ускорения в форму, которая может быть наглядна средствами. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Представляет сведения о предсборке для структуры ускорения райтраЦинг. Получите экземпляр этого структуру, вызвав [**жетрайтраЦингакцелератионструктурепребуилдинфо**](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Структура представления ресурсов шейдера (SRV) для хранения структуры ускорения райтраЦинг. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Описывает набор ограничивающих прямоугольников с согласованием по осям, которые используются в структуре [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) для предоставления входных данных операции построения структуры ускорения райтраЦинг. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Описывает набор геометрии, который используется в структуре [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) для предоставления входных данных операции построения структуры ускорения райтраЦинг. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Описывает набор треугольников, используемых в качестве райтраЦинг Geometry. Геометрия, на которую указывает эта структура, всегда находится в виде списка треугольников, индексируется или не индексируется. Ленты треугольников не поддерживаются. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Описывает экземпляр структуры ускорения райтраЦинг, используемый в памяти GPU во время процесса сборки структуры ускорения. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Подобъект State, представляющий конфигурацию конвейера райтраЦинг. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config1). Подобъект State, представляющий конфигурацию конвейера райтраЦинг с флагами. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Подобъект State, представляющий конфигурацию шейдера. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT объявляется как RECT. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Описывает доступ к ресурсам, запрашиваемым приложением при переходе на этап отрисовки. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Описывает пустое значение, в которое должны быть удалены ресурсы в начале этапа подготовки к просмотру. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Описывает привязку (фиксированную на время прохода отрисовки) в представление трафарета глубины (DSV), а также его начальные и конечные характеристики доступа. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Описывает доступ к ресурсам, запрашиваемым приложением при переходе с этапа прорисовки. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Описывает ресурс для разрешения при завершении прохода визуализации. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Описывает подресурсы, участвующие в разрешении при завершении этапа подготовки к просмотру. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Описывает привязки (фиксированные на время прохода отрисовки) в одно или несколько представлений целевого объекта отрисовки (RTVs), а также их начальные и конечные характеристики доступа. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Описывает состояние смешения для целевого объекта прорисовки. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Описывает подресурсы из ресурса, доступ к которому можно получить с помощью представления целевого объекта визуализации. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Описывает переход между использованием двух различных ресурсов, которые имеют сопоставления в одной куче. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Описывает параметры, необходимые для выделения ресурсов. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Описывает параметры, необходимые для выделения ресурсов, включая смещение. |
| [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier). Описывает барьер ресурсов (переход от использования ресурсов). |
| [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc). Описывает ресурс, например текстуру. Эта структура широко используется. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Описывает переход подресурсов между различными использованиями. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Представляет ресурс, в котором все доступ к UAV должны быть завершены, прежде чем начнется любой будущий доступ к UAV. |
| [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants). Описывает константы, встроенные в корневую подпись, которые отображаются в шейдере в виде одного буфера констант. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor). Описание встроенных дескрипторов в корневой сигнатуре версии 1,0, отображаемой в шейдерах. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Описание встроенных дескрипторов в корневой сигнатуре версии 1,1, отображаемой в шейдерах. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Описывает макет корневой сигнатуры 1,0 таблицы дескрипторов в виде коллекции диапазонов дескрипторов, которые отображаются один за другим в куче дескрипторов. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Описывает макет корневой сигнатуры 1,1 таблицы дескрипторов в виде коллекции диапазонов дескрипторов, которые отображаются один за другим в куче дескрипторов. |
| [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter). Описание слота корневой сигнатуры версии 1,0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1). Описание слота корневой сигнатуры версии 1,1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Описывает макет корневой сигнатуры версии 1,0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Описывает макет корневой сигнатуры версии 1,1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array). Заключает в оболочку массив форматов целевого объекта прорисовки. |
| [**D3D12_SAMPLE_POSITION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sample_position). Описывает пример позиции в виде подпикселя для использования с программируемыми положениями образцов. |
| [**D3D12_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_sampler_desc). Описывает состояние образца. |
| [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Описывает данные шейдера. |
| [**D3D12_SHADER_CACHE_SESSION_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_cache_session_desc). Описывает сеанс кэша шейдера. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Описывает представление «шейдер-ресурс». |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Описывает элемент вершины в буфере вершин в выходном слоте. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Описывает статический образец. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Описывает потоковый буфер вывода. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Описывает потоковый выходной буфер. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_data). Описывает данные о подресурсе. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Описывает формат, ширину, высоту, глубину и шаг строки вложенного ресурса в родительском ресурсе. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_info). Описывает данные о подресурсе. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Описывает диапазон памяти подресурсов. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Описывает объем мозаичных подресурсов. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Описывает подресурсы из массива одномерной текстуры для использования в представлении трафарета глубины. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Описывает подресурсы из массива одномерной текстуры для использования в представлении целевого объекта визуализации. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Описывает подресурсы из массива одномерной текстуры для использования в представлении ресурсов шейдера. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Описывает массив неупорядоченных ресурсов текстуры одномерного доступа. |
| [**D3D12_TEX1D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Описывает вложенный ресурс из текстуры 1D, доступной для представления трафарета глубины. |
| [**D3D12_TEX1D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Описывает подресурс из одномерной текстуры для использования в представлении целевого объекта визуализации. |
| [**D3D12_TEX1D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Указывает подресурс из текстуры 1D для использования в представлении ресурсов шейдера. |
| [**D3D12_TEX1D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Описывает неупорядоченный ресурс текстуры одномерного доступа. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Описывает подресурсы из массива двумерных текстур, доступных в представлении трафарета глубины. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Описывает подресурсы из массива двумерных текстур для использования в представлении целевого объекта визуализации. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Описывает подресурсы из массива двумерных текстур для использования в представлении ресурсов шейдера. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Описывает массив неупорядоченных ресурсов двухмерной текстуры с доступом. |
| [**D3D12_TEX2D_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Описывает вложенный ресурс из двухмерной текстуры, доступной для представления трафарета глубины. |
| [**D3D12_TEX2D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Описывает подресурс из двухмерной текстуры для использования в представлении целевого объекта визуализации. |
| [**D3D12_TEX2D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Описывает подресурс из двухмерной текстуры для использования в представлении ресурсов шейдера. |
| [**D3D12_TEX2D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Описывает неупорядоченный ресурс двухмерной текстуры. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Описывает подресурсы из массива двумерных текстур с несколькими примерами для представления набора элементов глубины. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Описывает подресурсы из массива из нескольких выборок 2D-текстур для использования в представлении целевого объекта визуализации. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Описывает подресурсы из массива из нескольких выборок 2D-текстур для использования в представлении "шейдер — представление ресурсов". |
| [**D3D12_TEX2DMS_DSV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Описывает вложенный ресурс из множественной выборки двухмерной текстуры, доступной для представления набора элементов глубины. |
| [**D3D12_TEX2DMS_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Описывает подресурс из множественной выборки 2D-текстуры для использования в представлении целевого объекта визуализации. |
| [**D3D12_TEX2DMS_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Описывает подресурсы из множественной выборки 2D-текстуры для использования в представлении "шейдер — представление ресурсов". |
| [**D3D12_TEX3D_RTV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Описывает подресурсы из трехмерной текстуры для использования в представлении целевого объекта визуализации. |
| [**D3D12_TEX3D_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Описывает подресурсы из трехмерной текстуры для использования в представлении ресурсов шейдера. |
| [**D3D12_TEX3D_UAV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Описывает неупорядоченный ресурс текстуры с доступом. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Описывает подресурсы из массива текстур Куба для использования в представлении ресурсов шейдера. |
| [**D3D12_TEXCUBE_SRV**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texcube_srv). Описывает подресурс из текстуры Куба для использования в представлении ресурсов шейдера. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Описывает часть текстуры, предназначенную для копирования текстур. |
| [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size). Описывает размер мозаичного региона. |
| [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape). Описывает форму плитки, указывая ее размеры. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Описывает координаты мозаичного ресурса. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Описывает подресурсы из ресурса, доступ к которому осуществляется с помощью представления неупорядоченного доступа. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Описывает представление буфера вершин. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Представление удаленных данных расширенных данных (НАПРАВЛЯТЬ) устройством с управлением версиями, чтобы отладчики и расширения отладчика могли получать доступ к данным НАПРАВЛЯТЬ. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Содержит любую версию описания корневой подписи и предназначена для использования с функциями сериализации и десериализации. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instance_location). Указывает окно просмотра/набор элементов и целевой объект отрисовки, связанный с экземпляром представления. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Указывает параметры, используемые при настройке создания экземпляров представления. |
| [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport). Описывает размеры окна просмотра. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Указывает немедленное значение и адрес назначения, написанный с помощью [**ID3D12CommandList2:: вритебуффериммедиате**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2). |

## <a name="related-topics"></a>Связанные темы

* [Справочник по основным](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)