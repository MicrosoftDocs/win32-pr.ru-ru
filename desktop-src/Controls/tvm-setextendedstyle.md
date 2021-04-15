---
title: Сообщение TVM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Информирует элемент управления представлением дерева о необходимости установки расширенных стилей. Отправьте это сообщение или используйте макрос TreeView \_ сетекстендедстиле.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Элементы управления Windows для TVM_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534343"
---
# <a name="tvm_setextendedstyle-message"></a>\_Сообщение TVM сетекстендедстиле

Информирует элемент управления представлением дерева о необходимости установки расширенных стилей. Отправьте это сообщение или используйте макрос [**TreeView \_ сетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маска, используемая для выбора устанавливаемых стилей.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение, указывающее расширенный стиль. Дополнительные сведения о стилях см. в разделе [Расширенные стили элемента управления "дерево-представление](tree-view-control-window-extended-styles.md)".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это сообщение завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Расширенные стили для элемента управления "дерево" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

