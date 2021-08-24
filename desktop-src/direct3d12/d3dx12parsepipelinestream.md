---
title: Функция D3DX12ParsePipelineStream (D3dx12. h)
description: Анализирует описание потока состояния конвейера, вызывая пользовательский обратный вызов для каждого анализируемого экземпляра подобъекта.
ms.assetid: BE4E8CC4-1E1F-4FE8-B109-05FAF93EB620
keywords:
- Функция D3DX12ParsePipelineStream
topic_type:
- apiref
api_name:
- D3DX12ParsePipelineStream
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbdd472d118a5ec9d49c5f105ee6b8e8ef2e3ea540f6f1954bad17273e9e030f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608564"
---
# <a name="d3dx12parsepipelinestream-function"></a>Функция D3DX12ParsePipelineStream

Анализирует описание потока состояния конвейера, вызывая пользовательский обратный вызов для каждого анализируемого экземпляра подобъекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT inline D3DX12ParsePipelineStream(
   const D3D12_PIPELINE_STATE_STREAM_DESC &Desc,
         ID3DX12PipelineParserCallbacks   *pCallbacks
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*DESC* \[ ЗНАЧ\]
</dt> <dd>

Тип: **[**\_ поток состояния const D3D12 конвейера — \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc)**

Описание потока состояния конвейера для синтаксического анализа.

</dd> <dt>

*пкаллбаккс* 
</dt> <dd>

Тип: **[ **ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)\***

Структура, указывающая обратные вызовы для вызова для каждого типа подобъекта и дополнительные обратные вызовы для вызова в случае ошибки синтаксического анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Этот метод возвращает значение HRESULT Success (**S \_ OK** или **E \_ INVALIDARG** Error), если обнаружен неизвестный тип подобъекта, если описание потока пустое, равно null или содержит дубликаты подобъектов (включая производные подобъекты) или если *пкаллбаккс* имеет значение null. В каждом случае, когда \_ возвращается E INVALIDARG, сначала вызывается соответствующий обратный вызов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Библиотека<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вспомогательные функции для D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





