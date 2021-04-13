---
title: Сообщение EM_GETEXTENDEDSTYLE (Коммктрл. h)
description: Возвращает расширенный стиль для элемента управления "поле ввода". Отправьте это сообщение явным образом или с помощью \_ макроса Edit жетекстендедстиле.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Элементы управления Windows для EM_GETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491814"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>Сообщение EM_GETEXTENDEDSTYLE (Коммктрл. h)

Возвращает расширенный стиль для элемента управления "дерево-представление". Отправьте это сообщение явным образом или с помощью макроса [**Edit \_ жетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение расширенного стиля. Дополнительные сведения о стилях см. в разделе [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Комментарии

Расширенные стили для элемента управления "поле ввода" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1809\]<br/>                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

