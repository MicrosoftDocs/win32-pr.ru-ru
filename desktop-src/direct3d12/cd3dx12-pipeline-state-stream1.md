---
title: Структура CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
description: Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См \_ . раздел State D3D12 графического \_ конвейера \_ \_ DESC and D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC. | Структура CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
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
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713517"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>\_ \_ Структура STREAM1 состояния КОНВЕЙЕРа CD3DX12 \_

Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См. раздел [**\_ State D3D12 графического \_ конвейера \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

\_Состояние конвейера CD3DX12 \_ \_ STREAM1 поддерживает обновление Windows 10 Creators Update с новыми функциями, такими как создание экземпляров для просмотра.

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

**\_STREAM1 состояния конвейера CD3DX12 \_ \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ состояния конвейера \_ \_ STREAM1.

</dd> <dt>

**\_Состояние конвейера CD3DX12 \_ \_ STREAM1 (const D3D12 \_ графическое \_ конвейер \_ State \_ DESC& DESC)**
</dt> <dd>

Создает новый экземпляр \_ состояния конвейера CD3DX12 \_ \_ STREAM1, который инициализируется значениями, скопированными из структуры **\_ \_ \_ STREAM1 состояния конвейера CD3DX12** .

</dd> <dt>

**CD3DX12 \_ состояние конвейера \_ \_ STREAM1 (const D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC& DESC)**
</dt> <dd>

Создает новый экземпляр \_ состояния конвейера CD3DX12 \_ \_ STREAM1, который инициализируется значениями, скопированными из структуры **\_ \_ \_ STREAM1 состояния конвейера CD3DX12** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Возвращает содержимое \_ объекта STREAM1 состояния конвейера CD3DX12 в \_ \_ виде \_ графического \_ конвейера D3D12 \_ \_ . Структура по значению. Обратите внимание, что D3D12 \_ графического \_ конвейера \_ \_ со значением DESC не включает элемент **CS** , поэтому при преобразовании это значение будет потеряно.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Возвращает содержимое \_ \_ объекта STREAM1 состояния конвейера CD3DX12 \_ как D3D12 \_ Вычисление \_ состояния конвейера \_ \_ по значению. Обратите внимание, что D3D12 \_ Вычисление \_ состояния конвейера не \_ \_ включает элементы **инпутлайаут**, **ибстрипкутвалуе**, **примитиветопологитипе**, **VS**, **GS**, **стреамаутпут**, **HS**, **DS**, **PS**, **блендстате,** **депсстенЦилстате**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** или **SampleMask** , поэтому эти значения теряются при преобразовании.

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

## <a name="remarks"></a>Комментарии

[**CD3DX12 \_ \_ \_ Поток состояния конвейера**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) поддерживает обновление для дизайнеров Windows 10, но не поддерживает типы подобъектов, добавленные в обновление Windows 10 Creators Update, например для создания экземпляров представления. Для поддержки новых типов подобъектов используйте \_ \_ вместо него состояние конвейера CD3DX12 \_ STREAM1.

Доступные переменные-члены этой структуры являются typedef \_ \_ \_ шаблона подобъекта потока состояния конвейера CD3DX12 \_ , который объединяет данные маркера типа и подобъекта в один объект, подходящий для описания потока.

Эти определения типов:

<dl> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Поток состояния конвейера CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[**D3D12 \_ графика \_ состояния графического конвейера \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**\_DESC для \_ состояния конвейера D3D12 COMPUTE \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





