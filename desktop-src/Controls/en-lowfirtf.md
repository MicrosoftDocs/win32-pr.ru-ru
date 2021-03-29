---
title: Код уведомления EN_LOWFIRTF (RichEdit. h)
description: Сообщает родительскому окну элемента управления Microsoft Rich Edit, что было получено Неподдерживаемое ключевое слово формата RTF. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде \_ сообщения WM notify.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535048"
---
# <a name="en_lowfirtf-notification-code"></a>\_Код уведомления EN ловфиртф

Сообщает родительскому окну элемента управления Microsoft Rich Edit, что было получено Неподдерживаемое ключевое слово формата RTF. Форматированный элемент управления "поле ввода" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Структура [**енловфиртф**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот код уведомления не возвращает значение.

## <a name="remarks"></a>Комментарии

Чтобы получить уведомление EN \_ ловфиртф, укажите \_ флаг енм ловфиртф в маске, отправляемой с сообщением [**EM \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 1 \[\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**енловфиртф**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> </dl>

 

 





