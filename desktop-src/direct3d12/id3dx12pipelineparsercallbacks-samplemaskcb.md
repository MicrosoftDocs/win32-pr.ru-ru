---
title: Метод ID3DX12PipelineParserCallbacks Самплемасккб (D3DX12. h)
description: Вызывает обратный вызов подобъекта образца маски для объекта, реализующего этот интерфейс.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Метод Самплемасккб
- Метод Самплемасккб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Самплемасккб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713483"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Самплемасккб

Вызывает обратный вызов подобъекта образца маски для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*самплемаск* 
</dt> <dd>

Тип: **uint**

Подробные сведения о примере подобъекта маски, проанализированном из потока состояния конвейера.

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
</dt> </dl>

 

 





