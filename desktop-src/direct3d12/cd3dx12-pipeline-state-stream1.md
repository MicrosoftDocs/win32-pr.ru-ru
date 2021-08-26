---
title: Структура CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
description: Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См. раздел [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) и [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219b198ae5c2da6d6e74db933d4c26771aa63975
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812541"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>Структура CD3DX12_PIPELINE_STATE_STREAM1

Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См. раздел [D3D12_GRAPHICS_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) и [D3D12_COMPUTE_PIPELINE_STATE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

CD3DX12_PIPELINE_STATE_STREAM1 поддерживает Windows 10 Fall Creators Update с новыми функциями, такими как создание экземпляров для просмотра.

См. статью [CD3DX12_PIPELINE_STATE_STREAM2](cd3dx12-pipeline-state-stream2.md) for OS Build 19041 + (где есть конвейер шейдера сетки).

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12_PIPELINE_STATE_STREAM1.

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1 (const D3D12_GRAPHICS_PIPELINE_STATE_DESC& DESC)**
</dt> <dd>

Создает новый экземпляр CD3DX12_PIPELINE_STATE_STREAM1, инициализируемый значениями, скопированными из структуры **CD3DX12_PIPELINE_STATE_STREAM1** .

</dd> <dt>

**CD3DX12_PIPELINE_STATE_STREAM1 (const D3D12_COMPUTE_PIPELINE_STATE_DESC& DESC)**
</dt> <dd>

Создает новый экземпляр CD3DX12_PIPELINE_STATE_STREAM1, инициализируемый значениями, скопированными из структуры **CD3DX12_PIPELINE_STATE_STREAM1** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Возвращает содержимое объекта CD3DX12_PIPELINE_STATE_STREAM1 в виде структуры D3D12_GRAPHICS_PIPELINE_STATE_DESC по значению. Обратите внимание, что D3D12_GRAPHICS_PIPELINE_STATE_DESC не включает элемент **CS** , поэтому при преобразовании это значение будет потеряно.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Возвращает содержимое объекта CD3DX12_PIPELINE_STATE_STREAM1 в виде структуры D3D12_COMPUTE_PIPELINE_STATE_DESC по значению. Обратите внимание, что D3D12_COMPUTE_PIPELINE_STATE_DESC не содержит членов  **инпутлайаут**, **ибстрипкутвалуе**, **примитиветопологитипе**, **VS**, **GS**, **стреамаутпут**, **HS**,  **DS**, **блендстате**, **депсстенЦилстате** **, DSVFormat** **, RasterizerState** или **NumRootSignature** , **поэтому** эти значения теряются при преобразовании. 

</dd> <dt>

**Флаги**
</dt> <dd>

Описывает флаги состояния конвейера, которые управляют такими функциями, как "Отладка инструмента".

</dd> <dt>

**нодемаск**
</dt> <dd>

Описывает маску узла состояния конвейера, которая используется для указания узлов (физических адаптеров устройства), к которым применяется PSO в сценариях с несколькими адаптерами. Каждый бит маски соответствует одному узлу. Для сценариев с одним адаптером присвойте этому параметру значение 0.

</dd> <dt>

**прутсигнатуре**
</dt> <dd>

Описывает корневую подпись.

</dd> <dt>

**инпутлайаут**
</dt> <dd>

Описывает формат входного буфера для этапа ассемблера ввода

</dd> <dt>

**ибстрипкутвалуе**
</dt> <dd>

Описывает особое значение индекса входного буфера, которое указывает на вырезание (прекращение) при использовании топологии ленты треугольника.

</dd> <dt>

**примитиветопологитипе**
</dt> <dd>

Описывает топологию примитива и ее порядок.

</dd> <dt>

**ЛИНЕЙЧАТ**
</dt> <dd>

Описывает шейдер вершин.

</dd> <dt>

**GS**
</dt> <dd>

Описывает шейдер Geometry.

</dd> <dt>

**стреамаутпут**
</dt> <dd>

Описывает потоковый выходной буфер.

</dd> <dt>

**HS**
</dt> <dd>

Описывает шейдер поверхности.

</dd> <dt>

**DS**
</dt> <dd>

Описывает Шейдер доменов.

</dd> <dt>

**PS**
</dt> <dd>

Описывает шейдер пикселей.

</dd> <dt>

**CS**
</dt> <dd>

Описывает вычисление шейдера.

</dd> <dt>

**блендстате**
</dt> <dd>

Описывает состояние смешения.

</dd> <dt>

**депсстенЦилстате**
</dt> <dd>

Описывает состояние шаблона глубины.

</dd> <dt>

**дсвформат**
</dt> <dd>

Описывает формат трафарета глубины.

</dd> <dt>

**растеризерстате**
</dt> <dd>

Описывает состояние средства программной прорисовки.

</dd> <dt>

**ртвформатс**
</dt> <dd>

Описывает форматы целевого объекта прорисовки.

</dd> <dt>

**сампледеск**
</dt> <dd>

Описывает количество образцов и качество.

</dd> <dt>

**самплемаск**
</dt> <dd>

Описывает образец маски, используемый в состоянии Blend.

</dd> <dt>

**качедпсо**
</dt> <dd>

Описывает кэшированный PSO.

</dd> </dl>

## <a name="remarks"></a>Remarks

[CD3DX12_PIPELINE_STATE_STREAM](cd3dx12-pipeline-state-stream.md) поддерживает Windows 10 Fall Creators Update, но не поддерживает типы подобъектов, добавленные в обновление для создателей Windows 10, например, для создания экземпляров представления. Для поддержки новых типов подобъектов используйте вместо него **CD3DX12_PIPELINE_STATE_STREAM1** .

Доступные переменные-члены этой структуры — это все определения типов шаблона [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](/windows/win32/direct3d12/cd3dx12-pipeline-state-stream-subobject) , которые объединяют данные маркера типа и подобъекта в один объект, подходящий для описания потока.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
* [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md)
* [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
* [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
