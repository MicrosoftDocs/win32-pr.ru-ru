---
title: Код уведомления EN_DROPFILES (RichEdit. h)
description: Сообщает родительскому окну элемента управления Rich Edit, что пользователь пытается удалить файлы в элемент управления. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify при получении сообщения WM \_ дропфилес.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8813d3d62883ab607bb898f4aa34a664cbab47b2c8214fbd83fc8cc7913e26ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047784"
---
# <a name="en_dropfiles-notification-code"></a>\_Код уведомления EN дропфилес

Сообщает родительскому окну элемента управления Rich Edit, что пользователь пытается удалить файлы в элемент управления. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) при получении сообщения [**WM \_ дропфилес**](/windows/desktop/shell/wm-dropfiles) .


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**ендропфилес**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) , которая получает сведения о пропущенных файлах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Чтобы разрешить операцию Drop, возвращайте ненулевое значение.

Возвращает ноль, чтобы пропустить операцию Drop.

## <a name="remarks"></a>Remarks

Чтобы элемент управления "поле ввода" получал сообщения [**WM \_ дропфилес**](/windows/desktop/shell/wm-dropfiles) , родительское окно должно зарегистрировать элемент управления как цель перетаскивания с помощью функции [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) . Элемент управления не регистрирует сам себя.

Чтобы получить \_ коды уведомлений EN дропфилес, укажите [**енм \_ дропфилес**](rich-edit-control-event-mask-flags.md) в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

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

[**ендропфилес**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

