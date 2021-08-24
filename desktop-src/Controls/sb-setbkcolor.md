---
title: Сообщение SB_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона в строке состояния.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- элементы управления Windows сообщений SB_SETBKCOLOR
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97893d49d475789b07c28e17e88097aa4df4336154d6b4e0f9c4fa081e52635
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637084"
---
# <a name="sb_setbkcolor-message"></a>\_Сообщение SB сетбкколор

Задает цвет фона в строке состояния.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение [**COLORREF**](/windows/desktop/gdi/colorref) , указывающее новый цвет фона. Укажите \_ значение по умолчанию CLR, чтобы строка состояния использовала цвет фона по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущий цвет фона или \_ значение по умолчанию CLR, если цвет фона является цветом по умолчанию.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

