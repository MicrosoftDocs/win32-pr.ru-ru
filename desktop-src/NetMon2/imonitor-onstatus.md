---
description: Метод МКСВК вызывает метод OnStatus для уведомления монитора о существовании события состояния НПП. Этот метод должен быть реализован монитором.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Метод Имонитор:: OnStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2a82594400bebc8a529290e0e0e881603172aa45c111d2d4d83ebcbd5ebfbeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779044"
---
# <a name="imonitoronstatus-method"></a>Метод Имонитор:: OnStatus

Метод МКСВК вызывает метод **OnStatus** для уведомления монитора о существовании события состояния НПП. Этот метод должен быть реализован монитором.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Событие* \[ окне\]
</dt> <dd>

Структура [ \_ событий Update](update-event.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод выполнен успешно, возвращается значение S \_ (то же, что и параметр noreturn), а мксвк передает возвращаемое значение обратно в НПП для обработки.

Если метод завершается неудачно, возвращается код ошибки. При возникновении ошибки МКСВК передает возвращенное значение обратно в НПП для обработки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




