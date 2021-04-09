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
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155107"
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



 

 




