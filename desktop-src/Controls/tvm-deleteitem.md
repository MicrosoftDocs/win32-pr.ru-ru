---
title: Сообщение TVM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент и все его дочерние элементы из элемента управления представления в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса DeleteItem TreeView.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- Элементы управления Windows для TVM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490845"
---
# <a name="tvm_deleteitem-message"></a>\_Сообщение TVM DELETEITEM

Удаляет элемент и все его дочерние элементы из элемента управления представления в виде дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ DeleteItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

**Хтриитем** для удаляемого элемента. Если параметру *lParam* присвоено значение Тви \_ root или **null**, удаляются все элементы. Для удаления всех элементов можно также использовать макрос [**\_ делетеаллитемс TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Удалять элементы в ответ на уведомление, например [ТВН \_ селчангинг](tvn-selchanging.md), необязательно.

После удаления элемента его маркер является недопустимым и не может быть использован.

Родительское окно получает код уведомления [ТВН \_ DELETEITEM](tvn-deleteitem.md) при удалении каждого элемента.

Если метка элемента редактируется, операция редактирования отменяется, а родительское окно получает код уведомления [ТВН \_ ендлабеледит](tvn-endlabeledit.md) .

Если удалить все элементы в элементе управления "дерево", у которого есть [**стиль \_ прокрутки "телевизоры**](tree-view-control-window-styles.md) ", элементы, добавленные позднее, могут отображаться неправильно. Дополнительные сведения см. в разделе [**TreeView \_ делетеаллитемс**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





