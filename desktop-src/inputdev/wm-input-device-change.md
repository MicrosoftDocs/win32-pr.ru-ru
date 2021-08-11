---
title: Сообщение WM_INPUT_DEVICE_CHANGE (Winuser. h)
description: Отправляется в окно, зарегистрированное для получения необработанных входных данных. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823aeaf5655703802f07fb238d5c6c5dc479defa12ae4a416423b4519fd2b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247890"
---
# <a name="wm_input_device_change-message"></a>Сообщение WM_INPUT_DEVICE_CHANGE

## <a name="description"></a>Описание

Отправляется в окно, зарегистрированное для получения необработанных входных данных. 

Необработанные входные уведомления доступны только после того, как приложение вызывает [регистерравинпутдевицес](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) с флагом [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) .

Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam*

</dt> <dd>

Тип: **wParam**

Этот параметр может принимать одно из указанных ниже значений.

| Значение                    | Значение                                    |
|--------------------------|--------------------------------------------|
| **\_прибытие гидк** </br>1 | В систему Добавлено новое устройство. </br> Чтобы получить дополнительные сведения об устройстве, можно вызвать [жетравинпутдевицеинфо](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) . |
| **\_Удаление гидк** </br>2 | Устройство было удалено из системы. |

</dd> <dt>

*lParam* 

</dt> <dd>

Тип: **lParam** .

**Обработчик** необработанного входного устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если приложение обрабатывает это сообщение, оно должно вернуть ноль.

## <a name="see-also"></a>См. также раздел

**Зрения**

[Необработанный ввод](/windows/desktop/inputdev/raw-input)

**Ссылка**

[регистерравинпутдевицес](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[Структура РАВИНПУТДЕВИЦЕ](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

