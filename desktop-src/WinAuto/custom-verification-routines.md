---
title: Пользовательские подпрограммы проверки
description: В этом разделе описано, как создать настраиваемую подпрограмму проверки для средства проверки специальных возможностей пользовательского интерфейса (Аккчеккер).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245865a0ab4aa6848d4a4361a30febbb341742208586ebf4ec5b35c34fa30534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030892"
---
# <a name="custom-verification-routines"></a>Пользовательские подпрограммы проверки

В этом разделе описано, как создать настраиваемую подпрограмму проверки для средства проверки специальных возможностей пользовательского интерфейса (Аккчеккер).

-   [Создание пользовательской проверки](#creating-a-custom-verification)
    -   [Пример пользовательской проверки](#sample-custom-verification)
-   [Использование пользовательской проверки](#using-a-custom-verification)
    -   [Графический пользовательский интерфейс Аккчеккер (GUI)](#the-accchecker-graphical-user-interface-gui)
    -   [Автоматизация Аккчеккер](#accchecker-automation)
-   [Связанные темы](#related-topics)

Проверка специальных возможностей пользовательского интерфейса (Аккчеккер) — это средство тестирования специальных возможностей, предназначенное для проверки реализации Microsoft Active Accessibility (MSAA) в пользовательском интерфейсе элемента управления или приложения. Проблемы с уровнем доступности, которые могут быть предоставлены реализацией MSAA, тестируются с помощью набора встроенных подпрограмм автоматической проверки. Эти встроенные подпрограммы проверки можно дополнить настраиваемыми подсистемами с помощью расширяемой платформы Аккчеккер.

## <a name="creating-a-custom-verification"></a>Создание пользовательской проверки

Пользовательская проверка создается как библиотека классов (DLL), реализующая один интерфейс (), `IVerificationRoutine` содержащий один элемент () `Execute` :


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Параметры**

*HWND*

Тип: **System. IntPtr**

HWND проверяемого элемента.

*средства ведения журнала*

Тип: **аккчекк. Logging. ILogger**

Выбранный метод ведения журнала. Возможные типы включают **аккумулатинглогжер** (используется аккчеккер для кэширования всех записей журнала до завершения проверки), **консолелогжер**, **текстфилелогжер** и **ксмлсериализинглогжер**.

*алловуи*

Тип: **bool** .

Указывает, отображает ли подпрограммы проверки пользовательский интерфейс, который тестирует. Обычно имеет значение false в сценариях автоматического тестирования.

*графика*

Тип: **аккчекк. графикшелпер**

Используется для снимков экрана и других визуализаций в Аккчеккер.

### <a name="sample-custom-verification"></a>Пример пользовательской проверки

В следующем примере показана пользовательская проверка C#, которая выполняет простую проверку глубины дерева элементов. Если глубина дерева элементов превышает 50 уровней, регистрируется ошибка, если дерево элементов имеет глубину от 20 до 50 уровней, а в противном случае информационное сообщение регистрируется в журнале.


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
> Microsoft Visual Studio решение, содержащее пример кода проверки, включено в справочную документацию. Файлы находятся в пути установки Аккчеккер.

 

## <a name="using-a-custom-verification"></a>Использование пользовательской проверки

В этом разделе описывается, как включить пользовательскую проверку в сценарии тестирования Аккчеккер.

### <a name="the-accchecker-graphical-user-interface-gui"></a>Графический пользовательский интерфейс Аккчеккер (GUI)

Чтобы включить пользовательскую подсистему проверки в приложение Аккчеккер, просто щелкните Открыть библиотеку DLL в меню файл и выберите библиотеку DLL для подпрограммы. Пользовательская подпрограммы будет добавлена в нижнюю часть списка проверок на панели "Выбор подпрограмм проверки".

На следующем снимке экрана показан пример пользовательской проверки глубины дерева проверки, добавленной в Аккчеккер.

![Пример пользовательской проверки глубины дерева, добавленной в пользовательский интерфейс аккчеккер](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Если в пользовательской процедуре проверки не указаны значения атрибутов проверки, проверка по-прежнему загружается в Аккчеккер, даже если она не отображается в пользовательском интерфейсе. Поскольку он не отображается в пользовательском интерфейсе, он не может быть снят и исключен из последующих запусков проверки.

 

### <a name="accchecker-automation"></a>Автоматизация Аккчеккер

Включение пользовательской подпрограммы проверки в автоматизированную Аккчеккер платформу — это просто добавление библиотеки DLL проверки и включение требуемых подпрограмм проверки.

в следующем фрагменте кода показано, как использовать API аккчеккер для тестирования функциональных возможностей вкладок в приложении панели управления брандмауэра Windows.


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
> решение Microsoft Visual Studio 2008, содержащее пример кода проверки, включено в справочную документацию. Файлы находятся в пути установки Аккчеккер.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Средство UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




