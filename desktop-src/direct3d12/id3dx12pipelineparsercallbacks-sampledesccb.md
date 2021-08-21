---
title: Метод ID3DX12PipelineParserCallbacks Сампледесккб (D3DX12. h)
description: Вызывает обратный вызов подобъекта описания образца для объекта, реализующего этот интерфейс.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Метод Сампледесккб
- Метод Сампледесккб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Сампледесккб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba360b8f6af83f0d5bd626793dedba4f830d94cd49dc984da807588ea186c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124032"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Сампледесккб

Вызывает обратный вызов подобъекта описания образца для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сампледеск* \[ ЗНАЧ\]
</dt> <dd>

Тип: **[**\_ образец \_**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) "const** " для DXGI

Сведения о подобъекте образца Description, проанализированном из потока состояния конвейера.

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

[**\_пример \_ DESC в DXGI**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

