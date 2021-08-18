---
title: Структура CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
description: Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См \_ . раздел State D3D12 графического \_ конвейера \_ \_ DESC and D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC. | Структура CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e45c46c39a21aaeb53a2980fa3c082947e92cd5bb4ab3eccbbb225001a6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733986"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>\_ \_ Структура потока состояния КОНВЕЙЕРа CD3DX12 \_

Вспомогательная структура для создания графики и работы с ними, а также для вычислений конвейеров через Объединенный интерфейс. См. раздел [**\_ State D3D12 графического \_ конвейера \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

\_поток состояния конвейера CD3DX12 \_ \_ поддерживает Windows 10 Creators Update и более поздних версий, но не поддерживает новые функции обновления, такие как создание экземпляров. Для поддержки функций обновления "создатели обновлений" используйте вместо этого [**CD3DX12 \_ конвейер \_ состояния \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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

**\_Поток состояния конвейера CD3DX12 \_ \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ .

</dd> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ (const D3D12 \_ графическое \_ конвейер \_ State \_ DESC& DESC)**
</dt> <dd>

Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ , инициализируемый значениями, скопированными из структуры **\_ \_ \_ потока состояния конвейера CD3DX12** .

</dd> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ (const D3D12 \_ COMPUTE \_ конвейер \_ State \_ DESC& DESC)**
</dt> <dd>

Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ , инициализируемый значениями, скопированными из структуры **\_ \_ \_ потока состояния конвейера CD3DX12** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Возвращает содержимое \_ объекта потока состояния конвейера CD3DX12 в \_ \_ виде \_ графического \_ конвейера D3D12 \_ состояние \_ структуры по значению. Обратите внимание, что D3D12 \_ графического \_ конвейера \_ \_ со значением DESC не включает элемент **CS** , поэтому при преобразовании это значение будет потеряно.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Возвращает содержимое \_ \_ объекта потока состояния конвейера CD3DX12 \_ как D3D12 \_ Вычисление \_ состояния конвейера в виде \_ \_ структуры по значению. Обратите внимание, что D3D12 \_ Вычисление \_ состояния конвейера не \_ \_ включает элементы **инпутлайаут**, **ибстрипкутвалуе**, **примитиветопологитипе**, **VS**, **GS**, **стреамаутпут**, **HS**, **DS**, **PS**, **блендстате,** **депсстенЦилстате**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** или **SampleMask** , поэтому эти значения теряются при преобразовании.

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

\_поток состояния конвейера CD3DX12 \_ \_ поддерживает Windows 10 Creators Update и более поздних версий, но не поддерживает типы подобъектов, добавленные в обновление для создателей Windows 10, например для создания экземпляров представления. Чтобы обеспечить поддержку типов подобъектов, добавленных в обновление авторов, используйте вместо него [**\_ состояние конвейера CD3DX12 \_ \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) .

Доступные переменные-члены этой структуры являются typedef \_ \_ \_ шаблона подобъекта потока состояния конвейера CD3DX12 \_ , который объединяет данные маркера типа и подобъекта в один объект, подходящий для описания потока.

Эти определения типов:

<dl> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_STREAM1 состояния конвейера CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**D3D12 \_ графика \_ состояния графического конвейера \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**\_DESC для \_ состояния конвейера D3D12 COMPUTE \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





