---
title: Код уведомления TVN_SETDISPINFO (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления, что оно должно обновлять сведения об элементе. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO кода уведомления элементы управления Windows
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
ms.openlocfilehash: 9b03e60ba7d8e6d7851c62fac030bd252cf957d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654439"
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

## <a name="remarks"></a>Комментарии

Если элемент **псзтекст** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение тексткаллбакк LPSTR, элемент управления отправляет это уведомление для задания текста элемента. В этом случае элемент **Mask** элемента *lParam* будет иметь \_ установленный флаг твиф Text.

Если элемент **иимаже** или **иселектедимаже** структуры [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) элемента имеет \_ значение имажекаллбакк I, элемент управления отправляет это уведомление для получения индекса отображаемого изображения значка. В этом случае элемент **Mask** параметра *lParam* будет иметь \_ установленный флаг твиф Image или твиф \_ селектедимаже.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТВН \_ СЕТДИСПИНФОВ** (Юникод) и **ТВН \_ сетдиспинфоа** (ANSI)<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**твитемекс**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[ТВН \_ жетдиспинфо](tvn-getdispinfo.md)
</dt> </dl>

 

 





