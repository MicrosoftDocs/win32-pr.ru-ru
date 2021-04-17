---
title: Метод ID3DX12PipelineParserCallbacks DepthStencilState1Cb (D3DX12. h)
description: Вызывает обратный вызов подобъекта состояния трафарета глубины (D3D12 \_ \_ трафарета \_ DESC1) объекта, реализующего этот интерфейс.
ms.assetid: C1AE06E5-B1FF-44C2-9C56-1540B97AD883
keywords:
- Метод DepthStencilState1Cb
- Метод DepthStencilState1Cb, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод DepthStencilState1Cb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilState1Cb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a42cf85f60dcf27a5751f77a346931bfad6b03e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703657"
---
# <a name="id3dx12pipelineparsercallbacksdepthstencilstate1cb-method"></a>ID3DX12PipelineParserCallbacks: метод:D epthStencilState1Cb

Вызывает обратный вызов подобъекта состояния трафарета глубины ([**D3D12 \_ \_ трафарета \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)) объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void DepthStencilState1Cb(
  [ref] const D3D12_DEPTH_STENCIL_DESC1 &DepthStencilState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ДепсстенЦилстате* \[ ЗНАЧ\]
</dt> <dd>

Тип: **const [**D3D12 \_ \_ набор элементов глубины \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**

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

[**D3D12 \_ \_ трафарета глубины \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> </dl>

 

 





