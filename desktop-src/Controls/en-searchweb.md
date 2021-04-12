---
title: Код уведомления EN_SEARCHWEB (Коммктрл. h)
description: Посылается, когда элемент управления "поле ввода" теряет фокус клавиатуры. Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ сообщение уведомления WM.
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489279"
---
# <a name="en_searchweb-notification-code"></a>\_Код уведомления EN сеарчвеб

Посылается после того, как элемент управления "поле ввода" выполнил Поиск в Интернете при включении функции "Поиск в Интернете", см. статью [EM_ENABLESEARCHWEB](em-enablesearchweb.md). Родительское окно элемента управления "поле ввода" получает этот код уведомления через сообщение [**\_ уведомления WM**](wm-notify.md) .


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик для элемента управления "поле ввода".

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмсеарчвеб**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ енаблесеарчвеб**](em-enablesearchweb.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**\_уведомление WM**](wm-notify.md)
</dt> </dl>

 

 





