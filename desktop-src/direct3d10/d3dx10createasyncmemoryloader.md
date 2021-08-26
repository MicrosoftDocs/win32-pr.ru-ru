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
ms.openlocfilehash: 897977147157c754c0f0da1c68e5e64b3fa64ea792c573c1f901aca6aec433fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989234"
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
| Заголовок<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
