---
description: Метод конструктора.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Конструктор Кбасеобжект. Кбасеобжект (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665152"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>Кбасеобжект. Кбасеобжект, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Строка, содержащая имя объекта для целей отладки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот метод увеличивает число активных объектов. (См. [**кбасеобжект:: обжектсактиве**](cbaseobject-objectsactive.md).)

Выделить параметр *pName* в статической памяти:


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



Макрос [**Name**](name.md) компилируется в **значение NULL** в розничных сборках, чтобы статические строки отображались только в отладочных сборках. Дополнительные сведения см. в разделе [**дбгдумпобжектрегистер**](dbgdumpobjectregister.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеобжект**](cbaseobject.md)
</dt> </dl>

 

 




