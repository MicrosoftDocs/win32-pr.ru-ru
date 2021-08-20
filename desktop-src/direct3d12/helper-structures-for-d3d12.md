---
title: Вспомогательные структуры для Direct3D 12
description: Эти вспомогательные структуры помогают инициализировать многие из структур Direct3D 12. Они объявляются в `d3dx12.h` .
ms.assetid: 822CACCE-4A45-4104-91BD-4968A657662E
keywords:
- Вспомогательные структуры
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 07/28/2021
ms.openlocfilehash: 16dfa0349a815a07db810d67c21747cb767f7c39
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812364"
---
# <a name="helper-structures-for-direct3d-12"></a>Вспомогательные структуры для Direct3D 12

Эти вспомогательные структуры помогают инициализировать многие из структур Direct3D 12. Они объявляются в `d3dx12.h` .

`d3dx12.h` доступен отдельно от заголовков Direct3D 12. Вы можете скачать `d3dx12.h` из [вспомогательной библиотеки D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**CD3DX12_BLEND_DESC**](cd3dx12-blend-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc) . |
| [**CD3DX12_BOX**](cd3dx12-box.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box) . |
| [**CD3DX12_CLEAR_VALUE**](cd3dx12-clear-value.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value) . |
| [**CD3DX12_CPU_DESCRIPTOR_HANDLE**](cd3dx12-cpu-descriptor-handle.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) . |
| [**CD3DX12_DEFAULT**](cd3dx12-default.md) | Передает **D3D12_DEFAULT** в конструктор для каждой вспомогательной структуры. Эта структура просто используется в качестве механизма установки параметров по умолчанию для других вспомогательных структур. |
| [**CD3DX12_DEPTH_STENCIL_DESC**](cd3dx12-depth-stencil-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) . |
| [**CD3DX12_DEPTH_STENCIL_DESC1**](cd3dx12-depth-stencil-desc1.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) . |
| [**CD3DX12_DESCRIPTOR_RANGE**](cd3dx12-descriptor-range.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range) . |
| [**CD3DX12_DESCRIPTOR_RANGE1**](cd3dx12-descriptor-range1.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1) . |
| [**CD3DX12_DXIL_LIBRARY_SUBOBJECT**](cd3dx12-dxil-library-subobject.md) | Вспомогательный класс для создания подобъекта состояния библиотеки ДКСИЛ. |
| [**CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**](cd3dx12-dxil-subobject-to-exports-association.md) | Вспомогательный класс для создания подобъекта состояния взаимосвязи ДКСИЛ-to-EXPORTS. |
| [**CD3DX12_EXISTING_COLLECTION_SUBOBJECT**](cd3dx12-existing-collection-subobject.md) | Вспомогательный класс для создания существующего вложенного объекта состояния коллекции. |
| [**CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-global-root-signature-subobject.md) | Вспомогательный класс для создания глобального корневого состояния подписи субожект. |
| [**CD3DX12_GPU_DESCRIPTOR_HANDLE**](cd3dx12-gpu-descriptor-handle.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) . |
| [**CD3DX12_HEAP_DESC**](cd3dx12-heap-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc) . |
| [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) . |
| [**CD3DX12_HIT_GROUP_SUBOBJECT**](cd3dx12-hit-group-subobject.md) | Вспомогательный класс для создания подобъекта состояния группы попаданий. |
| [**CD3DX12_NODE_MASK_SUBOBJECT**](cd3dx12-node-mask-subobject.md) | Вспомогательный класс для создания подобъекта State, определяющего узлы GPU, к которым применяется объект состояния. |
| [**CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-local-root-signature-subobject.md) | Вспомогательный класс для создания локального корневого состояния подписи субожект. |
| [**CD3DX12_PACKED_MIP_INFO**](cd3dx12-packed-mip-info.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info) . |
| [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md) | Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См. раздел [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) и [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM1**](cd3dx12-pipeline-state-stream1.md) | Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См. раздел [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) и [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM2**](cd3dx12-pipeline-state-stream2.md) | Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. |
| [**CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) | Вспомогательная структура, используемая для описания описания смешения в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO**](cd3dx12-pipeline-state-stream-cached-pso.md) | Вспомогательная структура, используемая для описания кэшированного PSO в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CS**](cd3dx12-pipeline-state-stream-cs.md) | Вспомогательная структура, используемая для описания шейдера вычислений в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md) | Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md) | Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md) | Вспомогательная структура, используемая для описания формата трафарета глубины в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DS**](cd3dx12-pipeline-state-stream-ds.md) | Вспомогательная структура, используемая для описания шейдера домена как одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_FLAGS**](cd3dx12-pipeline-state-stream-flags.md) | Вспомогательная структура, используемая для описания флагов состояния конвейера в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_GS**](cd3dx12-pipeline-state-stream-gs.md) | Вспомогательная структура, используемая для описания шейдера Geometry в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_HS**](cd3dx12-pipeline-state-stream-hs.md) | Вспомогательная структура, используемая для описания шейдера поверхности в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md) | Вспомогательная структура, используемая для описания значения вырезания полосы буфера индексов в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md) | Вспомогательная структура, используемая для описания входного макета в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK**](cd3dx12-pipeline-state-stream-node-mask.md) | Вспомогательная структура, используемая для описания маски узла в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER**](cd3dx12-pipeline-state-stream-parse-helper.md) | Создает внутренний объект CD3DX12_PIPELINE_STATE_STREAM из сведений о подобъекте, переданных в соответствующие функции элементов. Эта структура реализует интерфейс [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) . |
| [**CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY**](cd3dx12-pipeline-state-stream-primitive-topology.md) | Вспомогательная структура, используемая для описания топологии примитивов в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PS**](cd3dx12-pipeline-state-stream-ps.md) | Вспомогательная структура, используемая для описания шейдера пикселей в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) | Вспомогательная структура, используемая для описания описания средства развертки в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS**](cd3dx12-pipeline-state-stream-render-target-formats.md) | Вспомогательная структура, используемая для описания форматов целевого объекта отрисовки в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE**](cd3dx12-pipeline-state-stream-root-signature.md) | Вспомогательная структура, используемая для описания корневой подписи в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC**](cd3dx12-pipeline-state-stream-sample-desc.md) | Вспомогательная структура, используемая для описания образца описания как одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK**](cd3dx12-pipeline-state-stream-sample-mask.md) | Вспомогательная структура, используемая для описания образца маски в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md) | Вспомогательная структура, используемая для описания выходного описания потока в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) | Шаблонная вспомогательная структура, используемая для инкапсуляции типа подобъекта и пар данных подобъектов в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING**](cd3dx12-pipeline-state-stream-view-instancing.md) | Вспомогательная структура, используемая для создания оболочки структуры [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) . Позволяет шейдерам отображаться в нескольких представлениях с одним вызовом Draw; полезно для использования с стерео или кубической карты. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VS**](cd3dx12-pipeline-state-stream-vs.md) | Вспомогательная структура, используемая для описания шейдер вершин в виде одного объекта, подходящего для описания потока. |
| [**CD3DX12_RANGE**](cd3dx12-range.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range) . |
| [**CD3DX12_RANGE_UINT64**](cd3dx12-range-uint64.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64) . |
| [**CD3DX12_RASTERIZER_DESC**](cd3dx12-rasterizer-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) . |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**](cd3dx12-raytracing-pipeline-config-subobject.md) | Вспомогательный класс для создания подобъекта состояния конфигурации конвейера райтраЦинг. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**](cd3dx12-raytracing-pipeline-config1-subobject.md) | Вспомогательный класс для создания подобъекта состояния конфигурации конвейера райтраЦинг с флагами. |
| [**CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**](cd3dx12-raytracing-shader-config-subobject.md) | Вспомогательный класс для создания подобъекта состояния конфигурации райтраЦинг Shader. |
| [**CD3DX12_RECT**](cd3dx12-rect.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RECT**](d3d12-rect.md) . |
| [**CD3DX12_RESOURCE_ALLOCATION_INFO**](cd3dx12-resource-allocation-info.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) . |
| [**CD3DX12_RESOURCE_BARRIER**](cd3dx12-resource-barrier.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier) . |
| [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc) . |
| [**CD3DX12_RESOURCE_DESC1**](cd3dx12-resource-desc1.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) . |
| [**CD3DX12_ROOT_CONSTANTS**](cd3dx12-root-constants.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants) . |
| [**CD3DX12_ROOT_DESCRIPTOR**](cd3dx12-root-descriptor.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor) . |
| [**CD3DX12_ROOT_DESCRIPTOR1**](cd3dx12-root-descriptor1.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1) . |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE**](cd3dx12-root-descriptor-table.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) . |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE1**](cd3dx12-root-descriptor-table1.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) . |
| [**CD3DX12_ROOT_PARAMETER**](cd3dx12-root-parameter.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter) . |
| [**CD3DX12_ROOT_PARAMETER1**](cd3dx12-root-parameter1.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1) . |
| [**CD3DX12_ROOT_SIGNATURE_DESC**](cd3dx12-root-signature-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) . |
| [**CD3DX12_RT_FORMAT_ARRAY**](cd3dx12-rt-format-array.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array) . |
| [**CD3DX12_SHADER_BYTECODE**](cd3dx12-shader-bytecode.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) . |
| [**CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**](cd3dx12-state-object-config-subobject.md) | Вспомогательный класс для создания подобъекта, определяющего общие свойства объекта State. |
| [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) | Центральный класс вспомогательных функций создания объектов состояния D3DX12, которые представляют собой вспомогательные классы для создания объектов состояния из произвольного набора подобъектов. |
| [**CD3DX12_STATIC_SAMPLER_DESC**](cd3dx12-static-sampler-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) . |
| [**CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**](cd3dx12-subobject-to-exports-association-subobject.md) | Вспомогательный класс для создания подобъекта состояния связи "один объект в-экспортируемый". |
| [**CD3DX12_SUBRESOURCE_FOOTPRINT**](cd3dx12-subresource-footprint.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) . |
| [**CD3DX12_SUBRESOURCE_RANGE_UINT64**](cd3dx12-subresource-range-uint64.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) . |
| [**CD3DX12_SUBRESOURCE_TILING**](cd3dx12-subresource-tiling.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling) . |
| [**CD3DX12_TEXTURE_COPY_LOCATION**](cd3dx12-texture-copy-location.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location) . |
| [**CD3DX12_TILE_REGION_SIZE**](cd3dx12-tile-region-size.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) . |
| [**CD3DX12_TILE_SHAPE**](cd3dx12-tile-shape.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) . |
| [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) . |
| [**CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC**](cd3dx12-versioned-root-signature-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) . |
| [**CD3DX12_VIEW_INSTANCING_DESC**](cd3dx12-view-instancing-desc.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) . |
| [**CD3DX12_VIEWPORT**](cd3dx12-viewport.md) | Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport) . |
| [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) | Для [шейдеров сетки и усиления](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)можно использовать данные из [еффектпипелинестатедескриптион](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription)с **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, чтобы обеспечить все состояние. |

## <a name="related-topics"></a>Связанные темы

* [Вспомогательные структуры и функции для D3D12](helper-structures-and-functions-for-d3d12.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)
