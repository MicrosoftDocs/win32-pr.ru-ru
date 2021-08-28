---
title: Сообщение SBM_GETRANGE (Winuser. h)
description: Сообщение СБМ \_ -Range отправляется для получения минимального и максимального значений позиционирования для элемента управления "полоса прокрутки".
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- элементы управления Windows сообщений SBM_GETRANGE
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e66c6e7bf79c270d66fdeac0ece1a1ce82ed813d1638be3587be7237ecd30e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770044"
---
# <a name="sbm_getrange-message"></a>Сообщение СБМного \_ диапазона

Сообщение **СБМ- \_ Range** отправляется для получения минимального и максимального значений позиционирования для элемента управления "полоса прокрутки".

Приложения не должны отсылать это сообщение напрямую. Вместо этого они должны использовать функцию [**жетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Приложения, которые реализуют пользовательский элемент управления "полоса прокрутки", должны отвечать на эти сообщения, чтобы функция **жетскроллранже** работала правильно.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указатель на переменную, которая получает минимальное расположение прокрутки.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на переменную, которая получает максимальное значение позиции прокрутки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**СБМ \_ жетпос**](sbm-getpos.md)
</dt> <dt>

[**СБМ \_ сетпос**](sbm-setpos.md)
</dt> <dt>

[**СБМ \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**СБМ \_ сетранжередрав**](sbm-setrangeredraw.md)
</dt> </dl>

 

