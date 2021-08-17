---
title: Код уведомления CBEN_ENDEDIT (Коммктрл. h)
description: Посылается, когда пользователь завершает операцию в поле ввода или выбрал элемент из раскрывающегося списка элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae9205e84e4f1c0b10e516b1f406f2d167f1bc5cc38417a31379d20e16fcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413954"
---
# <a name="cben_endedit-notification-code"></a>\_Код уведомления кбен ENDEDIT

Посылается, когда пользователь завершает операцию в поле ввода или выбрал элемент из раскрывающегося списка элемента управления. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмкбиндедит**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) , которая содержит сведения о том, как пользователь завершил операцию изменения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

**Значение false** , чтобы принять код уведомления и разрешить элементу управления отображать выбранный элемент; в противном случае — **значение true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбен \_ ЕНДЕДИТВ** (Юникод) и **кбен \_ ендедита** (ANSI)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения об элементах управления ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





