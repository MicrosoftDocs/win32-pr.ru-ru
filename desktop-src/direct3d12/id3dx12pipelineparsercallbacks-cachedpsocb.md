---
title: Метод ID3DX12PipelineParserCallbacks Качедпсокб (D3DX12. h)
description: Вызывает обратный вызов подобъекта кэшированного PSO (объект состояния конвейера) объекта, реализующего этот интерфейс.
ms.assetid: 9EF8C468-1D86-4F49-9091-36B6125F1B68
keywords:
- Метод Качедпсокб
- Метод Качедпсокб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Качедпсокб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CachedPSOCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c168635a66eff012768a1eabbc803c6986a2c43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703886"
---
# <a name="id3dx12pipelineparsercallbackscachedpsocb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Качедпсокб

Вызывает обратный вызов подобъекта кэшированного PSO (объект состояния конвейера) объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void CachedPSOCb(
  [ref] const D3D12_CACHED_PIPELINE_STATE &CachedPSO
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Качедпсо* \[ ЗНАЧ\]
</dt> <dd>

Тип: **const [**D3D12 \_ кэшированное \_ \_ состояние конвейера**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)**

Сведения о кэшированном подобъекте PSO (объект состояния конвейера), проанализированном из потока состояния конвейера.

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

[**\_Состояние кэшированного \_ КОНВЕЙЕРа D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)
</dt> </dl>

 

 





