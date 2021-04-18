---
description: Создание загрузчика с асинхронной памятью.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: Функция D3DX10CreateAsyncMemoryLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713759"
---
# <a name="d3dx10createasyncmemoryloader-function"></a>Функция D3DX10CreateAsyncMemoryLoader

Создание загрузчика с асинхронной памятью.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на данные.

</dd> <dt>

*cbData* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

Размер данных.

</dd> <dt>

*ппдаталоадер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Адрес указателя на обработчик асинхронных данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
