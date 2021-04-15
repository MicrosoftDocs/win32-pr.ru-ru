---
title: Сообщение TB_SETCMDID (Коммктрл. h)
description: Задает идентификатор команды для кнопки панели инструментов.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- Элементы управления Windows для TB_SETCMDID сообщений
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654517"
---
# <a name="tb_setcmdid-message"></a>\_Сообщение СЕТКМДИД ТБ

Задает идентификатор команды для кнопки панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс кнопки, идентификатор команды которого необходимо задать.

</dd> <dt>

*lParam* 
</dt> <dd>

Идентификатор команды.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





