---
title: Сообщение PGM_GETBORDER (Коммктрл. h)
description: Возвращает текущий размер границы для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или воспользоваться макросом страничного навигатора \_ .
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- Элементы управления Windows для PGM_GETBORDER сообщений
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654574"
---
# <a name="pgm_getborder-message"></a>\_Сообщение о ВЫГРАНИЦЕ PGM

Возвращает текущий размер границы для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или воспользоваться макросом [**страничного навигатора \_**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа INT, которое содержит текущий размер границы (в пикселях).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТБОРДЕР PGM**](pgm-setborder.md)
</dt> </dl>

 

 





