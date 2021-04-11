---
description: В этом учебнике показано, как взять на себя многоязыковую программу и сделать ее готовой к международному использованию. Это приложение в виде полного решения, созданного в Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Добавление поддержки многоязычного пользовательского интерфейса в приложение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912563"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a><span data-ttu-id="3455b-104">Добавление поддержки многоязычного пользовательского интерфейса в приложение</span><span class="sxs-lookup"><span data-stu-id="3455b-104">Adding Multilingual User Interface Support to an Application</span></span>

<span data-ttu-id="3455b-105">В этом учебнике показано, как взять на себя многоязыковую программу и сделать ее готовой к международному использованию.</span><span class="sxs-lookup"><span data-stu-id="3455b-105">This tutorial demonstrates how to take a monolingual application and make it world-ready.</span></span> <span data-ttu-id="3455b-106">Это приложение в виде полного решения, созданного в Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3455b-106">This application is in the form of a complete solution that is built within Microsoft Visual Studio.</span></span>

-   [<span data-ttu-id="3455b-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="3455b-107">Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="3455b-108">Идея фонового интерфейса пользователя Hello</span><span class="sxs-lookup"><span data-stu-id="3455b-108">The Idea Behind Hello MUI</span></span>](#the-idea-behind-hello-mui)
-   [<span data-ttu-id="3455b-109">Настройка решения Hello MUI</span><span class="sxs-lookup"><span data-stu-id="3455b-109">Setting up the Hello MUI Solution</span></span>](#setting-up-the-hello-mui-solution)
    -   [<span data-ttu-id="3455b-110">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="3455b-110">Platform Requirements</span></span>](#platform-requirements)
    -   [<span data-ttu-id="3455b-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="3455b-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3455b-112">Шаг 0. Создание жестко закодированного пользовательского интерфейса Hello</span><span class="sxs-lookup"><span data-stu-id="3455b-112">Step 0: Creating the Hard-coded Hello MUI</span></span>](#step-0-creating-the-hard-coded-hello-mui)
-   [<span data-ttu-id="3455b-113">Шаг 1. Реализация базового модуля ресурсов</span><span class="sxs-lookup"><span data-stu-id="3455b-113">Step 1: Implementing the Basic Resource Module</span></span>](#step-1-implementing-the-basic-resource-module)
-   [<span data-ttu-id="3455b-114">Шаг 2. Создание базового модуля ресурсов</span><span class="sxs-lookup"><span data-stu-id="3455b-114">Step 2: Building the Basic Resource Module</span></span>](#step-2-building-the-basic-resource-module)
    -   [<span data-ttu-id="3455b-115">Разделение различных модулей языковых ресурсов: обзор</span><span class="sxs-lookup"><span data-stu-id="3455b-115">Splitting the Various Language Resource Modules: An Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="3455b-116">Разделение различных модулей языковых ресурсов: создание файлов</span><span class="sxs-lookup"><span data-stu-id="3455b-116">Splitting the Various Language Resource Modules: Creating the Files</span></span>](#splitting-the-various-language-resource-modules-creating-the-files)
-   [<span data-ttu-id="3455b-117">Шаг 3. Создание Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3455b-117">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>](#step-3-creating-a-resource-savvy-hello-mui)
-   [<span data-ttu-id="3455b-118">Шаг 4. Глобализация "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3455b-118">Step 4: Globalizing "Hello MUI"</span></span>](#step-4-globalizing-hello-mui)
-   [<span data-ttu-id="3455b-119">Шаг 5. Настройка "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3455b-119">Step 5: Customizing "Hello MUI"</span></span>](#step-5-customizing-hello-mui)
-   [<span data-ttu-id="3455b-120">Дополнительные рекомендации для MUI</span><span class="sxs-lookup"><span data-stu-id="3455b-120">Additional Considerations for MUI</span></span>](#additional-considerations-for-mui)
    -   [<span data-ttu-id="3455b-121">Поддержка консольных приложений</span><span class="sxs-lookup"><span data-stu-id="3455b-121">Support for Console Applications</span></span>](#support-for-console-applications)
    -   [<span data-ttu-id="3455b-122">Определение языков для поддержки во время выполнения</span><span class="sxs-lookup"><span data-stu-id="3455b-122">Determination of Languages to Support at Run-Time</span></span>](#determination-of-languages-to-support-at-run-time)
    -   [<span data-ttu-id="3455b-123">Поддержка сложных скриптов в версиях до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3455b-123">Complex Script Support in Versions Prior to Windows Vista</span></span>](#complex-script-support-in-versions-prior-to-windows-vista)
-   [<span data-ttu-id="3455b-124">Сводка</span><span class="sxs-lookup"><span data-stu-id="3455b-124">Summary</span></span>](#summary)

## <a name="overview"></a><span data-ttu-id="3455b-125">Обзор</span><span class="sxs-lookup"><span data-stu-id="3455b-125">Overview</span></span>

<span data-ttu-id="3455b-126">Начиная с Windows Vista, сама операционная система Windows разрабатывалась с нуля на многоязыковую платформу с дополнительной поддержкой, позволяющей создавать многоязыковые приложения, использующие модель ресурсов многоязыкового интерфейса пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="3455b-126">Beginning with Windows Vista, the Windows operating system itself was built from the ground up to be a multilingual platform, with additional support that enables you to create multilingual applications that use the Windows MUI resource model.</span></span>

<span data-ttu-id="3455b-127">В этом учебнике показана эта новая поддержка многоязычных приложений, охватывающая следующие аспекты:</span><span class="sxs-lookup"><span data-stu-id="3455b-127">This tutorial illustrates this new support for multilingual applications by covering the following aspects:</span></span>

-   <span data-ttu-id="3455b-128">Использует улучшенную поддержку платформы многоязыкового интерфейса пользователя для простого включения многоязычных приложений.</span><span class="sxs-lookup"><span data-stu-id="3455b-128">Uses the improved MUI platform support to easily enable multilingual applications.</span></span>
-   <span data-ttu-id="3455b-129">Расширяет многоязычные приложения для работы в версиях Windows до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3455b-129">Extends multilingual applications to run on versions of Windows prior to Windows Vista.</span></span>
-   <span data-ttu-id="3455b-130">Касается дополнительных вопросов, связанных с разработкой специализированных многоязычных приложений, таких как консольные приложения.</span><span class="sxs-lookup"><span data-stu-id="3455b-130">Touches on the additional considerations involved in developing specialized multilingual applications such as console applications.</span></span>

<span data-ttu-id="3455b-131">Эти ссылки помогут вам быстро обновить принципы интернационализации и MUI:</span><span class="sxs-lookup"><span data-stu-id="3455b-131">These links help provide a quick refresher on the concepts on internationalization and MUI:</span></span>

-   <span data-ttu-id="3455b-132">[Краткий обзор интернационализации](understanding-internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="3455b-132">[Quick overview of internationalization](understanding-internationalization.md).</span></span>
-   <span data-ttu-id="3455b-133">[Основные понятия многоязыкового интерфейса пользователя](understanding-mui.md).</span><span class="sxs-lookup"><span data-stu-id="3455b-133">[MUI Concepts](understanding-mui.md).</span></span>
-   <span data-ttu-id="3455b-134">[Использование многоязыкового интерфейса пользователя для разработки приложений Win32](using-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3455b-134">[Using MUI to develop Win32 applications](using-multilingual-user-interface.md).</span></span>

### <a name="the-idea-behind-hello-mui"></a><span data-ttu-id="3455b-135">Идея фонового интерфейса пользователя Hello</span><span class="sxs-lookup"><span data-stu-id="3455b-135">The Idea Behind Hello MUI</span></span>

<span data-ttu-id="3455b-136">Возможно, вы знакомы с классическим приложением Hello World, которое иллюстрирует основные понятия программирования.</span><span class="sxs-lookup"><span data-stu-id="3455b-136">You are probably familiar with the classic Hello World application, which illustrates basic programming concepts.</span></span> <span data-ttu-id="3455b-137">В этом руководстве используется аналогичный подход, демонстрирующий использование модели ресурсов многоязыкового интерфейса пользователя для обновления одноязыкового приложения для создания многоязычной версии с именем Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="3455b-137">This tutorial takes a similar approach to illustrate how to use the MUI resource model to update a monolingual application to create a multilingual version called Hello MUI.</span></span>

> [!Note]  
> <span data-ttu-id="3455b-138">Задачи, описанные в этом учебнике, описаны в разделе Подробное описание действий из-за точности, с которой эти действия должны быть выполнены, и необходимости объяснить сведения для разработчиков, которые испытывают немало опыта работы с этими задачами.</span><span class="sxs-lookup"><span data-stu-id="3455b-138">The tasks in this tutorial are described in detailed steps because of the precision with which these activities must be performed, and the need to explain the details to developers who have little experience with these tasks.</span></span>

 

## <a name="setting-up-the-hello-mui-solution"></a><span data-ttu-id="3455b-139">Настройка решения Hello MUI</span><span class="sxs-lookup"><span data-stu-id="3455b-139">Setting up the Hello MUI Solution</span></span>

<span data-ttu-id="3455b-140">Эти шаги описывают подготовку к созданию решения Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="3455b-140">These steps outline how to prepare to create the Hello MUI solution.</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="3455b-141">Требования к платформе</span><span class="sxs-lookup"><span data-stu-id="3455b-141">Platform Requirements</span></span>

<span data-ttu-id="3455b-142">Вы должны скомпилировать примеры кода в этом руководстве, используя пакет средств разработки программного обеспечения (SDK) для Windows 7 и Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="3455b-142">You must compile the code samples in this tutorial using the Windows Software Development Kit (SDK) for Windows 7 and Visual Studio 2008.</span></span> <span data-ttu-id="3455b-143">Пакет SDK для Windows 7 будет установлен в Windows XP, Windows Vista и Windows 7, а пример решения можно построить на любой из этих версий операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3455b-143">The Windows 7 SDK will install on Windows XP, Windows Vista and Windows 7, and the sample solution can be built on any of these operating system versions.</span></span>

<span data-ttu-id="3455b-144">Все примеры кода в этом учебнике предназначены для выполнения в операционных системах x86 и x64 Windows XP, Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3455b-144">All code samples in this tutorial are designed to be executed on x86 and x64 versions of Windows XP, Windows Vista and Windows 7.</span></span> <span data-ttu-id="3455b-145">Конкретные части, которые не будут работать в Windows XP, вызываются там, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="3455b-145">Specific parts that will not work on Windows XP are called out where appropriate.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3455b-146">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="3455b-146">Prerequisites</span></span>

1.  <span data-ttu-id="3455b-147">Установите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="3455b-147">Install Visual Studio 2008.</span></span>

    <span data-ttu-id="3455b-148">Дополнительные сведения см. в [центре разработчиков Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="3455b-148">For more information, see the [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

2.  <span data-ttu-id="3455b-149">Установите Windows SDK для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3455b-149">Install the Windows SDK for Windows 7.</span></span>

    <span data-ttu-id="3455b-150">Его можно установить на странице Windows SDK [центра разработчиков Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3455b-150">You can install it from the Windows SDK page of the [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="3455b-151">Пакет SDK включает служебные программы для разработки приложений для версий ОС, начиная с Windows XP и до последней версии.</span><span class="sxs-lookup"><span data-stu-id="3455b-151">The SDK includes utilities to develop applications for OS versions starting from Windows XP through the most recent.</span></span>

    > [!Note]  
    > <span data-ttu-id="3455b-152">Если пакет не устанавливается в расположение по умолчанию или если вы не устанавливаете на системный диск, который обычно является диском C, запишите путь установки.</span><span class="sxs-lookup"><span data-stu-id="3455b-152">If you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>

     

3.  <span data-ttu-id="3455b-153">Настройте параметры командной строки Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3455b-153">Configure the Visual Studio command line parameters.</span></span>

    1.  <span data-ttu-id="3455b-154">Откройте командное окно Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3455b-154">Open a Visual Studio command window.</span></span>
    2.  <span data-ttu-id="3455b-155">Введите **путь к множеству**.</span><span class="sxs-lookup"><span data-stu-id="3455b-155">Type **set path**.</span></span>
    3.  <span data-ttu-id="3455b-156">Убедитесь, что переменная PATH содержит путь к папке bin пакета SDK для Windows 7:... \\ \\ Корзина Windows версии 7.0 для Microsoft SDK \\</span><span class="sxs-lookup"><span data-stu-id="3455b-156">Confirm that the path variable includes the path of the bin folder of the Windows 7 SDK: ...Microsoft SDKs\\Windows\\v7.0\\bin</span></span>

4.  <span data-ttu-id="3455b-157">Установите дополнительный пакет API-интерфейсов нижнего уровня Microsoft NLS.</span><span class="sxs-lookup"><span data-stu-id="3455b-157">Install the Microsoft NLS downlevel APIs add-on package.</span></span>
    > [!Note]  
    > <span data-ttu-id="3455b-158">В контексте этого руководства этот пакет необходим только в том случае, если приложение будет настроено для работы в версиях Windows, предшествовавших Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3455b-158">In the context of this tutorial, this package is necessary only if you will be customizing the application to run on Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="3455b-159">См. раздел [Step 5: Настройка Hello MUI](#step-5-customizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="3455b-159">See [Step 5: Customizing Hello MUI](#step-5-customizing-hello-mui).</span></span>

     

    1.  <span data-ttu-id="3455b-160">Скачайте и установите пакет с [веб-сайта загрузки](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="3455b-160">Download and install the package from its [download site](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span></span>
    2.  <span data-ttu-id="3455b-161">Как и в случае с Windows SDK, если пакет не устанавливается в расположение по умолчанию или если вы не устанавливаете на системный диск, который обычно является диском C, запишите путь установки.</span><span class="sxs-lookup"><span data-stu-id="3455b-161">As with the Windows SDK, if you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>
    3.  <span data-ttu-id="3455b-162">Если ваша платформа разработки — Windows XP или Windows Server 2003, убедитесь, что Nlsdl.dll установлен и зарегистрирован правильно.</span><span class="sxs-lookup"><span data-stu-id="3455b-162">If your development platform is Windows XP or Windows Server 2003, confirm that Nlsdl.dll is installed and registered correctly.</span></span>

        1.  <span data-ttu-id="3455b-163">Перейдите в папку Redist в папке путь установки.</span><span class="sxs-lookup"><span data-stu-id="3455b-163">Browse to the "redist" folder under the install path location.</span></span>
        2.  <span data-ttu-id="3455b-164">Запустите соответствующий распространяемый \* нлсдл. exe, например nlsdl.x86.exe.</span><span class="sxs-lookup"><span data-stu-id="3455b-164">Run the appropriate redistributable Nlsdl.\*.exe, such as nlsdl.x86.exe.</span></span> <span data-ttu-id="3455b-165">На этом шаге выполняется установка и регистрация Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="3455b-165">This step installs and registers Nlsdl.dll.</span></span>

    > [!Note]  
    > <span data-ttu-id="3455b-166">Если вы разрабатываете приложение, использующее MUI, которое должно работать в версиях Windows, предшествовавших Windows Vista, Nlsdl.dll должны присутствовать на целевой платформе Windows.</span><span class="sxs-lookup"><span data-stu-id="3455b-166">If you develop an application that uses MUI and that must run on Windows versions prior to Windows Vista, Nlsdl.dll must be present on the destination Windows platform.</span></span> <span data-ttu-id="3455b-167">В большинстве случаев это означает, что приложению необходимо перенести и установить распространяемый установщик Нлсдл (а не просто копировать сам Nlsdl.dll).</span><span class="sxs-lookup"><span data-stu-id="3455b-167">In most cases, this means that the application needs to carry and install the redistributable Nlsdl installer (and not merely copy Nlsdl.dll itself).</span></span>

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a><span data-ttu-id="3455b-168">Шаг 0. Создание жестко закодированного пользовательского интерфейса Hello</span><span class="sxs-lookup"><span data-stu-id="3455b-168">Step 0: Creating the Hard-coded Hello MUI</span></span>

<span data-ttu-id="3455b-169">Этот учебник начинается с одноязычной версии приложения Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="3455b-169">This tutorial begins with the monolingual version of the Hello MUI application.</span></span> <span data-ttu-id="3455b-170">Приложение предполагает использование языка программирования C++, строк расширенных символов и функции [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) для вывода.</span><span class="sxs-lookup"><span data-stu-id="3455b-170">The application assumes the use of the C++ programming language, wide character strings, and the [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) function for output.</span></span>

<span data-ttu-id="3455b-171">Начните с создания начального приложения Гуистеп \_ 0, а также решения хелломуи, содержащего все приложения в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="3455b-171">Begin by creating the initial GuiStep\_0 application, as well as the HelloMUI solution, which contain all of the applications in this tutorial.</span></span>

1.  <span data-ttu-id="3455b-172">В Visual Studio 2008 создайте новый проект.</span><span class="sxs-lookup"><span data-stu-id="3455b-172">In Visual Studio 2008, create a new project.</span></span> <span data-ttu-id="3455b-173">Используйте следующие параметры и значения:</span><span class="sxs-lookup"><span data-stu-id="3455b-173">Use the following settings and values:</span></span>

    1.  <span data-ttu-id="3455b-174">Тип проекта: в разделе Visual C++ выберите Win32, а затем в разделе Установленные шаблоны Visual Studio выберите проект Win32.</span><span class="sxs-lookup"><span data-stu-id="3455b-174">Project type: Under Visual C++ select Win32, and then under Visual Studio installed templates select Win32 Project.</span></span>
    2.  <span data-ttu-id="3455b-175">Имя: Гуистеп \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3455b-175">Name: GuiStep\_0.</span></span>
    3.  <span data-ttu-id="3455b-176">Расположение: *прожектрутдиректори* (последующие шаги ссылаются на этот каталог).</span><span class="sxs-lookup"><span data-stu-id="3455b-176">Location: *ProjectRootDirectory* (Later steps reference this directory).</span></span>
    4.  <span data-ttu-id="3455b-177">Имя решения: Хелломуи.</span><span class="sxs-lookup"><span data-stu-id="3455b-177">Solution Name: HelloMUI.</span></span>
    5.  <span data-ttu-id="3455b-178">Установите флажок Создать каталог для решения.</span><span class="sxs-lookup"><span data-stu-id="3455b-178">Select Create directory for solution.</span></span>
    6.  <span data-ttu-id="3455b-179">В мастере приложений Win32 выберите тип приложения по умолчанию: приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="3455b-179">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3455b-180">Настройка потоковой модели проекта:</span><span class="sxs-lookup"><span data-stu-id="3455b-180">Configure the project threading model:</span></span>

    1.  <span data-ttu-id="3455b-181">В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 0, а затем выберите пункт Свойства.</span><span class="sxs-lookup"><span data-stu-id="3455b-181">In the Solution Explorer, right-click the project GuiStep\_0, and then select Properties.</span></span>
    2.  <span data-ttu-id="3455b-182">В диалоговом окне страницы свойств проекта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3455b-182">In the project Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3455b-183">В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3455b-183">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3455b-184">В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3455b-184">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3455b-185">Замените содержимое Гуистеп \_ 0. cpp следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="3455b-185">Replace the contents of GuiStep\_0.cpp with the following code:</span></span>
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

    

4.  <span data-ttu-id="3455b-186">Выполните сборку и запуск приложения.</span><span class="sxs-lookup"><span data-stu-id="3455b-186">Build and run the application.</span></span>

<span data-ttu-id="3455b-187">Простой исходный код, приведенный выше, делает упрощенный вариант разработки с жестким кодированием или внедрением, который будет видеть пользователь, в данном случае текст "Hello MUI".</span><span class="sxs-lookup"><span data-stu-id="3455b-187">The straightforward source code above makes the simplistic design choice of hard-coding, or embedding, all the output the user will see—in this case the text "Hello MUI".</span></span> <span data-ttu-id="3455b-188">Этот вариант ограничивает служебную программу приложения для пользователей, которые не распознают слово "Hello" на английском языке.</span><span class="sxs-lookup"><span data-stu-id="3455b-188">This choice limits the utility of the application for users who don't recognize the English word "Hello."</span></span> <span data-ttu-id="3455b-189">Поскольку многоязыковой интерфейс пользователя является словарем на основе технологий, для этого руководства предполагается, что строка остается "MUI" для всех языков.</span><span class="sxs-lookup"><span data-stu-id="3455b-189">Because MUI is a technology-based English acronym, it is assumed for this tutorial that the string remains "MUI" for all languages.</span></span>

## <a name="step-1-implementing-the-basic-resource-module"></a><span data-ttu-id="3455b-190">Шаг 1. Реализация базового модуля ресурсов</span><span class="sxs-lookup"><span data-stu-id="3455b-190">Step 1: Implementing the Basic Resource Module</span></span>

<span data-ttu-id="3455b-191">Microsoft Win32 обладает большой доступностью, позволяющей разработчикам приложений отделить данные ресурсов пользовательского интерфейса от исходного кода приложения.</span><span class="sxs-lookup"><span data-stu-id="3455b-191">Microsoft Win32 has long exposed the capability for application developers to separate their UI resource data from application source code.</span></span> <span data-ttu-id="3455b-192">Это разделение имеет форму модели ресурсов Win32, в которой строки, точечные рисунки, значки, сообщения и другие элементы, обычно отображаемые для пользователя, упаковываются в отдельный раздел исполняемого файла, отделенный от исполняемого кода.</span><span class="sxs-lookup"><span data-stu-id="3455b-192">This separation comes in the form of the Win32 resource model, in which strings, bitmaps, icons, messages and other items normally displayed to a user are packaged into a distinct section of the executable, separated from executable code.</span></span>

<span data-ttu-id="3455b-193">Чтобы проиллюстрировать это разделение между исполняемым кодом и упаковкой данных ресурса, на этом этапе учебник помещает ранее жестко запрограммированную строку "Hello" (ресурс "en-US") в раздел ресурсов модуля DLL в \_ проекте хелломодуле en \_ US.</span><span class="sxs-lookup"><span data-stu-id="3455b-193">To illustrate this separation between executable code and resource data packaging, in this step the tutorial places the previously hard-coded "Hello" string (the "en-US" resource) into the resource section of a DLL module in the HelloModule\_en\_us project.</span></span>

<span data-ttu-id="3455b-194">Эта библиотека DLL Win32 также может содержать исполняемые функции типа библиотеки (как любая другая библиотека DLL).</span><span class="sxs-lookup"><span data-stu-id="3455b-194">This Win32 DLL could also contain library type executable functionality (as any other DLL might).</span></span> <span data-ttu-id="3455b-195">Но чтобы сосредоточиться на аспектах, связанных с ресурсами Win32, мы оставляем код DLL времени выполнения создана в DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="3455b-195">But to help focus on the Win32 resource-related aspects, we leave the run-time DLL code stubbed out in dllmain.cpp.</span></span> <span data-ttu-id="3455b-196">В последующих разделах этого руководства мы будем использовать собранные здесь данные о ресурсах Хелломодуле, а также представим соответствующий код среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="3455b-196">Subsequent sections of this tutorial make use of the HelloModule resource data being built here and also present appropriate runtime code.</span></span>

<span data-ttu-id="3455b-197">Чтобы создать модуль ресурсов Win32, начните с создания библиотеки DLL с помощью функции создана out.</span><span class="sxs-lookup"><span data-stu-id="3455b-197">To construct a Win32 resource module, start by creating a DLL with a stubbed out dllmain:</span></span>

1.  <span data-ttu-id="3455b-198">Добавьте новый проект в решение Хелломуи:</span><span class="sxs-lookup"><span data-stu-id="3455b-198">Add a new project to the HelloMUI solution:</span></span>

    1.  <span data-ttu-id="3455b-199">В меню Файл выберите команду Добавить, а затем — новый проект.</span><span class="sxs-lookup"><span data-stu-id="3455b-199">From the File menu, select Add, and then New Project.</span></span>
    2.  <span data-ttu-id="3455b-200">Тип проекта: проект Win32.</span><span class="sxs-lookup"><span data-stu-id="3455b-200">Project type: Win32 Project.</span></span>
    3.  <span data-ttu-id="3455b-201">Имя: Хелломодуле \_ en \_ US.</span><span class="sxs-lookup"><span data-stu-id="3455b-201">Name: HelloModule\_en\_us.</span></span>
    4.  <span data-ttu-id="3455b-202">Расположение: *прожектрутдиректори* \\ хелломуи.</span><span class="sxs-lookup"><span data-stu-id="3455b-202">Location: *ProjectRootDirectory*\\HelloMUI.</span></span>
    5.  <span data-ttu-id="3455b-203">В мастере приложений Win32 выберите тип приложения: DLL.</span><span class="sxs-lookup"><span data-stu-id="3455b-203">In the Win32 Application Wizard, select Application type: DLL.</span></span>

2.  <span data-ttu-id="3455b-204">Настройка потоковой модели этого проекта:</span><span class="sxs-lookup"><span data-stu-id="3455b-204">Configure this project's threading model:</span></span>

    1.  <span data-ttu-id="3455b-205">В обозреватель решений щелкните правой кнопкой мыши проект Хелломодуле \_ en \_ US и выберите пункт Свойства.</span><span class="sxs-lookup"><span data-stu-id="3455b-205">In the Solution Explorer, right-click the project HelloModule\_en\_us and select Properties.</span></span>
    2.  <span data-ttu-id="3455b-206">В диалоговом окне страницы свойств проекта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3455b-206">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3455b-207">В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3455b-207">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3455b-208">В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3455b-208">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3455b-209">Изучите DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="3455b-209">Examine dllmain.cpp.</span></span> <span data-ttu-id="3455b-210">(Может потребоваться добавить нессылки \_ на Макросы параметров для созданного кода, как здесь, чтобы включить его для компиляции на уровне предупреждений 4.)</span><span class="sxs-lookup"><span data-stu-id="3455b-210">(You may want to add the UNREFERENCED\_PARAMETER macros to the generated code, as we have here, to enable it to compile at warning level 4.)</span></span>
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

    

4.  <span data-ttu-id="3455b-211">Добавьте в проект файл определения ресурса Хелломодуле. rc:</span><span class="sxs-lookup"><span data-stu-id="3455b-211">Add a resource-definition file HelloModule.rc to the project:</span></span>

    1.  <span data-ttu-id="3455b-212">В проекте Хелломодуле \_ en \_ US щелкните правой кнопкой мыши папку файлы ресурсов и выберите Добавить, а затем щелкните новый элемент.</span><span class="sxs-lookup"><span data-stu-id="3455b-212">Under the project HelloModule\_en\_us, right-click the Resource Files folder, and select Add, and then select New Item.</span></span>
    2.  <span data-ttu-id="3455b-213">В диалоговом окне Добавление нового элемента выберите следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="3455b-213">In the Add New Item dialog box, choose the following:</span></span>

        1.  <span data-ttu-id="3455b-214">Категории: в разделе Visual C++ выберите ресурс, а затем в разделе "установленные шаблоны Visual Studio" выберите файл ресурсов (. RC).</span><span class="sxs-lookup"><span data-stu-id="3455b-214">Categories: Under Visual C++ select Resource, and then under "Visual Studio installed templates" select Resource File (.rc).</span></span>
        2.  <span data-ttu-id="3455b-215">Имя: Хелломодуле.</span><span class="sxs-lookup"><span data-stu-id="3455b-215">Name: HelloModule.</span></span>
        3.  <span data-ttu-id="3455b-216">Расположение: примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3455b-216">Location: accept the default.</span></span>
        4.  <span data-ttu-id="3455b-217">Нажмите кнопку "Добавить".</span><span class="sxs-lookup"><span data-stu-id="3455b-217">Click Add.</span></span>

    3.  <span data-ttu-id="3455b-218">Укажите, что новый файл Хелломодуле. RC должен быть сохранен в Юникоде:</span><span class="sxs-lookup"><span data-stu-id="3455b-218">Specify that the new HelloModule.rc file is to be saved as Unicode:</span></span>

        1.  <span data-ttu-id="3455b-219">В обозреватель решений щелкните правой кнопкой мыши Хелломодуле. RC и выберите Просмотреть код.</span><span class="sxs-lookup"><span data-stu-id="3455b-219">In the Solution Explorer, right-click HelloModule.rc, and select View Code.</span></span>
        2.  <span data-ttu-id="3455b-220">Если появится сообщение о том, что файл уже открыт, и запросит, нужно ли его закрыть, нажмите кнопку Да.</span><span class="sxs-lookup"><span data-stu-id="3455b-220">If you see a message that tells you that the file is already open, and asks whether you want to close it, click Yes.</span></span>
        3.  <span data-ttu-id="3455b-221">Чтобы файл отображался как текст, выберите файл выбора меню, а затем дополнительные параметры сохранения.</span><span class="sxs-lookup"><span data-stu-id="3455b-221">With the file displayed as text, make the menu selection File and then Advanced Save Options.</span></span>
        4.  <span data-ttu-id="3455b-222">В разделе кодировка укажите Юникод-кодовую страницу 1200.</span><span class="sxs-lookup"><span data-stu-id="3455b-222">Under Encoding, specify Unicode - Codepage 1200.</span></span>
        5.  <span data-ttu-id="3455b-223">Щелкните ОК.</span><span class="sxs-lookup"><span data-stu-id="3455b-223">Click OK.</span></span>
        6.  <span data-ttu-id="3455b-224">Сохраните и закройте Хелломодуле. rc.</span><span class="sxs-lookup"><span data-stu-id="3455b-224">Save and close HelloModule.rc.</span></span>

    4.  <span data-ttu-id="3455b-225">Добавьте таблицу строк, содержащую строку "Hello":</span><span class="sxs-lookup"><span data-stu-id="3455b-225">Add a string table containing the "Hello" string:</span></span>

        1.  <span data-ttu-id="3455b-226">В представление ресурсов щелкните правой кнопкой мыши Хелломодуле. RC и выберите Добавить ресурс.</span><span class="sxs-lookup"><span data-stu-id="3455b-226">In the Resource View, right-click HelloModule.rc and select Add Resource.</span></span>
        2.  <span data-ttu-id="3455b-227">Выберите таблицу строк.</span><span class="sxs-lookup"><span data-stu-id="3455b-227">Select String Table.</span></span>
        3.  <span data-ttu-id="3455b-228">Нажмите кнопку New (Создать).</span><span class="sxs-lookup"><span data-stu-id="3455b-228">Click New.</span></span>
        4.  <span data-ttu-id="3455b-229">Добавьте строку в таблицу строк:</span><span class="sxs-lookup"><span data-stu-id="3455b-229">Add a string to the String Table:</span></span>

            1.  <span data-ttu-id="3455b-230">Идентификатор: HELLO \_ MUI \_ str \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3455b-230">ID: HELLO\_MUI\_STR\_0.</span></span>
            2.  <span data-ttu-id="3455b-231">Значение: 0.</span><span class="sxs-lookup"><span data-stu-id="3455b-231">Value: 0.</span></span>
            3.  <span data-ttu-id="3455b-232">Заголовок: Привет.</span><span class="sxs-lookup"><span data-stu-id="3455b-232">Caption: Hello.</span></span>

        <span data-ttu-id="3455b-233">Если просмотреть Хелломодуле. RC как текст, вы увидите различные части исходного кода, относящегося к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="3455b-233">If you view HelloModule.rc as text now, you will see various pieces of resource-specific source code.</span></span> <span data-ttu-id="3455b-234">Самым большим интересом является раздел, описывающий строку "Hello":</span><span class="sxs-lookup"><span data-stu-id="3455b-234">The one of greatest interest is the section that describes the "Hello" string:</span></span>

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

        

        <span data-ttu-id="3455b-235">Эта строка "Hello" — это ресурс, который должен быть локализован (т. е. переведен) на каждый язык, поддерживаемый приложением надеется.</span><span class="sxs-lookup"><span data-stu-id="3455b-235">This "Hello" string is the resource that needs to be localized (that is, translated) into every language that the application hopes to support.</span></span> <span data-ttu-id="3455b-236">Например, Хелломодуле \_ TA \_ в проекте (который вы создадите на следующем шаге) будет содержать собственную локализованную версию хелломодуле. RC для «TA-in»:</span><span class="sxs-lookup"><span data-stu-id="3455b-236">For example, the HelloModule\_ta\_in project (which you will create in the next step) will contain its own localized version of HelloModule.rc for "ta-IN":</span></span>

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

        

    5.  <span data-ttu-id="3455b-237">Создайте проект Хелломодуле \_ en \_ US, чтобы убедиться в отсутствии ошибок.</span><span class="sxs-lookup"><span data-stu-id="3455b-237">Build the HelloModule\_en\_us project to be sure there are no errors.</span></span>

5.  <span data-ttu-id="3455b-238">Создавайте шесть проектов в решении Хелломуи (или столько из них, сколько нужно), чтобы создать шесть дополнительных библиотек ресурсов для дополнительных языков.</span><span class="sxs-lookup"><span data-stu-id="3455b-238">Create six more projects in the HelloMUI solution (or as many of them as you wish) to create six more resource DLLs for additional languages.</span></span> <span data-ttu-id="3455b-239">Используйте значения из этой таблицы:</span><span class="sxs-lookup"><span data-stu-id="3455b-239">Use the values in this table:</span></span>

    | <span data-ttu-id="3455b-240">Имя проекта</span><span class="sxs-lookup"><span data-stu-id="3455b-240">Project name</span></span>        | <span data-ttu-id="3455b-241">Имя RC-файла</span><span class="sxs-lookup"><span data-stu-id="3455b-241">Name of .rc file</span></span> | <span data-ttu-id="3455b-242">Идентификатор строки</span><span class="sxs-lookup"><span data-stu-id="3455b-242">String ID</span></span>          | <span data-ttu-id="3455b-243">Строковое значение</span><span class="sxs-lookup"><span data-stu-id="3455b-243">String value</span></span> | <span data-ttu-id="3455b-244">Заголовок строки</span><span class="sxs-lookup"><span data-stu-id="3455b-244">String caption</span></span> |
    |---------------------|------------------|--------------------|--------------|----------------|
    | <span data-ttu-id="3455b-245">Хелломодуле \_ де \_ de</span><span class="sxs-lookup"><span data-stu-id="3455b-245">HelloModule\_de\_de</span></span> | <span data-ttu-id="3455b-246">хелломодуле</span><span class="sxs-lookup"><span data-stu-id="3455b-246">HelloModule</span></span>      | <span data-ttu-id="3455b-247">HELLO \_ MUI \_ str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3455b-247">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3455b-248">0</span><span class="sxs-lookup"><span data-stu-id="3455b-248">0</span></span>            | <span data-ttu-id="3455b-249">халло</span><span class="sxs-lookup"><span data-stu-id="3455b-249">Hallo</span></span>          |
    | <span data-ttu-id="3455b-250">Хелломодуле \_ ES \_</span><span class="sxs-lookup"><span data-stu-id="3455b-250">HelloModule\_es\_es</span></span> | <span data-ttu-id="3455b-251">хелломодуле</span><span class="sxs-lookup"><span data-stu-id="3455b-251">HelloModule</span></span>      | <span data-ttu-id="3455b-252">HELLO \_ MUI \_ str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3455b-252">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3455b-253">0</span><span class="sxs-lookup"><span data-stu-id="3455b-253">0</span></span>            | <span data-ttu-id="3455b-254">Hol</span><span class="sxs-lookup"><span data-stu-id="3455b-254">Hola</span></span>           |
    | <span data-ttu-id="3455b-255">Хелломодуле \_ fr \_ fr</span><span class="sxs-lookup"><span data-stu-id="3455b-255">HelloModule\_fr\_fr</span></span> | <span data-ttu-id="3455b-256">хелломодуле</span><span class="sxs-lookup"><span data-stu-id="3455b-256">HelloModule</span></span>      | <span data-ttu-id="3455b-257">HELLO \_ MUI \_ str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3455b-257">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3455b-258">0</span><span class="sxs-lookup"><span data-stu-id="3455b-258">0</span></span>            | <span data-ttu-id="3455b-259">Bonjour</span><span class="sxs-lookup"><span data-stu-id="3455b-259">Bonjour</span></span>        |
    | <span data-ttu-id="3455b-260">Хелломодуле \_ Hi \_ in</span><span class="sxs-lookup"><span data-stu-id="3455b-260">HelloModule\_hi\_in</span></span> | <span data-ttu-id="3455b-261">хелломодуле</span><span class="sxs-lookup"><span data-stu-id="3455b-261">HelloModule</span></span>      | <span data-ttu-id="3455b-262">HELLO \_ MUI \_ str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3455b-262">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3455b-263">0</span><span class="sxs-lookup"><span data-stu-id="3455b-263">0</span></span>            | <span data-ttu-id="3455b-264">नमस्</span><span class="sxs-lookup"><span data-stu-id="3455b-264">नमस्</span></span>           |
    | <span data-ttu-id="3455b-265">Хелломодуле \_ ru \_</span><span class="sxs-lookup"><span data-stu-id="3455b-265">HelloModule\_ru\_ru</span></span> | <span data-ttu-id="3455b-266">хелломодуле</span><span class="sxs-lookup"><span data-stu-id="3455b-266">HelloModule</span></span>      | <span data-ttu-id="3455b-267">HELLO \_ MUI \_ str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3455b-267">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3455b-268">0</span><span class="sxs-lookup"><span data-stu-id="3455b-268">0</span></span>            | <span data-ttu-id="3455b-269">здравствуйте</span><span class="sxs-lookup"><span data-stu-id="3455b-269">Здравствуйте</span></span>   |
    | <span data-ttu-id="3455b-270">Хелломодуле \_ TA \_ в</span><span class="sxs-lookup"><span data-stu-id="3455b-270">HelloModule\_ta\_in</span></span> | <span data-ttu-id="3455b-271">хелломодуле</span><span class="sxs-lookup"><span data-stu-id="3455b-271">HelloModule</span></span>      | <span data-ttu-id="3455b-272">HELLO \_ MUI \_ str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3455b-272">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3455b-273">0</span><span class="sxs-lookup"><span data-stu-id="3455b-273">0</span></span>            | <span data-ttu-id="3455b-274">வணக்கம்</span><span class="sxs-lookup"><span data-stu-id="3455b-274">வணக்கம்</span></span>        |

    

     

<span data-ttu-id="3455b-275">Дополнительные сведения о структуре и синтаксисе файла. RC см. в разделе [Общие сведения о файлах ресурсов](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="3455b-275">For more about .rc file structure and syntax, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

## <a name="step-2-building-the-basic-resource-module"></a><span data-ttu-id="3455b-276">Шаг 2. Создание базового модуля ресурсов</span><span class="sxs-lookup"><span data-stu-id="3455b-276">Step 2: Building the Basic Resource Module</span></span>

<span data-ttu-id="3455b-277">При использовании предыдущих моделей ресурсов создание одного из семи проектов Хелломодуле приведет к появлению семи отдельных библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="3455b-277">Using previous resource models, building any one of the seven HelloModule projects would result in seven separate DLLs.</span></span> <span data-ttu-id="3455b-278">Каждая библиотека DLL будет содержать раздел ресурсов с одной строкой, локализованной для соответствующего языка.</span><span class="sxs-lookup"><span data-stu-id="3455b-278">Each DLL would contain a resource section with a single string localized into the appropriate language.</span></span> <span data-ttu-id="3455b-279">Хотя это и подходит для модели ресурсов Win32 с предысторией, эта схема не использует преимущества многоязыкового интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="3455b-279">Although appropriate for the historic Win32 resource model, this design does not take advantage of MUI.</span></span>

<span data-ttu-id="3455b-280">В пакете SDK для Windows Vista и более поздних версиях MUI обеспечивает возможность разделения исполняемых файлов на исходный код и локализуемые модули содержимого.</span><span class="sxs-lookup"><span data-stu-id="3455b-280">In the Windows Vista SDK and later, MUI provides the ability to split executables into source code and localizable content modules.</span></span> <span data-ttu-id="3455b-281">С дополнительной настройкой, описанной далее на шаге 5, приложения могут быть включены для поддержки нескольких языковых версий до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3455b-281">With the additional customization that is covered later in Step 5, applications can be enabled for multi-lingual support to run on versions prior to Windows Vista.</span></span>

<span data-ttu-id="3455b-282">Основные механизмы, доступные для разбиения ресурсов из исполняемого кода, начиная с Windows Vista,:</span><span class="sxs-lookup"><span data-stu-id="3455b-282">The primary mechanisms available to split resources from executable code, starting with Windows Vista, are:</span></span>

-   <span data-ttu-id="3455b-283">С помощью rc.exe (компилятора RC) с конкретными переключателями или</span><span class="sxs-lookup"><span data-stu-id="3455b-283">Using rc.exe (the RC Compiler) with specific switches, or</span></span>
-   <span data-ttu-id="3455b-284">Использование инструмента разбиения стилей после сборки с именем muirct.exe.</span><span class="sxs-lookup"><span data-stu-id="3455b-284">Using a post-build style splitting tool named muirct.exe.</span></span>

<span data-ttu-id="3455b-285">Дополнительные сведения см. в разделе [Служебные программы](resource-utilities.md) .</span><span class="sxs-lookup"><span data-stu-id="3455b-285">See [Resource Utilities](resource-utilities.md) for more information.</span></span>

<span data-ttu-id="3455b-286">Для простоты в этом руководстве используется muirct.exe для разделения исполняемого файла "Hello MUI".</span><span class="sxs-lookup"><span data-stu-id="3455b-286">For the sake of simplicity, this tutorial uses muirct.exe to split the "Hello MUI" executable.</span></span>

### <a name="splitting-the-various-language-resource-modules-an-overview"></a><span data-ttu-id="3455b-287">Разделение различных модулей языковых ресурсов: обзор</span><span class="sxs-lookup"><span data-stu-id="3455b-287">Splitting the Various Language Resource Modules: An Overview</span></span>

<span data-ttu-id="3455b-288">Многокомпонентный процесс состоит в разделении библиотек DLL на один исполняемый HelloModule.dll, а также HelloModule.dll. MUI для каждого из семи поддерживаемых языков в рамках этого руководства.</span><span class="sxs-lookup"><span data-stu-id="3455b-288">A multi-part process is involved in splitting the DLLs into one executable HelloModule.dll, plus a HelloModule.dll.mui for each of the seven supported languages within this tutorial.</span></span> <span data-ttu-id="3455b-289">В этом обзоре описываются необходимые действия. в следующем разделе представлен командный файл, который выполняет эти действия.</span><span class="sxs-lookup"><span data-stu-id="3455b-289">This overview describes the required steps; the next section presents a command file that performs those steps.</span></span>

<span data-ttu-id="3455b-290">Сначала разделите модуль HelloModule.dll, поддерживающий только английский язык, с помощью команды:</span><span class="sxs-lookup"><span data-stu-id="3455b-290">First, split the English-only HelloModule.dll module by using the command:</span></span>


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



<span data-ttu-id="3455b-291">В командной строке выше используется файл конфигурации Дореверсемуилок. ркконфиг.</span><span class="sxs-lookup"><span data-stu-id="3455b-291">The command line above uses the configuration file DoReverseMuiLoc.rcconfig.</span></span> <span data-ttu-id="3455b-292">Этот тип файла конфигурации обычно используется muirct.exe для разделения ресурсов между DLL-библиотекой, не зависящей от языка (LN), и файлами MUI, зависящими от языка.</span><span class="sxs-lookup"><span data-stu-id="3455b-292">This type of configuration file is typically used by muirct.exe to split resources between the language-neutral (LN) DLL and the language-dependent .mui files.</span></span> <span data-ttu-id="3455b-293">В этом случае XML-файл Дореверсемуилок. ркконфиг (перечисленный в следующем разделе) указывает на множество типов ресурсов, но все они попадают в категорию файлов «localizedResources» или «MUI», и в категории, не зависящей от языка, отсутствуют ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3455b-293">In this case, the DoReverseMuiLoc.rcconfig xml file (listed in the next section) indicates many resource types, but they all fall into the "localizedResources" or .mui file category, and there are no resources in the language-neutral category.</span></span> <span data-ttu-id="3455b-294">Дополнительные сведения о подготовке файла конфигурации ресурсов см. в разделе [Подготовка файла конфигурации ресурса](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="3455b-294">For more information about how to prepare a resource configuration file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="3455b-295">Помимо создания файла HelloModule.dll. MUI, содержащего строку "Hello" на английском языке, muirct.exe также внедряет ресурс MUI в модуль HelloModule.dll во время разделения.</span><span class="sxs-lookup"><span data-stu-id="3455b-295">In addition to creating a HelloModule.dll.mui file which contains the English string "Hello", muirct.exe also embeds a MUI resource into the HelloModule.dll module during the splitting.</span></span> <span data-ttu-id="3455b-296">Чтобы обеспечить правильную загрузку во время выполнения соответствующих ресурсов из модулей HelloModule.dll. MUI для конкретного языка, каждый MUI-файл должен быть исправлен в соответствии с контрольными суммами в базовом модуле, нейтральном к языку LN.</span><span class="sxs-lookup"><span data-stu-id="3455b-296">In order to properly load at run-time the appropriate resources from the language-specific HelloModule.dll.mui modules, each .mui file must have its checksums fixed-up to match the checksums in the baseline language-neutral LN module.</span></span> <span data-ttu-id="3455b-297">Это делается с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="3455b-297">This is done by a command such as:</span></span>


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



<span data-ttu-id="3455b-298">Аналогичным образом, muirct.exe вызывается для создания файла HelloModule.dll. MUI для каждого из других языков.</span><span class="sxs-lookup"><span data-stu-id="3455b-298">Similarly, muirct.exe is invoked to create a HelloModule.dll.mui file for each of the other languages.</span></span> <span data-ttu-id="3455b-299">Однако в таких случаях библиотека DLL, не зависящая от языка, отбрасывается, так как потребуется только первая созданная.</span><span class="sxs-lookup"><span data-stu-id="3455b-299">However, in those cases the language-neutral DLL is discarded, as only the first one created will be needed.</span></span> <span data-ttu-id="3455b-300">Команды, которые обрабатывают ресурсы для испанского и французского языков, выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3455b-300">The commands that process the Spanish and French resources look like this:</span></span>


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



<span data-ttu-id="3455b-301">Одним из наиболее важных моментов, которые следует заметить в muirct.exe командных строк, является то, что для указания идентификатора целевого языка используется флаг-x.</span><span class="sxs-lookup"><span data-stu-id="3455b-301">One of the most important things to notice in the muirct.exe command lines above is that the -x flag is used to specify a target language ID.</span></span> <span data-ttu-id="3455b-302">Значение, указанное для muirct.exe, отличается для каждого зависящего от языка HelloModule.dll модуля.</span><span class="sxs-lookup"><span data-stu-id="3455b-302">The value provided to muirct.exe is different for each language-specific HelloModule.dll module.</span></span> <span data-ttu-id="3455b-303">Это значение языка является центральным и используется muirct.exe для соответствующей пометки MUI-файла во время разделения.</span><span class="sxs-lookup"><span data-stu-id="3455b-303">This language value is central and is used by muirct.exe to appropriately mark the .mui file during splitting.</span></span> <span data-ttu-id="3455b-304">Неверное значение приводит к сбоям при загрузке ресурсов для этого конкретного файла MUI во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3455b-304">An incorrect value produces resource loading failures for that particular .mui file at run-time.</span></span> <span data-ttu-id="3455b-305">Дополнительные сведения о сопоставлении имени языка с LCID см. в разделе [константы и строки идентификатора языка](language-identifier-constants-and-strings.md) .</span><span class="sxs-lookup"><span data-stu-id="3455b-305">See [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md) for more details on mapping language name to LCID.</span></span>

<span data-ttu-id="3455b-306">Каждый разделенный MUI-файл помещается в каталог, соответствующий имени языка, непосредственно под каталогом, в котором будет размещаться HelloModule.dll, не зависящее от языка.</span><span class="sxs-lookup"><span data-stu-id="3455b-306">Each split .mui file ends up being placed into a directory corresponding to its language name, immediately underneath the directory in which the language-neutral HelloModule.dll will reside.</span></span> <span data-ttu-id="3455b-307">Дополнительные сведения о размещении файлов MUI см. в разделе [развертывание приложения](application-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3455b-307">For more about .mui file placement, see [Application Deployment](application-deployment.md).</span></span>

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a><span data-ttu-id="3455b-308">Разделение различных модулей языковых ресурсов: создание файлов</span><span class="sxs-lookup"><span data-stu-id="3455b-308">Splitting the Various Language Resource Modules: Creating the Files</span></span>

<span data-ttu-id="3455b-309">В этом руководстве вы создадите командный файл, содержащий команды для разделения различных библиотек DLL, и вызываете их вручную.</span><span class="sxs-lookup"><span data-stu-id="3455b-309">For this tutorial you create a command file containing the commands to split the various DLLs, and you invoke it manually.</span></span> <span data-ttu-id="3455b-310">Обратите внимание, что в реальной работе по разработке можно уменьшить вероятность ошибок сборки, включив эти команды в качестве событий до или после сборки в решение Хелломуи, но это выходит за рамки данного руководства.</span><span class="sxs-lookup"><span data-stu-id="3455b-310">Note that in actual development work, you could reduce the potential for build errors by including these commands as pre-build or post-build events in the HelloMUI solution, but that is beyond the scope of this tutorial.</span></span>

<span data-ttu-id="3455b-311">Создайте файлы для отладочной сборки:</span><span class="sxs-lookup"><span data-stu-id="3455b-311">Create the files for the debug build:</span></span>

1.  <span data-ttu-id="3455b-312">Создайте командный файл Дореверсемуилок. cmd, содержащий следующие команды:</span><span class="sxs-lookup"><span data-stu-id="3455b-312">Create a command file DoReverseMuiLoc.cmd containing the following commands:</span></span>
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

    

2.  <span data-ttu-id="3455b-313">Создайте XML-файл Дореверсемуилок. ркконфиг, содержащий следующие строки:</span><span class="sxs-lookup"><span data-stu-id="3455b-313">Create an xml file DoReverseMuiLoc.rcconfig containing the following lines:</span></span>
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

    

3.  <span data-ttu-id="3455b-314">Скопируйте Дореверсемуилок. cmd и Дореверсемуилок. ркконфиг в *прожектрутдиректори* \\ хелломуи \\ Debug.</span><span class="sxs-lookup"><span data-stu-id="3455b-314">Copy DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig to *ProjectRootDirectory*\\HelloMUI\\Debug.</span></span>
4.  <span data-ttu-id="3455b-315">Откройте командную строку Visual Studio 2008 и перейдите в каталог Debug.</span><span class="sxs-lookup"><span data-stu-id="3455b-315">Open the Visual Studio 2008 command prompt and navigate to the Debug directory.</span></span>
5.  <span data-ttu-id="3455b-316">Запустите Дореверсемуилок. cmd.</span><span class="sxs-lookup"><span data-stu-id="3455b-316">Run DoReverseMuiLoc.cmd.</span></span>

<span data-ttu-id="3455b-317">При создании сборки выпуска вы копируете те же файлы Дореверсемуилок. cmd и Дореверсемуилок. ркконфиг в каталог выпуска и запускаете командный файл там.</span><span class="sxs-lookup"><span data-stu-id="3455b-317">When you create a release build, you copy the same DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig files to the Release directory and run the command file there.</span></span>

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a><span data-ttu-id="3455b-318">Шаг 3. Создание Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3455b-318">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>

<span data-ttu-id="3455b-319">Основываясь на первом0.exe Гуистеп примере с жестко запрограммированным \_ , можно расширить круг пользователей приложения на нескольких языках, выбрав внедрение модели ресурсов Win32.</span><span class="sxs-lookup"><span data-stu-id="3455b-319">Building on the initial hard-coded GuiStep\_0.exe example from above, you could extend the reach of the application to multiple language users by choosing to incorporate the Win32 resource model.</span></span> <span data-ttu-id="3455b-320">Новый код времени выполнения, представленный на этом шаге, включает логику загрузки модуля ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) и строки получения ([**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa)).</span><span class="sxs-lookup"><span data-stu-id="3455b-320">The new run-time code presented in this step includes the module loading ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) and string retrieval ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)) logic.</span></span>

1.  <span data-ttu-id="3455b-321">Добавьте новый проект в решение Хелломуи (с помощью файла выбора меню, добавьте и новый проект) со следующими параметрами и значениями:</span><span class="sxs-lookup"><span data-stu-id="3455b-321">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="3455b-322">Тип проекта: проект Win32.</span><span class="sxs-lookup"><span data-stu-id="3455b-322">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="3455b-323">Имя: Гуистеп \_ 1.</span><span class="sxs-lookup"><span data-stu-id="3455b-323">Name: GuiStep\_1.</span></span>
    3.  <span data-ttu-id="3455b-324">Расположение: примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3455b-324">Location: accept the default.</span></span>
    4.  <span data-ttu-id="3455b-325">В мастере приложений Win32 выберите тип приложения по умолчанию: приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="3455b-325">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3455b-326">Настройте этот проект для запуска в Visual Studio и настройте его потоковую модель:</span><span class="sxs-lookup"><span data-stu-id="3455b-326">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="3455b-327">В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 1 и выберите Назначить запускаемым проектом.</span><span class="sxs-lookup"><span data-stu-id="3455b-327">In the Solution Explorer, right-click the project GuiStep\_1 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="3455b-328">Щелкните его правой кнопкой мыши и выберите пункт Свойства.</span><span class="sxs-lookup"><span data-stu-id="3455b-328">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="3455b-329">В диалоговом окне страницы свойств проекта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3455b-329">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3455b-330">В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3455b-330">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3455b-331">В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3455b-331">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3455b-332">Замените содержимое файла Гуистеп \_ 1. cpp следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="3455b-332">Replace the contents of GuiStep\_1.cpp with the following code:</span></span>
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

    

4.  <span data-ttu-id="3455b-333">Выполните сборку и запуск приложения.</span><span class="sxs-lookup"><span data-stu-id="3455b-333">Build and run the application.</span></span> <span data-ttu-id="3455b-334">Выходные данные будут отображаться на языке, выбранном в качестве языка интерфейса компьютера (при условии, что это один из семи созданных нами языков).</span><span class="sxs-lookup"><span data-stu-id="3455b-334">The output will be displayed in the language currently set as the display language of the computer (provided it is one of the seven languages we have built).</span></span>

## <a name="step-4-globalizing-hello-mui"></a><span data-ttu-id="3455b-335">Шаг 4. Глобализация "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3455b-335">Step 4: Globalizing "Hello MUI"</span></span>

<span data-ttu-id="3455b-336">Несмотря на то, что предыдущий пример способен отображать выходные данные на разных языках, он оказывается коротким в нескольких областях.</span><span class="sxs-lookup"><span data-stu-id="3455b-336">Although the previous example is able to display its output in different languages, it falls short in a number of areas.</span></span> <span data-ttu-id="3455b-337">Возможно, наиболее заметным является то, что приложение доступно только в небольшом подмножестве языков по сравнению с самой операционной системой Windows.</span><span class="sxs-lookup"><span data-stu-id="3455b-337">Perhaps the most noticeable is that the application is only available in a small subset of languages when compared to the Windows operating system itself.</span></span> <span data-ttu-id="3455b-338">Если, например, \_ приложение гуистеп 1 из предыдущего шага было установлено в японской версии Windows, ошибки расположения ресурсов будут, скорее всего,.</span><span class="sxs-lookup"><span data-stu-id="3455b-338">If, for example, the GuiStep\_1 application from the previous step were installed on a Japanese build of Windows, resource location failures would be likely.</span></span>

<span data-ttu-id="3455b-339">Для решения этой ситуации у вас есть два основных варианта:</span><span class="sxs-lookup"><span data-stu-id="3455b-339">To address this situation, you have two primary options:</span></span>

-   <span data-ttu-id="3455b-340">Убедитесь, что включены ресурсы на предварительно определенном конечном языке.</span><span class="sxs-lookup"><span data-stu-id="3455b-340">Ensure that resources in a predetermined ultimate fallback language are included.</span></span>
-   <span data-ttu-id="3455b-341">Предоставить конечному пользователю способ настройки языковых настроек из подмножества языков, которые специально поддерживаются приложением.</span><span class="sxs-lookup"><span data-stu-id="3455b-341">Provide a way for the end user to configure their language preferences from among the subset of languages specifically supported by the application.</span></span>

<span data-ttu-id="3455b-342">Из этих вариантов мы настоятельно рекомендуем использовать такой вариант, который обеспечивает базовый язык, и реализуется в этом руководстве путем передачи флага-g в muirct.exe, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="3455b-342">Of these options, the one providing an ultimate fallback language is highly advisable and is implemented in this tutorial by passing the -g flag to muirct.exe, as seen above.</span></span> <span data-ttu-id="3455b-343">Этот флаг сообщает muirct.exe, что для конкретного языка (de-DE/0x0407) имеется конечный язык, связанный с модулем DLL, не зависящим от языка (HelloModule.dll).</span><span class="sxs-lookup"><span data-stu-id="3455b-343">This flag tells muirct.exe to make a specific language (de-DE / 0x0407) the ultimate fallback language associated with the language-neutral dll module (HelloModule.dll).</span></span> <span data-ttu-id="3455b-344">Во время выполнения этот параметр используется в качестве последнего средства для создания текста, отображаемого для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3455b-344">At run-time this parameter is used as a last resort to generate text to display to the user.</span></span> <span data-ttu-id="3455b-345">В случае, если не найден конечный язык и нет доступных ресурсов в двоичном файле, не зависящем от языка, загрузка ресурса завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3455b-345">In the event that an ultimate fallback language is not found and no appropriate resource is available in the language-neutral binary, loading of the resource fails.</span></span> <span data-ttu-id="3455b-346">Поэтому следует тщательно определить сценарии, которые могут возникнуть в приложении, и соответствующим образом спланировать конечный язык.</span><span class="sxs-lookup"><span data-stu-id="3455b-346">Therefore you should carefully determine the scenarios that your application might encounter and plan the ultimate fallback language accordingly.</span></span>

<span data-ttu-id="3455b-347">Другой вариант, позволяющий настроить языковые настройки и загружать ресурсы на основе этой пользовательской иерархии, может значительно повысить удовлетворенность клиента.</span><span class="sxs-lookup"><span data-stu-id="3455b-347">The other option of allowing for configurable language preferences and loading resources based on this user-defined hierarchy can greatly increase customer satisfaction.</span></span> <span data-ttu-id="3455b-348">К сожалению, она также усложняет функциональность, необходимую в приложении.</span><span class="sxs-lookup"><span data-stu-id="3455b-348">Unfortunately, it also complicates the functionality needed within the application.</span></span>

<span data-ttu-id="3455b-349">На этом шаге учебника используется упрощенный механизм работы с текстовыми файлами для включения пользовательской конфигурации языка пользователя.</span><span class="sxs-lookup"><span data-stu-id="3455b-349">This step of the tutorial uses a simplified text file mechanism to enable custom user language configuration.</span></span> <span data-ttu-id="3455b-350">Текстовый файл анализируется во время выполнения приложением, а список проанализированных и проверенных языков используется для создания настраиваемого списка резервных.</span><span class="sxs-lookup"><span data-stu-id="3455b-350">The text file is parsed at run-time by the application, and the parsed and validated language list is used in establishing a custom fallback list.</span></span> <span data-ttu-id="3455b-351">После того как список настраиваемых резервных элементов будет установлен, интерфейсы API Windows будут загружать ресурсы в соответствии с приоритетом языка, указанным в этом списке.</span><span class="sxs-lookup"><span data-stu-id="3455b-351">After the custom fallback list is established, the Windows APIs will load resources according to the language precedence set forth in this list.</span></span> <span data-ttu-id="3455b-352">Оставшаяся часть кода похожа на ту, которая была найдена на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="3455b-352">The remainder of the code is similar to that found in the preceding step.</span></span>

1.  <span data-ttu-id="3455b-353">Добавьте новый проект в решение Хелломуи (с помощью файла выбора меню, добавьте и новый проект) со следующими параметрами и значениями:</span><span class="sxs-lookup"><span data-stu-id="3455b-353">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="3455b-354">Тип проекта: проект Win32.</span><span class="sxs-lookup"><span data-stu-id="3455b-354">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="3455b-355">Имя: Гуистеп \_ 2.</span><span class="sxs-lookup"><span data-stu-id="3455b-355">Name: GuiStep\_2.</span></span>
    3.  <span data-ttu-id="3455b-356">Расположение: примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3455b-356">Location: accept the default.</span></span>
    4.  <span data-ttu-id="3455b-357">В мастере приложений Win32 выберите тип приложения по умолчанию: приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="3455b-357">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3455b-358">Настройте этот проект для запуска в Visual Studio и настройте его потоковую модель:</span><span class="sxs-lookup"><span data-stu-id="3455b-358">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="3455b-359">В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 2 и выберите Назначить запускаемым проектом.</span><span class="sxs-lookup"><span data-stu-id="3455b-359">In the Solution Explorer, right-click the project GuiStep\_2 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="3455b-360">Щелкните его правой кнопкой мыши и выберите пункт Свойства.</span><span class="sxs-lookup"><span data-stu-id="3455b-360">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="3455b-361">В диалоговом окне страницы свойств проекта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3455b-361">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3455b-362">В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3455b-362">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3455b-363">В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3455b-363">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3455b-364">Замените содержимое файла Гуистеп \_ 2. cpp следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="3455b-364">Replace the contents of GuiStep\_2.cpp with the following code:</span></span>
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

    

4.  <span data-ttu-id="3455b-365">Создайте текстовый файл в Юникоде langs.txt содержащий следующую строку:</span><span class="sxs-lookup"><span data-stu-id="3455b-365">Create a Unicode text file langs.txt containing the following line:</span></span>

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > <span data-ttu-id="3455b-366">Не забудьте сохранить файл как Юникод.</span><span class="sxs-lookup"><span data-stu-id="3455b-366">Be sure to save the file as Unicode.</span></span>

     

    <span data-ttu-id="3455b-367">Скопируйте langs.txt в каталог, из которого будет выполняться программа:</span><span class="sxs-lookup"><span data-stu-id="3455b-367">Copy langs.txt to the directory from which the program will run:</span></span>

    -   <span data-ttu-id="3455b-368">При запуске в Visual Studio скопируйте его в *прожектрутдиректори* \\ хелломуи \\ гуистеп \_ 2.</span><span class="sxs-lookup"><span data-stu-id="3455b-368">If running from within Visual Studio, copy it to *ProjectRootDirectory*\\HelloMUI\\GuiStep\_2.</span></span>
    -   <span data-ttu-id="3455b-369">При запуске из проводника Windows скопируйте его в тот же каталог, что и Гуистеп \_2.exe.</span><span class="sxs-lookup"><span data-stu-id="3455b-369">If running from Windows Explorer, copy it to the same directory as GuiStep\_2.exe.</span></span>

5.  <span data-ttu-id="3455b-370">Постройте и запустите проект.</span><span class="sxs-lookup"><span data-stu-id="3455b-370">Build and run the project.</span></span> <span data-ttu-id="3455b-371">Попробуйте изменить langs.txt, чтобы в начале списка появились разные языки.</span><span class="sxs-lookup"><span data-stu-id="3455b-371">Try editing langs.txt so that different languages appear at the front of the list.</span></span>

## <a name="step-5-customizing-hello-mui"></a><span data-ttu-id="3455b-372">Шаг 5. Настройка "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3455b-372">Step 5: Customizing "Hello MUI"</span></span>

<span data-ttu-id="3455b-373">Ряд функций времени выполнения, упомянутых до сих пор в рамках этого учебника, доступен только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3455b-373">A number of the run-time features mentioned so far within this tutorial are available only on Windows Vista and later.</span></span> <span data-ttu-id="3455b-374">Вы можете повторно использовать усилия, которые были потрачены на локализацию и разделение ресурсов, делая работу приложения более ранними версиями операционных систем Windows, например Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3455b-374">You may wish to re-use the effort invested in localizing and splitting resources by making the application work on downlevel Windows operating system versions, such as Windows XP.</span></span> <span data-ttu-id="3455b-375">Этот процесс включает в себя настройку предыдущего примера в двух ключевых областях:</span><span class="sxs-lookup"><span data-stu-id="3455b-375">This process involves adjusting the previous example in two key areas:</span></span>

-   <span data-ttu-id="3455b-376">Функции загрузки ресурсов, предшествующие Windows Vista (например, [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**лоадикон**](/windows/win32/api/winuser/nf-winuser-loadicona), [**лоадбитмап**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)и др.), не поддерживают MUI.</span><span class="sxs-lookup"><span data-stu-id="3455b-376">The pre-Windows Vista resource loading functions (such as [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), and others) are non-MUI aware.</span></span> <span data-ttu-id="3455b-377">Приложения, поставляемые с разделенными ресурсами (LN и MUI Files), должны загружать модули ресурсов с помощью одной из следующих двух функций:</span><span class="sxs-lookup"><span data-stu-id="3455b-377">Applications that ship with split resources (LN and .mui files) must load resource modules using one of these two functions:</span></span>

    -   <span data-ttu-id="3455b-378">Если приложение должно запускаться только в Windows Vista и более поздних версиях, необходимо загрузить модули ресурсов с помощью [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="3455b-378">If the application is to be run only on Windows Vista and later, it should load resource modules with [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>
    -   <span data-ttu-id="3455b-379">Если приложение должно выполняться в версиях до Windows Vista, а также в Windows Vista или более поздней версии, необходимо использовать [**лоадмуилибрари**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), который представляет собой конкретную функцию нижнего уровня, предоставляемую в пакете SDK для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3455b-379">If the application is to be run on versions prior to Windows Vista, as well as Windows Vista or later, it must use [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), which is a specific downlevel function provided in the Windows 7 SDK.</span></span>

-   <span data-ttu-id="3455b-380">Поддержка управления языками и порядками отката языка, предлагаемая в версиях операционных систем Windows, предшествующих Windows Vista, существенно отличается от Windows Vista и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="3455b-380">The language management and language fallback order support offered in pre-Windows Vista versions of the Windows operating system differs significantly from that in Windows Vista and later.</span></span> <span data-ttu-id="3455b-381">По этой причине приложения, которые позволяют выполнять настраиваемые пользователем действия языка, должны настраивать методы управления языками:</span><span class="sxs-lookup"><span data-stu-id="3455b-381">For this reason, applications that allow user-configured language fallback must adjust their language management practices:</span></span>

    -   <span data-ttu-id="3455b-382">Если приложение должно выполняться только в Windows Vista и более поздних версиях, установка списка языков с помощью [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) достаточно велика.</span><span class="sxs-lookup"><span data-stu-id="3455b-382">If the application is to be run only on Windows Vista and later, setting the language list using [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) is sufficient.</span></span>
    -   <span data-ttu-id="3455b-383">Если приложение должно выполняться во всех версиях Windows, необходимо создать код, который будет выполняться на платформах предыдущих версий для прохода по пользовательскому списку языков и проверки требуемого модуля ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3455b-383">If the application is to be run on all Windows versions, code must be constructed that will run on downlevel platforms to iterate through the user configured language list and probe for the desired resource module.</span></span> <span data-ttu-id="3455b-384">Это можно увидеть в разделах 1C и 2 кода, приведенного далее на этом шаге.</span><span class="sxs-lookup"><span data-stu-id="3455b-384">This can be seen in sections 1c and 2 of the code provided later in this step.</span></span>

<span data-ttu-id="3455b-385">Создайте проект, который может использовать локализованные модули ресурсов в любой версии Windows:</span><span class="sxs-lookup"><span data-stu-id="3455b-385">Create a project that can use the localized resource modules on any version of Windows:</span></span>

1.  <span data-ttu-id="3455b-386">Добавьте новый проект в решение Хелломуи (с помощью файла выбора меню, добавьте и новый проект) со следующими параметрами и значениями:</span><span class="sxs-lookup"><span data-stu-id="3455b-386">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="3455b-387">Тип проекта: проект Win32.</span><span class="sxs-lookup"><span data-stu-id="3455b-387">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="3455b-388">Имя: Гуистеп \_ 3.</span><span class="sxs-lookup"><span data-stu-id="3455b-388">Name: GuiStep\_3.</span></span>
    3.  <span data-ttu-id="3455b-389">Расположение: примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3455b-389">Location: accept the default.</span></span>
    4.  <span data-ttu-id="3455b-390">В мастере приложений Win32 выберите тип приложения по умолчанию: приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="3455b-390">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3455b-391">Настройте этот проект для запуска в Visual Studio и настройте его потоковую модель.</span><span class="sxs-lookup"><span data-stu-id="3455b-391">Set this project to run from within Visual Studio, and configure its threading model.</span></span> <span data-ttu-id="3455b-392">Кроме того, настройте его для добавления необходимых заголовков и библиотек.</span><span class="sxs-lookup"><span data-stu-id="3455b-392">Also, configure it to add the necessary headers and libraries.</span></span>

    > [!Note]  
    > <span data-ttu-id="3455b-393">В путях, используемых в этом руководстве, предполагается, что пакет SDK для Windows 7 и пакеты API нижнего уровня Microsoft NLS были установлены в каталоги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3455b-393">The paths used in this tutorial assume that the Windows 7 SDK and the Microsoft NLS downlevel APIs package were installed to their default directories.</span></span> <span data-ttu-id="3455b-394">Если это не так, измените пути соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="3455b-394">If that is not the case, modify the paths appropriately.</span></span>

     

    1.  <span data-ttu-id="3455b-395">В обозреватель решений щелкните правой кнопкой мыши проект Гуистеп \_ 3 и выберите Назначить запускаемым проектом.</span><span class="sxs-lookup"><span data-stu-id="3455b-395">In the Solution Explorer, right-click the project GuiStep\_3 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="3455b-396">Щелкните его правой кнопкой мыши и выберите пункт Свойства.</span><span class="sxs-lookup"><span data-stu-id="3455b-396">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="3455b-397">В диалоговом окне страницы свойств проекта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3455b-397">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3455b-398">В раскрывающемся списке слева в верхнем левом углу задайте для параметра Конфигурация значение все конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3455b-398">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3455b-399">В разделе Свойства конфигурации разверните C/C++, выберите Создание кода и задайте библиотеку времени выполнения: Многопоточная Отладка (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3455b-399">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>
        3.  <span data-ttu-id="3455b-400">Выберите Общие и добавьте в дополнительные каталоги включения:</span><span class="sxs-lookup"><span data-stu-id="3455b-400">Select General and add to Additional Include Directories:</span></span>

            -   <span data-ttu-id="3455b-401">"C: \\ API нижнего уровня Microsoft NLS \\ включают".</span><span class="sxs-lookup"><span data-stu-id="3455b-401">"C:\\Microsoft NLS Downlevel APIs\\Include".</span></span>

        4.  <span data-ttu-id="3455b-402">Выберите язык и задайте параметр обрабатывать WCHAR \_ t как встроенный тип: нет (/Zc: WCHAR \_ t-).</span><span class="sxs-lookup"><span data-stu-id="3455b-402">Select Language and set Treat wchar\_t as Built-in Type: No (/Zc:wchar\_t-).</span></span>
        5.  <span data-ttu-id="3455b-403">Выберите Дополнительно и задайте соглашение о вызовах: \_ STDCALL (/gz).</span><span class="sxs-lookup"><span data-stu-id="3455b-403">Select Advanced and set Calling Convention: \_stdcall (/Gz).</span></span>
        6.  <span data-ttu-id="3455b-404">В разделе Свойства конфигурации разверните компоновщик, выберите входные данные и добавьте дополнительные зависимости:</span><span class="sxs-lookup"><span data-stu-id="3455b-404">Under Configuration Properties expand Linker, select Input, and add to Additional Dependencies:</span></span>

            -   <span data-ttu-id="3455b-405">"C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ lib \\ муилоад. lib".</span><span class="sxs-lookup"><span data-stu-id="3455b-405">"C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Lib\\MUILoad.lib".</span></span>
            -   <span data-ttu-id="3455b-406">"C: \\ интерфейсы API нижнего уровня Microsoft NLS \\ lib \\ x86 \\ нлсдл. lib".</span><span class="sxs-lookup"><span data-stu-id="3455b-406">"C:\\Microsoft NLS Downlevel APIs\\Lib\\x86\\Nlsdl.lib".</span></span>

3.  <span data-ttu-id="3455b-407">Замените содержимое файла Гуистеп \_ 3. cpp следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="3455b-407">Replace the contents of GuiStep\_3.cpp with the following code:</span></span>
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

    

4.  <span data-ttu-id="3455b-408">Создайте или скопируйте langs.txt в соответствующий каталог, как описано в [шаге 4: глобализация "Hello MUI"](#step-4-globalizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="3455b-408">Create or copy langs.txt to the appropriate directory, as previously described in [Step 4: Globalizing "Hello MUI"](#step-4-globalizing-hello-mui).</span></span>
5.  <span data-ttu-id="3455b-409">Постройте и запустите проект.</span><span class="sxs-lookup"><span data-stu-id="3455b-409">Build and run the project.</span></span>

> [!Note]  
> <span data-ttu-id="3455b-410">Если приложение должно работать в версиях Windows, предшествовавших Windows Vista, ознакомьтесь с документами, поставляемыми вместе с пакетом [API-интерфейсов нижнего уровня Microsoft NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) , чтобы повторно распространить Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="3455b-410">If the application should run on Windows versions prior to Windows Vista, be sure to read the documents that came with the [Microsoft NLS downlevel APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) package on how to redistribute Nlsdl.dll.</span></span>

 

## <a name="additional-considerations-for-mui"></a><span data-ttu-id="3455b-411">Дополнительные рекомендации для MUI</span><span class="sxs-lookup"><span data-stu-id="3455b-411">Additional Considerations for MUI</span></span>

### <a name="support-for-console-applications"></a><span data-ttu-id="3455b-412">Поддержка консольных приложений</span><span class="sxs-lookup"><span data-stu-id="3455b-412">Support for Console Applications</span></span>

<span data-ttu-id="3455b-413">Методики, описанные в этом учебнике, также можно использовать в консольных приложениях.</span><span class="sxs-lookup"><span data-stu-id="3455b-413">The techniques covered in this tutorial can also be used in console applications.</span></span> <span data-ttu-id="3455b-414">Однако, в отличие от большинства стандартных элементов управления GUI, командное окно Windows не может отображать символы для всех языков.</span><span class="sxs-lookup"><span data-stu-id="3455b-414">However, unlike most standard GUI controls, the Windows command window cannot display characters for all languages.</span></span> <span data-ttu-id="3455b-415">Поэтому многоязыковые консольные приложения требуют особого внимания.</span><span class="sxs-lookup"><span data-stu-id="3455b-415">For this reason, multilingual console applications require special attention.</span></span>

<span data-ttu-id="3455b-416">Вызов API-интерфейсов [**сетсреадуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) или [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) с конкретными флагами фильтрации приводит к тому, что функции загрузки ресурсов удаляют языковые проверки ресурсов для определенных языков, которые обычно не отображаются в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="3455b-416">Calling the APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) with specific filtering flags causes the resource loading functions to remove language resource probes for specific languages that are not normally displayed within a command window.</span></span> <span data-ttu-id="3455b-417">Если эти флаги заданы, то алгоритмы настройки языка позволяют использовать в командном окне только те языки, которые будут отображаться правильно.</span><span class="sxs-lookup"><span data-stu-id="3455b-417">When these flags are set, the language-setting algorithms allow only those languages that will display properly in the command window to be on the fallback list.</span></span>

<span data-ttu-id="3455b-418">Дополнительные сведения об использовании этих API для создания многоязыкового консольного приложения см. в разделах "Примечания" [**сетсреадуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) и [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="3455b-418">For more information on using these APIs to build a multilingual console application, see the remarks sections of [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) and [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span>

### <a name="determination-of-languages-to-support-at-run-time"></a><span data-ttu-id="3455b-419">Определение языков для поддержки на Run-Time</span><span class="sxs-lookup"><span data-stu-id="3455b-419">Determination of Languages to Support at Run-Time</span></span>

<span data-ttu-id="3455b-420">Вы можете принять одно из следующих предложений по проектированию, чтобы определить, какие языки должно поддерживать приложение во время выполнения:</span><span class="sxs-lookup"><span data-stu-id="3455b-420">You can adopt one of the following design suggestions to determine which languages your application should support at run-time:</span></span>

-   <span data-ttu-id="3455b-421">**Во время установки включите конечного пользователя, чтобы выбрать предпочтительный язык из списка поддерживаемых языков.**</span><span class="sxs-lookup"><span data-stu-id="3455b-421">**During installation, enable the end user to select the preferred language from a list of supported languages**</span></span>

-   <span data-ttu-id="3455b-422">**Чтение списка языков из файла конфигурации**</span><span class="sxs-lookup"><span data-stu-id="3455b-422">**Read a language list from a configuration file**</span></span>

    <span data-ttu-id="3455b-423">Некоторые из проектов в этом учебнике содержат функцию, используемую для синтаксического анализа файла конфигурации langs.txt, который содержит список языков.</span><span class="sxs-lookup"><span data-stu-id="3455b-423">Some of the projects in this tutorial contain a function used to parse a langs.txt configuration file, which contains a language list.</span></span>

    <span data-ttu-id="3455b-424">Поскольку эта функция принимает внешние входные данные, проверьте языки, предоставленные в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="3455b-424">Because this function takes external input, validate the languages that are provided as input.</span></span> <span data-ttu-id="3455b-425">Дополнительные сведения о выполнении проверки см. в разделе функции [**исвалидлокаленаме**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) или [**довнлевеллокаленаметолЦид**](downlevellocalenametolcid.md) .</span><span class="sxs-lookup"><span data-stu-id="3455b-425">See the [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) or [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) functions for more details on performing that validation.</span></span>

-   <span data-ttu-id="3455b-426">**Запросите операционную систему, чтобы определить, какие языки установлены**</span><span class="sxs-lookup"><span data-stu-id="3455b-426">**Query the operating system to determine which languages are installed**</span></span>

    <span data-ttu-id="3455b-427">Такой подход позволяет приложению использовать тот же язык, что и операционная система.</span><span class="sxs-lookup"><span data-stu-id="3455b-427">This approach helps the application use the same language as the operating system.</span></span> <span data-ttu-id="3455b-428">Хотя это и не требует запроса пользователя, при выборе этого параметра следует помнить, что языки операционной системы могут быть добавлены или удалены в любое время и могут изменяться после установки приложения пользователем.</span><span class="sxs-lookup"><span data-stu-id="3455b-428">Although this does not require user prompting, if you choose this option, be aware that operating system languages can be added or removed at any time and can change after the user installs the application.</span></span> <span data-ttu-id="3455b-429">Кроме того, имейте в виду, что в некоторых случаях операционная система устанавливается с ограниченной поддержкой языка, а приложение предоставляет больше преимуществ, если поддерживает языки, не поддерживаемые операционной системой.</span><span class="sxs-lookup"><span data-stu-id="3455b-429">Also, be aware that in some cases, the operating system is installed with limited language support, and the application offers more value if it supports languages that the operating system does not support.</span></span>

    <span data-ttu-id="3455b-430">Дополнительные сведения о том, как определить установленные языки в операционной системе, см. в разделе Функция [**енумуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .</span><span class="sxs-lookup"><span data-stu-id="3455b-430">For more information on how to determine the currently installed languages in the operating system, see the [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) function.</span></span>

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a><span data-ttu-id="3455b-431">Поддержка сложных скриптов в версиях до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3455b-431">Complex Script Support in Versions Prior to Windows Vista</span></span>

<span data-ttu-id="3455b-432">Если приложение, поддерживающее определенные сложные сценарии, работает в версии Windows до Windows Vista, текст в этом сценарии может неправильно отображаться в компонентах графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3455b-432">When an application that supports certain complex scripts runs on a version of Windows prior to Windows Vista, text in that script may not display properly in GUI components.</span></span> <span data-ttu-id="3455b-433">Например, в проекте нижнего уровня в этом руководстве скрипты hi-IN и TA-IN могут не отображаться в окне сообщения из-за проблем с обработкой сложных сценариев и недостатком связанных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="3455b-433">For example, in the downlevel project within this tutorial, hi-IN and ta-IN scripts may not display in the message box due to issues with processing complex scripts and the lack of related fonts.</span></span> <span data-ttu-id="3455b-434">Как правило, проблемы этой природы представляют собой квадратные рамки в компоненте GUI.</span><span class="sxs-lookup"><span data-stu-id="3455b-434">Normally, problems of this nature present themselves as square boxes in the GUI component.</span></span>

<span data-ttu-id="3455b-435">Дополнительные сведения о том, как включить обработку сложных скриптов, можно найти в статье [Поддержка скриптов и шрифтов в Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span><span class="sxs-lookup"><span data-stu-id="3455b-435">More information about how to enable complex script processing can be found at [Script and Font Support in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="3455b-436">Сводка</span><span class="sxs-lookup"><span data-stu-id="3455b-436">Summary</span></span>

<span data-ttu-id="3455b-437">В этом учебнике мы расправили глобализованное приложение и продемонстрировали следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="3455b-437">This tutorial globalized a monolingual application and demonstrated the following best practices.</span></span>

-   <span data-ttu-id="3455b-438">Разработайте приложение, чтобы воспользоваться преимуществами модели ресурсов Win32.</span><span class="sxs-lookup"><span data-stu-id="3455b-438">Design the application to take advantage of the Win32 resource model.</span></span>
-   <span data-ttu-id="3455b-439">Использование разделения ресурсов многоязыкового интерфейса в вспомогательные двоичные файлы (MUI-файлы).</span><span class="sxs-lookup"><span data-stu-id="3455b-439">Utilize MUI splitting of resources into satellite binaries (.mui files).</span></span>
-   <span data-ttu-id="3455b-440">Убедитесь, что процесс локализации обновляет ресурсы в файлах MUI, чтобы они соответствовали целевому языку.</span><span class="sxs-lookup"><span data-stu-id="3455b-440">Ensure that the localization process updates the resources in the .mui files to be appropriate for the target language.</span></span>
-   <span data-ttu-id="3455b-441">Убедитесь, что упаковка и развертывание приложения, связанные файлы MUI и содержимое конфигурации выполняются правильно, чтобы разрешить API-интерфейсам загрузки ресурсов искать локализованное содержимое.</span><span class="sxs-lookup"><span data-stu-id="3455b-441">Ensure that packaging and deployment of the application, associated .mui files, and configuration content is done correctly to allow the resource loading APIs to find the localized content.</span></span>
-   <span data-ttu-id="3455b-442">Предоставьте конечному пользователю механизм для настройки языковой конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="3455b-442">Provide the end user a mechanism to adjust the language configuration of the application.</span></span>
-   <span data-ttu-id="3455b-443">Настройте код времени выполнения, чтобы воспользоваться преимуществами языковой конфигурации, чтобы сделать приложение более быстрым реагированием на потребности конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3455b-443">Adjust the run-time code to take advantage of language configuration, to make the application more responsive to end user needs.</span></span>

 

 
