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
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649018"
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

## <a name="remarks"></a>Комментарии

Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|------------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Библиотека вспомогательных API Windows версии 1,0 или более поздней<br/>                            |
| Header<br/>          | <dl> <dt>AUX \_ клиб. h</dt> </dl>   |
| Библиотека<br/>         | <dl> <dt>AUX \_ клиб. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ауксклибкуеримодулеинформатион**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




