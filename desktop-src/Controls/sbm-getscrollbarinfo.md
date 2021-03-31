---
title: Сообщение SBM_GETSCROLLBARINFO (Winuser. h)
description: Отправляется приложением для получения сведений об указанной полосе прокрутки.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Элементы управления Windows для SBM_GETSCROLLBARINFO сообщений
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802182"
---
# <a name="sbm_getscrollbarinfo-message"></a>\_Сообщение СБМ жетскроллбаринфо

Отправляется приложением для получения сведений об указанной полосе прокрутки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**скроллбаринфо**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) , которая получает сведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**жетскроллбаринфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**скроллбаринфо**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

