---
title: Интерфейс ID3DX12PipelineParserCallbacks (D3DX12. h)
description: Интерфейс, представляющий коллекцию обратных вызовов парсера и ошибок, используемых вспомогательной функцией D3DX12parsePipelineStream.
ms.assetid: CBC04D17-2E19-4755-B1CB-FC42BF5083E5
keywords:
- Интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, описание
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f83e0987009e60d5e207a9531cc4809f6cfcfbd5b50360a583df8cb0c01898f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733747"
---
# <a name="id3dx12pipelineparsercallbacks-interface"></a>Интерфейс ID3DX12PipelineParserCallbacks

Интерфейс, представляющий коллекцию обратных вызовов парсера и ошибок, используемых вспомогательной функцией [**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md) .

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX12PipelineParserCallbacks** содержит следующие методы.



| Метод                                                                                    | Описание                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BlendStateCb**](id3dx12pipelineparsercallbacks-blendstatecb.md)                       | Вызывает обратный вызов подобъекта описания состояния смешения для объекта, реализующего этот интерфейс.<br/>                                                                 |
| [**CachedPSOCb**](id3dx12pipelineparsercallbacks-cachedpsocb.md)                         | Вызывает обратный вызов подобъекта кэшированного PSO (объект состояния конвейера) объекта, реализующего этот интерфейс.<br/>                                                      |
| [**CSCb**](id3dx12pipelineparsercallbacks-cscb.md)                                       | Вызывает обратный вызов подобъекта COMPUTE Shader для объекта, реализующего этот интерфейс.<br/>                                                                          |
| [**DepthStencilState1Cb**](id3dx12pipelineparsercallbacks-depthstencilstate1cb.md)       | Вызывает обратный вызов подобъекта состояния трафарета глубины ([**D3D12 \_ \_ трафарета \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) объекта, реализующего этот интерфейс.<br/> |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-dsvformatcb.md)                 | Вызывает обратный вызов подобъекта формата значения шаблона глубины объекта, реализующего этот интерфейс.<br/>                                                              |
| [**DepthStencilStateCb**](id3dx12pipelineparsercallbacks-depthstencilstatecb.md)         | Вызывает обратный вызов подобъекта состояния шаблона глубины объекта, реализующего этот интерфейс.<br/>                                                                     |
| [**DSCb**](id3dx12pipelineparsercallbacks-dscb.md)                                       | Вызывает обратный вызов подобъекта шейдера домена для объекта, реализующего этот интерфейс.<br/>                                                                           |
| [**ErrorBadInputParameter**](id3dx12pipelineparsercallbacks-errorbadinputparameter.md)   | Вызывает недопустимый обратный вызов ошибки входного параметра объекта, реализующего этот интерфейс.<br/>                                                                         |
| [**ErrorDuplicateSubobject**](id3dx12pipelineparsercallbacks-errorduplicatesubobject.md) | Вызывает обратный вызов ошибки повторяющегося объекта для объекта, реализующего этот интерфейс.<br/>                                                                         |
| [**ErrorUnknownSubobject**](id3dx12pipelineparsercallbacks-errorunknownsubobject.md)     | Вызывает обратный вызов ошибки неизвестного подобъекта для объекта, реализующего этот интерфейс.<br/>                                                                           |
| [**FlagsCb**](id3dx12pipelineparsercallbacks-flagscb.md)                                 | Вызывает обратный вызов подобъекта flags объекта, реализующего этот интерфейс.<br/>                                                                                   |
| [**GSCb**](id3dx12pipelineparsercallbacks-gscb.md)                                       | Вызывает обратный вызов подобъекта шейдера Geometry для объекта, реализующего этот интерфейс.<br/>                                                                         |
| [**HSCb**](id3dx12pipelineparsercallbacks-hscb.md)                                       | Вызывает обратный вызов подобъекта шейдера поверхности объекта, реализующего этот интерфейс.<br/>                                                                             |
| [**IBStripCutValueCb**](id3dx12pipelineparsercallbacks-ibstripcutvaluecb.md)             | Вызывает обратный вызов подобъекта полосы буферного индекса для объекта, реализующего этот интерфейс.<br/>                                                            |
| [**InputLayoutCb**](id3dx12pipelineparsercallbacks-inputlayoutcb.md)                     | Вызывает обратный вызов подобъекта входной структуры для объекта, реализующего этот интерфейс.<br/>                                                                            |
| [**нодемасккб**](id3dx12pipelineparsercallbacks-nodemaskcb.md)                           | Вызывает обратный вызов подобъекта нодемаск объекта, реализующего этот интерфейс.<br/>                                                                                |
| [**PrimitiveTopologyTypeCb**](id3dx12pipelineparsercallbacks-primitivetopologytypecb.md) | Вызывает обратный вызов подобъекта типа топологии примитива объекта, реализующего этот интерфейс.<br/>                                                                 |
| [**PSCb**](id3dx12pipelineparsercallbacks-pscb.md)                                       | Вызывает обратный вызов подобъекта пиксельного шейдера для объекта, реализующего этот интерфейс.<br/>                                                                            |
| [**RasterizerStateCb**](id3dx12pipelineparsercallbacks-rasterizerstatecb.md)             | Вызывает обратный вызов подобъекта описания состояния средства программной прорисовки для объекта, реализующего этот интерфейс.<br/>                                                            |
| [**рутсигнатурекб**](id3dx12pipelineparsercallbacks-rootsignaturecb.md)                 | Вызывает обратный вызов подобъекта корневой подписи объекта, реализующего этот интерфейс.<br/>                                                                          |
| [**RTVFormatsCb**](id3dx12pipelineparsercallbacks-rtvformatscb.md)                       | Вызывает обратный вызов подобъекта массива формата целевого объекта прорисовки объекта, реализующего этот интерфейс.<br/>                                                              |
| [**SampleDescCb**](id3dx12pipelineparsercallbacks-sampledesccb.md)                       | Вызывает обратный вызов подобъекта описания образца для объекта, реализующего этот интерфейс.<br/>                                                                      |
| [**SampleMaskCb**](id3dx12pipelineparsercallbacks-samplemaskcb.md)                       | Вызывает обратный вызов подобъекта образца маски для объекта, реализующего этот интерфейс.<br/>                                                                             |
| [**StreamOutputCb**](id3dx12pipelineparsercallbacks-streamoutputcb.md)                   | Вызывает обратный вызов подобъекта описания потока вывода объекта, реализующего этот интерфейс.<br/>                                                               |
| [**VSCb**](id3dx12pipelineparsercallbacks-vscb.md)                                       | Вызывает обратный вызов подобъекта вершинного шейдера объекта, реализующего этот интерфейс.<br/>                                                                           |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные интерфейсы для Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**D3DX12parsePipelineStream**](d3dx12parsepipelinestream.md)
</dt> </dl>

 

 





