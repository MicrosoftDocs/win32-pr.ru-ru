---
title: Метод ID3DX12PipelineParserCallbacks Нодемасккб (D3DX12. h)
description: Вызывает обратный вызов подобъекта нодемаск объекта, реализующего этот интерфейс.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Метод Нодемасккб
- Метод Нодемасккб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Нодемасккб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356ddf6ea86980ee882ad7544096811db420ae0cf8224f315801b708b95ae98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045452"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Нодемасккб

Вызывает обратный вызов подобъекта нодемаск объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нодемаск* 
</dt> <dd>

Тип: **uint**

Сведения о подобъекте нодемаск, проанализированном из потока состояния конвейера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не возвращает ничего.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вспомогательные интерфейсы для Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





