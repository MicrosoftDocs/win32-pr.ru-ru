---
title: Сообщение IPM_SETFOCUS (Коммктрл. h)
description: Устанавливает фокус клавиатуры на указанное поле в элементе управления IP-адреса. Будет выбран весь текст в этом поле.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- элементы управления Windows сообщений IPM_SETFOCUS
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a74d98aa4d4259d11d7fef6e0bfdad2bfe741447ddffab27fa41545e7eda515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085574"
---
# <a name="ipm_setfocus-message"></a>\_Сообщение IPM SETFOCUS

Устанавливает фокус клавиатуры на указанное поле в элементе управления IP-адреса. Будет выбран весь текст в этом поле.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс поля, к которому должен быть установлен фокус. Если это значение больше числа полей, фокус устанавливается на первое пустое поле. Если все поля не пусты, фокус устанавливается на первое поле.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





