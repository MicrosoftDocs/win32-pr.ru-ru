---
title: Сообщение LB_GETLOCALE (Winuser. h)
description: Возвращает текущий языковой стандарт для списка. Языковой стандарт можно использовать для определения правильного порядка сортировки отображаемого текста (для списков с \_ стилем сортировки фунтов) и текста, добавленного \_ сообщением ADDSTRING балансировки нагрузки.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- элементы управления Windows сообщений LB_GETLOCALE
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
ms.openlocfilehash: 732bfac72502c38265f7c1651667dc235c440293c8435f16088eaee775a874f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544524"
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

## <a name="remarks"></a>Remarks

Идентификатор языка состоит из идентификатора подязыка и основного идентификатора языка. Используйте макрос [**примарилангид**](/windows/desktop/api/winnt/nf-winnt-primarylangid) для извлечения идентификатора основного языка из [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) возвращаемого значения и макроса [**сублангид**](/windows/desktop/api/winnt/nf-winnt-sublangid) для извлечения идентификатора этого языка.

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

 

