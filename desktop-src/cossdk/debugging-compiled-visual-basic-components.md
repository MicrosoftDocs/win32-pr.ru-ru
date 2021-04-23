---
description: Учитывая, что во многих случаях вы сможете отлаживать только часть функциональных возможностей компонентов в среде Microsoft Visual Basic, существуют ситуации, в которых потребуется отладка компонентов, созданных с Visual Basic после компиляции. Так как среда Visual Basic не включает это, необходимо использовать среду Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Отладка скомпилированных компонентов Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141459"
---
# <a name="debugging-compiled-visual-basic-components"></a><span data-ttu-id="01e28-104">Отладка скомпилированных компонентов Visual Basic</span><span class="sxs-lookup"><span data-stu-id="01e28-104">Debugging Compiled Visual Basic Components</span></span>

<span data-ttu-id="01e28-105">Учитывая, что во многих случаях вы сможете отлаживать только часть функциональных возможностей компонента в среде Microsoft Visual Basic, существуют ситуации, в которых потребуется отладка компонентов, созданных с Visual Basic после компиляции.</span><span class="sxs-lookup"><span data-stu-id="01e28-105">Given that in many cases you will be able to debug only a portion of your component's functionality within the Microsoft Visual Basic environment, there will be situations in which you will need to debug components built with Visual Basic after they have been compiled.</span></span> <span data-ttu-id="01e28-106">Так как среда Visual Basic не включает это, необходимо использовать среду Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="01e28-106">Since the Visual Basic environment doesn't enable this, you must instead use the Microsoft Visual C++ environment.</span></span>

<span data-ttu-id="01e28-107">**Отладка компонента Visual Basic в среде Visual C++**</span><span class="sxs-lookup"><span data-stu-id="01e28-107">**To debug a Visual Basic component in the Visual C++ environment**</span></span>

1.  <span data-ttu-id="01e28-108">В Visual Basic 6,0 откройте проект Visual Basic, который требуется отладить.</span><span class="sxs-lookup"><span data-stu-id="01e28-108">In Visual Basic 6.0, open the Visual Basic project that you want to debug.</span></span>

2.  <span data-ttu-id="01e28-109">В меню **файл** выберите команду **создать YourProject.dll**.</span><span class="sxs-lookup"><span data-stu-id="01e28-109">On the **File** menu, click **Make YourProject.dll**.</span></span>

3.  <span data-ttu-id="01e28-110">В диалоговом окне **Создание проекта** нажмите кнопку **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="01e28-110">In the **Make Project** dialog box, click **Options**.</span></span>

4.  <span data-ttu-id="01e28-111">В диалоговом окне **Свойства проекта** на вкладке **Компиляция** щелкните **компилировать в машинный код** **без оптимизации** и установите флажок **создать символьную отладочную информацию** .</span><span class="sxs-lookup"><span data-stu-id="01e28-111">In the **Project Properties** dialog box, on the **Compile** tab, click **Compile to Native Code** and **No Optimization** and select the **Create Symbolic Debug Info** check box.</span></span>

5.  <span data-ttu-id="01e28-112">Нажмите кнопку **ОК**, а затем еще раз нажмите кнопку **ОК** , чтобы скомпилировать проект.</span><span class="sxs-lookup"><span data-stu-id="01e28-112">Click **OK**, and then click **OK** again to compile your project.</span></span>

6.  <span data-ttu-id="01e28-113">Переместите скомпилированную библиотеку DLL в расположение, в котором обычно установлены приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="01e28-113">Move the compiled DLL to the location where COM+ applications are normally installed.</span></span>

    > [!Note]  
    > <span data-ttu-id="01e28-114">Если вы не перемещаете библиотеку DLL, может появиться сообщение об ошибке, информирующее о том, что не удалось найти символьную отладочную информацию для библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="01e28-114">If you don't move the DLL, you may get an error message informing you that symbolic debugging information for the DLL could not be located.</span></span> <span data-ttu-id="01e28-115">Если вы не можете заставить отладчик останавливаться на точках останова в компоненте, убедитесь, что библиотека DLL находится в каталоге стандартных пакетов, удалите компонент из пакета и повторно добавьте компонент.</span><span class="sxs-lookup"><span data-stu-id="01e28-115">If you have trouble getting the debugger to stop at breakpoints in your component, confirm that the DLL is in the standard packages directory, delete the component from its package, and re-add the component.</span></span>

     

7.  <span data-ttu-id="01e28-116">Запустите Visual C++.</span><span class="sxs-lookup"><span data-stu-id="01e28-116">Start Visual C++.</span></span>

8.  <span data-ttu-id="01e28-117">В меню **файл** выберите пункт **открыть рабочую область**.</span><span class="sxs-lookup"><span data-stu-id="01e28-117">On the **File** menu, click **Open Workspace**.</span></span>

9.  <span data-ttu-id="01e28-118">В диалоговом окне **открыть рабочую область** установите для **файлов типа** значение **все файлы ( \* . \* )**, выберите скомпилированный компонент и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="01e28-118">In the **Open Workspace** dialog box, set **Files of Type** to **All files(\*.\*)**, select your compiled component, and click **Open**.</span></span>

10. <span data-ttu-id="01e28-119">В меню **файл** выберите пункт **Открыть** (не **открыть рабочую область**) и откройте модуль Visual Basic (. BAS), форму (. frm) или класс (CLS), который требуется отладить.</span><span class="sxs-lookup"><span data-stu-id="01e28-119">From the **File** menu, click **Open** (not **Open Workspace**) and open the Visual Basic module (.bas), form (.frm), or class (.cls) that you want to debug.</span></span>

11. <span data-ttu-id="01e28-120">В меню **проект** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="01e28-120">On the **Project** menu, click **Settings**.</span></span>

12. <span data-ttu-id="01e28-121">В диалоговом окне **Параметры проекта** на вкладке **Отладка** выберите **Общие** в поле **Категория** .</span><span class="sxs-lookup"><span data-stu-id="01e28-121">In the **Project Settings** dialog box, on the **Debug** tab, select **General** in the **Category** box.</span></span>

13. <span data-ttu-id="01e28-122">В поле **исполняемый файл для сеанса отладки** введите полный путь к Dllhost.exe, за которым следует аргумент, указывающий идентификатор процесса приложения COM+, содержащего компонент.</span><span class="sxs-lookup"><span data-stu-id="01e28-122">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the process ID of the COM+ application containing the component.</span></span> <span data-ttu-id="01e28-123">Идентификатор процесса можно найти на вкладке **Общие** диалогового окна **свойства** приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="01e28-123">You will find the process ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="01e28-124">Ниже приведен пример: C: \\ WinNT \\ system32 \\Dllhost.exe/процессид: { <processID> }.</span><span class="sxs-lookup"><span data-stu-id="01e28-124">Following is an example: C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{<processID>}.</span></span>

14. <span data-ttu-id="01e28-125">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="01e28-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01e28-126">См. также</span><span class="sxs-lookup"><span data-stu-id="01e28-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01e28-127">Поддержка отладки Visual Basic COM+ отличается от MTS</span><span class="sxs-lookup"><span data-stu-id="01e28-127">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="01e28-128">Отладка в интегрированной среде разработки Visual Basic</span><span class="sxs-lookup"><span data-stu-id="01e28-128">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



