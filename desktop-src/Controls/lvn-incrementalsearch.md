---
title: Код уведомления LVN_INCREMENTALSEARCH (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что началось добавочный поиск. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654734"
---
# <a name="lvn_incrementalsearch-notification-code"></a>\_Код уведомления ЛВН INCREMENTALSEARCH

Сообщает родительскому окну элемента управления "представление списка", что началось добавочный поиск. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* \[ окне\]
</dt> <dd>

Указатель на структуру [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) , описывающую код уведомления. Вызывающий объект отвечает за выделение этой структуры, включая содержащиеся в ней структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) и [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) . Задайте элементы структуры **NMHDR** . Элемент **Code** должен иметь значение ЛВН \_ INCREMENTALSEARCH.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . Параметр *wParam* содержит идентификатор элемента управления, который отправляет этот код уведомления.

Этот код уведомления дает приложению (или получателю уведомления) возможность настроить добавочный поиск. Например, если элементы поиска являются числовыми, приложение может выполнить числовой Поиск вместо поиска строки.

Приложение устанавливает член **lParam** структуры [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , содержащейся в структуре [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) , в результат поиска или в другое определенное приложением значение, чтобы завершить поиск неудачей и указать элементу управления, как это делается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl>   |
| Имя в кодировке Юникод и ANSI<br/>   | **ЛВН \_ ИНКРЕМЕНТАЛСЕАРЧВ** (Юникод) и **ЛВН \_ инкременталсеарча** (ANSI)<br/> |



 

 





