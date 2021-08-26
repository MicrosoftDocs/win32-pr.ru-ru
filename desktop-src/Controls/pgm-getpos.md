---
title: Сообщение PGM_GETPOS (Коммктрл. h)
description: Извлекает текущее расположение прокрутки элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетпос пейджера.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- элементы управления Windows сообщений PGM_GETPOS
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f1d5608b720d5a5d3d661a368d094da9469d71108874a6cec5495bf120cc54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046874"
---
# <a name="pgm_getpos-message"></a>\_Сообщение ЖЕТПОС PGM

Извлекает текущее расположение прокрутки элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать макрос [**\_ жетпос пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа INT, содержащее текущую точку прокрутки в пикселях.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





