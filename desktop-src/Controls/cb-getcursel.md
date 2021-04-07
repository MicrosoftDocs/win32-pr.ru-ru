---
title: Сообщение CB_GETCURSEL (Winuser. h)
description: Приложение отправляет \_ сообщение с индексом CB для получения индекса выбранного в данный момент элемента в поле со списком.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- Элементы управления Windows для CB_GETCURSEL сообщений
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892850"
---
# <a name="cb_getcursel-message"></a>Сообщение с нерекурсивным превышем CB \_

Приложение отправляет сообщение с индексом **CB \_** для получения индекса выбранного в данный момент элемента в поле со списком.

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

Возвращаемое значение — это Отсчитываемый от нуля индекс текущего выбранного элемента. Если элемент не выбран, это значение равно CB \_ .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_СЕЛЕКТСТРИНГ CB**](cb-selectstring.md)
</dt> <dt>

[**\_СЕТКУРСЕЛ CB**](cb-setcursel.md)
</dt> </dl>

 

 





