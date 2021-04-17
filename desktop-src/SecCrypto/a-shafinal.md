---
description: Выполняет вычисление конечного хэша данных, вводимых функцией MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Функция A_SHAFinal (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665136"
---
# <a name="a_shafinal-function"></a>\_Функция шафинал

Выполняет вычисление конечного хэша данных, вводимых функцией MD5Update.

## <a name="syntax"></a>Синтаксис


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Контекст* \[ в, out\]
</dt> <dd>

Контекст SHA.

</dd> <dt>

*Результат* \[ заполняет\]
</dt> <dd>

Результирующая хэш-таблица.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция очень похожа на Шафинал, но вызывается непосредственно из библиотеки, а не направляется через криптографическую инфраструктуру. Дополнительные сведения см. в разделе [поставщики Нткриптографик Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Библиотека<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
