---
title: Сообщение HDM_HITTEST (Коммктрл. h)
description: Проверяет точку, чтобы определить, какой элемент заголовка, если таковой имеется, находится в указанной точке.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- Элементы управления Windows для HDM_HITTEST сообщений
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b6634396dbd5ecd4510a4f7341fc6380dbb0ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136434"
---
# <a name="hdm_hittest-message"></a>\_Сообщение HITTEST HDM

Проверяет точку, чтобы определить, какой элемент заголовка, если таковой имеется, находится в указанной точке.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**хдхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) , которая содержит позиции для проверки и получает сведения о результатах теста.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента в указанной позиции, если таковой имеется, или значение 1 в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





