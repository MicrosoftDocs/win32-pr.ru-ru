---
title: Сообщение PGM_GETPOS (Коммктрл. h)
description: Извлекает текущее расположение прокрутки элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетпос пейджера.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Элементы управления Windows для PGM_GETPOS сообщений
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
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654572"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





