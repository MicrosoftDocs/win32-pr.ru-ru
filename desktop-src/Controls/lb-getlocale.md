---
title: Сообщение LB_GETLOCALE (Winuser. h)
description: Возвращает текущий языковой стандарт для списка. Языковой стандарт можно использовать для определения правильного порядка сортировки отображаемого текста (для списков с \_ стилем сортировки фунтов) и текста, добавленного \_ сообщением ADDSTRING балансировки нагрузки.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Элементы управления Windows для LB_GETLOCALE сообщений
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491181"
---
# <a name="lb_getlocale-message"></a>\_Сообщение о НЕстандартной балансировке нагрузки

Возвращает текущий языковой стандарт для списка. Языковой стандарт можно использовать для определения правильного порядка сортировки отображаемого текста (для списков с стилем [**\_ сортировки фунтов**](list-box-styles.md) ) и текста, добавленного сообщением [**\_ ADDSTRING балансировки нагрузки**](lb-addstring.md) .

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

Возвращаемое значение указывает текущий языковой стандарт для списка. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит код страны или региона, а [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор языка.

## <a name="remarks"></a>Комментарии

Идентификатор языка состоит из идентификатора подязыка и основного идентификатора языка. Используйте макрос [**примарилангид**](/windows/desktop/api/winnt/nf-winnt-primarylangid) для извлечения идентификатора основного языка из [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) возвращаемого значения и макроса [**сублангид**](/windows/desktop/api/winnt/nf-winnt-sublangid) для извлечения идентификатора этого языка.

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

[**ADDSTRING балансировки нагрузки \_**](lb-addstring.md)
</dt> <dt>

[**ФУНТОВая \_ SETLOCALE**](lb-setlocale.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**примарилангид**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**сублангид**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

