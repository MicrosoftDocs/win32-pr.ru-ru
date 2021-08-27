---
description: Метод конструктора Кбасеобжект. Кбасеобжект.
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
ms.openlocfilehash: 35443d212fc244c80da958f2f87d03363c59348be4189393c1c3493521a0439b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076584"
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

## <a name="remarks"></a>Remarks

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеобжект**](cbaseobject.md)
</dt> </dl>

 

 




