---
title: Сообщение BM_SETSTYLE (Winuser. h)
description: Задает стиль кнопки. Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- элементы управления Windows сообщений BM_SETSTYLE
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f635a70bf806c6c26f5b236ea939bc453d27bf0fe135f8e2586aeb59021b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674422"
---
# <a name="bm_setstyle-message"></a>\_Сообщение BM SETSTYLE

Задает стиль кнопки. Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Стиль кнопки. Этот параметр может быть сочетанием стилей кнопок. Таблицу стилей кнопок см. в разделе [стили кнопок](button-styles.md).

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) объекта *lParam* — это **логическое** значение, указывающее, следует ли перерисовать кнопку. Значение **true** Перерисовывает кнопку; значение **false** не перерисовывает кнопку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение всегда возвращает ноль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



 

