---
title: Сообщение TVM_GETCOUNT (Коммктрл. h)
description: Извлекает число элементов в элементе управления "дерево". Это сообщение можно отправить явным образом или с помощью \_ макроса TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- элементы управления Windows сообщений TVM_GETCOUNT
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fce2d3ed6580acc875007ff3962bbeb21e9c0d3c3cb38128a2339da79597f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060354"
---
# <a name="tvm_getcount-message"></a>TVM \_ ВЫчислить сообщение

Извлекает число элементов в элементе управления "дерево". Это сообщение можно отправить явным образом или с помощью макроса [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число элементов.

## <a name="remarks"></a>Remarks

Число узлов, возвращенное [**TreeView- \_ Count**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) , ограничено целыми значениями. При добавлении узла за пределами 32767 макрос возвращает отрицательное значение. После добавления 65536 узлов счетчик возвращается к нулю. В этом случае элемент управления "представление дерева" отображается как пустой без полос прокрутки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





