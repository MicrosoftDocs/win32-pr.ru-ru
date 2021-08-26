---
title: Метод ID3DX12PipelineParserCallbacks Кскб (D3DX12. h)
description: Вызывает обратный вызов подобъекта COMPUTE Shader для объекта, реализующего этот интерфейс.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Метод Кскб
- Метод Кскб, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Кскб
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef816594b74ac3b09a73003de4bc5cf7984d2755a7b3769159a0e26a3bbf1af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894634"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a>Метод ID3DX12PipelineParserCallbacks:: Кскб

Вызывает обратный вызов подобъекта COMPUTE Shader для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*CS* \[ ЗНАЧ\]
</dt> <dd>

Тип: **Константный [**\_ \_ байт шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Сведения о подобъекте COMPUTE Shader, проанализированном из потока состояния конвейера.

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

 

 





