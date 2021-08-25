---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER (D3dx12. h)
description: Выполняет сборку внутреннего \_ \_ объекта потока состояния конвейера CD3DX12 \_ из сведений о подобъекте, переданных в соответствующие функции элементов. Эта структура реализует интерфейс ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d20c34fb2c32cc588a12ac820cd80083d3c3139fa85cbf36810379a21618e80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851254"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>\_ \_ \_ \_ Вспомогательная структура синтаксического анализа потока состояния конвейера CD3DX12 \_

Выполняет сборку внутреннего \_ \_ объекта потока состояния конвейера CD3DX12 \_ из сведений о подобъекте, переданных в соответствующие функции элементов. Эта структура реализует интерфейс [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**пипелинестреам**
</dt> <dd>

Внутреннее [**\_ состояние конвейера \_ CD3DX12 \_ STREAM1**](cd3dx12-pipeline-state-stream1.md). Его текущее состояние представляет собой совокупный результат методов обратного вызова, которые были вызваны для этого объекта.

</dd> <dt>

**Флагскб ( \_ \_ \_ Флаги флагов состояния конвейера D3D12)**
</dt> <dd>

Инициализирует член **flags** объекта **пипелинестреам** , используя значение параметра *flags* .

</dd> <dt>

**Нодемасккб (UINT Нодемаск)**
</dt> <dd>

Инициализирует член **нодемаск** объекта **пипелинестреам** , используя значение параметра *нодемаск* .

</dd> <dt>

**Рутсигнатурекб (ID3D12RootSignature \* прутсигнатуре)**
</dt> <dd>

Инициализирует член **прутсигнатуре** объекта **пипелинестреам** , используя значение параметра *прутсигнатуре* .

</dd> <dt>

**Инпутлайауткб (const D3D12 \_ входной \_ макет \_ DESC& инпутлайаут)**
</dt> <dd>

Инициализирует член **инпутлайаут** объекта **пипелинестреам** , используя значение параметра *инпутлайаут* .

</dd> <dt>

**Ибстрипкутвалуекб ( \_ БУФЕР D3D12 index, \_ \_ \_ вырезанное \_ значение ибстрипкутвалуе)**
</dt> <dd>

Инициализирует член **ибстрипкутвалуе** объекта **пипелинестреам** , используя значение параметра *ибстрипкутвалуе* .

</dd> <dt>

**Примитиветопологитипекб (тип D3D12- \_ примитивной \_ топологии \_ примитиветопологитипе)**
</dt> <dd>

Инициализирует член **примитиветопологитипе** объекта **пипелинестреам** , используя значение параметра *примитиветопологитипе* .

</dd> <dt>

**Вскб (константа- \_ байт шейдера const D3D12 \_& VS)**
</dt> <dd>

Инициализирует элемент **пипелинестреам** в **VS** (Вершинный шейдер), используя значение параметра *VS* .

</dd> <dt>

**ГСКБ (константный D3D12- \_ байт шейдера const \_& GS)**
</dt> <dd>

Инициализирует элемент **пипелинестреам** в **GS** (Geometry Shader), используя значение параметра *GS* .

</dd> <dt>

**Стреамаутпуткб (const D3D12 \_ Stream \_ вывода \_ DESC& стреамаутпут)**
</dt> <dd>

Инициализирует член **стреамаутпут** объекта **пипелинестреам** , используя значение параметра *стреамаутпут* .

</dd> <dt>

**Хскб (константа- \_ байт шейдера const D3D12 \_& HS)**
</dt> <dd>

Инициализирует элемент " **HS** " (шейдер поверхности) объекта **пипелинестреам** , используя значение параметра *HS* .

</dd> <dt>

**Дскб (константа- \_ байт шейдера const D3D12 \_& DS)**
</dt> <dd>

Инициализирует член **DS** (доменный шейдер) **пипелинестреам** , используя значение параметра *DS* .

</dd> <dt>

**Пскб (константа- \_ байт шейдера const D3D12 \_& PS)**
</dt> <dd>

Инициализирует член **PS** (Pixel Shader) элемента **пипелинестреам** , используя значение параметра *PS* .

</dd> <dt>

**Кскб (константа- \_ байт шейдера const D3D12 \_& CS)**
</dt> <dd>

Инициализирует член **CS** объекта **пипелинестреам** , используя значение параметра *CS* .

</dd> <dt>

**Блендстатекб (const D3D12 \_ Blend \_ DESC& блендстате)**
</dt> <dd>

Инициализирует член **блендстате** объекта **пипелинестреам** , используя значение параметра *блендстате* .

</dd> <dt>

**ДепсстенЦилстатекб (const D3D12 \_ трафарет Depth, \_ \_ DESC& депсстенЦилстате)**
</dt> <dd>

Инициализирует член **депсстенЦилстате** объекта **пипелинестреам** , используя значение параметра *депсстенЦилстате* , а также набор [**\_ элементов глубины D3D12 \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).

</dd> <dt>

**DepthStencilState1Cb (const D3D12 \_ \_ набор элементов глубины \_ DESC1& депсстенЦилстате)**
</dt> <dd>

Инициализирует член **депсстенЦилстате** объекта **пипелинестреам** , используя значение параметра *депсстенЦилстате* , [**D3D12 \_ \_ шаблона глубины \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**Дсвформаткб ( \_ Формат DXGI дсвформат)**
</dt> <dd>

Инициализирует член **дсвформат** объекта **пипелинестреам** , используя значение параметра *дсвформат* .

</dd> <dt>

**Растеризерстатекб (const D3D12 средство \_ растеризации \_ "DESC"& растеризерстате)**
</dt> <dd>

Инициализирует член **растеризерстате** объекта **пипелинестреам** , используя значение параметра *растеризерстате* .

</dd> <dt>

**Ртвформатскб (const D3D12 \_ \_ массив формата RT \_& ртвформатс)**
</dt> <dd>

Инициализирует член **ртвформатс** объекта **пипелинестреам** , используя значение параметра *ртвформатс* .

</dd> <dt>

**Сампледесккб (const, \_ образец \_ DESC, пример& сампледеск)**
</dt> <dd>

Инициализирует член **сампледеск** объекта **пипелинестреам** , используя значение параметра *сампледеск* .

</dd> <dt>

**Самплемасккб (UINT Самплемаск)**
</dt> <dd>

Инициализирует член **самплемаск** объекта **пипелинестреам** , используя значение параметра *самплемаск* .

</dd> <dt>

**ВиевинстанЦингкб (const D3D12 \_ представление \_ экземпляров \_ DESC& виевинстанЦингдеск)**
</dt> <dd>

Инициализирует член **виевинстанЦингдеск** объекта **пипелинестреам** , используя значение параметра *виевинстанЦингдеск* .

</dd> <dt>

**Качедпсокб (const D3D12 \_ кэшированное \_ состояние конвейера \_& качедпсо)**
</dt> <dd>

Инициализирует член **качедпсо** объекта **пипелинестреам** , используя значение параметра *качедпсо* .

</dd> <dt>

**Еррорбадинпутпараметер (UINT)**
</dt> <dd>

Не выполняет никаких действий.

</dd> <dt>

**Еррордупликатесубобжект ( \_ \_ \_ тип подобъекта состояния конвейера D3D12 \_ )**
</dt> <dd>

Не выполняет никаких действий.

</dd> <dt>

**Еррорункновнсубобжект (UINT)**
</dt> <dd>

Не выполняет никаких действий.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если передается в качестве второго параметра функции [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , сведения о внутреннем объекте [**\_ состояния конвейера CD3DX12 \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md) копируются из [**\_ \_ потока состояния конвейера \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) , переданного в качестве первого параметра. Этот процесс проверяет описание исходного потока. Если D3DX12ParsePipelineStream возвращает значение " **\_ ОК**", то как описание исходного потока, так и полученное **CD3DX12 \_ состояние конвейера \_ \_ STREAM1PipelineStream** являются допустимыми; в противном случае оба значения являются недопустимыми. Недопустимые потоки и другие ошибки выводятся только через возвращаемое значение D3DX12ParsePipelineStream; Эта структура реализует обратные вызовы ошибок, чтобы ничего не делать.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





