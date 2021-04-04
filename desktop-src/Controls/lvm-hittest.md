---
title: Сообщение LVM_HITTEST (Коммктрл. h)
description: Определяет, какой элемент списка (если имеется) находится в указанной позиции. Это сообщение можно отправить явно или с помощью \_ макроса HitTest ListView.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Элементы управления Windows для LVM_HITTEST сообщений
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
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989170"
---
# <a name="lvm_hittest-message"></a>\_Сообщение LVM HITTEST

Определяет, какой элемент списка (если имеется) находится в указанной позиции. Это сообщение можно отправить явно или с помощью макроса [**\_ HitTest ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должно быть равно 0. **Windows Vista.** Должен быть равен-1, если необходимо извлечь элементы **играуп** и **iSubItem** структуры *lParam* .</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) , которая содержит позиции для проверки попадания и получает сведения о результатах проверки попадания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента в указанной позиции, если таковой имеется, или значение-1 в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





