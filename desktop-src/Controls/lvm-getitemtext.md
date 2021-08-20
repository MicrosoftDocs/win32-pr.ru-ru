---
title: Сообщение LVM_GETITEMTEXT (Коммктрл. h)
description: Извлекает текст элемента представления списка или подэлемента. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемтекст ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- элементы управления Windows сообщений LVM_GETITEMTEXT
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d5292f9814b3ef62667d44582eab44a2f18ac6c274682d180dd26f1b7cdd9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062584"
---
# <a name="lvm_getitemtext-message"></a>\_Сообщение LVM жетитемтекст

Извлекает текст элемента представления списка или подэлемента. Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемтекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента представления списка.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Чтобы получить текст элемента, задайте для **iSubItem** значение 0. Чтобы получить текст подэлемента, установите **iSubItem** в качестве индекса подэлемента. Элемент **псзтекст** указывает на буфер, который получает текст. Элемент **кчтекстмакс** указывает количество символов в буфере.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение отправляется явным образом, оно возвращает число символов в элементе **псзтекст** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="remarks"></a>Remarks

Это сообщение можно также отправить, вызвав макрос [**\_ жетитемтекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) . Однако этот макрос не возвращает длину строки.

**LVM \_ ЖЕТИТЕМТЕКСТ** не поддерживается в стиле [**LVS \_ овнердата**](list-view-window-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **LVM \_ ЖЕТИТЕМТЕКСТВ** (Юникод) и **LVM \_ жетитемтекста** (ANSI)<br/>           |



 

 





