---
title: Метод ID3DX12PipelineParserCallbacks Блендстатекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания состояния смешения для объекта, реализующего этот интерфейс.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Метод Блендстатекб
- Метод Блендстатекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Блендстатекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a9d84e3648a54668211b8b9e590c653111c93553115aba43b5353f9549bfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528982"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Блендстатекб

Вызывает обратный вызов подобъекта описания состояния смешения для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Блендстате* \[ ЗНАЧ\]
</dt> <dd>

Тип: **const [**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Сведения о подобъекте описания состояния смешения, проанализированном из потока состояния конвейера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не возвращает ничего.

## <a name="requirements"></a>Requirements (Требования)



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

[**D3D12 \_ Blend, \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





