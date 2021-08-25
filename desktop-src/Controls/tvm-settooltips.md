---
title: Сообщение TVM_SETTOOLTIPS (Коммктрл. h)
description: Задает элемент управления дочерней подсказкой элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Сеттултипс TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- элементы управления Windows сообщений TVM_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd18a5217db0d105841722d208904c1b65199504750576acf1ff8035f31bd585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913964"
---
# <a name="tvm_settooltips-message"></a>\_Сообщение TVM сеттултипс

Задает элемент управления дочерней подсказкой элемента управления "дерево-представление". Это сообщение можно отправить явно или с помощью макроса [**\_ сеттултипс TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик для элемента управления ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер элемента управления ToolTip, установленный ранее для элемента управления "дерево-представление", или **значение NULL** , если подсказки ранее не использовались.

## <a name="remarks"></a>Remarks

При создании элементы управления "представление в виде дерева" автоматически создают дочерний элемент управления ToolTip. Чтобы элемент управления "дерево" не использовал всплывающие подсказки, создайте элемент управления с стилем " [**\_ подсказки" телевизоров**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**TVM \_ подсказки**](tvm-gettooltips.md)
</dt> </dl>

 

 





