---
title: Сообщение EM_REQUESTRESIZE (RichEdit. h)
description: Заставляет расширенный элемент управления "поле ввода" Отправить \_ код уведомления EN рекуестресизе в его родительское окно.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- элементы управления Windows сообщений EM_REQUESTRESIZE
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
ms.openlocfilehash: 7113f52e2fa3a293549443f779ba937bf20b85736c6751cd9ab77bdbecd45c3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440164"
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

## <a name="remarks"></a>Remarks

Это сообщение полезно при обработке [**\_ размера WM**](/windows/desktop/winmsg/wm-size) для родителя элемента управления неформатированного редактирования самого нижнего уровня.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылка**
</dt> <dt>

[**EN \_ рекуестресизе**](en-requestresize.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_Размер WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

