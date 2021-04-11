---
title: Код уведомления EN_UPDATE (Winuser. h)
description: Посылается, когда элемент управления "изменение" собирается перерисовывать себя.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137146"
---
# <a name="en_update-notification-code"></a>\_Код уведомления об обновлении EN

Посылается, когда элемент управления "изменение" собирается перерисовывать себя. Этот код уведомления отправляется после того, как элемент управления отформатирует текст, но перед отображением текста. Это позволяет изменить размер окна элемента управления редактированием, если это необходимо. Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_UPDATE

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

Маркер для элемента управления "поле ввода".

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Расширенное редактирование 1,0:** Чтобы получить \_ коды уведомлений о коротком обновлении, укажите [**\_ Обновление енм**](rich-edit-control-event-mask-flags.md) в маске, отправленной с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

**Расширенное редактирование 2,0 и более поздних версий:** Флаг [**\_ обновления енм**](rich-edit-control-event-mask-flags.md) игнорируется. \_Всегда получается код уведомления о коротком обновлении. Тем не менее, когда Microsoft Rich Editing 3,0 эмулирует Microsoft Rich Edit 1,0, чтобы получить \_ коды уведомлений для обновления EN, необходимо указать **енм \_ Обновление** в маске, отправленной с сообщением [**\_ SETEVENTMASK EM**](em-seteventmask.md) .

Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[\_изменение EN](en-change.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

