---
title: Сообщение TVM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент и все его дочерние элементы из элемента управления представления в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса DeleteItem TreeView.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- элементы управления Windows сообщений TVM_DELETEITEM
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
ms.openlocfilehash: 7ef0165ffaf1f0f04b32cda43e21c97fed012ad6d61b32f8919612f8924f7c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018692"
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

## <a name="remarks"></a>Remarks

Удалять элементы в ответ на уведомление, например [ТВН \_ селчангинг](tvn-selchanging.md), необязательно.

После удаления элемента его маркер является недопустимым и не может быть использован.

Родительское окно получает код уведомления [ТВН \_ DELETEITEM](tvn-deleteitem.md) при удалении каждого элемента.

Если метка элемента редактируется, операция редактирования отменяется, а родительское окно получает код уведомления [ТВН \_ ендлабеледит](tvn-endlabeledit.md) .

Если удалить все элементы в элементе управления "дерево", у которого есть [**стиль \_ прокрутки "телевизоры**](tree-view-control-window-styles.md) ", элементы, добавленные позднее, могут отображаться неправильно. Дополнительные сведения см. в разделе [**TreeView \_ делетеаллитемс**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





