---
title: Сообщение TB_SETDISABLEDIMAGELIST (Коммктрл. h)
description: Задает список изображений, который будет использоваться элементом управления Toolbar для вывода отключенных кнопок.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- элементы управления Windows сообщений TB_SETDISABLEDIMAGELIST
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
ms.openlocfilehash: 9125c5e5ac742f4692fc5464cd51c89e111558c4d0004e08d7cef9c862d03cbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167494"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





