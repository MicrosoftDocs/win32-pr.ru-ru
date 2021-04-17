---
title: Вопросы безопасности для вспомогательных технологий
description: Специальные технологии — это приложения, работающие на рабочем столе Windows и помогающие пользователям с поддержкой специальных возможностей взаимодействовать с операционной системой и другими приложениями, работающими на компьютере, включая приложения в новом пользовательском интерфейсе Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- атрибут uiAccess
- Модель автоматизации пользовательского интерфейса, атрибут uiAccess
- безопасность, атрибут uiAccess
- Тег requestedExecutionLevel
- Модель автоматизации пользовательского интерфейса, тег requestedExecutionLevel
- Модель автоматизации пользовательского интерфейса, вопросы безопасности
- Модель автоматизации пользовательского интерфейса, файлы манифеста
- файлы манифеста
- контроль учетных записей пользователей
- безопасность, контроль учетных записей
- безопасность, файлы манифеста
- безопасность, тег requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "105691707"
---
# <a name="security-considerations-for-assistive-technologies"></a><span data-ttu-id="1afd0-115">Вопросы безопасности для вспомогательных технологий</span><span class="sxs-lookup"><span data-stu-id="1afd0-115">Security Considerations for Assistive Technologies</span></span>

<span data-ttu-id="1afd0-116">Специальные технологии — это приложения, работающие на рабочем столе Windows и помогающие пользователям специальных возможностей взаимодействовать с операционной системой и другими приложениями, работающими на компьютере, включая приложения в новом пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="1afd0-116">Assistive technologies are applications that run on the Windows desktop and help accessibility users interact with the operating system and other applications running on the computer, including applications in the new Windows UI.</span></span> <span data-ttu-id="1afd0-117">Вспомогательные технологические приложения работают путем извлечения информации из операционной системы и других приложений, а затем представляют информацию в виде, доступном пользователю.</span><span class="sxs-lookup"><span data-stu-id="1afd0-117">Assistive technology applications work by retrieving information from the operating system and other applications, and then presenting the information in a way that is accessible to the user.</span></span> <span data-ttu-id="1afd0-118">Приложение с поддержкой специальных возможностей также может программно «заменять» операционную систему и другие приложения на основе входных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="1afd0-118">An assistive technology application can also programmatically "drive" the operating system and other applications based on input from the user.</span></span>

<span data-ttu-id="1afd0-119">Природа вспомогательных технологических приложений требует, чтобы они перекрестно обрабатывали границы процессов и имели доступ к процессам, выполняемым на более высоком уровне целостности (IL), чем сами по себе.</span><span class="sxs-lookup"><span data-stu-id="1afd0-119">The nature of assistive technology applications requires that they cross process boundaries, and that they have access to processes that run at a higher integrity level (IL) than themselves.</span></span> <span data-ttu-id="1afd0-120">(Приложение со специальными технологическими технологиями работает со средним IL.) Например, когда пользователь пытается выполнить задачу, для которой требуются права администратора, Windows выводит диалоговое окно, предлагающее пользователю подтвердить продолжение.</span><span class="sxs-lookup"><span data-stu-id="1afd0-120">(An assistive technology application runs at medium IL.) For example, when the user attempts to perform a task that requires administrative privileges, Windows presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="1afd0-121">Это диалоговое окно работает с более высоким IL, чтобы защитить его от межпроцессного взаимодействия, чтобы вредоносная программа не могла имитировать ввод данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="1afd0-121">This dialog box runs at a higher IL to protect it from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="1afd0-122">Аналогичным образом экран входа в систему работает на более высоком IL, чтобы предотвратить доступ других процессов к нему.</span><span class="sxs-lookup"><span data-stu-id="1afd0-122">Similarly, the desktop logon screen runs at a higher IL to prevent it from being accessed by other processes.</span></span>

<span data-ttu-id="1afd0-123">Приложениям с поддержкой специальных возможностей обычно требуется доступ к защищенным элементам пользовательского интерфейса системы или другим процессам, которые могут выполняться на более высоком уровне привилегий.</span><span class="sxs-lookup"><span data-stu-id="1afd0-123">Assistive technology applications typically need access to the protected system UI elements, or to other processes that might be running at a higher privilege level.</span></span> <span data-ttu-id="1afd0-124">Таким образом, приложения с поддержкой специальных возможностей должны быть доверенными для системы и должны запускаться с особыми привилегиями.</span><span class="sxs-lookup"><span data-stu-id="1afd0-124">Therefore, assistive technology applications must be trusted by the system, and must run with special privileges.</span></span>

<span data-ttu-id="1afd0-125">Чтобы получить доступ к более высоким процессам IL, приложение вспомогательной технологии должно установить флаг UIAccess в манифесте приложения и запустить пользователь с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="1afd0-125">To get access to higher IL processes, an assistive technology application must set the UIAccess flag in the application's manifest and be launched by a user with administrator privileges.</span></span>

> [!NOTE]
> <span data-ttu-id="1afd0-126">Права доступа ограничены следующим образом.</span><span class="sxs-lookup"><span data-stu-id="1afd0-126">Access privileges are constrained as follows:</span></span>
>
> - <span data-ttu-id="1afd0-127">Приложение, не имеющее UIAccess в манифесте, начинается с среднего IL и не может получить доступ к пользовательскому интерфейсу процесса с повышенными правами ("Medium +").</span><span class="sxs-lookup"><span data-stu-id="1afd0-127">An application that doesn't have UIAccess in the manifest starts with medium IL and cannot access elevated ("medium+" IL) process UI.</span></span>
> - <span data-ttu-id="1afd0-128">Приложение, которое имеет UIAccess в манифесте и запускается пользователем, не входящим в группу "Администраторы", запускается как "средний +" IL и не может получить доступ к пользовательскому интерфейсу с повышенными правами (не работает как "высокий" IL, например приложения, запускаемые с помощью **правой кнопки мыши > Запуск от имени администратора**).</span><span class="sxs-lookup"><span data-stu-id="1afd0-128">An application that has UIAccess in the manifest and is launched by a user who is not in the administrators group, starts as "medium+" IL and cannot access elevated UI (nothing running as "high" IL, such as apps launched through a **Right click -> Run as administrator**).</span></span>
> - <span data-ttu-id="1afd0-129">Приложение имеет доступ к пользовательскому интерфейсу и запускается пользователем-администратором, запускается как "высокий" IL и может получить доступ к пользовательскому интерфейсу с повышенными правами, так как он имеет тот же IL.</span><span class="sxs-lookup"><span data-stu-id="1afd0-129">An application has UI Access and is launched by an admin user starts as "high" IL and can access elevated UI because it has the same IL.</span></span>
>
> <span data-ttu-id="1afd0-130">UIAccess недостаточно для перемещения процесса через границу IL.</span><span class="sxs-lookup"><span data-stu-id="1afd0-130">UIAccess is not enough for a process to move up through the IL boundary.</span></span>

<span data-ttu-id="1afd0-131">Помимо доступа к процессам с более высоким IL, вспомогательное приложение с этими привилегиями может выполняться в качестве самого верхнего приложения в z-порядке в любое время, что означает, что вспомогательное приложение может быть видимым и доступным в любой момент, когда оно потребуется пользователю.</span><span class="sxs-lookup"><span data-stu-id="1afd0-131">In addition to having access to higher IL processes, an assistive technology application with these privileges can run as the topmost application in the z-order at any time, meaning that an assistive technology application can be visible and available whenever the user needs it.</span></span>

> [!Important]
> <span data-ttu-id="1afd0-132">Ни один из перечисленных выше сценариев не предоставляет доступ к пользовательскому интерфейсу, выполняющемуся в системе IL.</span><span class="sxs-lookup"><span data-stu-id="1afd0-132">None of the previously listed scenarios provide access to UI running under the system IL.</span></span> <span data-ttu-id="1afd0-133">Это возможно только в том случае, если процесс запускается в рабочем столе контроля учетных записей (UAC) в разделе SYSTEM (и System IL).</span><span class="sxs-lookup"><span data-stu-id="1afd0-133">This is only possible if the process is launched in the user account control (UAC) desktop under SYSTEM (and system IL).</span></span> <span data-ttu-id="1afd0-134">В этом случае установка UIAccess не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="1afd0-134">In this case, setting UIAccess has no effect.</span></span>

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a><span data-ttu-id="1afd0-135">Требования к UIAccess для приложений вспомогательной технологии</span><span class="sxs-lookup"><span data-stu-id="1afd0-135">UIAccess Requirements for Assistive Technology Applications</span></span>

<span data-ttu-id="1afd0-136">Приложение с поддержкой специальных возможностей — это классическое приложение Windows Windows, которое взаимодействует с другими процессами, запущенными на рабочем столе, и в новом пользовательском интерфейсе Windows для получения информации из системы и приложений.</span><span class="sxs-lookup"><span data-stu-id="1afd0-136">An assistive technology application is a Windows Windows desktop application that interacts with other processes running on the desktop and in the new Windows UI to get information from the system and applications.</span></span> <span data-ttu-id="1afd0-137">Затем приложение вспомогательной технологии может предоставить сведения пользователям специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="1afd0-137">The assistive technology application can then provide the information to accessibility users.</span></span>

<span data-ttu-id="1afd0-138">Приложение вспомогательной технологии получает доступ к другим процессам, устанавливая флаг UIAccess в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="1afd0-138">An assistive technology application gets access to other processes by setting the UIAccess flag in the application manifest.</span></span> <span data-ttu-id="1afd0-139">Чтобы использовать флаг UIAccess, приложение вспомогательной технологии должно соответствовать следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="1afd0-139">To use the UIAccess flag, an assistive technology application must meet the following requirements.</span></span>

-   <span data-ttu-id="1afd0-140">Требуется для отображения, взаимодействия с или отражения данных из другого приложения для предоставления сведений о сценарии специальных возможностей и (или)</span><span class="sxs-lookup"><span data-stu-id="1afd0-140">Require to display, interact with, or reflect information from another application to provide information for an accessibility scenario, and/or</span></span>
-   <span data-ttu-id="1afd0-141">Для получения или вывода этих сведений требуется запуск в качестве верхнего окна.</span><span class="sxs-lookup"><span data-stu-id="1afd0-141">Require running as the top-most window to obtain or display this information.</span></span>

<span data-ttu-id="1afd0-142">Чтобы использовать UIAccess, приложение вспомогательной технологии должно:</span><span class="sxs-lookup"><span data-stu-id="1afd0-142">To use UIAccess, an assistive technology application needs to:</span></span>

-   <span data-ttu-id="1afd0-143">Подписываться сертификатом для взаимодействия с приложениями, работающими на более высоком уровне привилегий.</span><span class="sxs-lookup"><span data-stu-id="1afd0-143">Be signed with a certificate to interact with applications running at a higher privilege level.</span></span>
-   <span data-ttu-id="1afd0-144">Быть доверенным для системы.</span><span class="sxs-lookup"><span data-stu-id="1afd0-144">Be trusted by the system.</span></span> <span data-ttu-id="1afd0-145">Приложение должно быть установлено в безопасном месте, требующем запроса контроля учетных записей (UAC) для доступа.</span><span class="sxs-lookup"><span data-stu-id="1afd0-145">The application must be installed in a secure location that requires a user account control (UAC) prompt for access.</span></span> <span data-ttu-id="1afd0-146">Например, папка Program Files.</span><span class="sxs-lookup"><span data-stu-id="1afd0-146">For example, the Program Files folder.</span></span>
-   <span data-ttu-id="1afd0-147">Сборка с помощью файла манифеста, включающего флаг uiAccess.</span><span class="sxs-lookup"><span data-stu-id="1afd0-147">Be built with a manifest file that includes the uiAccess flag.</span></span>

<span data-ttu-id="1afd0-148">Не следует использовать UIAccess:</span><span class="sxs-lookup"><span data-stu-id="1afd0-148">UIAccess should not be used:</span></span>

-   <span data-ttu-id="1afd0-149">Приложениями, не поддерживающими специальные технологии.</span><span class="sxs-lookup"><span data-stu-id="1afd0-149">By applications that are not assistive technologies.</span></span>
-   <span data-ttu-id="1afd0-150">Вспомогательными технологическими приложениями, которые отображают информацию или пользовательский интерфейс, не относящиеся к используемому сценарию доступности.</span><span class="sxs-lookup"><span data-stu-id="1afd0-150">By assistive technology applications that display information or UI that is not relevant to the accessibility scenario they target.</span></span>
-   <span data-ttu-id="1afd0-151">Приложениями, которые должны отображаться над другими приложениями в новом пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="1afd0-151">By applications that just want to appear above other applications in the new Windows UI.</span></span>
    > [!Note]  
    > <span data-ttu-id="1afd0-152">Приложения, разработанные для нового пользовательского интерфейса Windows, не имеют UIAccess в качестве доступного варианта.</span><span class="sxs-lookup"><span data-stu-id="1afd0-152">Applications developed for the new Windows UI do not have UIAccess as an available option.</span></span>

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a><span data-ttu-id="1afd0-153">Настройка UIAccess в файле манифеста приложения</span><span class="sxs-lookup"><span data-stu-id="1afd0-153">Setting UIAccess in the Application Manifest File</span></span>

<span data-ttu-id="1afd0-154">Чтобы получить доступ к защищенному системному ИНТЕРФЕЙСу, приложения должны быть построены с помощью файла манифеста, содержащего специальный атрибут в файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="1afd0-154">To gain access to the protected system UI, applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="1afd0-155">Этот атрибут **UIAccess** включен в тег **requestedExecutionLevel** , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="1afd0-155">This **uiAccess** attribute is included in the **requestedExecutionLevel** tag, as shown in the following code example.</span></span>


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



<span data-ttu-id="1afd0-156">Значение атрибута **Level** в этом коде является только примером.</span><span class="sxs-lookup"><span data-stu-id="1afd0-156">The value of the **level** attribute in this code is an example only.</span></span>

<span data-ttu-id="1afd0-157">По умолчанию **UIAccess** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="1afd0-157">**UIAccess** is "false" by default.</span></span> <span data-ttu-id="1afd0-158">Если атрибут пропущен или отсутствует манифест, приложение не сможет получить доступ к защищенному пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="1afd0-158">If the attribute is omitted, or if there is no manifest, the application cannot gain access to the protected UI.</span></span>

<span data-ttu-id="1afd0-159">Дополнительные сведения о безопасности Windows, о подписывании приложений, а также о создании манифестов см. в [статье Windows Vista и Windows Server 2008 для разработчиков. требования к разработке приложений Windows Vista для управления учетными записями пользователей (UAC)](/previous-versions/aa905330(v=msdn.10)) на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="1afd0-159">For more information on Windows security, on signing applications, and on creating manifests, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1afd0-160">См. также</span><span class="sxs-lookup"><span data-stu-id="1afd0-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1afd0-161">Основы модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="1afd0-161">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 