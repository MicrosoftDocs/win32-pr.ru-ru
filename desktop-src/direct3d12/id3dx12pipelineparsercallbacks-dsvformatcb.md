---
title: Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h) (DSV)
description: Вызывает обратный вызов подобъекта формата значения шаблона глубины объекта, реализующего этот интерфейс.
ms.assetid: BDD3AB24-34C6-41C8-984D-78A45867BF24
keywords:
- Метод ДепсстенЦилстатекб
- Метод ДепсстенЦилстатекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод ДепсстенЦилстатекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d26c13c70976c67bbe8d5910c4f3573010ff580
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105708634"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h)

Вызывает обратный вызов подобъекта формата значения шаблона глубины объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void DepthStencilStateCb(
   DXGI_FORMAT DepthStencilState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*депсстенЦилстате* 
</dt> <dd>

Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Сведения о подобъекте формата значения трафарета глубины, проанализированном из потока состояния конвейера.

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

[**\_Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

