---
title: Сообщение CB_SETTOPINDEX (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТТОПИНДЕКС CB, чтобы убедиться, что конкретный элемент отображается в списке поля со списком.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Элементы управления Windows для CB_SETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801240"
---
# <a name="cb_settopindex-message"></a>\_Сообщение СЕТТОПИНДЕКС CB

Приложение отправляет сообщение **\_ сеттопиндекс CB** , чтобы убедиться, что конкретный элемент отображается в списке поля со списком. Система прокручивает содержимое списка таким образом, чтобы указанный элемент появился в верхней части окна списка или был достигнут максимальный диапазон прокрутки.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает отсчитываемый от нуля индекс элемента списка.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение прошло успешно, возвращаемое значение равно нулю.

Если сообщение не выполняется, возвращается значение CB \_ Err.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТТОПИНДЕКС CB**](cb-gettopindex.md)
</dt> </dl>

 

 





