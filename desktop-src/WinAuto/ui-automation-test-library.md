---
title: Библиотека тестирования модели автоматизации пользовательского интерфейса
description: Библиотека тестирования модели автоматизации пользовательского интерфейса (библиотека тестирования UIA) — это API, который вызывается приложением драйвера в сценарии автоматического тестирования.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64200673d45f800e1e18dee2afd5c4acd2b604f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "104571354"
---
# <a name="ui-automation-test-library"></a><span data-ttu-id="4820b-103">Библиотека тестирования модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4820b-103">UI Automation Test Library</span></span>

<span data-ttu-id="4820b-104">Библиотека тестирования модели автоматизации пользовательского интерфейса (библиотека тестирования UIA) — это API, который вызывается приложением *драйвера* в сценарии автоматического тестирования.</span><span class="sxs-lookup"><span data-stu-id="4820b-104">The UI Automation Test Library (UIA Test Library) is an API that is called by the *driver* application in an automated testing scenario.</span></span> <span data-ttu-id="4820b-105">Драйвер — это приложение, которое получает элемент автоматизации (объект [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) из элемента управления, требующего проверки, и предоставляет его в библиотеку тестирования модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4820b-105">The driver is the application that obtains an automation element ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from a control that requires verification, and provides it to the UI Automation Test Library.</span></span> <span data-ttu-id="4820b-106">Затем библиотека тестирования проверяет и проверяет реализацию модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4820b-106">Then, the test library checks and validates the UI Automation implementation.</span></span> <span data-ttu-id="4820b-107">Дополнительные сведения об автоматизации пользовательского интерфейса и элементах автоматизации см. в разделе [основы автоматизации пользовательского интерфейса](entry-uiautocore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4820b-107">To learn more about UI Automation and automation elements, see [UI Automation Fundamentals](entry-uiautocore-overview.md).</span></span>

-   [<span data-ttu-id="4820b-108">Рабочий процесс библиотеки тестирования модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4820b-108">UI Automation Test Library Workflow</span></span>](#ui-automation-test-library-workflow)
-   [<span data-ttu-id="4820b-109">Ведение журнала с помощью библиотеки тестирования модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4820b-109">Logging with the UI Automation Test Library</span></span>](#logging-with-the-ui-automation-test-library)
    -   [<span data-ttu-id="4820b-110">Ведение журнала XML</span><span class="sxs-lookup"><span data-stu-id="4820b-110">XML Logging</span></span>](#xml-logging)
    -   [<span data-ttu-id="4820b-111">Ведение журнала консоли</span><span class="sxs-lookup"><span data-stu-id="4820b-111">Console Logging</span></span>](#console-logging)
    -   [<span data-ttu-id="4820b-112">Требования к коду для ведения журнала</span><span class="sxs-lookup"><span data-stu-id="4820b-112">Code Requirements for Logging</span></span>](#code-requirements-for-logging)
    -   [<span data-ttu-id="4820b-113">Примеры ведения журнала</span><span class="sxs-lookup"><span data-stu-id="4820b-113">Logging Examples</span></span>](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a><span data-ttu-id="4820b-114">Рабочий процесс библиотеки тестирования модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4820b-114">UI Automation Test Library Workflow</span></span>

<span data-ttu-id="4820b-115">На следующей диаграмме показан рабочий процесс, который включает библиотеку тестирования модели автоматизации пользовательского интерфейса с помощью консольного приложения в качестве драйвера.</span><span class="sxs-lookup"><span data-stu-id="4820b-115">The following diagram shows a test workflow that incorporates the UI Automation Test Library by using a console application as the driver.</span></span> <span data-ttu-id="4820b-116">В этом случае драйвер запускает экземпляр Notepad.exe и получает элемент автоматизации (т. е. объект [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) из элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="4820b-116">In this case, the driver starts an instance of Notepad.exe and obtains an automation element (that is, a [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from the edit control.</span></span> <span data-ttu-id="4820b-117">Затем драйвер создает объект библиотеки тестирования модели автоматизации пользовательского интерфейса на основе тестируемой платформы пользовательского интерфейса, а затем передает элемент автоматизации в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="4820b-117">Next, the driver creates a UI Automation Test Library object based on the UI platform being tested, and then passes in the automation element as a parameter.</span></span> <span data-ttu-id="4820b-118">Библиотека тестирования модели автоматизации пользовательского интерфейса определяет, что элемент автоматизации является типом элемента управления [документом](uiauto-supportdocumentcontroltype.md) , а затем выполняет тесты управления документами, тесты шаблона элемента управления [Text](uiauto-implementingtextandtextrange.md) и [Scroll](uiauto-implementingscroll.md) , а также тесты универсальных элементов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4820b-118">The UI Automation Test Library determines that the automation element is a [Document](uiauto-supportdocumentcontroltype.md) control type, and then executes the Document control tests, the [Text](uiauto-implementingtextandtextrange.md) and [Scroll](uiauto-implementingscroll.md) control pattern tests, and generic automation element tests.</span></span>

![Схема, показывающая поток драйвера для приложения в Уиатестлибрари с помощью красной стрелки.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a><span data-ttu-id="4820b-120">Ведение журнала с помощью библиотеки тестирования модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4820b-120">Logging with the UI Automation Test Library</span></span>

<span data-ttu-id="4820b-121">Библиотека тестирования модели автоматизации пользовательского интерфейса использует внешние библиотеки DLL для записи результатов тестовых запусков.</span><span class="sxs-lookup"><span data-stu-id="4820b-121">The UI Automation Test Library uses external DLLs to log results from test runs.</span></span> <span data-ttu-id="4820b-122">Он поддерживает ведение журнала в формате XML и ведение журнала в консоли.</span><span class="sxs-lookup"><span data-stu-id="4820b-122">It supports logging as XML and logging to the console.</span></span>

### <a name="xml-logging"></a><span data-ttu-id="4820b-123">Ведение журнала XML</span><span class="sxs-lookup"><span data-stu-id="4820b-123">XML Logging</span></span>

<span data-ttu-id="4820b-124">Ведение журнала в формате XML обычно используется визуальной автоматизацией пользовательского интерфейса, но оно также может быть включено в рабочий процесс командной строки.</span><span class="sxs-lookup"><span data-stu-id="4820b-124">XML logging is typically used by Visual UI Automation Verify, but it can also be incorporated into a command-line workflow.</span></span>

<span data-ttu-id="4820b-125">Если указано ведение журнала XML, приложение драйвера должно сериализовать выходные данные, создав объект **XmlWriter** и передав его методу **ксмллог. жеттеструнксмл** .</span><span class="sxs-lookup"><span data-stu-id="4820b-125">If XML logging is specified, the driver application must serialize the output by creating an **XmlWriter** object and passing it to the **XmlLog.GetTestRunXml** method.</span></span> <span data-ttu-id="4820b-126">Затем драйвер может использовать сериализованный XML внутренним образом или записать его в файл.</span><span class="sxs-lookup"><span data-stu-id="4820b-126">The driver can then use the serialized XML internally or write it to a file.</span></span>

<span data-ttu-id="4820b-127">Для ведения журнала XML требуются следующие библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="4820b-127">The following DLLs are required for XML logging.</span></span>

-   <span data-ttu-id="4820b-128">WUIALogging.dll</span><span class="sxs-lookup"><span data-stu-id="4820b-128">WUIALogging.dll</span></span>
-   <span data-ttu-id="4820b-129">WUIALoggerXml.dll</span><span class="sxs-lookup"><span data-stu-id="4820b-129">WUIALoggerXml.dll</span></span>

### <a name="console-logging"></a><span data-ttu-id="4820b-130">Ведение журнала консоли</span><span class="sxs-lookup"><span data-stu-id="4820b-130">Console Logging</span></span>

<span data-ttu-id="4820b-131">По умолчанию библиотека тестирования модели автоматизации пользовательского интерфейса использует ведение журнала консоли, где все выходные данные журнала передаются в окно консоли в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="4820b-131">By default, the UI Automation Test Library uses console logging, where all logging output is piped as plain text to the console window.</span></span> <span data-ttu-id="4820b-132">Для ведения журнала консоли требуется WUIALogging.dll.</span><span class="sxs-lookup"><span data-stu-id="4820b-132">WUIALogging.dll is required for console logging.</span></span>

### <a name="code-requirements-for-logging"></a><span data-ttu-id="4820b-133">Требования к коду для ведения журнала</span><span class="sxs-lookup"><span data-stu-id="4820b-133">Code Requirements for Logging</span></span>

<span data-ttu-id="4820b-134">Приложение драйвера должно включать следующие фрагменты кода для использования ведения журнала тестовой библиотеки модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4820b-134">A driver application must include the following code snippets to use UI Automation Test Library logging.</span></span>


```CSharp
\\ Include logging functionality.
using Microsoft.Test.UIAutomation.Logging;

...

\\ Select a logger.
UIAVerifyLogger.SetLoggerType(LogTypes.DefaultLogger | 
                              LogTypes.ConsoleLogger | 
                              LogTypes.XmlLogger);

...

\\ Output comment to selected logger.
UIAVerifyLogger.LogComment("...");
```



### <a name="logging-examples"></a><span data-ttu-id="4820b-135">Примеры ведения журнала</span><span class="sxs-lookup"><span data-stu-id="4820b-135">Logging Examples</span></span>

<span data-ttu-id="4820b-136">В следующих примерах демонстрируются основные функциональные возможности ведения журнала и показано, как использовать API библиотеки тестирования модели автоматизации пользовательского интерфейса в базовом приложении драйвера автоматизации тестирования.</span><span class="sxs-lookup"><span data-stu-id="4820b-136">The following examples demonstrate basic logging functionality and show how to use the UI Automation Test Library API in a basic test automation driver application.</span></span>


```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample logger.
//
//---------------------------------------------------------------------------
using System;

namespace WUITest
{
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {
        private TestMain() { }

        /// -----------------------------------------------------------------
        /// <summary>
        /// Entry point
        /// </summary>
        /// -----------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Call SetLogger() if you don't want to use the default logger.
            // To set the logger type, call SetLogger(<string>).
            // <string> can be specified from the command line or from the 
            // the UI Automation Test Library enumeration:
            //  
            //     Logger.SetLogger(LogTypes.ConsoleLogger);
            //     Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.StartTest("Test 1");
            Logger.LogComment("This is a comment");
            Logger.LogError(new Exception("My error"), false);
            Logger.EndTest();

            Logger.StartTest("Test 2");
            Logger.LogComment("This is a second comment");
            Logger.LogPass();
            Logger.EndTest();

            Logger.ReportResults();

        }
    }
}
```




```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample test automation.
//
//---------------------------------------------------------------------------

using System;
using System.Windows;

namespace WUITest
{
    using System.Diagnostics;
    using System.Threading;
    using System.Windows.Automation;
    using Microsoft.Test.UIAutomation;
    using Microsoft.Test.UIAutomation.Core;
    using Microsoft.Test.UIAutomation.TestManager;
    using Microsoft.Test.UIAutomation.Tests.Controls;
    using Microsoft.Test.UIAutomation.Tests.Patterns;
    using Microsoft.Test.UIAutomation.Tests.Scenarios;
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {

        // Time in milliseconds to wait for the application to start.
        static int MAXTIME = 5000;
        // Time in milliseconds to wait before trying to find the application.
        static int TIMEWAIT = 100; 

        /// -------------------------------------------------------------------
        /// <summary>
        /// Start Notepad, obtain an AutomationElement object, and run tests.
        /// </summary>
        /// -------------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Dump the information to the console window.  
            // Use a different LogTypes value if you need to dump to another logger, 
            // or create your own logger that complies with the interface.
            UIAVerifyLogger.SetLoggerType(LogTypes.ConsoleLogger);

            // Get the automation element.
            AutomationElement element = StartApplication("NOTEPAD.EXE", null);

            // Call the UI Automation Test Library tests.
            TestRuns.RunAllTests(element, true, TestPriorities.Pri0, 
                    TestCaseType.Generic, false, true, null);

            // Clean up.
            ((WindowPattern)element.GetCurrentPattern(WindowPattern.Pattern)).Close();

            // Dump the summary of results.
            UIAVerifyLogger.ReportResults();
        }

        /// -------------------------------------------------------------------------
        /// <summary>
        /// Start the application and retrieve its AutomationElement. 
        /// </summary>
        /// -------------------------------------------------------------------------
        static public AutomationElement StartApplication(string appPath, 
                string arguments)
        {
            Process process;

            Library.ValidateArgumentNonNull(appPath, "appPath");

            ProcessStartInfo psi = new ProcessStartInfo();

            process = new Process();
            psi.FileName = appPath;

            if (arguments != null)
            {
                psi.Arguments = arguments;
            }

            UIAVerifyLogger.LogComment("Starting({0})", appPath);
            process.StartInfo = psi;

            process.Start();

            int runningTime = 0;
            while (process.MainWindowHandle.Equals(IntPtr.Zero))
            {
                if (runningTime > MAXTIME)
                    throw new Exception("Could not find " + appPath);

                Thread.Sleep(TIMEWAIT);
                runningTime += TIMEWAIT;

                process.Refresh();
            }

            UIAVerifyLogger.LogComment("{0} started", appPath);

            UIAVerifyLogger.LogComment("Obtained an AutomationElement for {0}", appPath);
            return AutomationElement.FromHandle(process.MainWindowHandle);

        }
    }
}
```



 

 




