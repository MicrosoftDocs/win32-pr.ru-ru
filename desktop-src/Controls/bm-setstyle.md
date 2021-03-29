---
title: Сообщение BM_SETSTYLE (Winuser. h)
description: Задает стиль кнопки. Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Элементы управления Windows для BM_SETSTYLE сообщений
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
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988378"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



 

