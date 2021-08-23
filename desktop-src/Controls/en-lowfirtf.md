---
title: Код уведомления EN_LOWFIRTF (RichEdit. h)
description: Сообщает родительскому окну элемента управления Microsoft Rich Edit, что было получено Неподдерживаемое ключевое слово формата RTF. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffafccf7fc52506ce72c6591ae9d4b5e3f5ee8855788267fbfae98497165e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576324"
---
# <a name="en_lowfirtf-notification-code"></a>\_Код уведомления EN ловфиртф

Сообщает родительскому окну элемента управления Microsoft Rich Edit, что было получено Неподдерживаемое ключевое слово формата RTF. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**енловфиртф**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот код уведомления не возвращает значение.

## <a name="remarks"></a>Remarks

Чтобы получить уведомление EN \_ ловфиртф, укажите \_ флаг енм ловфиртф в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 1 (SP1), \[ только классические приложения\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**енловфиртф**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> </dl>

 

 





