---
title: Сообщение CB_SETTOPINDEX (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТТОПИНДЕКС CB, чтобы убедиться, что конкретный элемент отображается в списке поля со списком.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- элементы управления Windows сообщений CB_SETTOPINDEX
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
ms.openlocfilehash: d9364ef5013ef692adda76f96752f11691d5f4cc87c857386914105d16decb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832292"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТТОПИНДЕКС CB**](cb-gettopindex.md)
</dt> </dl>

 

 





