---
title: Сообщение TVM_SHOWINFOTIP (Коммктрл. h)
description: Отображает всплывающую подсказку для указанного элемента в элементе управления "представление дерева". Это сообщение можно отправить явно или с помощью \_ макроса Шовинфотип TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- элементы управления Windows сообщений TVM_SHOWINFOTIP
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1cf61511e8c9e69c42d89f99fc4ddae90de78701e5e75170ff1b793671120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913924"
---
# <a name="tvm_showinfotip-message"></a>\_Сообщение TVM шовинфотип

Отображает всплывающую подсказку для указанного элемента в элементе управления "представление дерева". Это сообщение можно отправить явно или с помощью макроса [**\_ шовинфотип TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Маркер для элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль.

## <a name="remarks"></a>Remarks

Большинство приложений не используют это сообщение. Инфотипс отображаются автоматически. Дополнительные сведения см. в разделе Использование Инфотипс в представлении "Общие сведения [об элементах управления Tree-View](tree-view-controls.md) ".

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





