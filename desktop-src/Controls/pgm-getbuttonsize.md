---
title: Сообщение PGM_GETBUTTONSIZE (Коммктрл. h)
description: Получает текущий размер кнопки для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетбуттонсизе пейджера.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Элементы управления Windows для PGM_GETBUTTONSIZE сообщений
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
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071813"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТБУТТОНСИЗЕ PGM**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





