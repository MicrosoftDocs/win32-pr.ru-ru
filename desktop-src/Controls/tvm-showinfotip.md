---
title: Сообщение TVM_SHOWINFOTIP (Коммктрл. h)
description: Отображает всплывающую подсказку для указанного элемента в элементе управления "представление дерева". Это сообщение можно отправить явно или с помощью \_ макроса Шовинфотип TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Элементы управления Windows для TVM_SHOWINFOTIP сообщений
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
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892714"
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

## <a name="remarks"></a>Комментарии

Большинство приложений не используют это сообщение. Инфотипс отображаются автоматически. Дополнительные сведения см. в разделе Использование Инфотипс в представлении "Общие сведения [об элементах управления Tree-View](tree-view-controls.md) ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





