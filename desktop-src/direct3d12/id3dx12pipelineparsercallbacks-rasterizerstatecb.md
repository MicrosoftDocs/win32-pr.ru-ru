---
title: Метод ID3DX12PipelineParserCallbacks Растеризерстатекб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания состояния средства программной прорисовки для объекта, реализующего этот интерфейс.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Метод Растеризерстатекб
- Метод Растеризерстатекб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Растеризерстатекб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a179f26d88f25027eb9ffc2b4b3712ac963b65179334fff1bfa4d6103ef76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528624"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Растеризерстатекб

Вызывает обратный вызов подобъекта описания состояния средства программной прорисовки для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Растеризерстате* \[ ЗНАЧ\]
</dt> <dd>

Тип: **const [**D3D12 средство \_ развертки \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Сведения о подобъекте описания состояния средства программной прорисовки, проанализированном из потока состояния конвейера.

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

[**D3D12 средство программной \_ прорисовки \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





