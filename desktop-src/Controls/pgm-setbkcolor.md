---
title: Сообщение PGM_SETBKCOLOR (Коммктрл. h)
description: Задает текущий цвет фона для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Сетбкколор пейджера.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- Элементы управления Windows для PGM_SETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135714"
---
# <a name="pgm_setbkcolor-message"></a>\_Сообщение СЕТБККОЛОР PGM

Задает текущий цвет фона для элемента управления страничного навигатора. Это сообщение можно отправить явным образом или использовать макрос [**\_ сетбкколор пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение **COLORREF** , содержащее новый цвет фона для элемента управления страничного навигатора.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **COLORREF** , содержащее предыдущий цвет фона.

## <a name="remarks"></a>Комментарии

По умолчанию элемент управления страничный навигатор будет использовать цвет значка системной кнопки в качестве цвета фона. Это тот же цвет, который можно извлечь, вызвав [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) с \_ бтнфаце Color.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

