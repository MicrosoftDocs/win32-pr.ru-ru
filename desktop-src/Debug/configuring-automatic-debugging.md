---
description: Пользователи могут настроить автоматическую отладку, чтобы они могли определить, почему система или приложение перестали отвечать на запросы.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Настройка автоматической отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140818"
---
# <a name="configuring-automatic-debugging"></a><span data-ttu-id="30e12-103">Настройка автоматической отладки</span><span class="sxs-lookup"><span data-stu-id="30e12-103">Configuring Automatic Debugging</span></span>

<span data-ttu-id="30e12-104">Пользователи могут настроить автоматическую отладку, чтобы они могли определить, почему система или приложение перестали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="30e12-104">Users can configure automatic debugging to help them determine why their system or an application has stopped responding.</span></span>

## <a name="configuring-automatic-debugging-for-system-crashes"></a><span data-ttu-id="30e12-105">Настройка автоматической отладки для сбоев системы</span><span class="sxs-lookup"><span data-stu-id="30e12-105">Configuring Automatic Debugging for System Crashes</span></span>

<span data-ttu-id="30e12-106">Чтобы настроить конечный компьютер для создания файла аварийного дампа при зависании системы, используйте **системное** приложение на панели управления.</span><span class="sxs-lookup"><span data-stu-id="30e12-106">To configure the target computer to generate a crash dump file when the system stops responding, use the **System** application in Control Panel.</span></span> <span data-ttu-id="30e12-107">Щелкните **Дополнительные параметры системы**, чтобы отобразить диалоговое окно **Свойства системы** .</span><span class="sxs-lookup"><span data-stu-id="30e12-107">Click **Advanced system settings**, which displays the **System Properties** dialog box.</span></span> <span data-ttu-id="30e12-108">На вкладке **Дополнительно** в этом поле щелкните **Параметры** в разделе **Запуск и восстановление**, а затем используйте соответствующие параметры восстановления.</span><span class="sxs-lookup"><span data-stu-id="30e12-108">On the **Advanced** tab of that box, click **Settings** under **Startup and Recovery**, and then use the appropriate recovery options.</span></span> <span data-ttu-id="30e12-109">Кроме того, можно настроить параметры аварийного дампа с помощью следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="30e12-109">Alternatively, you can configure crash dump options using the following registry key:</span></span>

<span data-ttu-id="30e12-110">**HKey \_ \_** \\  \\  \\  \\ **Крашконтрол** управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="30e12-110">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

<span data-ttu-id="30e12-111">Файл, который можно указать, является файлом аварийного дампа.</span><span class="sxs-lookup"><span data-stu-id="30e12-111">The file you can specify is the crash dump file.</span></span> <span data-ttu-id="30e12-112">Его имя по умолчанию — Memory. dmp.</span><span class="sxs-lookup"><span data-stu-id="30e12-112">Its default name is Memory.dmp.</span></span> <span data-ttu-id="30e12-113">Можно выполнить отладку аварийного дампа с помощью отладчика режима ядра, такого как WinDbg или KD.</span><span class="sxs-lookup"><span data-stu-id="30e12-113">You can debug a crash dump with a kernel-mode debugger, such as WinDbg or KD.</span></span> <span data-ttu-id="30e12-114">Дополнительные сведения см. в документации, прилагаемой к отладчику.</span><span class="sxs-lookup"><span data-stu-id="30e12-114">For more information, see the documentation included with the debugger.</span></span>

## <a name="configuring-automatic-debugging-for-application-crashes"></a><span data-ttu-id="30e12-115">Настройка автоматической отладки для сбоев приложений</span><span class="sxs-lookup"><span data-stu-id="30e12-115">Configuring Automatic Debugging for Application Crashes</span></span>

<span data-ttu-id="30e12-116">Когда приложение перестает отвечать (например, после нарушения прав доступа), система автоматически вызывает отладчик, указанный в реестре для отладки по подустранению, идентификатор процесса и обработчик события передаются в отладчик, если Командная строка настроена правильно.</span><span class="sxs-lookup"><span data-stu-id="30e12-116">When an application stops responding (for example, after an access violation), the system automatically invokes a debugger that is specified in the registry for postmortem debugging, The process ID and event handle are passed to the debugger if the command line is properly configured.</span></span> <span data-ttu-id="30e12-117">В следующей процедуре описывается, как указать отладчик в реестре.</span><span class="sxs-lookup"><span data-stu-id="30e12-117">The following procedure describes how to specify a debugger in the registry.</span></span>

<span data-ttu-id="30e12-118">**Настройка отладчика в качестве отладчика неустранимой**</span><span class="sxs-lookup"><span data-stu-id="30e12-118">**To set a debugger as the postmortem debugger**</span></span>

1.  <span data-ttu-id="30e12-119">Перейдите к следующему разделу реестра:</span><span class="sxs-lookup"><span data-stu-id="30e12-119">Go to the following registry key:</span></span>

    <span data-ttu-id="30e12-120">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **аедебуг**</span><span class="sxs-lookup"><span data-stu-id="30e12-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="30e12-121">Добавьте или измените значение **отладчика** , используя \_ строку reg SZ, которая указывает командную строку для отладчика.</span><span class="sxs-lookup"><span data-stu-id="30e12-121">Add or edit the **Debugger** value, using a REG\_SZ string that specifies the command line for the debugger.</span></span>

    <span data-ttu-id="30e12-122">Строка должна включать полный путь к исполняемому файлу отладчика.</span><span class="sxs-lookup"><span data-stu-id="30e12-122">The string should include the fully qualified path to the debugger executable.</span></span> <span data-ttu-id="30e12-123">Укажите идентификатор процесса и обработчик событий с параметрами "% ld" в командной строке отладчика.</span><span class="sxs-lookup"><span data-stu-id="30e12-123">Indicate the process ID and event handle with "%ld" parameters to the debugger command line.</span></span> <span data-ttu-id="30e12-124">Различные отладчики могут иметь собственные синтаксисы параметров для указания этих значений.</span><span class="sxs-lookup"><span data-stu-id="30e12-124">Different debuggers may have their own parameter syntaxes for indicating these values.</span></span> <span data-ttu-id="30e12-125">При вызове отладчика первый "% ld" заменяется ИДЕНТИФИКАТОРом процесса, а вторая "% ld" заменяется на обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="30e12-125">When the debugger is invoked, the first "%ld" is replaced with the process ID and the second "%ld" is replaced with the event handle.</span></span>

    <span data-ttu-id="30e12-126">Следующий текст является примером настройки WinDbg в качестве отладчика.</span><span class="sxs-lookup"><span data-stu-id="30e12-126">The following text is an example of how to setup up WinDbg as the debugger.</span></span>

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  <span data-ttu-id="30e12-127">Если вы хотите, чтобы отладчик вызывался без взаимодействия с пользователем, добавьте или измените значение **Auto** , используя \_ строку reg SZ, которая указывает, должна ли система отображать диалоговое окно пользователю перед вызовом отладчика.</span><span class="sxs-lookup"><span data-stu-id="30e12-127">If you want the debugger to be invoked without user interaction, add or edit the **Auto** value, using a REG\_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked.</span></span> <span data-ttu-id="30e12-128">Строка "1" отключает диалоговое окно; строка "0" включает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30e12-128">The string "1" disables the dialog box; the string "0" enables the dialog box.</span></span>

## <a name="excluding-an-application-from-automatic-debugging"></a><span data-ttu-id="30e12-129">Исключение приложения из автоматической отладки</span><span class="sxs-lookup"><span data-stu-id="30e12-129">Excluding an Application from Automatic Debugging</span></span>

<span data-ttu-id="30e12-130">Следующая процедура описывает, как исключить приложение из автоматической отладки после того, как параметр **Auto** в разделе **аедебуг** был установлен в значение 1.</span><span class="sxs-lookup"><span data-stu-id="30e12-130">The following procedure describes how to exclude an application from automatic debugging after the **Auto** value under the **AeDebug** key has been set to 1.</span></span>

<span data-ttu-id="30e12-131">**Исключение приложения из автоматической отладки**</span><span class="sxs-lookup"><span data-stu-id="30e12-131">**To exclude an application from automatic debugging**</span></span>

1.  <span data-ttu-id="30e12-132">Перейдите к следующему разделу реестра:</span><span class="sxs-lookup"><span data-stu-id="30e12-132">Go to the following registry key:</span></span>

    <span data-ttu-id="30e12-133">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **аедебуг**</span><span class="sxs-lookup"><span data-stu-id="30e12-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="30e12-134">Добавьте значение REG \_ DWORD в подраздел **аутоексклусионлист** , где name — это имя исполняемого файла, а — значение 1.</span><span class="sxs-lookup"><span data-stu-id="30e12-134">Add a REG\_DWORD value to the **AutoExclusionList** subkey, where the name is the name of the executable file and the value is 1.</span></span> <span data-ttu-id="30e12-135">По умолчанию диспетчер окон рабочего стола (Dwm.exe) исключается из автоматической отладки, так как в противном случае может произойти взаимоблокировка системы, если Dwm.exe перестает отвечать (пользователь не увидит интерфейс, отображаемый отладчиком, так как Dwm.exe не отвечает, и Dwm.exe не может завершиться, так как он удерживается отладчиком).</span><span class="sxs-lookup"><span data-stu-id="30e12-135">By default, the Desktop Window Manager (Dwm.exe) is excluded from automatic debugging because otherwise a system deadlock can occur if Dwm.exe stops responding (the user cannot see the interface displayed by the debugger because Dwm.exe isn't responding, and Dwm.exe cannot terminate because it is held by the debugger).</span></span>

    <span data-ttu-id="30e12-136">**Windows Server 2003 и Windows XP:** Подраздел **аутоексклусионлист** недоступен; Поэтому нельзя исключить какие либо приложения, включая Dwm.exe, из автоматической отладки.</span><span class="sxs-lookup"><span data-stu-id="30e12-136">**Windows Server 2003 and Windows XP:** The **AutoExclusionList** subkey is not available; thus you cannot exclude any application, including Dwm.exe, from automatic debugging.</span></span>

<span data-ttu-id="30e12-137">Записи реестра **аедебуг** по умолчанию можно представить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="30e12-137">The default **AeDebug** registry entries can be represented as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a><span data-ttu-id="30e12-138">См. также</span><span class="sxs-lookup"><span data-stu-id="30e12-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30e12-139">Включение отладки с помощью WinDbg</span><span class="sxs-lookup"><span data-stu-id="30e12-139">Enabling Postmortem Debugging with WinDbg</span></span>](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
