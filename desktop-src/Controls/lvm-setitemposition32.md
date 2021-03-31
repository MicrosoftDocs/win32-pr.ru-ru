---
title: Сообщение LVM_SETITEMPOSITION32 (Коммктрл. h)
description: Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Элементы управления Windows для LVM_SETITEMPOSITION32 сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071682"
---
# <a name="lvm_setitemposition32-message"></a>\_Сообщение LVM SETITEMPOSITION32

Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка). Это сообщение отличается от сообщения [**LVM \_ сетитемпоситион**](lvm-setitemposition.md) тем, что оно использует 32-разрядные координаты. Это сообщение можно отправить явно или с помощью макроса [**\_ SetItemPosition32 ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента представления списка, для которого задается позиция.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , содержащую новую позицию элемента, в координатах представления списка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

