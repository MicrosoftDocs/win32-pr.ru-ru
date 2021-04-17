---
description: Функция Дбгинитиалисе инициализирует библиотеку отладки. Игнорируется в розничных сборках.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Функция Дбгинитиалисе (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675403"
---
# <a name="dbginitialise-function"></a>Функция Дбгинитиалисе

Функция **дбгинитиалисе** инициализирует библиотеку отладки. Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хинст* 
</dt> <dd>

Обработчик для экземпляра модуля.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

В исполняемом файле вызовите этот метод перед использованием средств отладки DirectShow. Перед завершением работы исполняемого файла вызовите функцию [**дбгтерминате**](dbgterminate.md) для очистки отладочной библиотеки.

В библиотеке DLL, которая ссылается на библиотеку базового класса (Стрмбасе. lib), нет необходимости вызывать эту функцию. Функция вызывается автоматически при загрузке библиотеки DLL.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




