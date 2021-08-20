---
title: Сообщение EM_GETEXTENDEDSTYLE (Коммктрл. h)
description: Возвращает расширенный стиль для элемента управления "поле ввода". Отправьте это сообщение явным образом или с помощью \_ макроса Edit жетекстендедстиле.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- элементы управления Windows сообщений EM_GETEXTENDEDSTYLE
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
ms.openlocfilehash: 77aa5827cc256c040d34ca24574dfa0b12816accaff9e5c0e92b4400195cae2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019672"
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

## <a name="remarks"></a>Remarks

Расширенные стили для элемента управления "поле ввода" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, версия 1809 \[ только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2019\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

