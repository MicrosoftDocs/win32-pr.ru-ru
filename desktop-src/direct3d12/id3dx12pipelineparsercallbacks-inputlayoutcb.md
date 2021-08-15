---
title: Метод ID3DX12PipelineParserCallbacks Инпутлайауткб (D3DX12. h)
description: Вызывает обратный вызов подобъекта входной структуры для объекта, реализующего этот интерфейс.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Метод Инпутлайауткб
- Метод Инпутлайауткб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Инпутлайауткб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f7012686c85b38e94f8f3d2400cf406d614fc83ff0ba25e746ac0433b2e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528776"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Инпутлайауткб

Вызывает обратный вызов подобъекта входной структуры для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Инпутлайаут* \[ ЗНАЧ\]
</dt> <dd>

Тип: **const [**D3D12 \_ входной \_ Макет \_ Layout**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

Сведения о подобъекте макета входных данных, проанализированном из потока состояния конвейера.

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

[**D3D12 \_ входной \_ Макет \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





