---
title: Сообщение TDM_ENABLE_BUTTON (Коммктрл. h)
description: Включает или отключает кнопку отправки в диалоговом окне задачи.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- Элементы управления Windows для TDM_ENABLE_BUTTON сообщений
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654683"
---
# <a name="tdm_enable_button-message"></a>\_ \_ Сообщение кнопки "включить TDM"

Включает или отключает кнопку отправки в диалоговом окне задачи.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* \[ окне\]
</dt> <dd>

Значение **типа int** , указывающее идентификатор кнопки, которая должна быть включена или отключена.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указывает состояние кнопки. Задайте значение 0, чтобы отключить кнопку. Задайте для параметра значение ненулевой, чтобы включить кнопку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





