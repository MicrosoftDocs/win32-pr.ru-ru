---
title: Сообщение EM_NOSETFOCUS (Коммктрл. h)
description: Предотвращает получение фокуса клавиатуры с помощью однострочного элемента управления Edit Control. Это сообщение можно отправить явным образом или с помощью \_ макроса Edit носетфокус.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- Элементы управления Windows для EM_NOSETFOCUS сообщений
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136847"
---
# <a name="em_nosetfocus-message"></a>\_Сообщение НОСЕТФОКУС EM

\[Предназначен для внутреннего использования; не рекомендуется для использования в приложениях. Это сообщение может не поддерживаться в будущих версиях Windows.\]

Предотвращает получение фокуса клавиатуры с помощью однострочного элемента управления Edit Control. Это сообщение можно отправить явным образом или с помощью макроса [**Edit \_ носетфокус**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .

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

Возвращаемое значение не используется.

## <a name="security-considerations"></a>Соображения безопасности

Использование этого сообщения может нарушить безопасность программы.

## <a name="remarks"></a>Комментарии

Это сообщение пропускается, если элемент управления "поле ввода" не является элементом управления "поле ввода" с одной строкой.

После отправки сообщения этот результат будет постоянным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**Изменить \_ носетфокус**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM \_ такефокус**](em-takefocus.md)
</dt> </dl>

 

 





