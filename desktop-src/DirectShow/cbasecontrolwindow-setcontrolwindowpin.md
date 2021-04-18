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
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658059"
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

## <a name="remarks"></a>Комментарии

Эта функция члена задает \_ переменную члена m ппин, равную параметру ппин. Как описано в конструкторе, интерфейс можно вызывать только после успешного подключения фильтра. Объект передается через эту функцию-член в закрепление, с которым она должна быть синхронизирована; в большинстве случаев он определяет, подключен ли ПИН-код каждый раз, когда он имеет метод интерфейса, и \_ при сбое ВОЗВРАЩАЕТ VFW E \_ Not \_ Connected.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




