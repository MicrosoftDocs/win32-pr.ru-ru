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
# <a name="ui-automation-test-library"></a>Библиотека тестирования модели автоматизации пользовательского интерфейса

Библиотека тестирования модели автоматизации пользовательского интерфейса (библиотека тестирования UIA) — это API, который вызывается приложением *драйвера* в сценарии автоматического тестирования. Драйвер — это приложение, которое получает элемент автоматизации (объект [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) из элемента управления, требующего проверки, и предоставляет его в библиотеку тестирования модели автоматизации пользовательского интерфейса. Затем библиотека тестирования проверяет и проверяет реализацию модели автоматизации пользовательского интерфейса. Дополнительные сведения об автоматизации пользовательского интерфейса и элементах автоматизации см. в разделе [основы автоматизации пользовательского интерфейса](entry-uiautocore-overview.md).

-   [Рабочий процесс библиотеки тестирования модели автоматизации пользовательского интерфейса](#ui-automation-test-library-workflow)
-   [Ведение журнала с помощью библиотеки тестирования модели автоматизации пользовательского интерфейса](#logging-with-the-ui-automation-test-library)
    -   [Ведение журнала XML](#xml-logging)
    -   [Ведение журнала консоли](#console-logging)
    -   [Требования к коду для ведения журнала](#code-requirements-for-logging)
    -   [Примеры ведения журнала](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>Рабочий процесс библиотеки тестирования модели автоматизации пользовательского интерфейса

На следующей диаграмме показан рабочий процесс, который включает библиотеку тестирования модели автоматизации пользовательского интерфейса с помощью консольного приложения в качестве драйвера. В этом случае драйвер запускает экземпляр Notepad.exe и получает элемент автоматизации (т. е. объект [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) из элемента управления Edit. Затем драйвер создает объект библиотеки тестирования модели автоматизации пользовательского интерфейса на основе тестируемой платформы пользовательского интерфейса, а затем передает элемент автоматизации в качестве параметра. Библиотека тестирования модели автоматизации пользовательского интерфейса определяет, что элемент автоматизации является типом элемента управления [документом](uiauto-supportdocumentcontroltype.md) , а затем выполняет тесты управления документами, тесты шаблона элемента управления [Text](uiauto-implementingtextandtextrange.md) и [Scroll](uiauto-implementingscroll.md) , а также тесты универсальных элементов автоматизации.

![Схема, показывающая поток драйвера для приложения в Уиатестлибрари с помощью красной стрелки.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>Ведение журнала с помощью библиотеки тестирования модели автоматизации пользовательского интерфейса

Библиотека тестирования модели автоматизации пользовательского интерфейса использует внешние библиотеки DLL для записи результатов тестовых запусков. Он поддерживает ведение журнала в формате XML и ведение журнала в консоли.

### <a name="xml-logging"></a>Ведение журнала XML

Ведение журнала в формате XML обычно используется визуальной автоматизацией пользовательского интерфейса, но оно также может быть включено в рабочий процесс командной строки.

Если указано ведение журнала XML, приложение драйвера должно сериализовать выходные данные, создав объект **XmlWriter** и передав его методу **ксмллог. жеттеструнксмл** . Затем драйвер может использовать сериализованный XML внутренним образом или записать его в файл.

Для ведения журнала XML требуются следующие библиотеки DLL.

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>Ведение журнала консоли

По умолчанию библиотека тестирования модели автоматизации пользовательского интерфейса использует ведение журнала консоли, где все выходные данные журнала передаются в окно консоли в виде обычного текста. Для ведения журнала консоли требуется WUIALogging.dll.

### <a name="code-requirements-for-logging"></a>Требования к коду для ведения журнала

Приложение драйвера должно включать следующие фрагменты кода для использования ведения журнала тестовой библиотеки модели автоматизации пользовательского интерфейса.


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



### <a name="logging-examples"></a>Примеры ведения журнала

В следующих примерах демонстрируются основные функциональные возможности ведения журнала и показано, как использовать API библиотеки тестирования модели автоматизации пользовательского интерфейса в базовом приложении драйвера автоматизации тестирования.


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



 

 




