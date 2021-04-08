---
title: Сообщение HDM_SETBITMAPMARGIN (Коммктрл. h)
description: Задает ширину поля, заданное в пикселях точечного рисунка в существующем элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетбитмапмаргин.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Элементы управления Windows для HDM_SETBITMAPMARGIN сообщений
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892393"
---
# <a name="hdm_setbitmapmargin-message"></a>\_Сообщение СЕТБИТМАПМАРГИН HDM

Задает ширину поля, заданное в пикселях точечного рисунка в существующем элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетбитмапмаргин**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Ширина (в пикселях) поля, охватывающего точечный рисунок в существующем элементе управления "заголовок".

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ширину поля точечного рисунка в пикселях. Если поле точечного рисунка не было указано ранее, возвращается значение по умолчанию 3 \* [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ ккседже*).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТБИТМАПМАРГИН HDM**](hdm-getbitmapmargin.md)
</dt> </dl>

 

