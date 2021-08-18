---
title: Сообщение WM_TOUCHHITTESTING
description: Отправляются в окно касанием, чтобы определить наиболее вероятную цель касания.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 895c535330674767683d0155bd2e22b8a40389c08378187377497380d71d97b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829494"
---
# <a name="wm_touchhittesting-message"></a>Сообщение WM_TOUCHHITTESTING

Отправляются в окно касанием, чтобы определить наиболее вероятную цель касания.

> \[! Существенно\]  
> Для классических приложений следует учитывать DPI. Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI. Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его). Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) , содержащую данные контактной зоны касания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если один или несколько элементов находятся в области контактного лица, приложение должно вернуть результат [**пакктаучхиттестингпроксимитевалуатион**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).

Если в области контактного лица нет элементов, приложение должно задать значение **Score** в [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) для [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) и вызвать метод [**ПАККТАУЧХИТТЕСТИНГПРОКСИМИТЕВАЛУАТИОН**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) , чтобы получить возвращаемое значение LRESULT.

Если приложение не обрабатывает это сообщение, оно должно вызвать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Remarks

Это сообщение отправляется в Windows, которые регистрируются с помощью функции [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Сообщения](messages.md)
</dt> <dt>

[**Оценки проверки попадания касания**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

