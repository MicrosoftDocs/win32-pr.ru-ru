---
description: Метод Сетконтролвиндовпин задает ПИН-код для синхронизации.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Кбасеконтролвиндов. Сетконтролвиндовпин, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9ab7cbb5d199b0908c2eb51ffb5a70eda7eb1336bd66a1645daad61b3202d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056714"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>Кбасеконтролвиндов. Сетконтролвиндовпин, метод

`SetControlWindowPin`Метод задает ПИН-код для синхронизации.

## <a name="syntax"></a>Синтаксис


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Указатель на ПИН-код, с которым синхронизируется интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Эта функция члена задает \_ переменную члена m ппин, равную параметру ппин. Как описано в конструкторе, интерфейс можно вызывать только после успешного подключения фильтра. Объект передается через эту функцию-член в закрепление, с которым она должна быть синхронизирована; в большинстве случаев он определяет, подключен ли ПИН-код каждый раз, когда он имеет метод интерфейса, и \_ при сбое ВОЗВРАЩАЕТ VFW E \_ Not \_ Connected.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




