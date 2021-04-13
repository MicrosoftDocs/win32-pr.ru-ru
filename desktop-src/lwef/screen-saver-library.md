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
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487672"
---
# <a name="handling-screen-savers"></a><span data-ttu-id="b5101-107">Обработка экранных заставок</span><span class="sxs-lookup"><span data-stu-id="b5101-107">Handling Screen Savers</span></span>

<span data-ttu-id="b5101-108">Microsoft Win32 API поддерживает специальные приложения, которые называются *экранными заставками*.</span><span class="sxs-lookup"><span data-stu-id="b5101-108">The Microsoft Win32 API supports special applications called *screen savers*.</span></span> <span data-ttu-id="b5101-109">Экранные заставки начинают действовать, когда мышь и клавиатура простаивает в течение указанного периода времени.</span><span class="sxs-lookup"><span data-stu-id="b5101-109">Screen savers start when the mouse and keyboard have been idle for a specified period of time.</span></span> <span data-ttu-id="b5101-110">Они используются по следующим двум причинам:</span><span class="sxs-lookup"><span data-stu-id="b5101-110">They are used for these two reasons:</span></span>

-   <span data-ttu-id="b5101-111">Защита экрана от записи фосфор, вызванной статическими изображениями.</span><span class="sxs-lookup"><span data-stu-id="b5101-111">To protect a screen from phosphor burn caused by static images.</span></span>
-   <span data-ttu-id="b5101-112">Для скрытия конфиденциальной информации на экране.</span><span class="sxs-lookup"><span data-stu-id="b5101-112">To conceal sensitive information left on a screen.</span></span>

<span data-ttu-id="b5101-113">Этот раздел состоит из следующих подразделов.</span><span class="sxs-lookup"><span data-stu-id="b5101-113">This topic is divided into the following sections.</span></span>

-   [<span data-ttu-id="b5101-114">О экранных заставках</span><span class="sxs-lookup"><span data-stu-id="b5101-114">About Screen Savers</span></span>](#about-screen-savers)
-   [<span data-ttu-id="b5101-115">Использование функций экранной заставки</span><span class="sxs-lookup"><span data-stu-id="b5101-115">Using the Screen Saver Functions</span></span>](#using-the-screen-saver-functions)
    -   [<span data-ttu-id="b5101-116">Создание экранной заставки</span><span class="sxs-lookup"><span data-stu-id="b5101-116">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
    -   [<span data-ttu-id="b5101-117">Установка новых экранных заставок</span><span class="sxs-lookup"><span data-stu-id="b5101-117">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
    -   [<span data-ttu-id="b5101-118">Добавление справки в диалоговое окно "Настройка заставки экрана"</span><span class="sxs-lookup"><span data-stu-id="b5101-118">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a><span data-ttu-id="b5101-119">О экранных заставках</span><span class="sxs-lookup"><span data-stu-id="b5101-119">About Screen Savers</span></span>

<span data-ttu-id="b5101-120">Классическое приложение на панели управления Windows позволяет пользователям выбирать из списка экранных заставок, задавать, сколько времени должно пройти до запуска заставки, настраивать экранные заставки и просматривать экранные заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-120">The Desktop application in the Windows Control Panel lets users select from a list of screen savers, specify how much time should elapse before the screen saver starts, configure screen savers, and preview screen savers.</span></span> <span data-ttu-id="b5101-121">Заставки загружаются автоматически при запуске Windows или когда пользователь активирует экранную заставку с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="b5101-121">Screen savers are loaded automatically when Windows starts or when a user activates the screen saver through the Control Panel.</span></span>

<span data-ttu-id="b5101-122">После выбора заставки Windows отслеживает нажатия клавиш и движения мыши, а затем запускает экранную заставку после периода бездействия.</span><span class="sxs-lookup"><span data-stu-id="b5101-122">Once a screen saver is chosen, Windows monitors keystrokes and mouse movements and then starts the screen saver after a period of inactivity.</span></span> <span data-ttu-id="b5101-123">Однако Windows не запускает экранную заставку, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="b5101-123">However, Windows does not start the screen saver if any of the following conditions exist:</span></span>

-   <span data-ttu-id="b5101-124">Активное приложение не является приложением на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="b5101-124">The active application is not a Windows-based application.</span></span>
-   <span data-ttu-id="b5101-125">На компьютере установлено окно обучения (CBT).</span><span class="sxs-lookup"><span data-stu-id="b5101-125">A computer-based training (CBT) window is present.</span></span>
-   <span data-ttu-id="b5101-126">Активное приложение получает сообщение [WM \_ сискомманд](../menurc/wm-syscommand.md) с параметром *wParam* , установленным в значение SC \_ скринсаве, но не передает сообщение в функцию [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="b5101-126">The active application receives the [WM\_SYSCOMMAND](../menurc/wm-syscommand.md) message with the *wParam* parameter set to the SC\_SCREENSAVE value, but it does not pass the message to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="b5101-127">**Контекст безопасности экранной заставки**</span><span class="sxs-lookup"><span data-stu-id="b5101-127">**Security Context of the Screen Saver**</span></span>

<span data-ttu-id="b5101-128">Контекст безопасности экранной заставки зависит от того, вошел ли пользователь в интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="b5101-128">The security context of the screen saver is dependent on whether a user is interactively logged on.</span></span> <span data-ttu-id="b5101-129">Если пользователь интерактивно вошел в систему при вызове заставки экрана, экранная заставка запускается в контексте безопасности текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5101-129">If a user is interactively logged on when the screen saver is invoked, the screen saver runs in the security context of the interactive user.</span></span> <span data-ttu-id="b5101-130">Если ни один пользователь не вошел в систему, контекст безопасности экранной заставки зависит от используемой версии Windows.</span><span class="sxs-lookup"><span data-stu-id="b5101-130">If no user is logged on, the security context of the screen saver is dependent on the version of Windows being used.</span></span>

-   <span data-ttu-id="b5101-131">Windows XP и Windows 2000. Экранная заставка выполняется в контексте LocalSystem с ограниченными учетными записями.</span><span class="sxs-lookup"><span data-stu-id="b5101-131">Windows XP and Windows 2000 - screen saver runs in the context of LocalSystem with accounts restricted.</span></span>
-   <span data-ttu-id="b5101-132">Windows 2003. Экранная заставка выполняется в контексте локальной группы с отключенными удаленными полномочиями и группой администраторов.</span><span class="sxs-lookup"><span data-stu-id="b5101-132">Windows 2003 - screen saver runs in the context of LocalService with all privileges removed and administrators group disabled.</span></span>
-   <span data-ttu-id="b5101-133">Не применяется к Windows NT4.</span><span class="sxs-lookup"><span data-stu-id="b5101-133">Does not apply to Windows NT4.</span></span>

<span data-ttu-id="b5101-134">Контекст безопасности определяет уровень привилегированных операций, которые можно выполнять на экранной заставке.</span><span class="sxs-lookup"><span data-stu-id="b5101-134">The security context determines the level of privileged operations which can be done from a screen saver.</span></span>

<span data-ttu-id="b5101-135">**Windows Vista и более поздние версии:** Если защита паролем включена политикой, заставка запускается независимо от того, какое действие выполняет приложение с \_ уведомлением SC скринсаве.</span><span class="sxs-lookup"><span data-stu-id="b5101-135">**Windows Vista and later:** If password protection is enabled by policy, the screen saver is started regardless of what an application does with the SC\_SCREENSAVE notification.</span></span>

<span data-ttu-id="b5101-136">Экранные заставки содержат определенные экспортированные функции, определения ресурсов и объявления переменных.</span><span class="sxs-lookup"><span data-stu-id="b5101-136">Screen savers contain specific exported functions, resource definitions, and variable declarations.</span></span> <span data-ttu-id="b5101-137">Библиотека экранных заставок содержит функцию **Main** и другой код запуска, необходимый для экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-137">The screen saver library contains the **main** function and other startup code required for a screen saver.</span></span> <span data-ttu-id="b5101-138">При запуске экранной заставки код запуска в библиотеке заставок создает полноэкранное окно.</span><span class="sxs-lookup"><span data-stu-id="b5101-138">When a screen saver starts, the startup code in the screen saver library creates a full-screen window.</span></span> <span data-ttu-id="b5101-139">Класс окна для этого окна объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b5101-139">The window class for this window is declared as follows:</span></span>


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



<span data-ttu-id="b5101-140">Чтобы создать экранную заставку, большинство разработчиков создают модуль исходного кода, содержащий три необходимые функции, и связывает их с библиотекой экранных заставок.</span><span class="sxs-lookup"><span data-stu-id="b5101-140">To create a screen saver, most developers create a source code module containing three required functions and link them with the screen saver library.</span></span> <span data-ttu-id="b5101-141">Модуль экранной заставки отвечает только за настройку и предоставление визуальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="b5101-141">A screen saver module is responsible only for configuring itself and for providing visual effects.</span></span>

<span data-ttu-id="b5101-142">Одна из трех обязательных функций в модуле экранной заставки — [**скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="b5101-142">One of the three required functions in a screen saver module is [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="b5101-143">Эта функция обрабатывает определенные сообщения и передает все необработанные сообщения обратно в библиотеку экранных заставок.</span><span class="sxs-lookup"><span data-stu-id="b5101-143">This function processes specific messages and passes any unprocessed messages back to the screen saver library.</span></span> <span data-ttu-id="b5101-144">Ниже приведены некоторые типичные сообщения, обрабатываемые **скринсаверпрок**.</span><span class="sxs-lookup"><span data-stu-id="b5101-144">Following are some of the typical messages processed by **ScreenSaverProc**.</span></span>



| <span data-ttu-id="b5101-145">Сообщение</span><span class="sxs-lookup"><span data-stu-id="b5101-145">Message</span></span>        | <span data-ttu-id="b5101-146">Значение</span><span class="sxs-lookup"><span data-stu-id="b5101-146">Meaning</span></span>                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5101-147">\_Создание WM</span><span class="sxs-lookup"><span data-stu-id="b5101-147">WM\_CREATE</span></span>     | <span data-ttu-id="b5101-148">Получите данные инициализации из файла Regedit.ini.</span><span class="sxs-lookup"><span data-stu-id="b5101-148">Retrieve any initialization data from the Regedit.ini file.</span></span> <span data-ttu-id="b5101-149">Установка таймера окна для окна экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-149">Set a window timer for the screen saver window.</span></span> <span data-ttu-id="b5101-150">Выполните любую другую необходимую инициализацию.</span><span class="sxs-lookup"><span data-stu-id="b5101-150">Perform any other required initialization.</span></span>                                     |
| <span data-ttu-id="b5101-151">WM \_ ерасебкгнд</span><span class="sxs-lookup"><span data-stu-id="b5101-151">WM\_ERASEBKGND</span></span> | <span data-ttu-id="b5101-152">Стереть окно экранной заставки и подготовиться к последующим операциям рисования.</span><span class="sxs-lookup"><span data-stu-id="b5101-152">Erase the screen saver window and prepare for subsequent drawing operations.</span></span>                                                                                                               |
| <span data-ttu-id="b5101-153">\_таймер WM</span><span class="sxs-lookup"><span data-stu-id="b5101-153">WM\_TIMER</span></span>      | <span data-ttu-id="b5101-154">Выполнение операций рисования.</span><span class="sxs-lookup"><span data-stu-id="b5101-154">Perform drawing operations.</span></span>                                                                                                                                                                |
| <span data-ttu-id="b5101-155">WM \_ destroy</span><span class="sxs-lookup"><span data-stu-id="b5101-155">WM\_DESTROY</span></span>    | <span data-ttu-id="b5101-156">Уничтожайте таймеры, созданные при обработке приложением WM сообщения о [ \_ создании](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="b5101-156">Destroy the timers created when the application processed the [WM\_CREATE](../winmsg/wm-create.md) message.</span></span> <span data-ttu-id="b5101-157">Выполните все дополнительные необходимые действия по очистке.</span><span class="sxs-lookup"><span data-stu-id="b5101-157">Perform any additional required cleanup.</span></span> |



 

<span data-ttu-id="b5101-158">[**Скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) передает необработанные сообщения в библиотеку экранных заставок, вызывая функцию [**дефскринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="b5101-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passes unprocessed messages to the screen saver library by calling the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="b5101-159">В следующей таблице описано, как эта функция обрабатывает различные сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5101-159">The following table describes how this function processes various messages.</span></span>



| <span data-ttu-id="b5101-160">Сообщение</span><span class="sxs-lookup"><span data-stu-id="b5101-160">Message</span></span>         | <span data-ttu-id="b5101-161">Действие</span><span class="sxs-lookup"><span data-stu-id="b5101-161">Action</span></span>                                                                    |
|-----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b5101-162">WM \_ сеткурсор</span><span class="sxs-lookup"><span data-stu-id="b5101-162">WM\_SETCURSOR</span></span>   | <span data-ttu-id="b5101-163">Установите курсор на курсор null, удалив его с экрана.</span><span class="sxs-lookup"><span data-stu-id="b5101-163">Set the cursor to the null cursor, removing it from the screen.</span></span>           |
| <span data-ttu-id="b5101-164">WM \_ Paint</span><span class="sxs-lookup"><span data-stu-id="b5101-164">WM\_PAINT</span></span>       | <span data-ttu-id="b5101-165">Закрасьте фон экрана.</span><span class="sxs-lookup"><span data-stu-id="b5101-165">Paint the screen background.</span></span>                                              |
| <span data-ttu-id="b5101-166">WM \_ лбуттондовн</span><span class="sxs-lookup"><span data-stu-id="b5101-166">WM\_LBUTTONDOWN</span></span> | <span data-ttu-id="b5101-167">Завершите экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="b5101-167">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="b5101-168">WM \_ мбуттондовн</span><span class="sxs-lookup"><span data-stu-id="b5101-168">WM\_MBUTTONDOWN</span></span> | <span data-ttu-id="b5101-169">Завершите экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="b5101-169">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="b5101-170">WM \_ рбуттондовн</span><span class="sxs-lookup"><span data-stu-id="b5101-170">WM\_RBUTTONDOWN</span></span> | <span data-ttu-id="b5101-171">Завершите экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="b5101-171">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="b5101-172">WM \_ KeyDown</span><span class="sxs-lookup"><span data-stu-id="b5101-172">WM\_KEYDOWN</span></span>     | <span data-ttu-id="b5101-173">Завершите экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="b5101-173">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="b5101-174">WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="b5101-174">WM\_MOUSEMOVE</span></span>   | <span data-ttu-id="b5101-175">Завершите экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="b5101-175">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="b5101-176">\_Активация WM</span><span class="sxs-lookup"><span data-stu-id="b5101-176">WM\_ACTIVATE</span></span>    | <span data-ttu-id="b5101-177">Завершите экранную заставку, если параметру *wParam* присвоено значение **false**.</span><span class="sxs-lookup"><span data-stu-id="b5101-177">Terminate the screen saver if the *wParam* parameter is set to **FALSE**.</span></span> |



 

<span data-ttu-id="b5101-178">Вторая обязательная функция в модуле экранной заставки — [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span><span class="sxs-lookup"><span data-stu-id="b5101-178">The second required function in a screen saver module is [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span></span> <span data-ttu-id="b5101-179">Эта функция отображает диалоговое окно, позволяющее пользователю настроить экранную заставку (приложение должно предоставить соответствующий шаблон диалогового окна).</span><span class="sxs-lookup"><span data-stu-id="b5101-179">This function displays a dialog box that enables the user to configure the screen saver (an application must provide a corresponding dialog box template).</span></span> <span data-ttu-id="b5101-180">Windows отображает диалоговое окно Конфигурация, когда пользователь нажимает кнопку « **Настройка** » в диалоговом окне «Заставка» панели управления.</span><span class="sxs-lookup"><span data-stu-id="b5101-180">Windows displays the configuration dialog box when the user selects the **Setup** button in the Control Panel's Screen Saver dialog box.</span></span>

<span data-ttu-id="b5101-181">Третья обязательная функция в модуле экранной заставки — [**регистердиалогклассес**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span><span class="sxs-lookup"><span data-stu-id="b5101-181">The third required function in a screen saver module is [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span></span> <span data-ttu-id="b5101-182">Эта функция должна вызываться всеми приложениями экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-182">This function must be called by all screen saver applications.</span></span> <span data-ttu-id="b5101-183">Однако приложения, не требующие специальных окон или пользовательских элементов управления в диалоговом окне Конфигурация, могут просто возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b5101-183">However, applications that do not require special windows or custom controls in the configuration dialog box can simply return **TRUE**.</span></span> <span data-ttu-id="b5101-184">Приложения, которым требуются специальные окна или настраиваемые элементы управления, должны использовать эту функцию для регистрации соответствующих классов окон.</span><span class="sxs-lookup"><span data-stu-id="b5101-184">Applications requiring special windows or custom controls should use this function to register the corresponding window classes.</span></span>

<span data-ttu-id="b5101-185">Помимо создания модуля, поддерживающего только описанные выше три функции, экранная заставка должна предоставлять значок.</span><span class="sxs-lookup"><span data-stu-id="b5101-185">In addition to creating a module that supports the three functions just described, a screen saver should supply an icon.</span></span> <span data-ttu-id="b5101-186">Этот значок отображается только в том случае, если экранная заставка выполняется как автономное приложение.</span><span class="sxs-lookup"><span data-stu-id="b5101-186">This icon is visible only when the screen saver is run as a standalone application.</span></span> <span data-ttu-id="b5101-187">(Для запуска на панели управления экранная заставка должна иметь расширение SCR; для запуска в качестве автономного приложения оно должно иметь расширение EXE.) Значок должен быть идентифицирован в файле ресурсов экранной заставки с помощью приложения постоянного идентификатора \_ , которое определено в файле заголовка скрнсаве. h.</span><span class="sxs-lookup"><span data-stu-id="b5101-187">(To be run by the Control Panel, a screen saver must have the .scr file name extension; to be run as a standalone application, it must have the .exe file name extension.) The icon must be identified in the screen saver's resource file by the constant ID\_APP, which is defined in the Scrnsave.h header file.</span></span>

<span data-ttu-id="b5101-188">Одним из окончательных требований является строка описания заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-188">One final requirement is a screen saver description string.</span></span> <span data-ttu-id="b5101-189">Файл ресурсов для экранной заставки должен содержать строку, которая отображается в панели управления в качестве имени экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-189">The resource file for a screen saver must contain a string that the Control Panel displays as the screen saver name.</span></span> <span data-ttu-id="b5101-190">Строка описания должна быть первой строкой в таблице строк файла ресурсов (определяется порядковым номером 1).</span><span class="sxs-lookup"><span data-stu-id="b5101-190">The description string must be the first string in the resource file's string table (identified with the ordinal value 1).</span></span> <span data-ttu-id="b5101-191">Однако строка описания игнорируется панелью управления, если заставка имеет длинное имя файла.</span><span class="sxs-lookup"><span data-stu-id="b5101-191">However, the description string is ignored by the Control Panel if the screen saver has a long filename.</span></span> <span data-ttu-id="b5101-192">В этом случае имя файла будет использоваться в качестве строки описания.</span><span class="sxs-lookup"><span data-stu-id="b5101-192">In such case, the filename will be used as the description string.</span></span>

## <a name="using-the-screen-saver-functions"></a><span data-ttu-id="b5101-193">Использование функций экранной заставки</span><span class="sxs-lookup"><span data-stu-id="b5101-193">Using the Screen Saver Functions</span></span>

<span data-ttu-id="b5101-194">В этом разделе используется пример кода, взятый из приложения экранная заставка для иллюстрации следующих задач.</span><span class="sxs-lookup"><span data-stu-id="b5101-194">This section uses example code taken from a screen saver application to illustrate the following tasks:</span></span>

-   [<span data-ttu-id="b5101-195">Создание экранной заставки</span><span class="sxs-lookup"><span data-stu-id="b5101-195">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
-   [<span data-ttu-id="b5101-196">Установка новых экранных заставок</span><span class="sxs-lookup"><span data-stu-id="b5101-196">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
-   [<span data-ttu-id="b5101-197">Добавление справки в диалоговое окно "Настройка заставки экрана"</span><span class="sxs-lookup"><span data-stu-id="b5101-197">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a><span data-ttu-id="b5101-198">Создание экранной заставки</span><span class="sxs-lookup"><span data-stu-id="b5101-198">Creating a Screen Saver</span></span>

<span data-ttu-id="b5101-199">С интервалом в диапазоне от 1 до 10 секунд приложение в этом примере перерисовывает экран с одним из четырех цветов: белый, светло-серый, темно-серый и черный.</span><span class="sxs-lookup"><span data-stu-id="b5101-199">At intervals ranging from 1 through 10 seconds, the application in this example repaints the screen with one of four colors: white, light gray, dark gray, and black.</span></span> <span data-ttu-id="b5101-200">Приложение рисует экран каждый раз при получении сообщения [ \_ таймера WM](../winmsg/wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="b5101-200">The application paints the screen each time it receives a [WM\_TIMER](../winmsg/wm-timer.md) message.</span></span> <span data-ttu-id="b5101-201">Пользователь может настроить интервал отправки этого сообщения, выбрав диалоговое окно Конфигурация приложения и изменив одну горизонтальную полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b5101-201">The user can adjust the interval at which this message is sent by selecting the application's configuration dialog box and adjusting a single horizontal scroll bar.</span></span>

### <a name="screen-saver-library"></a><span data-ttu-id="b5101-202">Библиотека экранных заставок</span><span class="sxs-lookup"><span data-stu-id="b5101-202">Screen saver library</span></span>

<span data-ttu-id="b5101-203">Статические функции экранной заставки содержатся в библиотеке экранных заставок.</span><span class="sxs-lookup"><span data-stu-id="b5101-203">The static screen saver functions are contained in the screen saver library.</span></span> <span data-ttu-id="b5101-204">Доступны две версии библиотеки: Скрнсаве. lib и Скрнсавв. lib.</span><span class="sxs-lookup"><span data-stu-id="b5101-204">There are two versions of the library available, Scrnsave.lib and Scrnsavw.lib.</span></span> <span data-ttu-id="b5101-205">Необходимо связать проект с одним из этих элементов.</span><span class="sxs-lookup"><span data-stu-id="b5101-205">You must link your project with one of these.</span></span> <span data-ttu-id="b5101-206">Скрнсаве. lib используется для экранных заставок, использующих символы ANSI, а Скрнсавв. lib используется для экранных заставок, использующих символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="b5101-206">Scrnsave.lib is used for screen savers that use ANSI characters, and Scrnsavw.lib is used for screen savers that use Unicode characters.</span></span> <span data-ttu-id="b5101-207">Экранная заставка, связанная с Скрнсавв. lib, будет работать только на платформах Windows, поддерживающих Юникод, а экранная заставка, связанная с Скрнсаве. lib, будет выполняться на любой платформе Windows.</span><span class="sxs-lookup"><span data-stu-id="b5101-207">A screen saver that is linked with Scrnsavw.lib will only run on Windows platforms that support Unicode, while a screen saver linked with Scrnsave.lib will run on any Windows platform.</span></span>

### <a name="supporting-the-configuration-dialog-box"></a><span data-ttu-id="b5101-208">Поддержка диалогового окна «Конфигурация»</span><span class="sxs-lookup"><span data-stu-id="b5101-208">Supporting the configuration dialog box</span></span>

<span data-ttu-id="b5101-209">Большинство экранных заставок предоставляют диалоговое окно настройки, позволяющее пользователю задавать данные настройки, такие как уникальные цвета, скорости рисования, толщину линий, шрифты и т. д.</span><span class="sxs-lookup"><span data-stu-id="b5101-209">Most screen savers provide a configuration dialog box to let the user specify customization data such as unique colors, drawing speeds, line thickness, fonts, and so on.</span></span> <span data-ttu-id="b5101-210">Для поддержки диалогового окна Конфигурация приложение должно предоставить шаблон диалогового окна, а также должна поддерживать функцию [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) .</span><span class="sxs-lookup"><span data-stu-id="b5101-210">To support the configuration dialog box, the application must provide a dialog box template and must also support the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function.</span></span> <span data-ttu-id="b5101-211">Ниже приведен шаблон диалогового окна для примера приложения.</span><span class="sxs-lookup"><span data-stu-id="b5101-211">Following is the dialog box template for the sample application.</span></span>


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



<span data-ttu-id="b5101-212">Необходимо определить константу, используемую для определения шаблона диалогового окна с помощью десятичного значения 2003, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b5101-212">You must define the constant used to identify the dialog box template by using the decimal value 2003, as in the following example:</span></span>


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



<span data-ttu-id="b5101-213">В следующем примере показана функция [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , найденная в примере приложения.</span><span class="sxs-lookup"><span data-stu-id="b5101-213">The following example shows the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function found in the sample application.</span></span>


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



<span data-ttu-id="b5101-214">Помимо предоставления шаблона диалогового окна и поддержки функции [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , приложение также должно поддерживать функцию [**регистердиалогклассес**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) .</span><span class="sxs-lookup"><span data-stu-id="b5101-214">In addition to providing the dialog box template and supporting the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function, an application must also support the [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) function.</span></span> <span data-ttu-id="b5101-215">Эта функция регистрирует все нестандартные классы окон, необходимые для экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-215">This function registers any nonstandard window classes required by the screen saver.</span></span> <span data-ttu-id="b5101-216">Так как пример приложения использовал только стандартные классы окон в своей процедуре диалогового окна, эта функция просто возвращает **значение true**, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b5101-216">Because the sample application used only standard window classes in its dialog box procedure, this function simply returns **TRUE**, as in the following example:</span></span>


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a><span data-ttu-id="b5101-217">Поддержка процедуры окна экранной заставки</span><span class="sxs-lookup"><span data-stu-id="b5101-217">Supporting the screen saver window procedure</span></span>

<span data-ttu-id="b5101-218">Каждая экранная заставка должна поддерживать оконную процедуру с именем [**скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="b5101-218">Each screen saver must support a window procedure named [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="b5101-219">Как и в большинстве оконных процедур, **скринсаверпрок** обрабатывает набор конкретных сообщений и передает все необработанные сообщения в процедуру по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5101-219">Like most window procedures, **ScreenSaverProc** processes a set of specific messages and passes any unprocessed messages to a default procedure.</span></span> <span data-ttu-id="b5101-220">Однако вместо передачи их функции [Дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) **скринсаверпрок** передает необработанные сообщения в функцию [**дефскринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="b5101-220">However, instead of passing them to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function, **ScreenSaverProc** passes unprocessed messages to the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="b5101-221">Другое различие между **скринсаверпрок** и обычным окном заключается в том, что маркер, передаваемый в **скринсаверпрок** , определяет весь рабочий стол, а не клиентское окно.</span><span class="sxs-lookup"><span data-stu-id="b5101-221">Another difference between **ScreenSaverProc** and a normal window procedure is that the handle passed to **ScreenSaverProc** identifies the entire desktop rather than a client window.</span></span> <span data-ttu-id="b5101-222">В следующем примере показана процедура окна **скринсаверпрок** для образца экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="b5101-222">The following example shows the **ScreenSaverProc** window procedure for the sample screen saver.</span></span>


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



### <a name="creating-a-module-definition-file"></a><span data-ttu-id="b5101-223">Создание файла определения модуля</span><span class="sxs-lookup"><span data-stu-id="b5101-223">Creating a module-definition file</span></span>

<span data-ttu-id="b5101-224">Функции [**скринсаверпрок**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) и [**скринсаверконфигуредиалог**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) должны быть экспортированы в файл определения модуля приложения; Однако [**регистердиалогклассес**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) не следует экспортировать.</span><span class="sxs-lookup"><span data-stu-id="b5101-224">The [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) and [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) functions must be exported in the application's module-definition file; [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) should not be exported, however.</span></span> <span data-ttu-id="b5101-225">В следующем примере показан файл определения модуля для примера приложения.</span><span class="sxs-lookup"><span data-stu-id="b5101-225">The following example shows the module-definition file for the sample application.</span></span>


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



### <a name="installing-new-screen-savers"></a><span data-ttu-id="b5101-226">Установка новых экранных заставок</span><span class="sxs-lookup"><span data-stu-id="b5101-226">Installing New Screen Savers</span></span>

<span data-ttu-id="b5101-227">При компиляции списка доступных экранных заставок панель управления ищет в каталоге запуска Windows файлы с расширением SCR.</span><span class="sxs-lookup"><span data-stu-id="b5101-227">When compiling the list of available screen savers, the Control Panel searches the Windows Startup directory for files with the .scr extension.</span></span> <span data-ttu-id="b5101-228">Так как заставки являются стандартными исполняемыми файлами Windows с расширением. exe, их необходимо переименовать так, чтобы они имели расширение SCR и скопировали их в правильный каталог.</span><span class="sxs-lookup"><span data-stu-id="b5101-228">Because screen savers are standard Windows executable files with .exe extensions, you must rename them so they have .scr extensions and copy them to the correct directory.</span></span>

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a><span data-ttu-id="b5101-229">Добавление справки в диалоговое окно "Настройка заставки экрана"</span><span class="sxs-lookup"><span data-stu-id="b5101-229">Adding Help to the Screen Saver Configuration Dialog Box</span></span>

<span data-ttu-id="b5101-230">Диалоговое окно Конфигурация для экранной заставки обычно включает кнопку **Справка** .</span><span class="sxs-lookup"><span data-stu-id="b5101-230">The configuration dialog box for a screen saver typically includes a **Help** button.</span></span> <span data-ttu-id="b5101-231">Приложения-заставки могут проверять идентификатор кнопки справки и вызывать функцию [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) точно так же, как и в других приложениях на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="b5101-231">Screen saver applications can check for the Help button identifier and call the [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) function in the same way Help is provided in other Windows-based applications.</span></span>

 

 