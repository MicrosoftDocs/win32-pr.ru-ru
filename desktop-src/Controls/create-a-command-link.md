---
title: Создание ссылки на команду
description: В этом разделе описывается один из способов создания ссылки на команду.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c61888921f06e017ec1ea625730c3cc52de5ab364db22fc01fd021ce5629c63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920904"
---
# <a name="how-to-create-a-command-link"></a>Создание ссылки на команду

В этом разделе описывается один из способов создания ссылки на команду.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Шаг 1. Создайте экземпляр кнопки «ссылка на команду».

В следующем примере кода C++ константа стиля " [**BS" \_ коммандлинк**](button-styles.md) Указывает кнопку как кнопку Command Link.


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Шаг 2. Задание метки и текста описания для ссылки на команду

Используйте функцию [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , чтобы задать метку ссылки на команду и дополнительный текст с помощью сообщения [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) и сообщения [**BCM \_ сетноте**](bcm-setnote.md) соответственно.


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[О кнопках](about-buttons.md)
</dt> <dt>

[Справочник по элементу управления Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Использование кнопок](using-buttons.md)
</dt> <dt>

[Кнопка](buttons.md)
</dt> </dl>

 

 