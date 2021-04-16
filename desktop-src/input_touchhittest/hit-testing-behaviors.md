---
title: Поведение при проверке нажатия касания
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для указания того, как сообщения для проверки попадания касания обрабатываются Windows, зарегистрированными с помощью функции Регистертаучхиттестингвиндов.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719206"
---
# <a name="touch-hit-testing-behaviors"></a>Поведение при проверке нажатия касания

Следующие константы используются приложениями или платформами пользовательского интерфейса для указания того, как сообщения для проверки попадания касания обрабатываются Windows, зарегистрированными с помощью функции [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

| Константа/значение | Описание |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0) | Указывает, что [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) сообщения не отправляются в целевое окно, но отправляются в дочерние окна.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Указывает, что [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) сообщения отправляются в целевое окно.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)          | Указывает, что [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) сообщения не отправляются в целевое окно или дочерние окна.<br/>              |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                           |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Header<br/>                   | <dl> <dt>Winuser. h |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы](constants.md)
