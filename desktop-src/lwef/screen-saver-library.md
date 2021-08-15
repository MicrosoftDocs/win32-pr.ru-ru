---
title: Обработка экранных заставок
description: Microsoft Win32 API поддерживает специальные приложения, которые называются экранными заставками.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- экранные заставки
- Панель управления, заставки
- скринсаверконфигуредиалог
- файлы определения модуля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61343cd586ed022c334b797a77320ee25eccdf48653b4732adc597f4aedde26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975724"
---
# <a name="handling-screen-savers"></a>Обработка экранных заставок

Microsoft Win32 API поддерживает специальные приложения, которые называются *экранными заставками*. Экранные заставки начинают действовать, когда мышь и клавиатура простаивает в течение указанного периода времени. Они используются по следующим двум причинам:

-   Защита экрана от записи фосфор, вызванной статическими изображениями.
-   Для скрытия конфиденциальной информации на экране.

Этот раздел состоит из следующих подразделов.

-   [О экранных заставках](#about-screen-savers)
-   [Использование функций экранной заставки](#using-the-screen-saver-functions)
    -   [Создание экранной заставки](#creating-a-screen-saver)
    -   [Установка новых экранных заставок](#installing-new-screen-savers)
    -   [Добавление справки в диалоговое окно "Настройка заставки экрана"](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>О экранных заставках

классическое приложение на панели управления Windows позволяет пользователям выбирать из списка экранных заставок, задавать, сколько времени должно пройти перед запуском заставки, настраивать экранные заставки и заставку экранных заставок. заставки загружаются автоматически при Windows запуске или когда пользователь активирует экранную заставку с помощью панели управления.

после выбора экранной заставки Windows отслеживает нажатия клавиш и движения мыши, а затем запускает экранную заставку после периода бездействия. однако Windows не запускает экранную заставку, если выполняется одно из следующих условий.

-   активное приложение не является приложением на основе Windows.
-   На компьютере установлено окно обучения (CBT).
-   Активное приложение получает сообщение [WM \_ сискомманд](../menurc/wm-syscommand.md) с параметром *wParam* , установленным в значение SC \_ скринсаве, но не передает сообщение в функцию [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

**Контекст безопасности экранной заставки**

Контекст безопасности экранной заставки зависит от того, вошел ли пользователь в интерактивный режим. Если пользователь интерактивно вошел в систему при вызове заставки экрана, экранная заставка запускается в контексте безопасности текущего пользователя. если ни один пользователь не вошел в систему, контекст безопасности экранной заставки зависит от используемой версии Windows.

-   Windows XP и Windows 2000-экранная заставка выполняется в контексте LocalSystem с ограниченными учетными записями.
-   Windows 2003-экранная заставка выполняется в контексте локальной группы с отключенными удаленными привилегиями и группой администраторов.
-   не применяется к Windows NT4.

Контекст безопасности определяет уровень привилегированных операций, которые можно выполнять на экранной заставке.

**Windows Vista и более поздних версий:** Если защита паролем включена политикой, заставка запускается независимо от того, какое действие выполняет приложение с \_ уведомлением SC скринсаве.

Экранные заставки содержат определенные экспортированные функции, определения ресурсов и объявления переменных. Библиотека экранных заставок содержит функцию **Main** и другой код запуска, необходимый для экранной заставки. При запуске экранной заставки код запуска в библиотеке заставок создает полноэкранное окно. Класс окна для этого окна объявляется следующим образом:


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



Чтобы создать экранную заставку, большинство разработчиков создают модуль исходного кода, содержащий три необходимые функции, и связывает их с библиотекой экранных заставок. Модуль экранной заставки отвечает только за настройку и предоставление визуальных эффектов.

Одна из трех обязательных функций в модуле экранной заставки — [**скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Эта функция обрабатывает определенные сообщения и передает все необработанные сообщения обратно в библиотеку экранных заставок. Ниже приведены некоторые типичные сообщения, обрабатываемые **скринсаверпрок**.



| Сообщение        | Значение                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Создание WM     | Получите данные инициализации из файла Regedit.ini. Установка таймера окна для окна экранной заставки. Выполните любую другую необходимую инициализацию.                                     |
| WM \_ ерасебкгнд | Стереть окно экранной заставки и подготовиться к последующим операциям рисования.                                                                                                               |
| \_таймер WM      | Выполнение операций рисования.                                                                                                                                                                |
| WM \_ destroy    | Уничтожайте таймеры, созданные при обработке приложением WM сообщения о [ \_ создании](../winmsg/wm-create.md) . Выполните все дополнительные необходимые действия по очистке. |



 

[**Скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) передает необработанные сообщения в библиотеку экранных заставок, вызывая функцию [**дефскринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . В следующей таблице описано, как эта функция обрабатывает различные сообщения.



| Message         | Действие                                                                    |
|-----------------|---------------------------------------------------------------------------|
| WM \_ сеткурсор   | Установите курсор на курсор null, удалив его с экрана.           |
| WM \_ Paint       | Paint фон экрана.                                              |
| WM \_ лбуттондовн | Завершите экранную заставку.                                               |
| WM \_ мбуттондовн | Завершите экранную заставку.                                               |
| WM \_ рбуттондовн | Завершите экранную заставку.                                               |
| WM \_ KeyDown     | Завершите экранную заставку.                                               |
| WM \_ MOUSEMOVE   | Завершите экранную заставку.                                               |
| \_Активация WM    | Завершите экранную заставку, если параметру *wParam* присвоено значение **false**. |



 

Вторая обязательная функция в модуле экранной заставки — [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog). Эта функция отображает диалоговое окно, позволяющее пользователю настроить экранную заставку (приложение должно предоставить соответствующий шаблон диалогового окна). Windows отображает диалоговое окно конфигурация, когда пользователь нажимает кнопку « **настройка** » в диалоговом окне «заставка» панели управления.

Третья обязательная функция в модуле экранной заставки — [**регистердиалогклассес**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses). Эта функция должна вызываться всеми приложениями экранной заставки. Однако приложения, не требующие специальных окон или пользовательских элементов управления в диалоговом окне Конфигурация, могут просто возвращать **значение true**. Приложения, которым требуются специальные окна или настраиваемые элементы управления, должны использовать эту функцию для регистрации соответствующих классов окон.

Помимо создания модуля, поддерживающего только описанные выше три функции, экранная заставка должна предоставлять значок. Этот значок отображается только в том случае, если экранная заставка выполняется как автономное приложение. (Для запуска на панели управления экранная заставка должна иметь расширение. SCR. для запуска в качестве автономного приложения оно должно иметь расширение .exe File.) Значок должен быть идентифицирован в файле ресурсов экранной заставки с помощью приложения постоянного идентификатора \_ , которое определено в файле заголовка скрнсаве. h.

Одним из окончательных требований является строка описания заставки. Файл ресурсов для экранной заставки должен содержать строку, которая отображается в панели управления в качестве имени экранной заставки. Строка описания должна быть первой строкой в таблице строк файла ресурсов (определяется порядковым номером 1). Однако строка описания игнорируется панелью управления, если заставка имеет длинное имя файла. В этом случае имя файла будет использоваться в качестве строки описания.

## <a name="using-the-screen-saver-functions"></a>Использование функций экранной заставки

В этом разделе используется пример кода, взятый из приложения экранная заставка для иллюстрации следующих задач.

-   [Создание экранной заставки](#creating-a-screen-saver)
-   [Установка новых экранных заставок](#installing-new-screen-savers)
-   [Добавление справки в диалоговое окно "Настройка заставки экрана"](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>Создание экранной заставки

С интервалом в диапазоне от 1 до 10 секунд приложение в этом примере перерисовывает экран с одним из четырех цветов: белый, светло-серый, темно-серый и черный. Приложение рисует экран каждый раз при получении сообщения [ \_ таймера WM](../winmsg/wm-timer.md) . Пользователь может настроить интервал отправки этого сообщения, выбрав диалоговое окно Конфигурация приложения и изменив одну горизонтальную полосу прокрутки.

### <a name="screen-saver-library"></a>Библиотека экранных заставок

Статические функции экранной заставки содержатся в библиотеке экранных заставок. Доступны две версии библиотеки: Скрнсаве. lib и Скрнсавв. lib. Необходимо связать проект с одним из этих элементов. Скрнсаве. lib используется для экранных заставок, использующих символы ANSI, а Скрнсавв. lib используется для экранных заставок, использующих символы Юникода. экранная заставка, связанная с скрнсавв. lib, будет работать только на платформах Windows, поддерживающих юникод, а экранная заставка, связанная с скрнсаве. lib, будет выполняться на любой платформе Windows.

### <a name="supporting-the-configuration-dialog-box"></a>Поддержка диалогового окна «Конфигурация»

Большинство экранных заставок предоставляют диалоговое окно настройки, позволяющее пользователю задавать данные настройки, такие как уникальные цвета, скорости рисования, толщину линий, шрифты и т. д. Для поддержки диалогового окна Конфигурация приложение должно предоставить шаблон диалогового окна, а также должна поддерживать функцию [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) . Ниже приведен шаблон диалогового окна для примера приложения.


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



Необходимо определить константу, используемую для определения шаблона диалогового окна с помощью десятичного значения 2003, как показано в следующем примере:


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



В следующем примере показана функция [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , найденная в примере приложения.


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



Помимо предоставления шаблона диалогового окна и поддержки функции [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , приложение также должно поддерживать функцию [**регистердиалогклассес**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) . Эта функция регистрирует все нестандартные классы окон, необходимые для экранной заставки. Так как пример приложения использовал только стандартные классы окон в своей процедуре диалогового окна, эта функция просто возвращает **значение true**, как показано в следующем примере:


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>Поддержка процедуры окна экранной заставки

Каждая экранная заставка должна поддерживать оконную процедуру с именем [**скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc). Как и в большинстве оконных процедур, **скринсаверпрок** обрабатывает набор конкретных сообщений и передает все необработанные сообщения в процедуру по умолчанию. Однако вместо передачи их функции [Дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) **скринсаверпрок** передает необработанные сообщения в функцию [**дефскринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) . Другое различие между **скринсаверпрок** и обычным окном заключается в том, что маркер, передаваемый в **скринсаверпрок** , определяет весь рабочий стол, а не клиентское окно. В следующем примере показана процедура окна **скринсаверпрок** для образца экранной заставки.


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a>Создание файла определения модуля

Функции [**скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) и [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) должны быть экспортированы в файл определения модуля приложения; Однако [**регистердиалогклассес**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) не следует экспортировать. В следующем примере показан файл определения модуля для примера приложения.


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a>Установка новых экранных заставок

при компиляции списка доступных экранных заставок панель управления ищет в каталоге запуска Windows файлы с расширением scr. так как заставки являются стандартными Windows исполняемые файлы с расширениями .exe, их необходимо переименовать так, чтобы они имели расширение scr и скопировали их в правильный каталог.

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>Добавление справки в диалоговое окно "Настройка заставки экрана"

Диалоговое окно Конфигурация для экранной заставки обычно включает кнопку **Справка** . приложения-заставки могут проверять идентификатор кнопки справки и вызывать функцию [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) точно так же, как и в других приложениях на основе Windows.

 

 