---
title: Сообщение LVM_GETITEMTEXT (Коммктрл. h)
description: Извлекает текст элемента представления списка или подэлемента. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемтекст ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Элементы управления Windows для LVM_GETITEMTEXT сообщений
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
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137114"
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

## <a name="remarks"></a>Комментарии

Это сообщение можно также отправить, вызвав макрос [**\_ жетитемтекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) . Однако этот макрос не возвращает длину строки.

**LVM \_ ЖЕТИТЕМТЕКСТ** не поддерживается в стиле [**LVS \_ овнердата**](list-view-window-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **LVM \_ ЖЕТИТЕМТЕКСТВ** (Юникод) и **LVM \_ жетитемтекста** (ANSI)<br/>           |



 

 





