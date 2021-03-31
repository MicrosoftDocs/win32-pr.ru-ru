---
title: Сообщение TB_INDETERMINATE (Коммктрл. h)
description: Задает или очищает неопределенное состояние указанной кнопки на панели инструментов.
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- Элементы управления Windows для TB_INDETERMINATE сообщений
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
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071449"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

