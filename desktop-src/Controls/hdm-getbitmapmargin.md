---
title: Сообщение HDM_GETBITMAPMARGIN (Коммктрл. h)
description: Возвращает ширину поля точечного рисунка для элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса жетбитмапмаргин.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- Элементы управления Windows для HDM_GETBITMAPMARGIN сообщений
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988695"
---
# <a name="hdm_getbitmapmargin-message"></a>\_Сообщение ЖЕТБИТМАПМАРГИН HDM

Возвращает ширину поля точечного рисунка для элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ жетбитмапмаргин**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ширину поля точечного рисунка в пикселях. Если поле точечного рисунка не было указано ранее, возвращается значение по умолчанию 3 \* [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ ккседже).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТБИТМАПМАРГИН HDM**](hdm-setbitmapmargin.md)
</dt> </dl>

 

