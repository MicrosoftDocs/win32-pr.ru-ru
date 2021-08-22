---
title: Метод ID3DX12PipelineParserCallbacks Ибстрипкутвалуекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта полосы буферного индекса для объекта, реализующего этот интерфейс.
ms.assetid: 702CA90A-FF20-4554-9469-C86428C203BC
keywords:
- Метод Ибстрипкутвалуекб
- Метод Ибстрипкутвалуекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Ибстрипкутвалуекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.IBStripCutValueCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdbbe2d66ae38a3bcd04ee84e6db15841d8f74a3b0d311552a51a892445b38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124072"
---
# <a name="id3dx12pipelineparsercallbacksibstripcutvaluecb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Ибстрипкутвалуекб

Вызывает обратный вызов подобъекта полосы буферного индекса для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void IBStripCutValueCb(
   D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ибстрипкутвалуе* 
</dt> <dd>

Тип: **[ **D3D12 \_ \_ \_ \_ \_ значение вырезанной полосы буфера индекса**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)**

Сведения о полосе буферов индексов — вырезанное значение подобъект, проанализированный из потока состояния конвейера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не возвращает ничего.

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

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**\_Отрезать \_ \_ \_ \_ значение для буфера D3D12 индекса**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)
</dt> </dl>

 

 





