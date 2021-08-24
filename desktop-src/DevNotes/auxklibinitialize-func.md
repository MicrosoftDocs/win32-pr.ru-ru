---
description: Инициализирует библиотеку AUX \_ клиб.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Функция Ауксклибинитиализе (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: f35d2d17d581d17a6d89a7bc10d185a67a5fb0b695a29492922f5950241f2ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654884"
---
# <a name="auxklibinitialize-function"></a>Функция Ауксклибинитиализе

Инициализирует библиотеку AUX \_ клиб. Эта функция должна вызываться до вызова любой другой функции в библиотеке.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается значение STATUS \_ Success.

Если функция завершается ошибкой, возвращаемое значение может быть одним из кодов состояния, определенных в файле Ntstatus. h, который доступен в WDK.

## <a name="remarks"></a>Remarks

Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|------------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Windows Вспомогательная библиотека API версии 1,0 или более поздней<br/>                            |
| Заголовок<br/>          | <dl> <dt>AUX \_ клиб. h</dt> </dl>   |
| Библиотека<br/>         | <dl> <dt>AUX \_ клиб. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ауксклибкуеримодулеинформатион**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




