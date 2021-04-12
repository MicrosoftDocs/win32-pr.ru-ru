---
description: Сведения о методе конструктора для Кженериклист. Кженериклист (Вкслист. h). Этот метод использует параметры "pName" и "Иитемс".
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Конструктор Кженериклист. Кженериклист (Вкслист. h)
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
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356200"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a>Конструктор Кженериклист. Кженериклист (Вкслист. h) — pName, параметры Иитемс

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на имя списка.

</dd> <dt>

*иитемс* 
</dt> <dd>

Размер кэша узлов.

</dd> <dt>

*Блок* 
</dt> <dd>

Не используется.

</dd> <dt>

*балерт* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для повышения эффективности `CGenericList` класс поддерживает кэш узлов списка. Если вы понимаете, сколько элементов будет храниться в списке, используйте эту версию конструктора.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Header | Вкслист. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




