---
title: Код уведомления EN_ALIGN_RTL_EC (Winuser. h)
description: Посылается, когда пользователь изменяет направление элемента управления Edit на "справа налево". Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b44ecd143715eb5c1bc895ca5c20fa066b17b71ab31ee667e2d6b2b6a0852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437094"
---
# <a name="en_align_rtl_ec-notification-code"></a>EN — \_ выровняйте \_ \_ код уведомления EC справа налево

Посылается, когда пользователь изменяет направление элемента управления Edit на "справа налево". Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода". [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер элемента управления редактирования, отправляющего код уведомления.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если в системе установлен двунаправленный язык, например арабский или иврит, можно изменить направление элемента управления редактирования с помощью клавиш CTRL + ЛШИФТ (слева направо) и CTRL + РШИФТ (справа налево).

**Расширенное редактирование:** Этот код уведомления не поддерживается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

