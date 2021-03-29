---
title: Сообщение TVM_GETCOUNT (Коммктрл. h)
description: Извлекает число элементов в элементе управления "дерево". Это сообщение можно отправить явным образом или с помощью \_ макроса TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Элементы управления Windows для TVM_GETCOUNT сообщений
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
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492372"
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

## <a name="remarks"></a>Комментарии

Число узлов, возвращенное [**TreeView- \_ Count**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) , ограничено целыми значениями. При добавлении узла за пределами 32767 макрос возвращает отрицательное значение. После добавления 65536 узлов счетчик возвращается к нулю. В этом случае элемент управления "представление дерева" отображается как пустой без полос прокрутки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





