---
description: отправляется в приложение, которое инициировало обучение с помощью Windows справки.
title: Сообщение WM_TCARD (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85435c5674ad6a2ac4e05edaa5d450dc61de9eac6dae05d3b19662aec91a61f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856989"
---
# <a name="wm_tcard-message"></a>\_Сообщение ТКАРД WM

отправляется в приложение, которое инициировало обучение с помощью Windows справки. Сообщение информирует приложение, когда пользователь щелкает настраиваемую кнопку. Приложение инициирует учебную карточку, указывая \_ команду Help ткард в вызове функции [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*идактион* 
</dt> <dd>

Значение, указывающее действие, выполненное пользователем. Это может быть одно из следующих значений.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**идаборт**


</dt> <dd>

Пользователь щелкнул настраиваемую кнопку **прерывания** .

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**идканцел**


</dt> <dd>

Пользователь щелкнул настраиваемую кнопку **отмены** .

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**идклосе**


</dt> <dd>

Пользователь закрыл карточку обучения.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**идхелп**


</dt> <dd>

пользователь щелкнул Windows кнопку " **справка** ".

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**идигноре**


</dt> <dd>

Пользователь щелкнул кнопку " **пропустить** ", которая является автором.

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**идок**


</dt> <dd>

Пользователь щелкнул настраиваемую кнопку **ОК** .

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**идно**


</dt> <dd>

Пользователь щелкнул элемент "Автор" **без** кнопки.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**идретри**


</dt> <dd>

Пользователь щелкнул настраиваемую кнопку **повтора** .

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**Справка \_ ткард \_ данных**


</dt> <dd>

Пользователь щелкнул настраиваемую кнопку. Параметр *двактиондата* содержит длинное целое число, заданное автором справки.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**Помогите \_ ткард \_ другим \_ вызывающим**


</dt> <dd>

Другое приложение запросило карточки обучения.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**идес**


</dt> <dd>

Пользователь щелкнул настраиваемую кнопку **Да** .

</dd> </dl> </dd> <dt>

*двактиондата* 
</dt> <dd>

Если *идактион* указывает Help \_ ткард \_ Data, этот параметр является **длинным** , заданным автором справки. В противном случае этот параметр равен нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется; Используйте нуль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 




