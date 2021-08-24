---
description: Метод Get « \_ Автопросмотр» извлекает текущий флаг состояния автоотображения.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Метод CBaseControlWindow.get_AutoShow (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a5c16e0b460d07255cae113194f672ca3dace6f46827ac613c9559370284beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158797"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>Кбасеконтролвиндов. Get, \_ метод автоотображения

`get_AutoShow`Метод получает текущий флаг состояния автоотображения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Автоотображение* 
</dt> <dd>

Указатель на логический флаг автоматизации (0 — Off, 1 — включено).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**ивидеовиндов:: Get для \_ автоотображения**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) . Это свойство упрощает доступ к окнам для приложений. Если задано значение 1 (включено), то окно, которое обычно скрыто после подключения фильтра, будет отображаться автоматически при приостановке или запуске фильтра. Однако окно не должно быть скрыто при остановке фильтра. Если этот параметр имеет значение 0 (OFF), окно становится видимым только тогда, когда приложение вызывает [**кбасеконтролвиндов::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) или [**кбасеконтролвиндов::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) с соответствующими параметрами.

Эта функция-член предназначена для вызова внешними объектами через интерфейс [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и, следовательно, блокирует критический раздел для синхронизации с соответствующим фильтром. Вызовите функцию члена [**кбасеконтролвиндов:: исаутошовенаблед**](cbasecontrolwindow-isautoshowenabled.md) , чтобы получить это свойство, если не выполняется вызов из внешнего объекта.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




