---
title: Сообщение WM_INPUT (Winuser. h)
description: Отправляется в окно, которое получает необработанные входные данные. Окно получает это сообщение через функцию WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415296"
---
# <a name="wm_input-message"></a>\_Входное сообщение WM

Отправляется в окно, которое получает необработанные входные данные.

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam*

</dt> <dd>

Входной код. Чтобы получить это значение, используйте макрос [**Get \_ равинпут \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) .

Может иметь одно из следующих значений:

| Значение | Значение |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**RIM \_ ВХОДные данные**</dt> <dt>0</dt> </dl> | Входные данные были выполнены, пока приложение находилось на переднем плане. </br> Приложение должно вызвать [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , чтобы система могла выполнить очистку. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**RIM \_ ИНПУТСИНК**</dt> <dt>1</dt> </dl> | Входные данные были выполнены, пока приложение не находилось на переднем плане. |

</dd> <dt>

*lParam* 

</dt> <dd>

Обработчик **хравинпут** для структуры [**равинпут**](/windows/win32/api/winuser/ns-winuser-rawinput) , которая содержит необработанные данные от устройства. Чтобы получить необработанные данные, используйте этот маркер в вызове [**жетравинпутдата**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="remarks"></a>Комментарии

Необработанные входные данные доступны, только если приложение вызывает [**регистерравинпутдевицес**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) с допустимыми спецификациями устройств.

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------------|-------------------------------------------|
| Минимальная версия клиента | Только для \[ классических приложений Windows XP\] |
| Минимальная версия сервера | \[Только для настольных приложений Windows Server 2003\] |
| Header | <dl> <dt>**Winuser. h (включение Windows. h)**</dt> </dl> |

## <a name="see-also"></a>См. также раздел

**Ссылки**

[**жетравинпутдата**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**регистерравинпутдевицес**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**равинпут**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**ПОЛУЧИТЬ \_ равинпут \_ код \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Зрения**

[Необработанный ввод](raw-input.md)
