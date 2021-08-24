---
title: Сообщение TB_INDETERMINATE (Коммктрл. h)
description: Задает или очищает неопределенное состояние указанной кнопки на панели инструментов.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- элементы управления Windows сообщений TB_INDETERMINATE
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90845f269d0af1e690d5ddeb02f2a8ec2a2f63ff4f698f1dd0f3e2729d98b72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078268"
---
# <a name="tb_indeterminate-message"></a>\_Неопределенное сообщение ТБ

Задает или очищает неопределенное состояние указанной кнопки на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор команды, неопределенное состояние которой необходимо установить или удалить.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **логическое** значение, указывающее, следует ли устанавливать или очищать неопределенное состояние. При **значении true** задается неопределенное состояние. Если **значение равно false**, состояние снимается.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) должен быть равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

