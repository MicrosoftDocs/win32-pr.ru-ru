---
title: Сообщение LVM_HITTEST (Коммктрл. h)
description: Определяет, какой элемент списка (если имеется) находится в указанной позиции. Это сообщение можно отправить явно или с помощью \_ макроса HitTest ListView.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- элементы управления Windows сообщений LVM_HITTEST
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81308249992b134dd3fa2bd0bc43ff0074bc3bae7048072ada7d68b0a867a979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958173"
---
# <a name="lvm_hittest-message"></a>\_Сообщение LVM HITTEST

Определяет, какой элемент списка (если имеется) находится в указанной позиции. Это сообщение можно отправить явно или с помощью макроса [**\_ HitTest ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должно быть равно 0. **Windows Системе.** Должен быть равен-1, если необходимо извлечь элементы **играуп** и **iSubItem** структуры *lParam* .</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) , которая содержит позиции для проверки попадания и получает сведения о результатах проверки попадания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента в указанной позиции, если таковой имеется, или значение-1 в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





