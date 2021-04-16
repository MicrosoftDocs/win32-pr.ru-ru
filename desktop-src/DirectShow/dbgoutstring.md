---
description: Функция Дбгаутстринг отправляет строку в расположение выходных данных отладки. Игнорируется в розничных сборках.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Функция Дбгаутстринг (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657222"
---
# <a name="dbgoutstring-function"></a>Функция Дбгаутстринг

Функция **дбгаутстринг** отправляет строку в расположение выходных данных отладки. Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псз* 
</dt> <dd>

Строка для вывода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

В отладочных сборках эта функция всегда выводит строку, независимо от текущих уровней выходных данных отладки. Для более точного управления выходными данными используйте макрос [**дбглог**](dbglog.md) .

## <a name="examples"></a>Примеры


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




