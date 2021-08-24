---
title: Структура CD3DX12_PIPELINE_STATE_STREAM2 (D3dx12. h)
description: Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс.
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM2
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM2
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: 18b662217f5e2a59c7925e0f401a9288ea710e8a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812334"
---
# <a name="cd3dx12_pipeline_state_stream2-structure"></a>Структура CD3DX12_PIPELINE_STATE_STREAM2

Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См. раздел [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) и [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

**CD3DX12_PIPELINE_STATE_STREAM2** поддерживает OS Build 19041 + (где есть конвейер построителя сети).

## <a name="syntax"></a>Синтаксис

```cpp
struct CD3DX12_PIPELINE_STATE_STREAM2
{
    CD3DX12_PIPELINE_STATE_STREAM2();
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS Flags;
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK NodeMask;
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE pRootSignature;
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT InputLayout;
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE IBStripCutValue;
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY PrimitiveTopologyType;
    CD3DX12_PIPELINE_STATE_STREAM_VS VS;
    CD3DX12_PIPELINE_STATE_STREAM_GS GS;
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT StreamOutput;
    CD3DX12_PIPELINE_STATE_STREAM_HS HS;
    CD3DX12_PIPELINE_STATE_STREAM_DS DS;
    CD3DX12_PIPELINE_STATE_STREAM_PS PS;
    CD3DX12_PIPELINE_STATE_STREAM_AS AS;
    CD3DX12_PIPELINE_STATE_STREAM_MS MS;
    CD3DX12_PIPELINE_STATE_STREAM_CS CS;
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC BlendState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 DepthStencilState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT DSVFormat;
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER RasterizerState;
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC SampleDesc;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK SampleMask;
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO CachedPSO;
    CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING ViewInstancingDesc;
    D3D12_GRAPHICS_PIPELINE_STATE_DESC GraphicsDescV0() const noexcept;
    D3D12_COMPUTE_PIPELINE_STATE_DESC ComputeDescV0() const noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_PIPELINE_STATE_STREAM2`

Конструктор по умолчанию. Создает новый, неинициализированный экземпляр **CD3DX12_PIPELINE_STATE_STREAM2**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_PIPELINE_STATE_STREAM2** , инициализируемый с помощью содержимого структуры [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .

Затем необходимо установить сетку и шейдеры усиления вручную, так как они не имеют представления в **D3D12_GRAPHICS_PIPELINE_STATE_DESC**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_PIPELINE_STATE_STREAM2** , инициализируемый с помощью содержимого структуры [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) .

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_PIPELINE_STATE_STREAM2** , инициализируемый с помощью содержимого структуры [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .

`Flags`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_FLAGS](cd3dx12-pipeline-state-stream-flags.md)**

Флаги (например, чтобы указать, что состояние конвейера должно быть скомпилировано с дополнительными сведениями для помощи в отладке).

`NodeMask`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK](cd3dx12-pipeline-state-stream-node-mask.md)**

Описывает маску узла состояния конвейера, которая используется для указания узлов (физических адаптеров устройства), к которым применяется PSO в сценариях с несколькими адаптерами. Каждый бит маски соответствует одному узлу. Для сценариев с одним адаптером используйте значение 0.

`pRootSignature`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE](cd3dx12-pipeline-state-stream-root-signature.md)**

Описывает корневую подпись.

`InputLayout`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT](cd3dx12-pipeline-state-stream-input-layout.md)**

Описывает формат входного буфера для этапа ассемблера ввода

`IBStripCutValue`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)**

Описывает особое значение индекса входного буфера, которое указывает на вырезание (прекращение) при использовании топологии ленты треугольника.

`PrimitiveTopologyType`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY](cd3dx12-pipeline-state-stream-primitive-topology.md)**

Описывает топологию примитива и ее порядок.

`VS`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_VS](cd3dx12-pipeline-state-stream-vs.md)**

Описывает шейдер вершин.

`GS`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_GS](cd3dx12-pipeline-state-stream-gs.md)**

Описывает шейдер Geometry.

`StreamOutput`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT](cd3dx12-pipeline-state-stream-stream-output.md)**

Описывает потоковый выходной буфер.

`HS`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_HS](cd3dx12-pipeline-state-stream-hs.md)**

Описывает шейдер поверхности.

`DS`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_DS](cd3dx12-pipeline-state-stream-ds.md)**

Описывает Шейдер доменов.

`PS`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_PS](cd3dx12-pipeline-state-stream-ps.md)**

Описывает шейдер пикселей.

`AS`

Тип: **CD3DX12_PIPELINE_STATE_STREAM_AS**

Описывает шейдер усиления.

`MS`

Тип: **CD3DX12_PIPELINE_STATE_STREAM_MS**

Описывает шейдер сетки.

`CS`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_CS](cd3dx12-pipeline-state-stream-cs.md)**

Описывает вычисление шейдера.

`BlendState`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC](cd3dx12-pipeline-state-stream-blend-desc.md)**

Описывает состояние смешения.

`DepthStencilState`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1](cd3dx12-pipeline-state-stream-depth-stencil1.md)**

Описывает состояние шаблона глубины.

`DSVFormat`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT](cd3dx12-pipeline-state-stream-depth-stencil-format.md)**

Описывает формат трафарета глубины.

`RasterizerState`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER](cd3dx12-pipeline-state-stream-rasterizer.md)**

Описывает состояние средства программной прорисовки.

`RTVFormats`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS](cd3dx12-pipeline-state-stream-render-target-formats.md)**

Описывает форматы целевого объекта прорисовки.

`SampleDesc`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC](cd3dx12-pipeline-state-stream-sample-desc.md)**

Описывает количество образцов и качество.

`SampleMask`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK](cd3dx12-pipeline-state-stream-sample-mask.md)**

Описывает образец маски, используемый в состоянии Blend.

`CachedPSO`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO](cd3dx12-pipeline-state-stream-cached-pso.md)**

Описывает кэшированный PSO.

`ViewInstancingDesc`

Тип: **[CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING](cd3dx12-pipeline-state-stream-view-instancing.md)**

Описывает конфигурацию создания экземпляров представления.

`GraphicsDescV0`

Возвращает [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc).

Возвращает содержимое объекта **CD3DX12_PIPELINE_STATE_STREAM2** в виде структуры **D3D12_GRAPHICS_PIPELINE_STATE_DESC** по значению. **D3D12_GRAPHICS_PIPELINE_STATE_DESC** не содержит элемент *CS* , поэтому в преобразовании это значение будет потеряно.

`ComputeDescV0`

Возвращает [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

Возвращает содержимое объекта **CD3DX12_PIPELINE_STATE_STREAM2** в виде структуры **D3D12_COMPUTE_PIPELINE_STATE_DESC** по значению. **D3D12_COMPUTE_PIPELINE_STATE_DESC** не включает элементы *инпутлайаут*, *ибстрипкутвалуе*, *примитиветопологитипе*, *VS*, *GS*, *стреамаутпут*, *HS*, *DS*, *PS*, *блендстате*, *депсстенЦилстате*, *DSVFormat*, *RasterizerState*, *NumRootSignature*, *RTVFormats*, *SampleDesc* и *SampleMask*, поэтому эти значения теряются при преобразовании.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
