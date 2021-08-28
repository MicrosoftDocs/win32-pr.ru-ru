---
title: Сообщение WM_UNDO (Winuser. h)
description: Приложение отправляет \_ сообщение об отмене WM в элемент управления "поле ввода" для отмены последней операции. При отправке этого сообщения в элемент управления правки ранее удаленный текст восстанавливается или удаляется ранее добавленный текст.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- элементы управления Windows сообщений WM_UNDO
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6e4bd0715b7eeb5f99f34f5142ac3198c5c1eae53cf4486c3efce9dace19a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311344"
---
# <a name="wm_undo-message"></a>\_Сообщение об отмене WM

Приложение отправляет сообщение об **\_ отмене WM** в элемент управления "поле ввода" для отмены последней операции. При отправке этого сообщения в элемент управления правки ранее удаленный текст восстанавливается или удаляется ранее добавленный текст.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение прошло удачно, возвращается значение **true**.

Если сообщение не выполняется, возвращается значение **false**.

## <a name="remarks"></a>Remarks

**Расширенное редактирование:** Вместо команды **\_ отмены WM** рекомендуется использовать [**\_ отмену EM**](em-undo.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Другие ресурсы**
</dt> <dt>

[**WM \_ clear**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**\_копия WM**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**Вырезание WM \_**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**\_Вставка WM**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

