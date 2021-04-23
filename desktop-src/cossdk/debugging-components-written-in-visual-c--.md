---
description: Когда вы будете готовы к отладке функциональных возможностей COM+ в компонентах Microsoft Visual C++, можно настроить Visual C++ проект или средство администрирования служб компонентов для запуска отладчика.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Отладка компонентов, написанных на Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701176"
---
# <a name="debugging-components-written-in-visual-c"></a><span data-ttu-id="80c5d-103">Отладка компонентов, написанных на Visual C++</span><span class="sxs-lookup"><span data-stu-id="80c5d-103">Debugging Components Written in Visual C++</span></span>

<span data-ttu-id="80c5d-104">Когда вы будете готовы к отладке функциональных возможностей COM+ в компонентах Microsoft Visual C++, можно настроить Visual C++ проект или средство администрирования служб компонентов для запуска отладчика.</span><span class="sxs-lookup"><span data-stu-id="80c5d-104">When you are ready to debug the COM+ functionality in your Microsoft Visual C++ components, you can configure Visual C++ project or the Component Services administrative tool to launch the debugger.</span></span> <span data-ttu-id="80c5d-105">При использовании Visual C++ можно выполнять отладку с помощью удаленного клиента, используя OLE RPC и JIT-отладку.</span><span class="sxs-lookup"><span data-stu-id="80c5d-105">If you are using Visual C++, you can debug with a remote client using OLE RPC and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="80c5d-106">Если не удается запустить клиент в отладчике или если клиент запущен на другом компьютере, можно использовать параметр **запустить com+ в отладчике** .</span><span class="sxs-lookup"><span data-stu-id="80c5d-106">If you are unable to run your client under the debugger or if the client is running on another machine, you can use the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="80c5d-107">Это можно найти в средстве администрирования "службы компонентов" как флажок на вкладке " **Дополнительно** " диалогового окна " **свойства** приложения COM+".</span><span class="sxs-lookup"><span data-stu-id="80c5d-107">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span>

<span data-ttu-id="80c5d-108">После завершения отладки следует завершить работу отлаживаемого приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="80c5d-108">When you are finished debugging, you should shut down the COM+ applications you are debugging.</span></span> <span data-ttu-id="80c5d-109">Если серверный процесс остался на работе, при следующей попытке построить БИБЛИОТЕКУ DLL может появиться сообщение об ошибке, если существующая библиотека DLL все еще загружена в память.</span><span class="sxs-lookup"><span data-stu-id="80c5d-109">If a server process is left running, you might get an error message the next time you try to build a DLL when the existing DLL is still loaded in memory.</span></span> <span data-ttu-id="80c5d-110">Чтобы завершить работу приложения COM+, щелкните правой кнопкой мыши приложение в дереве консоли и выберите пункт **Завершение работы**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-110">To shut down a COM+ application, right-click the application in the console tree and then click **Shut down**.</span></span>

> [!Note]  
> <span data-ttu-id="80c5d-111">При использовании транзакций может также потребоваться увеличить время ожидания транзакции, значение по умолчанию — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="80c5d-111">If you are using transactions, you might also want to increase the transaction time-out, which defaults to 60 seconds.</span></span> <span data-ttu-id="80c5d-112">Можно также указать значение 0, фактически указав бесконечное время ожидания транзакции.</span><span class="sxs-lookup"><span data-stu-id="80c5d-112">You can also specify a value of 0, effectively specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="80c5d-113">С помощью средства администрирования "службы компонентов" измените значение параметра время ожидания транзакции на вкладке **Параметры** окна **Мой компьютер свойства** .</span><span class="sxs-lookup"><span data-stu-id="80c5d-113">Using the Component Services administrative tool, change the transaction time-out setting on the **Options** tab of the **My Computer Properties** window.</span></span>

 

## <a name="debugging-server-application-components-with-visual-c"></a><span data-ttu-id="80c5d-114">Отладка компонентов серверного приложения с помощью Visual C++</span><span class="sxs-lookup"><span data-stu-id="80c5d-114">Debugging Server Application Components with Visual C++</span></span>

<span data-ttu-id="80c5d-115">При отладке серверных приложений COM+ может потребоваться отладка удаленных вызовов путем загрузки клиента и серверного приложения в отладчик.</span><span class="sxs-lookup"><span data-stu-id="80c5d-115">When debugging COM+ server applications, you may want to debug remote calls by loading both the client and the server application into the debugger.</span></span> <span data-ttu-id="80c5d-116">С помощью Visual C++ можно отлаживать удаленные вызовы к компонентам, используя параметры JIT и OLE RPC.</span><span class="sxs-lookup"><span data-stu-id="80c5d-116">With Visual C++, you can debug remote calls to your components through the just-in-time (JIT) and OLE RPC settings.</span></span> <span data-ttu-id="80c5d-117">Параметр JIT заставляет скомпилированный компонент запускать отладчик Visual C++ при возникновении ошибки; параметр OLE RPC позволяет отладчику выполнять шаг от клиента к компоненту при пошаговом выполнении кода.</span><span class="sxs-lookup"><span data-stu-id="80c5d-117">The JIT setting causes the compiled component to start the Visual C++ debugger when an error occurs; the OLE RPC setting enables the debugger to step from client to component as you step through your code.</span></span>

<span data-ttu-id="80c5d-118">После включения этих функций можно запустить клиент в отладчике.</span><span class="sxs-lookup"><span data-stu-id="80c5d-118">When these features are enabled, you can start your client under the debugger.</span></span> <span data-ttu-id="80c5d-119">Когда клиент выполняет вызов компонента, отладчик будет выполнять шаг с заходом в код компонента в серверном процессе, даже если сервер находится на другом компьютере в сети.</span><span class="sxs-lookup"><span data-stu-id="80c5d-119">When the client makes a call to your component, the debugger will step into the component's code in the server process, even if the server is on a different computer on the network.</span></span> <span data-ttu-id="80c5d-120">При необходимости сеанс отладки автоматически запускается на компьютере сервера.</span><span class="sxs-lookup"><span data-stu-id="80c5d-120">A debugging session is automatically started on the server computer if necessary.</span></span> <span data-ttu-id="80c5d-121">Аналогичным образом, один шаг после оператора return в коде компонента вернет отладку к следующему оператору в коде клиента.</span><span class="sxs-lookup"><span data-stu-id="80c5d-121">Similarly, single stepping past the return statement in the component's code will return debugging to the next statement in the client's code.</span></span>

> [!Note]  
> <span data-ttu-id="80c5d-122">Вы можете сохранить несколько шагов, используя параметр **запуска com+ в отладчике** .</span><span class="sxs-lookup"><span data-stu-id="80c5d-122">You may be able to save a few steps by using the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="80c5d-123">Это позволяет указать Visual C++ (или другой) отладчик без необходимости создавать специальные параметры отладки в среде Visual C++.</span><span class="sxs-lookup"><span data-stu-id="80c5d-123">This allows you to specify the Visual C++ (or other) debugger without having to make special debug settings in the Visual C++ environment.</span></span> <span data-ttu-id="80c5d-124">Это можно найти в средстве администрирования "службы компонентов" как флажок на вкладке " **Дополнительно** " диалогового окна " **свойства** приложения COM+".</span><span class="sxs-lookup"><span data-stu-id="80c5d-124">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span> <span data-ttu-id="80c5d-125">Дополнительные сведения см. в подразделе «отладка без Visual C++» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="80c5d-125">For more information, see "Debugging Without Visual C++" in this topic.</span></span>

 

<span data-ttu-id="80c5d-126">Если приложение COM+, содержащее компонент, является серверным приложением, необходимо завершить работу приложения с помощью средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="80c5d-126">When the COM+ application containing your component is a server application, you must begin by shutting down the application using the Component Services administrative tool.</span></span> <span data-ttu-id="80c5d-127">Для этого щелкните правой кнопкой мыши приложение COM+ в дереве консоли и выберите пункт **Завершение работы**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-127">To do this, right-click the COM+ application in the console tree and then click **Shut down**.</span></span>

<span data-ttu-id="80c5d-128">**Включение отладки RPC в Visual C++**</span><span class="sxs-lookup"><span data-stu-id="80c5d-128">**To enable RPC debugging in Visual C++**</span></span>

1.  <span data-ttu-id="80c5d-129">В Visual C++ в меню **Сервис** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-129">In Visual C++, on the **Tools** menu, click **Options**.</span></span>

2.  <span data-ttu-id="80c5d-130">В диалоговом окне **Параметры** на вкладке **Отладка** установите флажки Отладка и **JIT-** Отладка **OLE RPC** .</span><span class="sxs-lookup"><span data-stu-id="80c5d-130">In the **Options** dialog box, on the **Debug** tab, select the **OLE RPC debugging** and **Just-in time debugging** check boxes.</span></span>

3.  <span data-ttu-id="80c5d-131">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-131">Click **OK**.</span></span>

<span data-ttu-id="80c5d-132">Чтобы начать отладку, Запустите клиентский проект в отладчике.</span><span class="sxs-lookup"><span data-stu-id="80c5d-132">To begin debugging, start your client project in the debugger.</span></span>

<span data-ttu-id="80c5d-133">Вы также можете отлаживать компонент, не запуская клиент в отладчике.</span><span class="sxs-lookup"><span data-stu-id="80c5d-133">You can also debug your component without launching your client in the debugger.</span></span> <span data-ttu-id="80c5d-134">В этом случае компонент должен запустить отладчик самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="80c5d-134">In this case, your component must launch the debugger on its own.</span></span> <span data-ttu-id="80c5d-135">Для этого в проекте компонента необходимо указать исполняемый файл для сеанса отладки, а также идентификатор приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="80c5d-135">To do this, your component project must specify an executable for the debug session, along with the COM+ application ID.</span></span>

<span data-ttu-id="80c5d-136">**Включение компонента серверного приложения для запуска отладчика Visual C++**</span><span class="sxs-lookup"><span data-stu-id="80c5d-136">**To enable a server application component to launch the Visual C++ debugger**</span></span>

1.  <span data-ttu-id="80c5d-137">В меню **проект** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-137">On the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="80c5d-138">В диалоговом окне **Параметры проекта** в поле **параметры для** выберите **Отладка Win32**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-138">In the **Project Settings** dialog box, in the **Settings For** box, select **Win32 Debug**.</span></span>

3.  <span data-ttu-id="80c5d-139">На вкладке **Отладка** в поле **Категория** выберите **Общие**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-139">On the **Debug** tab, in the **Category** box, select **General**.</span></span>

4.  <span data-ttu-id="80c5d-140">В поле **исполняемый файл для сеанса отладки** введите полный путь к Dllhost.exe, за которым следует аргумент, указывающий идентификатор приложения COM+, содержащего компонент.</span><span class="sxs-lookup"><span data-stu-id="80c5d-140">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the application ID of the COM+ application containing the component.</span></span>

    > [!Note]  
    > <span data-ttu-id="80c5d-141">С помощью средства администрирования "службы компонентов" вы увидите идентификатор приложения на вкладке **Общие** диалогового окна **свойства** приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="80c5d-141">Using the Component Services administrative tool, you will find the application ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="80c5d-142">Ниже приведен пример:</span><span class="sxs-lookup"><span data-stu-id="80c5d-142">Following is an example:</span></span>

     

    > [!Note]  
    > <span data-ttu-id="80c5d-143">C: \\ WinNT \\ system32 \\Dllhost.exe/Процессид: {applicationID}</span><span class="sxs-lookup"><span data-stu-id="80c5d-143">C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{applicationID}</span></span>

     

5.  <span data-ttu-id="80c5d-144">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-144">Click **OK**.</span></span>

<span data-ttu-id="80c5d-145">Теперь можно задать точки останова, запустить отладчик и начать вызов компонента.</span><span class="sxs-lookup"><span data-stu-id="80c5d-145">You can now set breakpoints, start the debugger, and begin making calls to your component.</span></span>

## <a name="debugging-library-application-components-with-visual-c"></a><span data-ttu-id="80c5d-146">Отладка компонентов библиотечного приложения с помощью Visual C++</span><span class="sxs-lookup"><span data-stu-id="80c5d-146">Debugging Library Application Components with Visual C++</span></span>

<span data-ttu-id="80c5d-147">Для отладки компонентов в библиотечном приложении необходимо настроить проект клиента, так как в процессе клиента будет размещаться приложение библиотеки.</span><span class="sxs-lookup"><span data-stu-id="80c5d-147">To debug components in a library application, you must configure the client's project because the client's process will host the library application.</span></span>

<span data-ttu-id="80c5d-148">**Включение отладки библиотечного приложения с помощью Visual C++**</span><span class="sxs-lookup"><span data-stu-id="80c5d-148">**To enable library application debugging with Visual C++**</span></span>

1.  <span data-ttu-id="80c5d-149">В Visual C++ в меню **проект** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-149">In Visual C++, on the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="80c5d-150">В диалоговом окне **Параметры проекта** в поле **параметры для** выберите пункт **Отладка Win32**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-150">In the **Project Settings** dialog box, in the **Settings For** box, click **Win32 Debug**.</span></span>

3.  <span data-ttu-id="80c5d-151">На вкладке **Отладка** в поле **Категория** щелкните **дополнительные библиотеки DLL**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-151">On the **Debug** tab, in the **Category** box, click **Additional DLLs**.</span></span>

4.  <span data-ttu-id="80c5d-152">В списке **модули** добавьте библиотеки DLL компонентов в приложение библиотеки.</span><span class="sxs-lookup"><span data-stu-id="80c5d-152">In the **Modules** list, add the component DLLs in your library application.</span></span> <span data-ttu-id="80c5d-153">Это позволяет устанавливать точки останова до фактической загрузки библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="80c5d-153">This allows you to set breakpoints before your DLL is actually loaded.</span></span>

5.  <span data-ttu-id="80c5d-154">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-154">Click **OK**.</span></span>

## <a name="debugging-without-visual-c"></a><span data-ttu-id="80c5d-155">Отладка без Visual C++</span><span class="sxs-lookup"><span data-stu-id="80c5d-155">Debugging Without Visual C++</span></span>

<span data-ttu-id="80c5d-156">Независимо от того, используете ли вы Visual C++ для отладки, можно использовать параметр **запустить в отладчике** , чтобы указать отладчик, в котором должны выполняться компоненты.</span><span class="sxs-lookup"><span data-stu-id="80c5d-156">Whether or not you are using Visual C++ for debugging, you can use the **Launch in debugger** setting to specify the debugger in which your components should run.</span></span>

<span data-ttu-id="80c5d-157">**Указание отладчика с помощью средства администрирования "службы компонентов"**</span><span class="sxs-lookup"><span data-stu-id="80c5d-157">**To specify a debugger from the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="80c5d-158">В дереве консоли выберите приложение библиотеки COM+, содержащее компоненты, которые вы хотите отладить.</span><span class="sxs-lookup"><span data-stu-id="80c5d-158">In the console tree, select the COM+ library application containing the components you wish to debug.</span></span>

2.  <span data-ttu-id="80c5d-159">Щелкните приложение правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-159">Right-click the application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="80c5d-160">В диалоговом окне **Свойства** приложения перейдите на вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="80c5d-160">In the application's **Properties** dialog box, click the **Advanced** tab.</span></span>

4.  <span data-ttu-id="80c5d-161">В разделе **Отладка** установите флажок **запустить в отладчике** .</span><span class="sxs-lookup"><span data-stu-id="80c5d-161">Under **Debugging**, select the **Launch in debugger** check box.</span></span>

5.  <span data-ttu-id="80c5d-162">В поле **путь к отладчику** введите путь к отладчику, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="80c5d-162">In the **Debugger path** box, enter path to the debugger you want to use.</span></span> <span data-ttu-id="80c5d-163">Можно также нажать кнопку **Обзор** , чтобы найти отладчик.</span><span class="sxs-lookup"><span data-stu-id="80c5d-163">You can also click **Browse** to locate the debugger.</span></span> <span data-ttu-id="80c5d-164">Ниже приведен пример: C: \\ WinNT \\ system32 \\Ntsd.exe.</span><span class="sxs-lookup"><span data-stu-id="80c5d-164">Following is an example: C:\\Winnt\\System32\\Ntsd.exe.</span></span>

6.  <span data-ttu-id="80c5d-165">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="80c5d-165">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80c5d-166">См. также</span><span class="sxs-lookup"><span data-stu-id="80c5d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c5d-167">Отладка компонентов, написанных на Visual Basic</span><span class="sxs-lookup"><span data-stu-id="80c5d-167">Debugging Components Written in Visual Basic</span></span>](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



