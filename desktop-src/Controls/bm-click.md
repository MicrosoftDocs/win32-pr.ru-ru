---
title: Сообщение BM_CLICK (Winuser. h)
description: Имитирует нажатие пользователем кнопки. Это сообщение приводит к тому, что кнопка получает \_ сообщения WM лбуттондовн и WM \_ лбуттонуп, а родительское окно кнопки — для получения млрд доллного \_ кода уведомления.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- элементы управления Windows сообщений BM_CLICK
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fdf1e206546bcdb3fa0888276414bd44b927e96a8478be4ae8a5ce2d2a5169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674986"
---
# <a name="bm_click-message"></a>BM \_ щелкните сообщение

Имитирует нажатие пользователем кнопки. Это сообщение приводит к тому, что кнопка получает сообщения [**WM \_ Лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) и [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) , а родительское окно кнопки — для получения [млрд доллного \_](bn-clicked.md) кода уведомления.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Если кнопка находится в диалоговом окне, а диалоговое окно неактивно, сообщение **BM \_ Click** может завершиться ошибкой. Чтобы обеспечить успешное выполнение в этой ситуации, вызовите функцию [**сетактивевиндов**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) , чтобы активировать диалоговое окно перед отправкой сообщения о **\_ нажатии кнопки BM** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



 

