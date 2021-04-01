---
title: Сообщение EM_REQUESTRESIZE (RichEdit. h)
description: Заставляет расширенный элемент управления "поле ввода" Отправить \_ код уведомления EN рекуестресизе в его родительское окно.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Элементы управления Windows для EM_REQUESTRESIZE сообщений
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262222"
---
# <a name="em_requestresize-message"></a>\_Сообщение РЕКУЕСТРЕСИЗЕ EM

Заставляет расширенный элемент управления "поле ввода" отправить код уведомления [**en \_ рекуестресизе**](en-requestresize.md) в его родительское окно.

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

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Это сообщение полезно при обработке [**\_ размера WM**](/windows/desktop/winmsg/wm-size) для родителя элемента управления неформатированного редактирования самого нижнего уровня.

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

[**EN \_ рекуестресизе**](en-requestresize.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_Размер WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

