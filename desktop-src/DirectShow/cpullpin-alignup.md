---
description: Метод Алигнуп Округляет значение до указанной границы выравнивания. примечание удалено в Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Кпуллпин. Алигнуп, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34c45fe4a34e21647cd976adbf29dfe6723e4216d58166e7d1599d4c8d64d47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687764"
---
# <a name="cpullpinalignup-method"></a>Кпуллпин. Алигнуп, метод

Метод **алигнуп** Округляет значение до указанной границы выравнивания.

> [!Note]  
> удалено в Windows 7.

 

## <a name="syntax"></a>Синтаксис


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*залив* 
</dt> <dd>

Указывает число для выровняйте.

</dd> <dt>

*лалигн* 
</dt> <dd>

Задает границу выравнивания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает согласованный результат.

## <a name="remarks"></a>Remarks

> [!Caution]  
> Этот метод может привести к числу переполнений, если *все* + (*лалигн* -1) переполнены.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




