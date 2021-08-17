---
title: Сообщение EM_NOSETFOCUS (Коммктрл. h)
description: Предотвращает получение фокуса клавиатуры с помощью однострочного элемента управления Edit Control. Это сообщение можно отправить явным образом или с помощью \_ макроса Edit носетфокус.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- элементы управления Windows сообщений EM_NOSETFOCUS
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
ms.openlocfilehash: 02ac35a30ff3deac7e9d6d227a6e8c403e6096e272ea89067dd817add9b2426e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831197"
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

## <a name="remarks"></a>Remarks

Это сообщение пропускается, если элемент управления "поле ввода" не является элементом управления "поле ввода" с одной строкой.

После отправки сообщения этот результат будет постоянным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**Изменить \_ носетфокус**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM \_ такефокус**](em-takefocus.md)
</dt> </dl>

 

 





