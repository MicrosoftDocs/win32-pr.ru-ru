---
title: Сообщение TCM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент из элемента управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- элементы управления Windows сообщений TCM_DELETEITEM
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc9e90ab63e34545628019cd9dcde74c7b4e953fb6ee0b9eed138151129e7b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077878"
---
# <a name="tcm_deleteitem-message"></a>\_Сообщение DELETEITEM TCM

Удаляет элемент из элемента управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс удаляемого элемента.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





