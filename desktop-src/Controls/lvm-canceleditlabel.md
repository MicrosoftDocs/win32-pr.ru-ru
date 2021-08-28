---
title: Сообщение LVM_CANCELEDITLABEL (Коммктрл. h)
description: Отменяет операцию изменения текста элемента.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- элементы управления Windows сообщений LVM_CANCELEDITLABEL
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0b105c1082457c2cafd14e7a36361100f8e82197db7e5d76ae51447f945897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698804"
---
# <a name="lvm_canceleditlabel-message"></a>\_Сообщение LVM канцеледитлабел

Отменяет операцию изменения текста элемента.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

Это сообщение вызывает отправку уведомления [ЛВН \_ ендлабеледит](lvn-endlabeledit.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





