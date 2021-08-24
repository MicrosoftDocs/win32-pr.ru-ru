---
title: Сообщение TVM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Информирует элемент управления представлением дерева о необходимости установки расширенных стилей. Отправьте это сообщение или используйте макрос TreeView \_ сетекстендедстиле.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- элементы управления Windows сообщений TVM_SETEXTENDEDSTYLE
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
ms.openlocfilehash: d13d99a2f7a27475c30867f007f45d7525118d3077ebdce235c6bd33e1f8aafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750964"
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

## <a name="remarks"></a>Remarks

Расширенные стили для элемента управления "дерево" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

