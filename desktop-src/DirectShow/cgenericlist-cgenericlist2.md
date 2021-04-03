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
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103914835"
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

## <a name="remarks"></a>Комментарии

Для повышения эффективности `CGenericList` класс поддерживает кэш узлов списка. Эта версия конструктора использует размер кэша по умолчанию.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Header | Вкслист. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




