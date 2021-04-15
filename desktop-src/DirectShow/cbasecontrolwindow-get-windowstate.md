---
description: Метод Get \_ WindowState извлекает текущее состояние окна.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Метод CBaseControlWindow.get_WindowState (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669235"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a>Кбасеконтролвиндов. Get \_ WindowState, метод

`get_WindowState`Метод получает текущее состояние окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиндовстате* 
</dt> <dd>

Указатель на состояние окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Эта функция-член возвращает подмножество параметров функции Microsoft Win32 **ShowWindow** . В частности, он возвращает SW \_ / \_ Hide, в зависимости от текущей видимости окна. В \_ \_ зависимости от того, является ли окно значком или развернутым, он также возвращает значение по раскрытому программному и уменьшенному.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




