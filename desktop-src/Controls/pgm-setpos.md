---
title: Сообщение PGM_SETPOS (Коммктрл. h)
description: Задает текущую точку прокрутки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Сетпос пейджера.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- элементы управления Windows сообщений PGM_SETPOS
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
ms.openlocfilehash: a7a056d55d0ec70b3ff3068580c1e9923b363efa15e9ab26bf8aa67f476cc147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046834"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





