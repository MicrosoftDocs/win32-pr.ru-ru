---
title: Сообщение TVM_GETITEMHEIGHT (Коммктрл. h)
description: Извлекает текущую высоту каждого элемента представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса GetItemHeight TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- Элементы управления Windows для TVM_GETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892786"
---
# <a name="tvm_getitemheight-message"></a>\_Сообщение TVM GETITEMHEIGHT

Извлекает текущую высоту каждого элемента представления дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ GetItemHeight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает высоту каждого элемента в пикселях.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ сетитемхеигхт**](tvm-setitemheight.md)
</dt> </dl>

 

 





