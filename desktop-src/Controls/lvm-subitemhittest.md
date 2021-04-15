---
title: Сообщение LVM_SUBITEMHITTEST (Коммктрл. h)
description: Определяет, какой элемент представления списка или подэлемент находится в заданной позиции. Это сообщение можно отправить явно или с помощью \_ макроса Субитемхиттест ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Элементы управления Windows для LVM_SUBITEMHITTEST сообщений
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489258"
---
# <a name="lvm_subitemhittest-message"></a>\_Сообщение LVM субитемхиттест

Определяет, какой элемент представления списка или подэлемент находится в заданной позиции. Это сообщение можно отправить явно или с помощью макроса [**\_ субитемхиттест ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должно быть равно 0. **Windows Vista.** Должен быть равен-1, если требуется извлечь элемент **играуп** объекта *lParam* .</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) . Для структуры [**точек**](/previous-versions//dd162805(v=vs.85)) в **лвхиттестинфо** должны быть заданы клиентские координаты для проверки попадания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента или подэлемента, который был протестирован, если он есть, или значение-1 в противном случае. Если элемент или подэлемент имеет заданные координаты, поля структуры [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) будут заполнены соответствующими сведениями о попадании.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

