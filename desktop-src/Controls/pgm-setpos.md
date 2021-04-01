---
title: Сообщение PGM_SETPOS (Коммктрл. h)
description: Задает текущую точку прокрутки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Сетпос пейджера.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Элементы управления Windows для PGM_SETPOS сообщений
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802068"
---
# <a name="pgm_setpos-message"></a>\_Сообщение СЕТПОС PGM

Задает текущую точку прокрутки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать макрос [**\_ сетпос пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение типа **int** , содержащее новую точку прокрутки в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





