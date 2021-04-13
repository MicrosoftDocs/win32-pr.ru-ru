---
title: Отключение сочетаний клавиш в играх
description: В этой статье описывается временное отключение сочетаний клавиш в Microsoft Windows для предотвращения сбоев игр в полноэкранном режиме.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff426e0d728150cf5f6ac3cd8d46a711c9b4f8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487925"
---
# <a name="disabling-shortcut-keys-in-games"></a><span data-ttu-id="f6f18-103">Отключение сочетаний клавиш в играх</span><span class="sxs-lookup"><span data-stu-id="f6f18-103">Disabling Shortcut Keys in Games</span></span>

<span data-ttu-id="f6f18-104">В этой статье описывается временное отключение сочетаний клавиш в Microsoft Windows для предотвращения сбоев игр в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="f6f18-104">This articles describes how to temporarily disable keyboard shortcuts in Microsoft Windows to prevent disruption of game play for full screen games.</span></span> <span data-ttu-id="f6f18-105">Клавиша SHIFT и клавиша CTRL часто используются в качестве пожара или запуска кнопок в играх.</span><span class="sxs-lookup"><span data-stu-id="f6f18-105">The SHIFT key and the CTRL key are often used as fire or run buttons in games.</span></span> <span data-ttu-id="f6f18-106">Если пользователи случайно нажимают клавишу Windows (расположенную рядом с этими ключами), они могут привести к внезапному переходу из приложения, руинс работу с игрой.</span><span class="sxs-lookup"><span data-stu-id="f6f18-106">If users accidentally press the Windows key (located near these keys), they can cause themselves to suddenly jump out of the application, which ruins the game experience.</span></span> <span data-ttu-id="f6f18-107">Простое использование клавиши SHIFT в качестве кнопки игры может привести к непреднамеренному выполнению сочетания клавиш, которое может отображать диалоговое окно предупреждения.</span><span class="sxs-lookup"><span data-stu-id="f6f18-107">Simply using the SHIFT key as a game button can inadvertently execute the StickyKeys shortcut which may display a warning dialog.</span></span> <span data-ttu-id="f6f18-108">Чтобы избежать этих проблем, следует отключить эти ключи при работе в полноэкранном режиме и либо включить ключи обратно в обработчики по умолчанию при работе в оконном режиме, либо выйти из приложения.</span><span class="sxs-lookup"><span data-stu-id="f6f18-108">To avoid these issues, you should disable these keys when running in full-screen mode, and either enable the keys back to their default handlers when running in windowed mode or exit the application.</span></span>

<span data-ttu-id="f6f18-109">В этой статье описывается, как выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f6f18-109">This article describes how to do the following:</span></span>

-   [<span data-ttu-id="f6f18-110">Отключение клавиши Windows с помощью обработчика клавиатуры</span><span class="sxs-lookup"><span data-stu-id="f6f18-110">Disable the Windows Key with a Keyboard Hook</span></span>](#disable-the-windows-key-with-a-keyboard-hook)
-   [<span data-ttu-id="f6f18-111">Отключение сочетаний клавиш для специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="f6f18-111">Disable the Accessibility Shortcut Keys</span></span>](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a><span data-ttu-id="f6f18-112">Отключение клавиши Windows с помощью обработчика клавиатуры</span><span class="sxs-lookup"><span data-stu-id="f6f18-112">Disable the Windows Key with a Keyboard Hook</span></span>

<span data-ttu-id="f6f18-113">Используйте клавиатурный обработчик низкого уровня, чтобы отфильтровать клавишу Windows из обработки.</span><span class="sxs-lookup"><span data-stu-id="f6f18-113">Use a low-level keyboard hook to filter out the Windows key from being processed.</span></span> <span data-ttu-id="f6f18-114">Обработчик клавиатур низкого уровня, показанный в примере 1, остается в силе, даже если пользователь свертывает окно или переключается на другое приложение.</span><span class="sxs-lookup"><span data-stu-id="f6f18-114">The low-level keyboard hook shown in Example 1 remains in effect even if a user minimizes the window or switches to another application.</span></span> <span data-ttu-id="f6f18-115">Это означает, что необходимо соблюдать осторожность, чтобы при деактивации приложения ключ Windows не был отключен.</span><span class="sxs-lookup"><span data-stu-id="f6f18-115">This means that you must be careful to ensure that the Windows key is not disabled when the application is deactivated.</span></span> <span data-ttu-id="f6f18-116">Код в примере 1 делает это, обрабатывая сообщение WM \_ активатеапп.</span><span class="sxs-lookup"><span data-stu-id="f6f18-116">The code in Example 1 does this by handling the WM\_ACTIVATEAPP message.</span></span>

> [!Note]  
> <span data-ttu-id="f6f18-117">Этот метод работает в Windows 2000 и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="f6f18-117">This method works on Windows 2000 and later versions of Windows.</span></span> <span data-ttu-id="f6f18-118">Этот метод также работает с учетными записями пользователей с минимальными привилегиями (также известными как учетные записи с ограниченными правами).</span><span class="sxs-lookup"><span data-stu-id="f6f18-118">This method also works with least-privileged user accounts (also known as limited-user accounts).</span></span>

 

<span data-ttu-id="f6f18-119">Этот метод используется ДКСУТ и демонстрируется в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f6f18-119">This method is used by DXUT and is illustrated in the following code example.</span></span>

<span data-ttu-id="f6f18-120">**Пример 1. Использование обработчика клавиатуры низкого уровня для отключения ключа Windows**</span><span class="sxs-lookup"><span data-stu-id="f6f18-120">**Example 1. Using a low-level keyboard hook to disable the Windows key**</span></span>


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



## <a name="disable-the-accessibility-shortcut-keys"></a><span data-ttu-id="f6f18-121">Отключение сочетаний клавиш для специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="f6f18-121">Disable the Accessibility Shortcut Keys</span></span>

<span data-ttu-id="f6f18-122">В состав Windows входят специальные возможности, такие как залипание клавиш, режим фильтрации и озвучивание (см. раздел [Специальные возможности Windows](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span><span class="sxs-lookup"><span data-stu-id="f6f18-122">Windows includes accessibility features such as StickyKeys, FilterKeys, and ToggleKeys (see [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span></span> <span data-ttu-id="f6f18-123">Для каждого из них используется другая цель; Например, залипание залипания клавиш предназначено для пользователей, которые испытывают трудности одновременного нажатия двух или более ключей.</span><span class="sxs-lookup"><span data-stu-id="f6f18-123">Each of these serves a different purpose; StickyKeys for example, is designed for people who have difficulty holding down two or more keys simultaneously.</span></span> <span data-ttu-id="f6f18-124">У каждой из этих специальных возможностей также есть сочетание клавиш, которое позволяет включить или отключить функцию.</span><span class="sxs-lookup"><span data-stu-id="f6f18-124">Each of these accessibility features also has a keyboard shortcut that allows the feature to be turned on or off.</span></span> <span data-ttu-id="f6f18-125">Например, нажатие клавиши SHIFT вызывается пять раз.</span><span class="sxs-lookup"><span data-stu-id="f6f18-125">For example, the StickyKeys shortcut is triggered by pressing the SHIFT key five times.</span></span> <span data-ttu-id="f6f18-126">Если клавиша SHIFT также используется в игре, пользователь может случайно активировать это сочетание клавиш во время игры.</span><span class="sxs-lookup"><span data-stu-id="f6f18-126">If the SHIFT key is also used in the game, the user could accidentally trigger this shortcut during game play.</span></span> <span data-ttu-id="f6f18-127">При активации ярлыка Windows (по умолчанию) выводит предупреждение в диалоговом окне, что приведет к уменьшению числа игр, работающих в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="f6f18-127">When the shortcut is triggered, Windows (by default) presents a warning in a dialog box, which would cause Windows to minimize a game running in full-screen mode.</span></span> <span data-ttu-id="f6f18-128">Это, конечно, может существенно повлиять на игру.</span><span class="sxs-lookup"><span data-stu-id="f6f18-128">This, of course, can have a drastic effect on game play.</span></span>

<span data-ttu-id="f6f18-129">Специальные возможности необходимы для некоторых клиентов и не влияют на полноэкранные игры. Поэтому не следует изменять параметры специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="f6f18-129">The accessibility features are required for some customers and do not themselves interfere with full-screen games; therefore, you should not change the accessibility settings.</span></span> <span data-ttu-id="f6f18-130">Однако, поскольку сочетания клавиш для специальных возможностей могут нарушить воспроизведение игры, если оно запускается случайно, следует отключить ярлык специальных возможностей только в том случае, если эта функция не включена путем вызова [**системпараметерсинфо**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="f6f18-130">However, because the shortcuts for accessibility features can disrupt game play if triggered accidentally, you should turn off an accessibility shortcut only when that feature is not enabled by calling [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span></span>

<span data-ttu-id="f6f18-131">Ярлык специальных возможностей, отключенный [**системпараметерсинфо**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) , остается отключенным даже после завершения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="f6f18-131">An accessibility shortcut that is turned off by [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) remains turned off even after the application has exited.</span></span> <span data-ttu-id="f6f18-132">Это означает, что необходимо восстановить параметры перед выходом из приложения.</span><span class="sxs-lookup"><span data-stu-id="f6f18-132">This means that you must restore the settings before exiting the application.</span></span> <span data-ttu-id="f6f18-133">Так как приложение может завершить работу неправильно, следует записать эти параметры в постоянное хранилище, чтобы их можно было восстановить при повторном запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="f6f18-133">Because it is possible for the application to fail to exit correctly, you should write these settings to persistent storage so that they can be restored when the application is run again.</span></span> <span data-ttu-id="f6f18-134">Можно также использовать обработчик исключений для восстановления этих параметров в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="f6f18-134">You could also use an exception handler to restore these settings if a crash occurs.</span></span>

<span data-ttu-id="f6f18-135">**Отключение этих сочетаний клавиш**</span><span class="sxs-lookup"><span data-stu-id="f6f18-135">**To turn off these shortcuts**</span></span>

1.  <span data-ttu-id="f6f18-136">Запишите текущие параметры специальных возможностей перед их отключением.</span><span class="sxs-lookup"><span data-stu-id="f6f18-136">Capture the current accessibility settings before disabling them.</span></span>
2.  <span data-ttu-id="f6f18-137">Отключите ярлык специальных возможностей при переходе приложения в полноэкранный режим, если функция специальных возможностей отключена.</span><span class="sxs-lookup"><span data-stu-id="f6f18-137">Disable the accessibility shortcut when the application goes into full-screen mode if the accessibility feature is off.</span></span>
3.  <span data-ttu-id="f6f18-138">Восстановление параметров специальных возможностей при переходе приложения в режим окон или выход из него.</span><span class="sxs-lookup"><span data-stu-id="f6f18-138">Restore the accessibility settings when the application goes into windowed mode or exits.</span></span>

<span data-ttu-id="f6f18-139">Этот метод используется в ДКСУТ и показан в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f6f18-139">This method is used in DXUT, and is illustrated in the following code example.</span></span>

> [!Note]  
> <span data-ttu-id="f6f18-140">Этот метод работает при работе с ограниченной учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6f18-140">This method works when running on a limited user account.</span></span>

 

<span data-ttu-id="f6f18-141">**Пример 2. Отключение сочетаний клавиш для специальных возможностей**</span><span class="sxs-lookup"><span data-stu-id="f6f18-141">**Example 2. Disabling accessibility shortcut keys**</span></span>


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



 

 