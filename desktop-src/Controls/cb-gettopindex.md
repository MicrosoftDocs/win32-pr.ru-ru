---
title: Сообщение CB_GETTOPINDEX (Winuser. h)
description: Приложение отправляет \_ сообщение ЖЕТТОПИНДЕКС CB, чтобы получить Отсчитываемый от нуля индекс первого видимого элемента в списке в поле со списком.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Элементы управления Windows для CB_GETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988639"
---
# <a name="cb_gettopindex-message"></a>\_Сообщение ЖЕТТОПИНДЕКС CB

Приложение отправляет сообщение **\_ жеттопиндекс CB** , чтобы получить Отсчитываемый от нуля индекс первого видимого элемента в списке в поле со списком. Изначально элемент с индексом 0 находится в верхней части окна списка, но если содержимое списка было прокручено, то в верхней части может находиться другой элемент.

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

Если сообщение прошло успешно, возвращается значение индекса первого видимого элемента в поле со списком.

Если сообщение не выполняется, возвращается значение CB \_ Err.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТТОПИНДЕКС CB**](cb-settopindex.md)
</dt> </dl>

 

 





