---
title: Сообщение TVM_SETITEMHEIGHT (Коммктрл. h)
description: Задает высоту элементов представления дерева. Это сообщение можно отправить явно или с помощью \_ макроса Сетитемхеигхт TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Элементы управления Windows для TVM_SETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988817"
---
# <a name="tvm_setitemheight-message"></a>\_Сообщение TVM сетитемхеигхт

Задает высоту элементов представления дерева. Это сообщение можно отправить явно или с помощью макроса [**\_ сетитемхеигхт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Новая высота каждого элемента в представлении в виде дерева (в пикселях). Высота меньше 1 будет равна 1. Если этот аргумент не является четным, а элемент управления "представление дерева" не имеет [**стиля \_ Ноневенхеигхт "телевизоры**](tree-view-control-window-styles.md) ", это значение округляется вниз до ближайшего четного значения. Если этот аргумент равен-1, элемент управления вернется к использованию высоты элемента по умолчанию.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущую высоту элементов в пикселях.

## <a name="remarks"></a>Комментарии

Элемент управления "представление дерева" использует это значение для высоты всех элементов. Чтобы изменить высоту отдельных элементов, см. Описание элемента **иинтеграл** структуры [**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 





