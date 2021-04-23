---
description: В этом разделе описывается отладка библиотек DLL расширения оболочки и пространства имен.
title: Отладка с помощью оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540530"
---
# <a name="debugging-with-the-shell"></a><span data-ttu-id="08698-103">Отладка с помощью оболочки</span><span class="sxs-lookup"><span data-stu-id="08698-103">Debugging with the Shell</span></span>

<span data-ttu-id="08698-104">В этом разделе описывается отладка библиотек DLL расширения оболочки и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="08698-104">This topic explains how to debug Shell and namespace extension DLLs.</span></span>

-   [<span data-ttu-id="08698-105">Запуск оболочки в отладчике</span><span class="sxs-lookup"><span data-stu-id="08698-105">Running the Shell Under a Debugger</span></span>](#running-the-shell-under-a-debugger)
-   [<span data-ttu-id="08698-106">Выполнение и тестирование расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="08698-106">Running and Testing Shell Extensions</span></span>](#running-and-testing-shell-extensions)
-   [<span data-ttu-id="08698-107">Выгрузка библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="08698-107">Unloading the DLL</span></span>](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a><span data-ttu-id="08698-108">Запуск оболочки в отладчике</span><span class="sxs-lookup"><span data-stu-id="08698-108">Running the Shell Under a Debugger</span></span>

<span data-ttu-id="08698-109">Чтобы выполнить отладку расширения, необходимо запустить оболочку из отладчика.</span><span class="sxs-lookup"><span data-stu-id="08698-109">To debug your extension, you need to run the Shell from the debugger.</span></span> <span data-ttu-id="08698-110">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="08698-110">Follow these steps:</span></span>

1.  <span data-ttu-id="08698-111">Загрузите проект расширения в отладчик, но не запускайте его.</span><span class="sxs-lookup"><span data-stu-id="08698-111">Load the extension's project into the debugger, but do not run it.</span></span>
2.  <span data-ttu-id="08698-112">Завершите работу оболочки.</span><span class="sxs-lookup"><span data-stu-id="08698-112">Shut down the Shell.</span></span>

    -   <span data-ttu-id="08698-113">Для Windows Vista и более поздних версий:</span><span class="sxs-lookup"><span data-stu-id="08698-113">For Windows Vista and later:</span></span>
        1.  <span data-ttu-id="08698-114">Отображение меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="08698-114">Display the **Start** menu.</span></span>
        2.  <span data-ttu-id="08698-115">Нажмите клавиши CTRL + SHIFT и щелкните правой кнопкой мыши фон правой половины меню **Пуск** .</span><span class="sxs-lookup"><span data-stu-id="08698-115">Press CTRL+SHIFT and right-click on the background of the right half of the **Start** menu.</span></span>
        3.  <span data-ttu-id="08698-116">В появившемся меню выберите **выход из проводника**.</span><span class="sxs-lookup"><span data-stu-id="08698-116">From the menu that appears, choose **Exit Explorer**.</span></span>
    -   <span data-ttu-id="08698-117">Для Windows XP:</span><span class="sxs-lookup"><span data-stu-id="08698-117">For Windows XP:</span></span>
        1.  <span data-ttu-id="08698-118">В меню **Пуск** выберите команду **Завершение работы**.</span><span class="sxs-lookup"><span data-stu-id="08698-118">From the **Start** menu, choose **Shut down**.</span></span>
        2.  <span data-ttu-id="08698-119">Нажмите клавиши CTRL + ALT + SHIFT и выберите **нет** в диалоговом окне **Завершение работы Windows** .</span><span class="sxs-lookup"><span data-stu-id="08698-119">Press CTRL+ALT+SHIFT, and click **No** in the **Shut Down Windows** dialog box.</span></span>

    <span data-ttu-id="08698-120">Теперь оболочка завершает работу, но все остальные приложения по-прежнему выполняются, включая отладчик.</span><span class="sxs-lookup"><span data-stu-id="08698-120">The Shell is now shut down, but all other applications are still running, including the debugger.</span></span>

3.  <span data-ttu-id="08698-121">Настройте отладчик для запуска библиотеки DLL расширения с Explorer.exe из каталога **Windows** .</span><span class="sxs-lookup"><span data-stu-id="08698-121">Set the debugger to run the extension DLL with Explorer.exe from the **Windows** directory.</span></span>
4.  <span data-ttu-id="08698-122">Запустите проект из отладчика.</span><span class="sxs-lookup"><span data-stu-id="08698-122">Run the project from the debugger.</span></span> <span data-ttu-id="08698-123">Оболочка запустится как обычно, но отладчик будет присоединен к процессу оболочки.</span><span class="sxs-lookup"><span data-stu-id="08698-123">The Shell will launch as usual, but the debugger will be attached to the Shell's process.</span></span>

## <a name="running-and-testing-shell-extensions"></a><span data-ttu-id="08698-124">Выполнение и тестирование расширений оболочки</span><span class="sxs-lookup"><span data-stu-id="08698-124">Running and Testing Shell Extensions</span></span>

<span data-ttu-id="08698-125">Вы можете запускать и тестировать расширения в отдельном процессе проводника Windows, чтобы избежать остановки и перезапуска рабочего стола и панели задач.</span><span class="sxs-lookup"><span data-stu-id="08698-125">You can run and test your extensions in a separate Windows Explorer process to avoid stopping and restarting the desktop and taskbar.</span></span> <span data-ttu-id="08698-126">Рабочий стол и панель задач по-прежнему можно использовать при запуске и тестировании расширений.</span><span class="sxs-lookup"><span data-stu-id="08698-126">Your desktop and taskbar can still be used while you run and test the extensions.</span></span>

<span data-ttu-id="08698-127">Чтобы включить эту функцию, добавьте в реестр следующий параметр REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="08698-127">To enable this feature, add the following REG\_DWORD entry to the registry.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

<span data-ttu-id="08698-128">Чтобы эта запись вступила в силу, необходимо выйти из системы и снова войти в нее.</span><span class="sxs-lookup"><span data-stu-id="08698-128">For this entry to take effect, you must log off and log on again.</span></span> <span data-ttu-id="08698-129">Этот параметр приводит к тому, что окна рабочего стола и панели задач создаются в одном Explorer.exe процессе, а все остальные окна проводника и папок открываются в другом процессе Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="08698-129">This setting causes the desktop and taskbar windows to be created in one Explorer.exe process and all other Explorer and folder windows to be opened in a different Explorer.exe process.</span></span>

<span data-ttu-id="08698-130">Кроме того, чтобы сделать работу и тестирование расширений более удобным, этот параметр также делает Рабочий стол более надежным по мере того, как он связан с расширениями оболочки.</span><span class="sxs-lookup"><span data-stu-id="08698-130">In addition to making the running and testing of your extensions more convenient, this setting also makes the desktop more robust as it relates to Shell extensions.</span></span> <span data-ttu-id="08698-131">Многие такие расширения (например, расширения контекстного меню) будут загружены в рабочий процесс Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="08698-131">Many such extensions (shortcut menu extensions, for example) will be loaded into the nondesktop Explorer.exe process.</span></span> <span data-ttu-id="08698-132">Если этот процесс завершится, Рабочий стол и панель задач не будут затронуты, а в следующем окне проводника или папки будет создан повторно завершенный процесс.</span><span class="sxs-lookup"><span data-stu-id="08698-132">If this process terminates, the desktop and taskbar will be unaffected, and the next Explorer or folder window will re-create the terminated process.</span></span>

## <a name="unloading-the-dll"></a><span data-ttu-id="08698-133">Выгрузка библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="08698-133">Unloading the DLL</span></span>

<span data-ttu-id="08698-134">Оболочка автоматически выгружает любую библиотеку DLL, если ее значение счетчика использования равно нулю, но только после того, как библиотека DLL не использовалась в течение определенного времени.</span><span class="sxs-lookup"><span data-stu-id="08698-134">The Shell automatically unloads any DLL when its usage count is zero, but only after the DLL has not been used for a period of time.</span></span> <span data-ttu-id="08698-135">Этот неактивный период может быть неприемлемым, особенно при отладке библиотеки DLL расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="08698-135">This inactive period might be unacceptably long at times, especially when a Shell extension DLL is being debugged.</span></span> <span data-ttu-id="08698-136">Вы можете сократить неактивный период, добавив в реестр следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="08698-136">You can shorten the inactive period by adding the following information to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



