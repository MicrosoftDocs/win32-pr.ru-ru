---
title: Метод ID3DX12PipelineParserCallbacks Еррордупликатесубобжект (D3DX12. h)
description: Вызывает обратный вызов ошибки повторяющегося объекта для объекта, реализующего этот интерфейс.
ms.assetid: 625C72C4-7BFB-4DAD-8D39-EDDBC7189499
keywords:
- Метод Еррордупликатесубобжект
- Метод Еррордупликатесубобжект, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Еррордупликатесубобжект
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorDuplicateSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b00dae4675ff05a43e566a8ead815ea24f6c16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713829"
---
# <a name="id3dx12pipelineparsercallbackserrorduplicatesubobject-method"></a>Метод ID3DX12PipelineParserCallbacks:: Еррордупликатесубобжект

Вызывает обратный вызов ошибки повторяющегося объекта для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void ErrorDuplicateSubobject(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE DuplicateType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*дупликатетипе* 
</dt> <dd>

Тип: **[ **\_ \_ \_ \_ тип подобъекта состояния конвейера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**

Тип подобъекта, который был дублирован.

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

[**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

