---
title: Код уведомления HDN_GETDISPINFO (Коммктрл. h)
description: Посылается владельцу элемента управления "заголовок", когда элементу управления требуются сведения об элементе заголовка обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6e6cbc9559cda3312ecdca341aa7c7ad2b44dc5cc29e50690ddf10b2729a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435454"
---
# <a name="hdn_getdispinfo-notification-code"></a>\_Код уведомления ХДН жетдиспинфо

Посылается владельцу элемента управления "заголовок", когда элементу управления требуются сведения об элементе заголовка обратного вызова. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмхддиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) . В поле входные данные поля структуры указывают требуемые сведения и интересующий элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает LRESULT.

## <a name="remarks"></a>Remarks

Заполните соответствующие члены структуры, чтобы вернуть запрошенные сведения в элемент управления "заголовок". Если обработчик сообщений устанавливает для элемента **маски** структуры [**нмхддиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) значение HDi \_ di \_ сетитем, то элемент управления "заголовок" сохраняет информацию и не запрашивает их снова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ХДН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ХДН \_ жетдиспинфоа** (ANSI)<br/>           |



 

 





