---
title: Сообщение PBM_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона на индикаторе выполнения.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- элементы управления Windows сообщений PBM_SETBKCOLOR
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54bdee330aba5a4ff96fc5b26fa7f99553ff8331dd8822fcd350fbae5813c813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986184"
---
# <a name="pbm_setbkcolor-message"></a>\_Сообщение СЕТБККОЛОР PBM

Задает цвет фона на индикаторе выполнения.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение **COLORREF** , указывающее новый цвет фона. Укажите \_ значение по умолчанию CLR, чтобы индикатор выполнения использовал цвет фона по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущий цвет фона или \_ значение по умолчанию CLR, если цвет фона является цветом по умолчанию.

## <a name="remarks"></a>Remarks

Если стили оформления включены, это сообщение не действует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





