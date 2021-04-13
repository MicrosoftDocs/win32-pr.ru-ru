---
title: Сообщение TVM_GETTOOLTIPS (Коммктрл. h)
description: Получает маркер для дочернего элемента управления ToolTip, используемого элементом управления "дерево-представление". Это сообщение можно отправить явным образом или с помощью \_ макроса TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Элементы управления Windows для TVM_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489789"
---
# <a name="tvm_gettooltips-message"></a>Сообщение TVM с \_ ПОДсказками

Получает маркер для дочернего элемента управления ToolTip, используемого элементом управления "дерево-представление". Это сообщение можно отправить явным образом или с помощью макроса [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на дочерний элемент управления ToolTip или **значение NULL** , если элемент управления не использует подсказки.

## <a name="remarks"></a>Комментарии

При создании элементы управления "представление в виде дерева" автоматически создают дочерний элемент управления ToolTip. Чтобы элемент управления "дерево" не использовал подсказки, создайте элемент управления с стилем " [**\_ подсказки" телевизоров**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ сеттултипс**](tvm-settooltips.md)
</dt> </dl>

 

 





