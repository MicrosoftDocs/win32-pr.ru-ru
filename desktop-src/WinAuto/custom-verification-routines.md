---
title: Пользовательские подпрограммы проверки
description: В этом разделе описано, как создать настраиваемую подпрограмму проверки для средства проверки специальных возможностей пользовательского интерфейса (Аккчеккер).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986258"
---
# <a name="custom-verification-routines"></a><span data-ttu-id="c7665-103">Пользовательские подпрограммы проверки</span><span class="sxs-lookup"><span data-stu-id="c7665-103">Custom Verification Routines</span></span>

<span data-ttu-id="c7665-104">В этом разделе описано, как создать настраиваемую подпрограмму проверки для средства проверки специальных возможностей пользовательского интерфейса (Аккчеккер).</span><span class="sxs-lookup"><span data-stu-id="c7665-104">This section describes how to create a custom verification routine for the UI Accessibility Checker (AccChecker) tool.</span></span>

-   [<span data-ttu-id="c7665-105">Создание пользовательской проверки</span><span class="sxs-lookup"><span data-stu-id="c7665-105">Creating a Custom Verification</span></span>](#creating-a-custom-verification)
    -   [<span data-ttu-id="c7665-106">Пример пользовательской проверки</span><span class="sxs-lookup"><span data-stu-id="c7665-106">Sample Custom Verification</span></span>](#sample-custom-verification)
-   [<span data-ttu-id="c7665-107">Использование пользовательской проверки</span><span class="sxs-lookup"><span data-stu-id="c7665-107">Using a Custom Verification</span></span>](#using-a-custom-verification)
    -   [<span data-ttu-id="c7665-108">Графический пользовательский интерфейс Аккчеккер (GUI)</span><span class="sxs-lookup"><span data-stu-id="c7665-108">The AccChecker Graphical User Interface (GUI)</span></span>](#the-accchecker-graphical-user-interface-gui)
    -   [<span data-ttu-id="c7665-109">Автоматизация Аккчеккер</span><span class="sxs-lookup"><span data-stu-id="c7665-109">AccChecker Automation</span></span>](#accchecker-automation)
-   [<span data-ttu-id="c7665-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c7665-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="c7665-111">Проверка специальных возможностей пользовательского интерфейса (Аккчеккер) — это средство тестирования специальных возможностей, предназначенное для проверки реализации Microsoft Active Accessibility (MSAA) в пользовательском интерфейсе элемента управления или приложения.</span><span class="sxs-lookup"><span data-stu-id="c7665-111">UI Accessibility Checker (AccChecker) is an accessibility test tool designed to verify the implementation of Microsoft Active Accessibility (MSAA) in a control or application UI.</span></span> <span data-ttu-id="c7665-112">Проблемы с уровнем доступности, которые могут быть предоставлены реализацией MSAA, тестируются с помощью набора встроенных подпрограмм автоматической проверки.</span><span class="sxs-lookup"><span data-stu-id="c7665-112">High impact accessibility issues that might be exposed by the MSAA implementation are tested with a set of built-in automated verification routines.</span></span> <span data-ttu-id="c7665-113">Эти встроенные подпрограммы проверки можно дополнить настраиваемыми подсистемами с помощью расширяемой платформы Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="c7665-113">These native verification routines can be augmented with customized routines using the extensible AccChecker platform.</span></span>

## <a name="creating-a-custom-verification"></a><span data-ttu-id="c7665-114">Создание пользовательской проверки</span><span class="sxs-lookup"><span data-stu-id="c7665-114">Creating a Custom Verification</span></span>

<span data-ttu-id="c7665-115">Пользовательская проверка создается как библиотека классов (DLL), реализующая один интерфейс (), `IVerificationRoutine` содержащий один элемент () `Execute` :</span><span class="sxs-lookup"><span data-stu-id="c7665-115">A custom verification is built as a class library (DLL) that implements a single interface (`IVerificationRoutine`) containing one member (`Execute`):</span></span>


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



<span data-ttu-id="c7665-116">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="c7665-116">**Parameters**</span></span>

<span data-ttu-id="c7665-117">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c7665-117">*hwnd*</span></span>

<span data-ttu-id="c7665-118">Тип: **System. IntPtr**</span><span class="sxs-lookup"><span data-stu-id="c7665-118">Type: **System.IntPtr**</span></span>

<span data-ttu-id="c7665-119">HWND проверяемого элемента.</span><span class="sxs-lookup"><span data-stu-id="c7665-119">The HWND of the element being verified.</span></span>

<span data-ttu-id="c7665-120">*средства ведения журнала*</span><span class="sxs-lookup"><span data-stu-id="c7665-120">*logger*</span></span>

<span data-ttu-id="c7665-121">Тип: **аккчекк. Logging. ILogger**</span><span class="sxs-lookup"><span data-stu-id="c7665-121">Type: **AccCheck.Logging.ILogger**</span></span>

<span data-ttu-id="c7665-122">Выбранный метод ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="c7665-122">The selected logging method.</span></span> <span data-ttu-id="c7665-123">Возможные типы включают **аккумулатинглогжер** (используется аккчеккер для кэширования всех записей журнала до завершения проверки), **консолелогжер**, **текстфилелогжер** и **ксмлсериализинглогжер**.</span><span class="sxs-lookup"><span data-stu-id="c7665-123">Possible types include **AccumulatingLogger** (used by AccChecker to cache all log entries until verifications are complete), **ConsoleLogger**, **TextFileLogger**, and **XMLSerializingLogger**.</span></span>

<span data-ttu-id="c7665-124">*алловуи*</span><span class="sxs-lookup"><span data-stu-id="c7665-124">*AllowUI*</span></span>

<span data-ttu-id="c7665-125">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="c7665-125">Type: **bool**</span></span>

<span data-ttu-id="c7665-126">Указывает, отображает ли подпрограммы проверки пользовательский интерфейс, который тестирует.</span><span class="sxs-lookup"><span data-stu-id="c7665-126">Indicates whether the verification routine displays the UI it is testing.</span></span> <span data-ttu-id="c7665-127">Обычно имеет значение false в сценариях автоматического тестирования.</span><span class="sxs-lookup"><span data-stu-id="c7665-127">Generally set to false in automated testing scenarios.</span></span>

<span data-ttu-id="c7665-128">*рисунка*</span><span class="sxs-lookup"><span data-stu-id="c7665-128">*graphics*</span></span>

<span data-ttu-id="c7665-129">Тип: **аккчекк. графикшелпер**</span><span class="sxs-lookup"><span data-stu-id="c7665-129">Type: **AccCheck.GraphicsHelper**</span></span>

<span data-ttu-id="c7665-130">Используется для снимков экрана и других визуализаций в Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="c7665-130">Used for screenshots and other visualizations within AccChecker.</span></span>

### <a name="sample-custom-verification"></a><span data-ttu-id="c7665-131">Пример пользовательской проверки</span><span class="sxs-lookup"><span data-stu-id="c7665-131">Sample Custom Verification</span></span>

<span data-ttu-id="c7665-132">В следующем примере показана пользовательская проверка C#, которая выполняет простую проверку глубины дерева элементов.</span><span class="sxs-lookup"><span data-stu-id="c7665-132">The following example is a C# custom verification that performs a simple element tree depth check.</span></span> <span data-ttu-id="c7665-133">Если глубина дерева элементов превышает 50 уровней, регистрируется ошибка, если дерево элементов имеет глубину от 20 до 50 уровней, а в противном случае информационное сообщение регистрируется в журнале.</span><span class="sxs-lookup"><span data-stu-id="c7665-133">An error is logged if the element tree is greater than 50 levels deep, a warning is logged if the element tree is 20 to 50 levels deep, and an informational message is logged otherwise.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="c7665-134">Microsoft Visual Studio решение, содержащее пример кода проверки, включено в справочную документацию.</span><span class="sxs-lookup"><span data-stu-id="c7665-134">A Microsoft Visual Studio solution that contains verification sample code is included with the help documentation.</span></span> <span data-ttu-id="c7665-135">Файлы находятся в пути установки Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="c7665-135">The files are located in the AccChecker installation path.</span></span>

 

## <a name="using-a-custom-verification"></a><span data-ttu-id="c7665-136">Использование пользовательской проверки</span><span class="sxs-lookup"><span data-stu-id="c7665-136">Using a Custom Verification</span></span>

<span data-ttu-id="c7665-137">В этом разделе описывается, как включить пользовательскую проверку в сценарии тестирования Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="c7665-137">This section describes how to incorporate a custom verification into AccChecker test scenarios.</span></span>

### <a name="the-accchecker-graphical-user-interface-gui"></a><span data-ttu-id="c7665-138">Графический пользовательский интерфейс Аккчеккер (GUI)</span><span class="sxs-lookup"><span data-stu-id="c7665-138">The AccChecker Graphical User Interface (GUI)</span></span>

<span data-ttu-id="c7665-139">Чтобы включить пользовательскую подсистему проверки в приложение Аккчеккер, просто щелкните Открыть библиотеку DLL в меню файл и выберите библиотеку DLL для подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="c7665-139">To include a custom verification routine in the AccChecker application, simply click Open DLL from the File menu and locate the DLL for the routine.</span></span> <span data-ttu-id="c7665-140">Пользовательская подпрограммы будет добавлена в нижнюю часть списка проверок на панели "Выбор подпрограмм проверки".</span><span class="sxs-lookup"><span data-stu-id="c7665-140">The custom routine will be added to the bottom of the list of verifications in the Select verification routines pane.</span></span>

<span data-ttu-id="c7665-141">На следующем снимке экрана показан пример пользовательской проверки глубины дерева проверки, добавленной в Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="c7665-141">The following screen shot shows the Sample Check Tree Depth custom verification added to AccChecker.</span></span>

![Пример пользовательской проверки глубины дерева, добавленной в пользовательский интерфейс аккчеккер](images/accchecker-sample-custom-verification.png)

> [!Note]  
> <span data-ttu-id="c7665-143">Если в пользовательской процедуре проверки не указаны значения атрибутов проверки, проверка по-прежнему загружается в Аккчеккер, даже если она не отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="c7665-143">If the verification attribute values are not specified in the custom verification routine, the verification is still loaded into AccChecker even though it does not appear in the UI.</span></span> <span data-ttu-id="c7665-144">Поскольку он не отображается в пользовательском интерфейсе, он не может быть снят и исключен из последующих запусков проверки.</span><span class="sxs-lookup"><span data-stu-id="c7665-144">Since it is not displayed in the UI, it cannot be unchecked and excluded from subsequent verification runs.</span></span>

 

### <a name="accchecker-automation"></a><span data-ttu-id="c7665-145">Автоматизация Аккчеккер</span><span class="sxs-lookup"><span data-stu-id="c7665-145">AccChecker Automation</span></span>

<span data-ttu-id="c7665-146">Включение пользовательской подпрограммы проверки в автоматизированную Аккчеккер платформу — это просто добавление библиотеки DLL проверки и включение требуемых подпрограмм проверки.</span><span class="sxs-lookup"><span data-stu-id="c7665-146">Incorporating a custom verification routine into an automated AccChecker framework is as simple as adding the verification DLL and enabling the desired verification routines.</span></span>

<span data-ttu-id="c7665-147">В следующем фрагменте кода показано, как использовать API Аккчеккер для тестирования функциональных возможностей вкладок в приложении панели управления брандмауэра Windows.</span><span class="sxs-lookup"><span data-stu-id="c7665-147">The following code snippet demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> Решение Microsoft Visual Studio 2008, содержащее пример кода проверки, включено в справочную документацию. <span data-ttu-id="c7665-149">Файлы находятся в пути установки Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="c7665-149">The files are located in the AccChecker installation path.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c7665-150">См. также</span><span class="sxs-lookup"><span data-stu-id="c7665-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7665-151">Средство UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="c7665-151">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




