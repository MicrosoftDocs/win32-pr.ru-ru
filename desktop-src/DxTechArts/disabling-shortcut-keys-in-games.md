---
title: Отключение сочетаний клавиш в играх
description: в этой статье описывается временное отключение сочетаний клавиш в Microsoft Windows для предотвращения сбоев игр в полноэкранном режиме.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eae2ee1b30e78b17440f2c6144c529de4e6d7b6272a5d497de5c5e631ac1c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070524"
---
# <a name="disabling-shortcut-keys-in-games"></a>Отключение сочетаний клавиш в играх

в этой статье описывается временное отключение сочетаний клавиш в Microsoft Windows для предотвращения сбоев игр в полноэкранном режиме. Клавиша SHIFT и клавиша CTRL часто используются в качестве пожара или запуска кнопок в играх. если пользователь случайно нажимает клавишу Windows (находится рядом с этими ключами), они могут привести к внезапному переходу из приложения, что руинс работу игры. Простое использование клавиши SHIFT в качестве кнопки игры может привести к непреднамеренному выполнению сочетания клавиш, которое может отображать диалоговое окно предупреждения. Чтобы избежать этих проблем, следует отключить эти ключи при работе в полноэкранном режиме и либо включить ключи обратно в обработчики по умолчанию при работе в оконном режиме, либо выйти из приложения.

В этой статье описывается, как выполнить следующие действия.

-   [отключение ключа Windows с помощью обработчика клавиатуры](#disable-the-windows-key-with-a-keyboard-hook)
-   [Отключение сочетаний клавиш для специальных возможностей](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>отключение ключа Windows с помощью обработчика клавиатуры

используйте клавиатурный обработчик низкого уровня, чтобы отфильтровать Windowsный ключ от обработки. Обработчик клавиатур низкого уровня, показанный в примере 1, остается в силе, даже если пользователь свертывает окно или переключается на другое приложение. это означает, что следует следить за тем, чтобы ключ Windows не был отключен при деактивации приложения. Код в примере 1 делает это, обрабатывая сообщение WM \_ активатеапп.

> [!Note]  
> этот метод работает с Windows 2000 и более поздними версиями Windows. Этот метод также работает с учетными записями пользователей с минимальными привилегиями (также известными как учетные записи с ограниченными правами).

 

Этот метод используется ДКСУТ и демонстрируется в следующем примере кода.

**Пример 1. использование обработчика клавиатуры низкого уровня для отключения ключа Windows**


```C++
HHOOK g_hKeyboardHook;
BOOL g_bFullscreen;
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Initialization
    g_hKeyboardHook = SetWindowsHookEx( WH_KEYBOARD_LL,  LowLevelKeyboardProc, GetModuleHandle(NULL), 0 );
 
    // 
    // main application code here
    // 
 
    // Cleanup before shutdown
    UnhookWindowsHookEx( g_hKeyboardHook );
}
 
 
LRESULT CALLBACK LowLevelKeyboardProc( int nCode, WPARAM wParam, LPARAM lParam )
{
    if (nCode < 0 || nCode != HC_ACTION )  // do not process message 
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam); 
 
    bool bEatKeystroke = false;
    KBDLLHOOKSTRUCT* p = (KBDLLHOOKSTRUCT*)lParam;
    switch (wParam) 
    {
        case WM_KEYDOWN:  
        case WM_KEYUP:    
        {
            bEatKeystroke = (g_bFullscreen && g_bWindowActive && ((p->vkCode == VK_LWIN) || (p->vkCode == VK_RWIN)));
            break;
        }
    }
 
    if( bEatKeystroke )
        return 1;
    else
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam );
}
 
 
LRESULT CALLBACK WndProc( HWND hWnd, UINT uMsg, WPARAM wParam, LPARAM lParam )
{
    switch( uMsg )
    {
       case WM_ACTIVATEAPP:
            // g_bWindowActive is used to control if the Windows key is filtered by the keyboard hook or not.
            if( wParam == TRUE )
                g_bWindowActive  = true;           
            else 
                g_bWindowActive  = false;           
            break;
    }
}
```



## <a name="disable-the-accessibility-shortcut-keys"></a>Отключение сочетаний клавиш для специальных возможностей

Windows включает специальные возможности, такие как залипание клавиш, режим фильтрации и озвучивание (см. раздел [Windows специальные](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))возможности). Для каждого из них используется другая цель; Например, залипание залипания клавиш предназначено для пользователей, которые испытывают трудности одновременного нажатия двух или более ключей. У каждой из этих специальных возможностей также есть сочетание клавиш, которое позволяет включить или отключить функцию. Например, нажатие клавиши SHIFT вызывается пять раз. Если клавиша SHIFT также используется в игре, пользователь может случайно активировать это сочетание клавиш во время игры. при запуске ярлыка Windows (по умолчанию) выводит предупреждение в диалоговом окне, что приведет к тому, что Windows снизит игру, запущенную в полноэкранном режиме. Это, конечно, может существенно повлиять на игру.

Специальные возможности необходимы для некоторых клиентов и не влияют на полноэкранные игры. Поэтому не следует изменять параметры специальных возможностей. Однако, поскольку сочетания клавиш для специальных возможностей могут нарушить воспроизведение игры, если оно запускается случайно, следует отключить ярлык специальных возможностей только в том случае, если эта функция не включена путем вызова [**системпараметерсинфо**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).

Ярлык специальных возможностей, отключенный [**системпараметерсинфо**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) , остается отключенным даже после завершения работы приложения. Это означает, что необходимо восстановить параметры перед выходом из приложения. Так как приложение может завершить работу неправильно, следует записать эти параметры в постоянное хранилище, чтобы их можно было восстановить при повторном запуске приложения. Можно также использовать обработчик исключений для восстановления этих параметров в случае сбоя.

**Отключение этих сочетаний клавиш**

1.  Запишите текущие параметры специальных возможностей перед их отключением.
2.  Отключите ярлык специальных возможностей при переходе приложения в полноэкранный режим, если функция специальных возможностей отключена.
3.  Восстановление параметров специальных возможностей при переходе приложения в режим окон или выход из него.

Этот метод используется в ДКСУТ и показан в следующем примере кода.

> [!Note]  
> Этот метод работает при работе с ограниченной учетной записью пользователя.

 

**Пример 2. Отключение сочетаний клавиш для специальных возможностей**


```C++
STICKYKEYS g_StartupStickyKeys = {sizeof(STICKYKEYS), 0};
TOGGLEKEYS g_StartupToggleKeys = {sizeof(TOGGLEKEYS), 0};
FILTERKEYS g_StartupFilterKeys = {sizeof(FILTERKEYS), 0};    
 
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Save the current sticky/toggle/filter key settings so they can be restored them later
    SystemParametersInfo(SPI_GETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
    SystemParametersInfo(SPI_GETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
    SystemParametersInfo(SPI_GETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
 
    // Disable when full screen
    AllowAccessibilityShortcutKeys( true );
 
    // Restore back when going to windowed or shutting down
    AllowAccessibilityShortcutKeys( false );
}
 
 
void AllowAccessibilityShortcutKeys( bool bAllowKeys )
{
    if( bAllowKeys )
    {
        // Restore StickyKeys/etc to original state and enable Windows key      
        STICKYKEYS sk = g_StartupStickyKeys;
        TOGGLEKEYS tk = g_StartupToggleKeys;
        FILTERKEYS fk = g_StartupFilterKeys;
        
        SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
        SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
        SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
    }
    else
    {
        // Disable StickyKeys/etc shortcuts but if the accessibility feature is on, 
        // then leave the settings alone as its probably being usefully used
 
        STICKYKEYS skOff = g_StartupStickyKeys;
        if( (skOff.dwFlags & SKF_STICKYKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            skOff.dwFlags &= ~SKF_HOTKEYACTIVE;
            skOff.dwFlags &= ~SKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &skOff, 0);
        }
 
        TOGGLEKEYS tkOff = g_StartupToggleKeys;
        if( (tkOff.dwFlags & TKF_TOGGLEKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            tkOff.dwFlags &= ~TKF_HOTKEYACTIVE;
            tkOff.dwFlags &= ~TKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &tkOff, 0);
        }
 
        FILTERKEYS fkOff = g_StartupFilterKeys;
        if( (fkOff.dwFlags & FKF_FILTERKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            fkOff.dwFlags &= ~FKF_HOTKEYACTIVE;
            fkOff.dwFlags &= ~FKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &fkOff, 0);
        }
    }
}
```



 

 