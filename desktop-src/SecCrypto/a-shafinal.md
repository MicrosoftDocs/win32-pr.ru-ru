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
ms.openlocfilehash: 42a22cfca32409fdfa02586bb90c76f8e8f2489b22cfe2769b50d928d2564af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960293"
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

## <a name="remarks"></a>Remarks

Эта функция очень похожа на Шафинал, но вызывается непосредственно из библиотеки, а не направляется через криптографическую инфраструктуру. дополнительные сведения см. в статье [Windows поставщики нткриптографик](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Библиотека<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
