---
title: Сообщение TB_SETDISABLEDIMAGELIST (Коммктрл. h)
description: Задает список изображений, который будет использоваться элементом управления Toolbar для вывода отключенных кнопок.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- Элементы управления Windows для TB_SETDISABLEDIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071857"
---
# <a name="tb_setdisabledimagelist-message"></a>\_Сообщение СЕТДИСАБЛЕДИМАЖЕЛИСТ ТБ

Задает список изображений, который будет использоваться элементом управления Toolbar для вывода отключенных кнопок.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Обрабатываемый набор изображений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер списка изображений, который ранее использовался для вывода отключенных кнопок, или **значение NULL** , если список изображений ранее не был задан.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





