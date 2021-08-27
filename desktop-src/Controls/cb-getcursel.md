---
title: Сообщение CB_GETCURSEL (Winuser. h)
description: Приложение отправляет \_ сообщение с индексом CB для получения индекса выбранного в данный момент элемента в поле со списком.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- элементы управления Windows сообщений CB_GETCURSEL
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
ms.openlocfilehash: e9bc51f43fd28563be4bc3f024bf6afd35c297648aa6c6cad677aca4582c3737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089264"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**\_СЕЛЕКТСТРИНГ CB**](cb-selectstring.md)
</dt> <dt>

[**\_СЕТКУРСЕЛ CB**](cb-setcursel.md)
</dt> </dl>

 

 





