---
title: Сообщение PGM_GETBKCOLOR (Коммктрл. h)
description: Возвращает текущий цвет фона для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетбкколор пейджера.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- элементы управления Windows сообщений PGM_GETBKCOLOR
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3ee3a4be09a948654d337a47eecdd2a7b15d16b0602016aa99500cd1c3728c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985944"
---
# <a name="pgm_getbkcolor-message"></a>\_Сообщение ЖЕТБККОЛОР PGM

Возвращает текущий цвет фона для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать макрос [**\_ жетбкколор пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **COLORREF** , содержащее текущий цвет фона.

## <a name="remarks"></a>Remarks

По умолчанию элемент управления страничный навигатор будет использовать цвет значка системной кнопки в качестве цвета фона. Это тот же цвет, который можно извлечь, вызвав [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) с \_ бтнфаце Color.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

