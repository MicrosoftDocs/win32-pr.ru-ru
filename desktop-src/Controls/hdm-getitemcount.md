---
title: Сообщение HDM_GETITEMCOUNT (Коммктрл. h)
description: Возвращает число элементов в элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса GetItemCount.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- элементы управления Windows сообщений HDM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4500277528cc76012631734d6f7316b29fdcb7a5a92cec3cf7b6bbb42693ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436034"
---
# <a name="hdm_getitemcount-message"></a>\_Сообщение GETITEMCOUNT HDM

Возвращает число элементов в элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество элементов в случае успеха или значение-1 в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





