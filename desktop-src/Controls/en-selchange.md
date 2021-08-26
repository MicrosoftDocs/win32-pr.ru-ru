---
title: Код уведомления EN_SELCHANGE (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что текущее выделение изменилось. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a2398abd5058f57eeef6ad73f559a723e7df29315d38dfc9794a707740c89f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047424"
---
# <a name="en_selchange-notification-code"></a>\_Код уведомления EN селчанже

Сообщает родительскому окну элемента управления Rich Edit, что текущее выделение изменилось. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**селчанже**](/windows/desktop/api/Richedit/ns-richedit-selchange) , которая получает сведения о выделенном фрагменте.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот код уведомления не возвращает значение.

## <a name="remarks"></a>Remarks

Чтобы получить \_ коды уведомлений EN селчанже, укажите [**енм \_ селчанже**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

Этот код уведомления отправляется при изменении позиции курсора и если текст не выбран (выделение пусто). Позиции курсора могут изменяться, когда пользователь щелкает мышью, вводит или нажимает клавишу со стрелкой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**селчанже**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> </dl>

 

 





