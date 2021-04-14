---
title: Код уведомления CBEN_ENDEDIT (Коммктрл. h)
description: Посылается, когда пользователь завершает операцию в поле ввода или выбрал элемент из раскрывающегося списка элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT кода уведомления элементы управления Windows
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
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414809"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Кбен \_ ЕНДЕДИТВ** (Юникод) и **кбен \_ ендедита** (ANSI)<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сведения об элементах управления ComboBoxEx](comboboxex-controls.md)
</dt> </dl>

 

 





