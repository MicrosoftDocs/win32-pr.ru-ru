---
title: Метод ID3DX12PipelineParserCallbacks Стреамаутпуткб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания потока вывода объекта, реализующего этот интерфейс.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Метод Стреамаутпуткб
- Метод Стреамаутпуткб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Стреамаутпуткб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713482"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Стреамаутпуткб

Вызывает обратный вызов подобъекта описания потока вывода объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стреамаутпут* \[ ЗНАЧ\]
</dt> <dd>

Тип: **const [**D3D12 \_ поток \_ вывода \_ Output**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

Сведения о подобъекте описания выходного потока, проанализированном из потока состояния конвейера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не возвращает ничего.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные интерфейсы для Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**D3D12 \_ поток \_ вывода \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





