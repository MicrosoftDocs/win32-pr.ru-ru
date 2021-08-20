---
title: Метод ID3DX12PipelineParserCallbacks Пскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта пиксельного шейдера для объекта, реализующего этот интерфейс.
ms.assetid: 3397B018-C26A-426F-88BB-89013BACBEEA
keywords:
- Метод Пскб
- Метод Пскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Пскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c15b09598218259d5cdeedfb3453aaf2a4f669242ddb76e676093e81e0dd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894574"
---
# <a name="id3dx12pipelineparsercallbackspscb-method"></a>ID3DX12PipelineParserCallbacks: метод:P СКБ

Вызывает обратный вызов подобъекта пиксельного шейдера для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void PSCb(
  [ref] const D3D12_SHADER_BYTECODE &PS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PS* \[ ЗНАЧ\]
</dt> <dd>

Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Сведения о подобъекте шейдера пикселей, проанализированном из потока состояния конвейера.

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
</dt> <dt>

[**\_Байтовый код шейдера D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





