---
title: Сообщение BCM_SETSPLITINFO (Коммктрл. h)
description: Задает сведения для элемента управления "разворачивающаяся кнопка". Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки сетсплитинфо.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- элементы управления Windows сообщений BCM_SETSPLITINFO
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17332ce5f10fa612d739598222e4973000961435fa525190a650adaa9aa9fc4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921424"
---
# <a name="bcm_setsplitinfo-message"></a>\_Сообщение СЕТСПЛИТИНФО BCM

Задает сведения для элемента управления "разворачивающаяся кнопка". Отправляйте это сообщение явным образом или с помощью макроса [**кнопки \_ сетсплитинфо**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указатель на структуру [**\_ сплитинфо кнопки**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) , содержащую сведения о разворачивающейся кнопке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Это сообщение используется только с стилями кнопки " [**BS \_**](button-styles.md) " и " [**BS \_ дефсплитбуттон**](button-styles.md) ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[Стили кнопок](button-styles.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Типы кнопок](button-types-and-styles.md)
</dt> </dl>

 

 





