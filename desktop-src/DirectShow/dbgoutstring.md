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
ms.openlocfilehash: b6d8b74b5f0643f619a58beeea2dcd5526889d1a65de4815b06d2d6047777d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821564"
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

## <a name="remarks"></a>Remarks

В отладочных сборках эта функция всегда выводит строку, независимо от текущих уровней выходных данных отладки. Для более точного управления выходными данными используйте макрос [**дбглог**](dbglog.md) .

## <a name="examples"></a>Примеры


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




