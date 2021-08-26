---
title: Сообщение PGM_GETBUTTONSIZE (Коммктрл. h)
description: Получает текущий размер кнопки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетбуттонсизе пейджера.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- элементы управления Windows сообщений PGM_GETBUTTONSIZE
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a77bbfdbac95c10afc721cfbae41798083ea98f4dd78e9dfdec9099871d7afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985903"
---
# <a name="pgm_getbuttonsize-message"></a>\_Сообщение ЖЕТБУТТОНСИЗЕ PGM

Получает текущий размер кнопки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать макрос [**\_ жетбуттонсизе пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа INT, которое содержит текущий размер кнопки в пикселях.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТБУТТОНСИЗЕ PGM**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





