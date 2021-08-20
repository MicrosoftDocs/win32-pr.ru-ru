---
title: Сообщение TB_SETCMDID (Коммктрл. h)
description: Задает идентификатор команды для кнопки панели инструментов.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- элементы управления Windows сообщений TB_SETCMDID
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
ms.openlocfilehash: 539fb03899a6a763a94a7cd2fd1b7e8be071f04e26e21f19e9ff53640b87be1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167609"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





