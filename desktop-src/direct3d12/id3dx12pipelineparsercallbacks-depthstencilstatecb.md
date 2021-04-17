---
title: Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта состояния шаблона глубины объекта, реализующего этот интерфейс.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
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
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694088"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>Метод ID3DX12PipelineParserCallbacks ДепсстенЦилстатекб (D3DX12. h)

Вызывает обратный вызов подобъекта состояния шаблона глубины объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ДепсстенЦилстате* \[ ЗНАЧ\]
</dt> <dd>

Тип: **const [**D3D12 \_ \_ набор элементов \_ глубины**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**

Сведения о подобъекте состояния шаблона глубины, проанализированном из потока состояния конвейера.

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

[**D3D12 \_ \_ трафарета \_ глубины**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





