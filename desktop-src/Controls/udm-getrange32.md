---
title: Сообщение UDM_GETRANGE32 (Коммктрл. h)
description: Извлекает 32-разрядный диапазон элемента управления "вверх/вниз".
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- Элементы управления Windows для UDM_GETRANGE32 сообщений
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490182"
---
# <a name="udm_getrange32-message"></a>\_Сообщение GETRANGE32 UDM

Извлекает 32-разрядный диапазон элемента управления "вверх/вниз".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указатель на целое число со знаком, которое получает нижнюю границу диапазона управления "вверх/вниз". Этот параметр может иметь **значение NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на целое число со знаком, которое получает верхний предел диапазона управления "вверх/вниз". Этот параметр может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





