---
title: Код уведомления HDN_GETDISPINFO (Коммктрл. h)
description: Посылается владельцу элемента управления "заголовок", когда элементу управления требуются сведения об элементе заголовка обратного вызова. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO кода уведомления элементы управления Windows
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
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071197"
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

## <a name="remarks"></a>Комментарии

Заполните соответствующие члены структуры, чтобы вернуть запрошенные сведения в элемент управления "заголовок". Если обработчик сообщений устанавливает для элемента **маски** структуры [**нмхддиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) значение HDi \_ di \_ сетитем, то элемент управления "заголовок" сохраняет информацию и не запрашивает их снова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ХДН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ХДН \_ жетдиспинфоа** (ANSI)<br/>           |



 

 





