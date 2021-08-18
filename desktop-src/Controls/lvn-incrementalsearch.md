---
title: Код уведомления LVN_INCREMENTALSEARCH (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что началось добавочный поиск. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH кода уведомления Windows элементы управления
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
ms.openlocfilehash: 0ec3207fbb16bca23bf44ac61fee58bb6e4fad1ff74c38d7b56910ed52997f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826124"
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

## <a name="remarks"></a>Remarks

Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . Параметр *wParam* содержит идентификатор элемента управления, который отправляет этот код уведомления.

Этот код уведомления дает приложению (или получателю уведомления) возможность настроить добавочный поиск. Например, если элементы поиска являются числовыми, приложение может выполнить числовой Поиск вместо поиска строки.

Приложение устанавливает член **lParam** структуры [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , содержащейся в структуре [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) , в результат поиска или в другое определенное приложением значение, чтобы завершить поиск неудачей и указать элементу управления, как это делается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl>   |
| Имя в кодировке Юникод и ANSI<br/>   | **ЛВН \_ ИНКРЕМЕНТАЛСЕАРЧВ** (Юникод) и **ЛВН \_ инкременталсеарча** (ANSI)<br/> |



 

 





