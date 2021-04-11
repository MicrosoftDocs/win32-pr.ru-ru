---
title: Код уведомления EN_REQUESTRESIZE (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что содержимое элемента управления меньше или превышает размер окна элемента управления. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136443"
---
# <a name="en_requestresize-notification-code"></a>\_Код уведомления EN рекуестресизе

Сообщает родительскому окну элемента управления Rich Edit, что содержимое элемента управления меньше или превышает размер окна элемента управления. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**рекресизе**](/windows/desktop/api/Richedit/ns-richedit-reqresize) , которая получает запрошенный размер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот код уведомления не возвращает значение.

## <a name="remarks"></a>Комментарии

Для поддержки нижнего поведения элемента управления Rich Edit родительское окно должно изменить размер элемента управления при получении этого кода уведомления.

Чтобы получить \_ коды уведомлений EN рекуестресизе, укажите [**енм \_ рекуестресизе**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**рекресизе**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> </dl>

 

 





