---
description: Считывает двоичные данные. Не рекомендуется.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'Метод Идиректксфилебинари:: Read (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081912"
---
# <a name="idirectxfilebinaryread-method"></a>Метод Идиректксфилебинари:: Read

Считывает двоичные данные. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на буфер, который получает считанные данные.

</dd> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Размер буфера, на который указывает Пвдата, в байтах.

</dd> <dt>

*пкбреад* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпдворд**](../winprog/windows-data-types.md)**

Указатель на число фактически считанных байтов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ номоредата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилебинари](idirectxfilebinary.md)
</dt> </dl>

 

 
