---
title: Код уведомления TVN_SETDISPINFO (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления, что оно должно обновлять сведения об элементе. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO кода уведомления Windows элементы управления
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88a9b5fed4260fa88f5f40431113456950d99985ad2f2e0e97c2e951dce96bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957773"
---
# <a name="tvn_setdispinfo-notification-code"></a>\_Код уведомления ТВН сетдиспинфо

Сообщает родительскому окну элемента управления иерархического представления, что оно должно обновлять сведения об элементе. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмтвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) , описывающую обновляемый элемент. Член **хитем** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) указывает обновляемый элемент, а элемент **Mask** указывает, какие атрибуты элемента обновляются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение игнорируется.

## <a name="remarks"></a>Remarks

Если элемент **псзтекст** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение тексткаллбакк LPSTR, элемент управления отправляет это уведомление для задания текста элемента. В этом случае элемент **Mask** элемента *lParam* будет иметь \_ установленный флаг твиф Text.

Если элемент **иимаже** или **иселектедимаже** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение имажекаллбакк I, элемент управления отправляет это уведомление для получения индекса отображаемого изображения значка. В этом случае элемент **Mask** параметра *lParam* будет иметь \_ установленный флаг твиф Image или твиф \_ селектедимаже.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ СЕТДИСПИНФОВ** (Юникод) и **ТВН \_ сетдиспинфоа** (ANSI)<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[ТВН \_ жетдиспинфо](tvn-getdispinfo.md)
</dt> </dl>

 

 





