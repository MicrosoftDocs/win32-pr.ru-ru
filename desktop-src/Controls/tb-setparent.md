---
title: Сообщение TB_SETPARENT (Коммктрл. h)
description: Задает окно, в котором элемент управления "панель инструментов" отправляет сообщения уведомления.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- элементы управления Windows сообщений TB_SETPARENT
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd97cdab230317feea65f2bffce74a7dec34ee336d69bb46ec4c6963ca9b3eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078148"
---
# <a name="tb_setparent-message"></a>\_Сообщение СЕТПАРЕНТ ТБ

Задает окно, в котором элемент управления "панель инструментов" отправляет сообщения уведомления.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик окна для получения сообщений с уведомлениями.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение представляет собой обработчик предыдущего окна уведомления или **значение NULL** , если предыдущее окно уведомления отсутствует.

## <a name="remarks"></a>Remarks

Сообщение **\_ Сетпарент в ТБ** не изменяет родительское окно, указанное при создании элемента управления. Вызов функции [**"**](/windows/desktop/api/winuser/nf-winuser-getparent) noreturn" для элемента управления ToolBar возвратит фактическое родительское окно, а не окно, указанное **в \_ сетпарент ТБ**. Чтобы изменить родительское окно элемента управления, вызовите функцию [**сетпарент**](/windows/desktop/api/winuser/nf-winuser-setparent) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

