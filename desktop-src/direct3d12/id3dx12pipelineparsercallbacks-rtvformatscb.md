---
title: Метод ID3DX12PipelineParserCallbacks Ртвформатскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта массива формата целевого объекта прорисовки объекта, реализующего этот интерфейс.
ms.assetid: 0D5F0BC4-D9E2-4B16-99B5-509454AF8C02
keywords:
- Метод Ртвформатскб
- Метод Ртвформатскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Ртвформатскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RTVFormatsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d826bd2c2f3c5f1c0783a4be2cba132e4874f5a54776c227590dd87f5365d347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045442"
---
# <a name="id3dx12pipelineparsercallbacksrtvformatscb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Ртвформатскб

Вызывает обратный вызов подобъекта массива формата целевого объекта прорисовки объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void RTVFormatsCb(
  [ref] const D3D12_RT_FORMAT_ARRAY &RTVFormats
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ртвформатс* \[ ЗНАЧ\]
</dt> <dd>

Тип: **Константный [**\_ \_ \_ массив формата D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)**

Сведения о подобъекте массива целевого формата визуализации, проанализированном из потока состояния конвейера.

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

[**\_ \_ Массив формата D3D12 \_ RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





