---
title: Сообщение TCM_GETITEMCOUNT (Коммктрл. h)
description: Извлекает число вкладок в наборе вкладок. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- элементы управления Windows сообщений TCM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9bbb954c75a19f15ecee9f946e338a186b6e9903a405aa1c550fb0ccc31392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104884"
---
# <a name="tcm_getitemcount-message"></a>\_Сообщение GETITEMCOUNT TCM

Извлекает число вкладок в наборе вкладок. Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество элементов в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





