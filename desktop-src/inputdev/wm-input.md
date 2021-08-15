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
ms.openlocfilehash: 5d317ba21c69b22ae9c6b7cb5be0be84cd15f561b34ec65f1f99e7335cd1badb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884291"
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

## <a name="remarks"></a>Remarks

Необработанные входные данные доступны, только если приложение вызывает [**регистерравинпутдевицес**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) с допустимыми спецификациями устройств.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|--------------------------|-------------------------------------------|
| Минимальная версия клиента | Windows \[Только классические приложения XP\] |
| Минимальная версия сервера | Windows Только для \[ настольных приложений сервера 2003\] |
| Header | <dl> <dt>**Winuser. h (включает Windows. h)**</dt> </dl> |

## <a name="see-also"></a>См. также раздел

**Ссылки**

[**жетравинпутдата**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**регистерравинпутдевицес**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**равинпут**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**ПОЛУЧИТЬ \_ равинпут \_ код \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Зрения**

[Необработанный ввод](raw-input.md)
