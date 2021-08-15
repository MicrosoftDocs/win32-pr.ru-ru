---
title: Метод ID3DX12PipelineParserCallbacks Флагскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта flags объекта, реализующего этот интерфейс.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Метод Флагскб
- Метод Флагскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Флагскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d14e8b507ae04a5f35b2786ca4ba7ab6ec19bb449492aa2c40f32510cd3ecb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528786"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Флагскб

Вызывает обратный вызов подобъекта flags объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* 
</dt> <dd>

Тип: **[ **D3D12 \_ . \_ \_ флаги состояния конвейера**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Сведения о подобъекте flags, проанализированном из потока состояния конвейера.

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

[**\_ \_ Флаги состояния КОНВЕЙЕРа D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





