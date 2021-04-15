---
title: Получение и задание сочетания клавиш
description: В этом разделе показано, как извлечь или задать сочетание клавиш для элемента управления горячего ключа.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105654397"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a>Получение и задание сочетания клавиш

В этом разделе показано, как извлечь или задать сочетание клавиш для элемента управления горячего ключа. Сообщение [**ХКМ \_ сесоткэй**](hkm-sethotkey.md) позволяет приложению установить сочетание клавиш для элемента управления "горячая клавиша". Приложения используют сообщение [**ХКМ- \_ горячих**](hkm-gethotkey.md) клавиш, чтобы получить виртуальный код ключа и флаги модификатора для сочетания клавиш, выбранного пользователем.

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления Windows](window-controls.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование пользовательского интерфейса Windows

## <a name="instructions"></a>Инструкции


Используйте сообщение [**ХКМ- \_ горячих**](hkm-gethotkey.md) клавиш, чтобы получить ключ виртуального ключа и клавиши-модификаторы, описывающие горячие клавиши, выбранные пользователем. Используйте сообщение [**ХКМ \_ сесоткэй**](hkm-sethotkey.md) , чтобы задать эти значения для сочетания клавиш.

В следующем примере кода C++ определяемая приложением функция использует сообщение [**ХКМ- \_ горячих**](hkm-gethotkey.md) клавиш для получения сочетания клавиш из элемента управления горячих клавиш, а затем использует сообщение [**WM \_ сесоткэй**](/windows/desktop/inputdev/wm-sethotkey) для установки глобального горячего ключа. Обратите внимание, что нельзя задать глобальную горячую клавишу для окна, имеющего стиль [**\_ дочернего окна WS**](/windows/desktop/winmsg/window-styles) .



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на элемент управления ключами](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Сведения об элементах управления горячей клавиши](hot-key-controls.md)
</dt> <dt>

[Использование элементов управления горячими ключами](using-hot-key-controls.md)
</dt> </dl>

 

 