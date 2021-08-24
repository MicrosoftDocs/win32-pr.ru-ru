---
description: В этом учебнике показано, как взять на себя многоязыковую программу и сделать ее готовой к международному использованию. Это приложение в виде полного решения, созданного в Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: добавление поддержки многоязычный пользовательский интерфейс в приложение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5ca1ddba2574610cde1f375f7fab2b07461008665f2092c9c8e88ae9b51f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147697"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>добавление поддержки многоязычный пользовательский интерфейс в приложение

В этом учебнике показано, как взять на себя многоязыковую программу и сделать ее готовой к международному использованию. Это приложение в виде полного решения, созданного в Microsoft Visual Studio.

-   [Обзор](#splitting-the-various-language-resource-modules-an-overview)
    -   [Идея фонового интерфейса пользователя Hello](#the-idea-behind-hello-mui)
-   [Настройка решения Hello MUI](#setting-up-the-hello-mui-solution)
    -   [Требования к платформе](#platform-requirements)
    -   [Предварительные требования](#prerequisites)
-   [Шаг 0. Создание жестко закодированного пользовательского интерфейса Hello](#step-0-creating-the-hard-coded-hello-mui)
-   [Шаг 1. Реализация базового модуля ресурсов](#step-1-implementing-the-basic-resource-module)
-   [Шаг 2. Создание базового модуля ресурсов](#step-2-building-the-basic-resource-module)
    -   [Разделение различных модулей языковых ресурсов: обзор](#splitting-the-various-language-resource-modules-an-overview)
    -   [Разделение различных модулей языковых ресурсов: создание файлов](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Шаг 3. Создание Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Шаг 4. Глобализация "Hello MUI"](#step-4-globalizing-hello-mui)
-   [Шаг 5. Настройка "Hello MUI"](#step-5-customizing-hello-mui)
-   [Дополнительные рекомендации для MUI](#additional-considerations-for-mui)
    -   [Поддержка консольных приложений](#support-for-console-applications)
    -   [Определение языков для поддержки во время выполнения](#determination-of-languages-to-support-at-run-time)
    -   [поддержка сложных скриптов в версиях до Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Сводка](#summary)

## <a name="overview"></a>Обзор

начиная с версии Windows Vista, сама Windowsная операционная система была создана с нуля на многоязыковую платформу с дополнительной поддержкой, позволяющей создавать многоязыковые приложения, использующие модель ресурсов Windows MUI.

В этом учебнике показана эта новая поддержка многоязычных приложений, охватывающая следующие аспекты:

-   Использует улучшенную поддержку платформы многоязыкового интерфейса пользователя для простого включения многоязычных приложений.
-   расширяет многоязычные приложения для работы в версиях Windows до Windows Vista.
-   Касается дополнительных вопросов, связанных с разработкой специализированных многоязычных приложений, таких как консольные приложения.

Эти ссылки помогут вам быстро обновить принципы интернационализации и MUI:

-   [Краткий обзор интернационализации](understanding-internationalization.md).
-   [Основные понятия многоязыкового интерфейса пользователя](understanding-mui.md).
-   [Использование многоязыкового интерфейса пользователя для разработки приложений Win32](using-multilingual-user-interface.md).

### <a name="the-idea-behind-hello-mui"></a>Идея фонового интерфейса пользователя Hello

Возможно, вы знакомы с классическим приложением Hello World, которое иллюстрирует основные понятия программирования. В этом руководстве используется аналогичный подход, демонстрирующий использование модели ресурсов многоязыкового интерфейса пользователя для обновления одноязыкового приложения для создания многоязычной версии с именем Hello MUI.

> [!Note]  
> Задачи, описанные в этом учебнике, описаны в разделе Подробное описание действий из-за точности, с которой эти действия должны быть выполнены, и необходимости объяснить сведения для разработчиков, которые испытывают немало опыта работы с этими задачами.

 

## <a name="setting-up-the-hello-mui-solution"></a>Настройка решения Hello MUI

Эти шаги описывают подготовку к созданию решения Hello MUI.

### <a name="platform-requirements"></a>Требования к платформе

примеры кода, приведенные в этом руководстве, необходимо скомпилировать с помощью Windows пакета средств разработки программного обеспечения (SDK) для Windows 7 и Visual Studio 2008. пакет SDK для Windows 7 будет установлен на Windows XP, Windows Vista и Windows 7, а пример решения можно построить на любой из этих версий операционной системы.

все примеры кода в этом учебнике предназначены для выполнения в версиях x86 и x64 Windows XP, Windows Vista и Windows 7. конкретные части, которые не будут работать в Windows XP, вызываются там, где это необходимо.

### <a name="prerequisites"></a>Предварительные требования

1.  установите Visual Studio 2008.

    дополнительные сведения см. в [центре разработчиков Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).

2.  установите Windows SDK для Windows 7.

    его можно установить на странице Windows SDK [центра разработчиков Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx). пакет SDK включает служебные программы для разработки приложений для версий ос, начиная с Windows XP и до последней версии.

    > [!Note]  
    > Если пакет не устанавливается в расположение по умолчанию или если вы не устанавливаете на системный диск, который обычно является диском C, запишите путь установки.

     

3.  настройте параметры командной строки Visual Studio.

    1.  откройте Visual Studio командное окно.
    2.  Введите **путь к множеству**.
    3.  убедитесь, что переменная path содержит путь к папке bin пакета SDK для Windows 7:... Microsoft sdk \\ Windows \\ v 7.0 \\ bin

4.  Установите дополнительный пакет API-интерфейсов нижнего уровня Microsoft NLS.
    > [!Note]  
    > в контексте этого руководства этот пакет необходим только в том случае, если вы настраиваете приложение для работы в Windows версиях, предшествовавших Windows Vista. См. раздел [Step 5: Настройка Hello MUI](#step-5-customizing-hello-mui).

     

    1.  Скачайте и установите пакет с [веб-сайта загрузки](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).
    2.  как и в случае с Windows SDK, если пакет не устанавливается в расположение по умолчанию или если вы не устанавливаете на системный диск, который обычно является диском C, запишите путь установки.
    3.  если ваша платформа разработки имеет Windows XP или Windows Server 2003, убедитесь, что Nlsdl.dll установлена и зарегистрирована правильно.

        1.  Перейдите в папку Redist в папке путь установки.
        2.  Запустите соответствующий распространяемый пакет Нлсдл. \*.exe, например nlsdl.x86.exe. На этом шаге выполняется установка и регистрация Nlsdl.dll.

    > [!Note]  
    > если вы разрабатываете приложение, использующее MUI, которое должно выполняться в Windows версиях до Windows Vista, Nlsdl.dll должно присутствовать на целевой Windows платформе. В большинстве случаев это означает, что приложению необходимо перенести и установить распространяемый установщик Нлсдл (а не просто копировать сам Nlsdl.dll).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Шаг 0. Создание жестко закодированного пользовательского интерфейса Hello

Этот учебник начинается с одноязычной версии приложения Hello MUI. Приложение предполагает использование языка программирования C++, строк расширенных символов и функции [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) для вывода.

Начните с создания начального приложения Гуистеп \_ 0, а также решения хелломуи, содержащего все приложения в этом руководстве.

1.  в Visual Studio 2008 создайте новый проект. Используйте следующие параметры и значения:

    1.  тип Project: в разделе Visual C++ выберите win32, а затем в разделе Visual Studio установленные шаблоны выберите Project Win32.
    2.  Имя: Гуистеп \_ 0.
    3.  Расположение: *прожектрутдиректори* (последующие шаги ссылаются на этот каталог).
    4.  Имя решения: Хелломуи.
    5.  Установите флажок Создать каталог для решения.
    6.  в мастере приложений Win32 выберите тип приложения по умолчанию: Windows приложение.

2.  Настройка потоковой модели проекта:

    1.  В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 0, а затем выберите пункт Свойства.
    2.  В диалоговом окне страницы свойств проекта выполните следующие действия.

        1.  В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.
        2.  В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).

3.  Замените содержимое Гуистеп \_ 0. cpp следующим кодом:
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  Создайте и запустите приложение.

Простой исходный код, приведенный выше, делает упрощенный вариант разработки с жестким кодированием или внедрением, который будет видеть пользователь, в данном случае текст "Hello MUI". Этот вариант ограничивает служебную программу приложения для пользователей, которые не распознают слово "Hello" на английском языке. Поскольку многоязыковой интерфейс пользователя является словарем на основе технологий, для этого руководства предполагается, что строка остается "MUI" для всех языков.

## <a name="step-1-implementing-the-basic-resource-module"></a>Шаг 1. Реализация базового модуля ресурсов

Microsoft Win32 обладает большой доступностью, позволяющей разработчикам приложений отделить данные ресурсов пользовательского интерфейса от исходного кода приложения. Это разделение имеет форму модели ресурсов Win32, в которой строки, точечные рисунки, значки, сообщения и другие элементы, обычно отображаемые для пользователя, упаковываются в отдельный раздел исполняемого файла, отделенный от исполняемого кода.

Чтобы проиллюстрировать это разделение между исполняемым кодом и упаковкой данных ресурса, на этом этапе учебник помещает ранее жестко запрограммированную строку "Hello" (ресурс "en-US") в раздел ресурсов модуля DLL в \_ проекте хелломодуле en \_ US.

Эта библиотека DLL Win32 также может содержать исполняемые функции типа библиотеки (как любая другая библиотека DLL). Но чтобы сосредоточиться на аспектах, связанных с ресурсами Win32, мы оставляем код DLL времени выполнения создана в DllMain. cpp. В последующих разделах этого руководства мы будем использовать собранные здесь данные о ресурсах Хелломодуле, а также представим соответствующий код среды выполнения.

Чтобы создать модуль ресурсов Win32, начните с создания библиотеки DLL с помощью функции создана out.

1.  Добавьте новый проект в решение Хелломуи:

    1.  В меню Файл выберите Добавить, а затем новый Project.
    2.  тип Project: Project Win32.
    3.  Имя: Хелломодуле \_ en \_ US.
    4.  Расположение: *прожектрутдиректори* \\ хелломуи.
    5.  В мастере приложений Win32 выберите тип приложения: DLL.

2.  Настройка потоковой модели этого проекта:

    1.  В обозреватель решений щелкните правой кнопкой мыши проект Хелломодуле \_ en \_ US и выберите пункт Свойства.
    2.  В диалоговом окне страницы свойств проекта выполните следующие действия.

        1.  В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.
        2.  В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).

3.  Изучите DllMain. cpp. (Может потребоваться добавить нессылки \_ на Макросы параметров для созданного кода, как здесь, чтобы включить его для компиляции на уровне предупреждений 4.)
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  Добавьте в проект файл определения ресурса Хелломодуле. rc:

    1.  В проекте Хелломодуле \_ en \_ US щелкните правой кнопкой мыши папку файлы ресурсов и выберите Добавить, а затем щелкните новый элемент.
    2.  В диалоговом окне Добавление нового элемента выберите следующие элементы.

        1.  категории: в разделе Visual C++ выберите ресурс, а затем в разделе "Visual Studio установленные шаблоны" выберите файл ресурсов (. rc).
        2.  Имя: Хелломодуле.
        3.  Расположение: примите значение по умолчанию.
        4.  Нажмите кнопку "Добавить".

    3.  Укажите, что новый файл Хелломодуле. RC должен быть сохранен в Юникоде:

        1.  В обозреватель решений щелкните правой кнопкой мыши Хелломодуле. RC и выберите Просмотреть код.
        2.  Если появится сообщение о том, что файл уже открыт, и запросит, нужно ли его закрыть, нажмите кнопку Да.
        3.  Чтобы файл отображался как текст, выберите файл выбора меню, а затем дополнительные параметры сохранения.
        4.  В разделе кодировка укажите Юникод-кодовую страницу 1200.
        5.  Щелкните ОК.
        6.  Сохраните и закройте Хелломодуле. rc.

    4.  Добавьте таблицу строк, содержащую строку "Hello":

        1.  В представление ресурсов щелкните правой кнопкой мыши Хелломодуле. RC и выберите Добавить ресурс.
        2.  Выберите таблицу строк.
        3.  Нажмите кнопку New (Создать).
        4.  Добавьте строку в таблицу строк:

            1.  Идентификатор: HELLO \_ MUI \_ str \_ 0.
            2.  Значение: 0.
            3.  Заголовок: Привет.

        Если просмотреть Хелломодуле. RC как текст, вы увидите различные части исходного кода, относящегося к ресурсам. Самым большим интересом является раздел, описывающий строку "Hello":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        Эта строка "Hello" — это ресурс, который должен быть локализован (т. е. переведен) на каждый язык, поддерживаемый приложением надеется. Например, Хелломодуле \_ TA \_ в проекте (который вы создадите на следующем шаге) будет содержать собственную локализованную версию хелломодуле. RC для «TA-in»:

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  Создайте проект Хелломодуле \_ en \_ US, чтобы убедиться в отсутствии ошибок.

5.  Создавайте шесть проектов в решении Хелломуи (или столько из них, сколько нужно), чтобы создать шесть дополнительных библиотек ресурсов для дополнительных языков. Используйте значения из этой таблицы:

    | Имя проекта        | Имя RC-файла | Идентификатор строки          | Строковое значение | Заголовок строки |
    |---------------------|------------------|--------------------|--------------|----------------|
    | Хелломодуле \_ де \_ de | хелломодуле      | HELLO \_ MUI \_ str \_ 0 | 0            | халло          |
    | Хелломодуле \_ ES \_ | хелломодуле      | HELLO \_ MUI \_ str \_ 0 | 0            | Hol           |
    | Хелломодуле \_ fr \_ fr | хелломодуле      | HELLO \_ MUI \_ str \_ 0 | 0            | Bonjour        |
    | Хелломодуле \_ Hi \_ in | хелломодуле      | HELLO \_ MUI \_ str \_ 0 | 0            | नमस्           |
    | Хелломодуле \_ ru \_ | хелломодуле      | HELLO \_ MUI \_ str \_ 0 | 0            | здравствуйте   |
    | Хелломодуле \_ TA \_ в | хелломодуле      | HELLO \_ MUI \_ str \_ 0 | 0            | வணக்கம்        |

    

     

Дополнительные сведения о структуре и синтаксисе файла. RC см. в разделе [Общие сведения о файлах ресурсов](../menurc/about-resource-files.md).

## <a name="step-2-building-the-basic-resource-module"></a>Шаг 2. Создание базового модуля ресурсов

При использовании предыдущих моделей ресурсов создание одного из семи проектов Хелломодуле приведет к появлению семи отдельных библиотек DLL. Каждая библиотека DLL будет содержать раздел ресурсов с одной строкой, локализованной для соответствующего языка. Хотя это и подходит для модели ресурсов Win32 с предысторией, эта схема не использует преимущества многоязыкового интерфейса пользователя.

в пакете SDK для Windows Vista и более поздних версиях MUI позволяет разбивать исполняемые файлы на исходный код и локализуемые модули содержимого. с дополнительной настройкой, описанной далее на шаге 5, приложения могут быть включены для поддержки многоязычных версий до Windows Vista.

основные механизмы, доступные для разбиения ресурсов из исполняемого кода, начиная с Windows Vista:

-   С помощью rc.exe (компилятора RC) с конкретными переключателями или
-   Использование инструмента разбиения стилей после сборки с именем muirct.exe.

Дополнительные сведения см. в разделе [Служебные программы](resource-utilities.md) .

Для простоты в этом руководстве используется muirct.exe для разделения исполняемого файла "Hello MUI".

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Разделение различных модулей языковых ресурсов: обзор

Многокомпонентный процесс состоит в разделении библиотек DLL на один исполняемый HelloModule.dll, а также HelloModule.dll. MUI для каждого из семи поддерживаемых языков в рамках этого руководства. В этом обзоре описываются необходимые действия. в следующем разделе представлен командный файл, который выполняет эти действия.

Сначала разделите модуль HelloModule.dll, поддерживающий только английский язык, с помощью команды:


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



В командной строке выше используется файл конфигурации Дореверсемуилок. ркконфиг. Этот тип файла конфигурации обычно используется muirct.exe для разделения ресурсов между DLL-библиотекой, не зависящей от языка (LN), и файлами MUI, зависящими от языка. В этом случае XML-файл Дореверсемуилок. ркконфиг (перечисленный в следующем разделе) указывает на множество типов ресурсов, но все они попадают в категорию файлов «localizedResources» или «MUI», и в категории, не зависящей от языка, отсутствуют ресурсы. Дополнительные сведения о подготовке файла конфигурации ресурсов см. в разделе [Подготовка файла конфигурации ресурса](preparing-a-resource-configuration-file.md).

Помимо создания файла HelloModule.dll. MUI, содержащего строку "Hello" на английском языке, muirct.exe также внедряет ресурс MUI в модуль HelloModule.dll во время разделения. Чтобы обеспечить правильную загрузку во время выполнения соответствующих ресурсов из модулей HelloModule.dll. MUI для конкретного языка, каждый MUI-файл должен быть исправлен в соответствии с контрольными суммами в базовом модуле, нейтральном к языку LN. Это делается с помощью следующей команды:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



Аналогичным образом, muirct.exe вызывается для создания файла HelloModule.dll. MUI для каждого из других языков. Однако в таких случаях библиотека DLL, не зависящая от языка, отбрасывается, так как потребуется только первая созданная. Команды, которые обрабатывают ресурсы для испанского и французского языков, выглядят следующим образом:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Одним из наиболее важных моментов, которые следует заметить в muirct.exe командных строк, является то, что для указания идентификатора целевого языка используется флаг-x. Значение, указанное для muirct.exe, отличается для каждого зависящего от языка HelloModule.dll модуля. Это значение языка является центральным и используется muirct.exe для соответствующей пометки MUI-файла во время разделения. Неверное значение приводит к сбоям при загрузке ресурсов для этого конкретного файла MUI во время выполнения. Дополнительные сведения о сопоставлении имени языка с LCID см. в разделе [константы и строки идентификатора языка](language-identifier-constants-and-strings.md) .

Каждый разделенный MUI-файл помещается в каталог, соответствующий имени языка, непосредственно под каталогом, в котором будет размещаться HelloModule.dll, не зависящее от языка. Дополнительные сведения о размещении файлов MUI см. в разделе [развертывание приложения](application-deployment.md).

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Разделение различных модулей языковых ресурсов: создание файлов

В этом руководстве вы создадите командный файл, содержащий команды для разделения различных библиотек DLL, и вызываете их вручную. Обратите внимание, что в реальной работе по разработке можно уменьшить вероятность ошибок сборки, включив эти команды в качестве событий до или после сборки в решение Хелломуи, но это выходит за рамки данного руководства.

Создайте файлы для отладочной сборки:

1.  Создайте командный файл Дореверсемуилок. cmd, содержащий следующие команды:
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  Создайте XML-файл Дореверсемуилок. ркконфиг, содержащий следующие строки:
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  Скопируйте Дореверсемуилок. cmd и Дореверсемуилок. ркконфиг в *прожектрутдиректори* \\ хелломуи \\ Debug.
4.  откройте командную строку Visual Studio 2008 и перейдите в каталог отладки.
5.  Запустите Дореверсемуилок. cmd.

При создании сборки выпуска вы копируете те же файлы Дореверсемуилок. cmd и Дореверсемуилок. ркконфиг в каталог выпуска и запускаете командный файл там.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Шаг 3. Создание Resource-Savvy "Hello MUI"

Основываясь на первом0.exe Гуистеп примере с жестко запрограммированным \_ , можно расширить круг пользователей приложения на нескольких языках, выбрав внедрение модели ресурсов Win32. Новый код времени выполнения, представленный на этом шаге, включает логику загрузки модуля ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) и строки получения ([**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  добавьте новый проект в решение хелломуи (с помощью файла выбора меню, добавьте и новый Project) со следующими параметрами и значениями:

    1.  тип Project: Project Win32.
    2.  Имя: Гуистеп \_ 1.
    3.  Расположение: примите значение по умолчанию.
    4.  в мастере приложений Win32 выберите тип приложения по умолчанию: Windows приложение.

2.  настройте выполнение этого проекта в Visual Studio и настройте его потоковую модель:

    1.  В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 1 и выберите Задать в качестве Project запуска.
    2.  Щелкните его правой кнопкой мыши и выберите пункт Свойства.
    3.  В диалоговом окне страницы свойств проекта выполните следующие действия.

        1.  В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.
        2.  В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).

3.  Замените содержимое файла Гуистеп \_ 1. cpp следующим кодом:
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  Создайте и запустите приложение. Выходные данные будут отображаться на языке, выбранном в качестве языка интерфейса компьютера (при условии, что это один из семи созданных нами языков).

## <a name="step-4-globalizing-hello-mui"></a>Шаг 4. Глобализация "Hello MUI"

Несмотря на то, что предыдущий пример способен отображать выходные данные на разных языках, он оказывается коротким в нескольких областях. возможно, наиболее заметным является то, что приложение доступно только в небольшом подмножестве языков по сравнению с Windows самой операционной системой. если, например, \_ приложение гуистеп 1 из предыдущего шага было установлено на японской сборке Windows, могут возникнет сбои размещения ресурсов.

Для решения этой ситуации у вас есть два основных варианта:

-   Убедитесь, что включены ресурсы на предварительно определенном конечном языке.
-   Предоставить конечному пользователю способ настройки языковых настроек из подмножества языков, которые специально поддерживаются приложением.

Из этих вариантов мы настоятельно рекомендуем использовать такой вариант, который обеспечивает базовый язык, и реализуется в этом руководстве путем передачи флага-g в muirct.exe, как показано выше. Этот флаг сообщает muirct.exe, что для конкретного языка (de-DE/0x0407) имеется конечный язык, связанный с модулем DLL, не зависящим от языка (HelloModule.dll). Во время выполнения этот параметр используется в качестве последнего средства для создания текста, отображаемого для пользователя. В случае, если не найден конечный язык и нет доступных ресурсов в двоичном файле, не зависящем от языка, загрузка ресурса завершается ошибкой. Поэтому следует тщательно определить сценарии, которые могут возникнуть в приложении, и соответствующим образом спланировать конечный язык.

Другой вариант, позволяющий настроить языковые настройки и загружать ресурсы на основе этой пользовательской иерархии, может значительно повысить удовлетворенность клиента. К сожалению, она также усложняет функциональность, необходимую в приложении.

На этом шаге учебника используется упрощенный механизм работы с текстовыми файлами для включения пользовательской конфигурации языка пользователя. Текстовый файл анализируется во время выполнения приложением, а список проанализированных и проверенных языков используется для создания настраиваемого списка резервных. после того как список настраиваемых резервных элементов будет установлен, Windows api загрузит ресурсы в соответствии с приоритетом языка, указанным в этом списке. Оставшаяся часть кода похожа на ту, которая была найдена на предыдущем шаге.

1.  добавьте новый проект в решение хелломуи (с помощью файла выбора меню, добавьте и новый Project) со следующими параметрами и значениями:

    1.  тип Project: Project Win32.
    2.  Имя: Гуистеп \_ 2.
    3.  Расположение: примите значение по умолчанию.
    4.  в мастере приложений Win32 выберите тип приложения по умолчанию: Windows приложение.

2.  настройте выполнение этого проекта в Visual Studio и настройте его потоковую модель:

    1.  В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 2 и выберите установить как Project запуска.
    2.  Щелкните его правой кнопкой мыши и выберите пункт Свойства.
    3.  В диалоговом окне страницы свойств проекта выполните следующие действия.

        1.  В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.
        2.  В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).

3.  Замените содержимое файла Гуистеп \_ 2. cpp следующим кодом:
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Создайте текстовый файл в Юникоде langs.txt содержащий следующую строку:

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > Не забудьте сохранить файл как Юникод.

     

    Скопируйте langs.txt в каталог, из которого будет выполняться программа:

    -   при запуске из в Visual Studio скопируйте его в *прожектрутдиректори* \\ хелломуи \\ гуистеп \_ 2.
    -   при запуске из проводника Windows скопируйте его в тот же каталог, что и гуистеп \_2.exe.

5.  Постройте и запустите проект. Попробуйте изменить langs.txt, чтобы в начале списка появились разные языки.

## <a name="step-5-customizing-hello-mui"></a>Шаг 5. Настройка "Hello MUI"

ряд функций времени выполнения, упомянутых до сих пор в рамках этого руководства, доступен только в Windows Vista и более поздних версиях. вы можете повторно использовать усилия, которые были потрачены на локализацию и разделение ресурсов, делая работу приложения более ранними Windows версиями операционных систем, например Windows XP. Этот процесс включает в себя настройку предыдущего примера в двух ключевых областях:

-   функции загрузки ресурсов, предшествующие Windows Vista (например, [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**лоадикон**](/windows/win32/api/winuser/nf-winuser-loadicona), [**лоадбитмап**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)и др.), не поддерживают MUI. Приложения, поставляемые с разделенными ресурсами (LN и MUI Files), должны загружать модули ресурсов с помощью одной из следующих двух функций:

    -   если приложение должно запускаться только в Windows Vista и более поздних версий, необходимо загрузить модули ресурсов с помощью [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).
    -   если приложение должно выполняться в версиях, предшествовавших Windows vista, а также Windows Vista или более поздней версии, оно должно использовать [**лоадмуилибрари**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), который представляет собой конкретную функцию нижнего уровня, предоставляемую в пакете SDK для Windows 7.

-   поддержка управления языками и порядками отката на языке, предлагаемая в версиях операционных систем Windows, предшествующих Windows vista, существенно отличается от версии в Windows vista и более поздних версиях. По этой причине приложения, которые позволяют выполнять настраиваемые пользователем действия языка, должны настраивать методы управления языками:

    -   если приложение должно запускаться только в Windows Vista и более поздних версий, установка списка языков с помощью [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) достаточно велика.
    -   если приложение должно выполняться на всех Windows версиях, необходимо создать код, который будет выполняться на платформах предыдущих версий для прохода по пользовательскому списку языков и проверки требуемого модуля ресурсов. Это можно увидеть в разделах 1C и 2 кода, приведенного далее на этом шаге.

Создайте проект, который может использовать локализованные модули ресурсов в любой версии Windows:

1.  добавьте новый проект в решение хелломуи (с помощью файла выбора меню, добавьте и новый Project) со следующими параметрами и значениями:

    1.  тип Project: Project Win32.
    2.  Имя: Гуистеп \_ 3.
    3.  Расположение: примите значение по умолчанию.
    4.  в мастере приложений Win32 выберите тип приложения по умолчанию: Windows приложение.

2.  настройте этот проект для запуска из Visual Studio и настройте его потоковую модель. Кроме того, настройте его для добавления необходимых заголовков и библиотек.

    > [!Note]  
    > в путях, используемых в этом руководстве, предполагается, что пакет SDK для Windows 7 и пакеты api нижнего уровня Microsoft NLS были установлены в каталоги по умолчанию. Если это не так, измените пути соответствующим образом.

     

    1.  В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 3 и выберите пункт назначить Project запуска.
    2.  Щелкните его правой кнопкой мыши и выберите пункт Свойства.
    3.  В диалоговом окне страницы свойств проекта выполните следующие действия.

        1.  В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.
        2.  В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).
        3.  Выберите Общие и добавьте в дополнительные каталоги включения:

            -   "C: \\ API нижнего уровня Microsoft NLS \\ включают".

        4.  Выберите язык и задайте параметр обрабатывать WCHAR \_ t как встроенный тип: нет (/Zc: WCHAR \_ t-).
        5.  Выберите Дополнительно и задайте соглашение о вызовах: \_ STDCALL (/gz).
        6.  В разделе Свойства конфигурации разверните компоновщик, выберите входные данные и добавьте дополнительные зависимости:

            -   "C: \\ Program files \\ Microsoft sdks \\ Windows \\ v 7.0 \\ lib \\ муилоад. Lib".
            -   "C: \\ интерфейсы API нижнего уровня Microsoft NLS \\ lib \\ x86 \\ нлсдл. lib".

3.  Замените содержимое файла Гуистеп \_ 3. cpp следующим кодом:
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Создайте или скопируйте langs.txt в соответствующий каталог, как описано в [шаге 4: глобализация "Hello MUI"](#step-4-globalizing-hello-mui).
5.  Постройте и запустите проект.

> [!Note]  
> если приложение должно выполняться в Windows версиях до Windows Vista, обязательно ознакомьтесь с документами, прилагаемыми к пакету api- [интерфейсов нижнего уровня Microsoft NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) , в котором описано повторное распространение Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Дополнительные рекомендации для MUI

### <a name="support-for-console-applications"></a>Поддержка консольных приложений

Методики, описанные в этом учебнике, также можно использовать в консольных приложениях. однако, в отличие от большинства стандартных элементов управления GUI, окно команд Windows не может отображать символы для всех языков. Поэтому многоязыковые консольные приложения требуют особого внимания.

Вызов API-интерфейсов [**сетсреадуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) или [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) с конкретными флагами фильтрации приводит к тому, что функции загрузки ресурсов удаляют языковые проверки ресурсов для определенных языков, которые обычно не отображаются в окне командной строки. Если эти флаги заданы, то алгоритмы настройки языка позволяют использовать в командном окне только те языки, которые будут отображаться правильно.

Дополнительные сведения об использовании этих API для создания многоязыкового консольного приложения см. в разделах "Примечания" [**сетсреадуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) и [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Определение языков для поддержки на Run-Time

Вы можете принять одно из следующих предложений по проектированию, чтобы определить, какие языки должно поддерживать приложение во время выполнения:

-   **Во время установки включите конечного пользователя, чтобы выбрать предпочтительный язык из списка поддерживаемых языков.**

-   **Чтение списка языков из файла конфигурации**

    Некоторые из проектов в этом учебнике содержат функцию, используемую для синтаксического анализа файла конфигурации langs.txt, который содержит список языков.

    Поскольку эта функция принимает внешние входные данные, проверьте языки, предоставленные в качестве входных данных. Дополнительные сведения о выполнении проверки см. в разделе функции [**исвалидлокаленаме**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) или [**довнлевеллокаленаметолЦид**](downlevellocalenametolcid.md) .

-   **Запросите операционную систему, чтобы определить, какие языки установлены**

    Такой подход позволяет приложению использовать тот же язык, что и операционная система. Хотя это и не требует запроса пользователя, при выборе этого параметра следует помнить, что языки операционной системы могут быть добавлены или удалены в любое время и могут изменяться после установки приложения пользователем. Кроме того, имейте в виду, что в некоторых случаях операционная система устанавливается с ограниченной поддержкой языка, а приложение предоставляет больше преимуществ, если поддерживает языки, не поддерживаемые операционной системой.

    Дополнительные сведения о том, как определить установленные языки в операционной системе, см. в разделе Функция [**енумуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>поддержка сложных скриптов в версиях до Windows Vista

если приложение, поддерживающее определенные сложные сценарии, работает в версии Windows до Windows Vista, текст в этом сценарии может отображаться неправильно в компонентах графического пользовательского интерфейса. Например, в проекте нижнего уровня в этом руководстве скрипты hi-IN и TA-IN могут не отображаться в окне сообщения из-за проблем с обработкой сложных сценариев и недостатком связанных шрифтов. Как правило, проблемы этой природы представляют собой квадратные рамки в компоненте GUI.

Дополнительные сведения о том, как включить обработку сложных скриптов, можно найти в статье [Поддержка скриптов и шрифтов в Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Сводка

В этом учебнике мы расправили глобализованное приложение и продемонстрировали следующие рекомендации.

-   Разработайте приложение, чтобы воспользоваться преимуществами модели ресурсов Win32.
-   Использование разделения ресурсов многоязыкового интерфейса в вспомогательные двоичные файлы (MUI-файлы).
-   Убедитесь, что процесс локализации обновляет ресурсы в файлах MUI, чтобы они соответствовали целевому языку.
-   Убедитесь, что упаковка и развертывание приложения, связанные файлы MUI и содержимое конфигурации выполняются правильно, чтобы разрешить API-интерфейсам загрузки ресурсов искать локализованное содержимое.
-   Предоставьте конечному пользователю механизм для настройки языковой конфигурации приложения.
-   Настройте код времени выполнения, чтобы воспользоваться преимуществами языковой конфигурации, чтобы сделать приложение более быстрым реагированием на потребности конечного пользователя.

 

 
