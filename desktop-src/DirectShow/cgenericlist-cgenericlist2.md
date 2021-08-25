---
description: Сведения о методе конструктора для Кженериклист. Кженериклист (Вкслист. h). Этот метод использует параметр "pName".
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Кженериклист. Кженериклист-конструктор (Вкслист. h) — параметр pName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 117138e80db91529d6a2baf93577a6a4dfd542d2975bf2ce6f89124a3d7aefe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813844"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a>Кженериклист. Кженериклист-конструктор (Вкслист. h) — параметр pName

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на имя списка.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для повышения эффективности `CGenericList` класс поддерживает кэш узлов списка. Эта версия конструктора использует размер кэша по умолчанию.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Заголовок | вкслист. h (включает Потоки. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




