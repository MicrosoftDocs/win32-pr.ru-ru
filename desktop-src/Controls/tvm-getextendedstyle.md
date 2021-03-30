---
title: Сообщение TVM_GETEXTENDEDSTYLE (Коммктрл. h)
description: Возвращает расширенный стиль для элемента управления "дерево-представление". Отправьте это сообщение явно или с помощью \_ макроса Жетекстендедстиле TreeView.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Элементы управления Windows для TVM_GETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892605"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>Сообщение TVM_GETEXTENDEDSTYLE (Коммктрл. h)

Возвращает расширенный стиль для элемента управления "дерево-представление". Отправьте это сообщение явно или с помощью макроса [**\_ жетекстендедстиле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение расширенного стиля. Дополнительные сведения о стилях см. в разделе [Расширенные стили элемента управления "дерево-представление](tree-view-control-window-extended-styles.md)".

## <a name="remarks"></a>Комментарии

Расширенные стили для элемента управления "дерево" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

