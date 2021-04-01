---
title: Сообщение CB_GETLOCALE (Winuser. h)
description: Возвращает текущий языковой стандарт поля со списком. Языковой стандарт используется для определения правильного порядка сортировки отображаемого текста для полей со списком, имеющих \_ стиль сортировки CBS и текст, добавленный с помощью \_ сообщения ADDSTRING CB.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Элементы управления Windows для CB_GETLOCALE сообщений
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071615"
---
# <a name="cb_getlocale-message"></a>\_Сообщение о локализации CB

Возвращает текущий языковой стандарт поля со списком. Языковой стандарт используется для определения правильного порядка сортировки отображаемого текста для полей со списком, имеющих [**стиль \_ сортировки CBS**](combo-box-styles.md) и текст, добавленный с помощью сообщения [**\_ ADDSTRING CB**](cb-addstring.md) .

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

Возвращаемое значение задает текущий языковой стандарт для поля со списком. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит код страны или региона, а [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор языка.

## <a name="remarks"></a>Комментарии

Идентификатор языка состоит из идентификатора подязыка и основного идентификатора языка. Макрос [**примарилангид**](/windows/desktop/api/winnt/nf-winnt-primarylangid) получает основной идентификатор языка, а макрос [**сублангид**](/windows/desktop/api/winnt/nf-winnt-sublangid) получает идентификатор этого языка.

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

[**\_ADDSTRING CB**](cb-addstring.md)
</dt> <dt>

[**CB \_ SETLOCALE**](cb-setlocale.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**примарилангид**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**сублангид**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

