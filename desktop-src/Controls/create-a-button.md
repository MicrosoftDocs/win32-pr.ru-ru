---
title: Создание кнопки
description: Для динамического создания кнопок используется функция CreateWindow или CreateWindowEx. В этом разделе показано, как использовать функцию CreateWindow для создания кнопки отправки по умолчанию.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070884"
---
# <a name="how-to-create-a-button"></a>Создание кнопки

Для динамического создания кнопок используется функция [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . В этом разделе показано, как использовать функцию **CreateWindow** для создания кнопки отправки по умолчанию.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Используйте функцию [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) для создания элемента управления "Кнопка".

В следующем примере C++ параметр *m \_ HWND* является дескриптором родительского окна. Стиль " [**BS \_ дефпушбуттон**](button-styles.md) " указывает, что должна быть создана кнопка принудительной установки по умолчанию. Обратите внимание, что значения размера и расположения должны быть заданы, так как при использовании **\_ Уседефаулт во Вт** . для кнопки устанавливаются нулевые значения.


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[О кнопках](about-buttons.md)
</dt> <dt>

[Справочник по элементу управления Button](bumper-button-button-control-reference.md)
</dt> <dt>

[Использование кнопок](using-buttons.md)
</dt> <dt>

[Кнопка](buttons.md)
</dt> </dl>

 

 