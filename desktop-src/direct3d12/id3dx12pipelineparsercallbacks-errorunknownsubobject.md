---
title: Метод ID3DX12PipelineParserCallbacks Еррорункновнсубобжект (D3DX12. h)
description: Вызывает обратный вызов ошибки неизвестного подобъекта для объекта, реализующего этот интерфейс.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Метод Еррорункновнсубобжект
- Метод Еррорункновнсубобжект, интерфейс ID3DX12PipelineParserCallbacks
- Интерфейс ID3DX12PipelineParserCallbacks, метод Еррорункновнсубобжект
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713827"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a>Метод ID3DX12PipelineParserCallbacks:: Еррорункновнсубобжект

Вызывает обратный вызов ошибки неизвестного подобъекта для объекта, реализующего этот интерфейс.

## <a name="syntax"></a>Синтаксис


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ункновнтипевалуе* 
</dt> <dd>

Тип: **uint**

Нераспознанный тип подобъекта предпринятого подобъекта.

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
</dt> </dl>

 

 





