---
title: Сообщение BCM_SETSPLITINFO (Коммктрл. h)
description: Задает сведения для элемента управления "разворачивающаяся кнопка". Отправляйте это сообщение явным образом или с помощью \_ макроса кнопки сетсплитинфо.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- Элементы управления Windows для BCM_SETSPLITINFO сообщений
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
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654527"
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

## <a name="remarks"></a>Комментарии

Это сообщение используется только с стилями кнопки " [**BS \_**](button-styles.md) " и " [**BS \_ дефсплитбуттон**](button-styles.md) ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



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

 

 





