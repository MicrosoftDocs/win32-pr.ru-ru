---
title: Сообщение LVM_GETITEMPOSITION (Коммктрл. h)
description: Возвращает позицию элемента представления списка. Это сообщение можно отправить явно или с помощью \_ макроса Жетитемпоситион ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Элементы управления Windows для LVM_GETITEMPOSITION сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892453"
---
# <a name="lvm_getitemposition-message"></a>\_Сообщение LVM жетитемпоситион

Возвращает позицию элемента представления списка. Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемпоситион ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс элемента представления списка.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , которая получает позицию верхнего левого угла элемента в координатах представления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

