---
title: Сообщение LVM_SETITEMPOSITION32 (Коммктрл. h)
description: Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- элементы управления Windows сообщений LVM_SETITEMPOSITION32
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
ms.openlocfilehash: 737b9aa78067bd4851c907da4ac51bd2645a833d8f3335c90a6e81a902d3a30a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656254"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

