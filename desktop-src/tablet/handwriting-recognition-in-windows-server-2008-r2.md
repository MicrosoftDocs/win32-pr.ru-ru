---
description: Windows Server 2008 R2 добавляет поддержку распознавания рукописного текста на стороне сервера в Windows. В этом разделе описывается распознавание рукописного ввода в Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Распознавание рукописного текста в Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070819"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a><span data-ttu-id="e32cb-104">Распознавание рукописного текста в Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e32cb-104">Handwriting Recognition in Windows Server 2008 R2</span></span>

<span data-ttu-id="e32cb-105">Windows Server 2008 R2 поддерживает распознавание рукописного ввода на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="e32cb-105">Windows Server 2008 R2 supports server-side handwriting recognition.</span></span> <span data-ttu-id="e32cb-106">Распознавание на стороне сервера позволяет серверу распознать содержимое из перьевого ввода на веб-страницах.</span><span class="sxs-lookup"><span data-stu-id="e32cb-106">Server-side recognition lets a server recognize content from pen input on Web pages.</span></span> <span data-ttu-id="e32cb-107">Это особенно полезно, когда пользователи в сети будут указывать термины, интерпретируемые с помощью пользовательского словаря.</span><span class="sxs-lookup"><span data-stu-id="e32cb-107">This is particularly useful when users on a network will be specifying terms that are interpreted using a custom dictionary.</span></span> <span data-ttu-id="e32cb-108">Например, если у вас есть медицинские приложения, которые запрашивают серверную базу данных для имен пациента, эти имена можно добавить в другую базу данных, на которую можно перекрестно ссылаться при выполнении поиска из рукописной формы Silverlight.</span><span class="sxs-lookup"><span data-stu-id="e32cb-108">For example, if you had a medical application that queried a server database for patient names, those names could be added to another database that would be cross-referenced when performing searches from a handwritten Silverlight form.</span></span>

## <a name="set-up-your-server-for-server-side-recognition"></a><span data-ttu-id="e32cb-109">Настройка сервера для распознавания Server-Side</span><span class="sxs-lookup"><span data-stu-id="e32cb-109">Set up your Server for Server-Side Recognition</span></span>

<span data-ttu-id="e32cb-110">Чтобы настроить распознавание на стороне сервера, следует выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e32cb-110">The following steps should be followed to set up server-side recognition.</span></span>

- <span data-ttu-id="e32cb-111">Установка службы рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="e32cb-111">Install Ink and Handwriting Services</span></span>
- <span data-ttu-id="e32cb-112">Установка поддержки веб-сервера (IIS) и сервера приложений</span><span class="sxs-lookup"><span data-stu-id="e32cb-112">Install Support for Web Server (IIS) and Application Server</span></span>
- <span data-ttu-id="e32cb-113">Включение роли "возможности рабочего стола"</span><span class="sxs-lookup"><span data-stu-id="e32cb-113">Enable the Desktop Experience Role</span></span>
- <span data-ttu-id="e32cb-114">Запуск службы ввода Tablet PC</span><span class="sxs-lookup"><span data-stu-id="e32cb-114">Start the Tablet PC Input Service</span></span>

### <a name="install-ink-and-handwriting-services"></a><span data-ttu-id="e32cb-115">Установка службы рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="e32cb-115">Install Ink and Handwriting Services</span></span>

<span data-ttu-id="e32cb-116">Чтобы установить службы рукописного ввода и рукописного текста, откройте Диспетчер серверов, щелкнув значок диспетчера серверов в области быстрого запуска.</span><span class="sxs-lookup"><span data-stu-id="e32cb-116">To install Ink and Handwriting services, open the server manager by clicking the server manager icon from the Quick Launch tray.</span></span> <span data-ttu-id="e32cb-117">В меню **функции** выберите команду **Добавить компоненты**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-117">From the **Features** menu, click **Add Features**.</span></span> <span data-ttu-id="e32cb-118">Убедитесь, что установлен флажок **службы рукописного ввода** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-118">Make sure that you select the **Ink and Handwriting Services** check box.</span></span> <span data-ttu-id="e32cb-119">На следующем рисунке показано диалоговое окно **Выбор компонентов** с выбранным **службы рукописного ввода** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-119">The following image shows the **Select Features** dialog box with **Ink and Handwriting Services** selected.</span></span>

<span data-ttu-id="e32cb-120">![Диалоговое окно "Выбор компонентов" с установленным рукописным вводом и службами рукописного ввода](images/setup-server-1-ink-and-handwriting.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-120">![Select features dialog box with ink and handwriting services check box selected](images/setup-server-1-ink-and-handwriting.png)</span></span><br/>
<span data-ttu-id="e32cb-121">*Диалоговое окно "Выбор компонентов" с установленным рукописным вводом и службами рукописного ввода*</span><span class="sxs-lookup"><span data-stu-id="e32cb-121">*Select features dialog box with ink and handwriting services check box selected*</span></span>

### <a name="installation-support-for-web-server-iis-and-application-server"></a><span data-ttu-id="e32cb-122">Поддержка установки веб-сервера (IIS) и сервера приложений</span><span class="sxs-lookup"><span data-stu-id="e32cb-122">Installation Support for Web Server (IIS) and Application Server</span></span>

<span data-ttu-id="e32cb-123">Откройте диспетчер сервера, как это делалось на первом шаге.</span><span class="sxs-lookup"><span data-stu-id="e32cb-123">Open the server manager as you did for the first step.</span></span> <span data-ttu-id="e32cb-124">Далее необходимо добавить роли "веб-сервер (IIS)" и "сервер приложений".</span><span class="sxs-lookup"><span data-stu-id="e32cb-124">Next, you will need to add the Web Server (IIS) and Application Server roles.</span></span> <span data-ttu-id="e32cb-125">В меню **роли** выберите команду **Добавить роли**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-125">From the **Roles** menu, click **Add Roles**.</span></span> <span data-ttu-id="e32cb-126">Откроется мастер добавления ролей.</span><span class="sxs-lookup"><span data-stu-id="e32cb-126">The Add Roles wizard appears.</span></span> <span data-ttu-id="e32cb-127">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-127">Click **Next**.</span></span> <span data-ttu-id="e32cb-128">Убедитесь, что выбран **сервер приложений** и **веб-сервер (IIS)** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-128">Make sure **Application Server** and **Web Server (IIS)** are selected.</span></span> <span data-ttu-id="e32cb-129">На следующем рисунке показано диалоговое окно **Выбор ролей сервера** с выбранными ролями **веб-сервер (IIS)** и **сервер приложений** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-129">The following image shows the **Select Server Roles** dialog box with the **Web Server (IIS)** and **Application Server** roles selected.</span></span>

<span data-ttu-id="e32cb-130">![Диалоговое окно "Выбор ролей сервера" с выбранными ролями веб-сервера (IIS) и сервера приложений](images/setup-server-2-select-server-roles.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-130">![Select server roles dialog box with web server (iis) and application server roles selected](images/setup-server-2-select-server-roles.png)</span></span><br/>
<span data-ttu-id="e32cb-131">*Диалоговое окно "Выбор ролей сервера" с выбранными ролями веб-сервера (IIS) и сервера приложений*</span><span class="sxs-lookup"><span data-stu-id="e32cb-131">*Select server roles dialog box with web server (iis) and application server roles selected*</span></span>

<span data-ttu-id="e32cb-132">При выборе **сервера приложений** будет предложено установить платформу ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="e32cb-132">When you select **Application Server**, you will be asked to install the ASP.NET framework.</span></span> <span data-ttu-id="e32cb-133">Нажмите кнопку **Добавить необходимые компоненты** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-133">Click the **Add the Required Features** button.</span></span> <span data-ttu-id="e32cb-134">После нажатия кнопки " **Далее**" отобразится диалоговое окно "Обзор". Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-134">After you click **Next**, you will be presented with an overview dialog box; click **Next**.</span></span> <span data-ttu-id="e32cb-135">Теперь должно быть доступно диалоговое окно **Выбор служб ролей** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-135">The **Select Role Services** dialog box should now be available.</span></span> <span data-ttu-id="e32cb-136">Убедитесь, что выбран **веб-сервер (IIS)** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-136">Make sure that **Web Server (IIS)** is selected.</span></span> <span data-ttu-id="e32cb-137">На следующем рисунке показано диалоговое окно **Выбор служб ролей** с включенным веб-сервером (IIS).</span><span class="sxs-lookup"><span data-stu-id="e32cb-137">The following image shows the **Select Role Services** dialog box with Web Server (IIS) enabled.</span></span>

<span data-ttu-id="e32cb-138">![Диалоговое окно "Выбор служб ролей" с включенным веб-сервером (IIS)](images/setup-server-3-select-role-services.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-138">![Select role services dialog box with web server (iis) enabled](images/setup-server-3-select-role-services.png)</span></span><br/>
<span data-ttu-id="e32cb-139">*Диалоговое окно "Выбор служб ролей" с включенным веб-сервером (IIS)*</span><span class="sxs-lookup"><span data-stu-id="e32cb-139">*Select role services dialog box with web server (iis) enabled*</span></span>

<span data-ttu-id="e32cb-140">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-140">Click **Next**.</span></span> <span data-ttu-id="e32cb-141">Откроется диалоговое окно обзора. еще раз нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-141">An overview dialog box appears; click **Next** again.</span></span> <span data-ttu-id="e32cb-142">Теперь отобразится страница с предложением параметров для ролей веб-сервера (IIS).</span><span class="sxs-lookup"><span data-stu-id="e32cb-142">You will now be presented with a page offering you options for roles for Web Server (IIS).</span></span> <span data-ttu-id="e32cb-143">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-143">Click **Next**.</span></span> <span data-ttu-id="e32cb-144">На следующей странице кнопка " **установить** " станет активной.</span><span class="sxs-lookup"><span data-stu-id="e32cb-144">On the next page, the **Install** button will become active.</span></span> <span data-ttu-id="e32cb-145">Нажмите кнопку **установить** , после чего будет установлена поддержка веб-сервера (IIS) и сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="e32cb-145">Click **Install** and you will install support for Web Server (IIS) and Application Server.</span></span>

### <a name="enable-the-desktop-experience-role"></a><span data-ttu-id="e32cb-146">Включение роли "возможности рабочего стола"</span><span class="sxs-lookup"><span data-stu-id="e32cb-146">Enable the Desktop Experience Role</span></span>

<span data-ttu-id="e32cb-147">Чтобы включить возможности рабочего стола, нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем щелкните **Диспетчер сервера**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-147">To enable the desktop experience, click **Start**, click **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="e32cb-148">Выберите **Добавить службы** , а затем выберите службу " **возможности рабочего стола** ".</span><span class="sxs-lookup"><span data-stu-id="e32cb-148">Select **Add Services** and then select the **Desktop Experience** service.</span></span> <span data-ttu-id="e32cb-149">На следующем рисунке показано диалоговое окно **Выбор компонентов** с установленным элементом "возможности рабочего стола".</span><span class="sxs-lookup"><span data-stu-id="e32cb-149">The following image shows the **Select Features** dialog box with the Desktop Experience item installed.</span></span>

<span data-ttu-id="e32cb-150">![Диалоговое окно "Выбор компонентов" с выбранной службой "возможности рабочего стола"](images/setup-server-4-desktop-experience.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-150">![Select features dialog box with desktop experience service selected](images/setup-server-4-desktop-experience.png)</span></span><br/>
<span data-ttu-id="e32cb-151">*Диалоговое окно "Выбор компонентов" с выбранной службой "возможности рабочего стола"*</span><span class="sxs-lookup"><span data-stu-id="e32cb-151">*Select features dialog box with desktop experience service selected*</span></span>

<span data-ttu-id="e32cb-152">Нажмите кнопку **Далее** , чтобы установить возможности рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="e32cb-152">Click **Next** to install the Desktop Experience.</span></span>

### <a name="start-the-tablet-service"></a><span data-ttu-id="e32cb-153">Запуск службы планшета</span><span class="sxs-lookup"><span data-stu-id="e32cb-153">Start the Tablet Service</span></span>

<span data-ttu-id="e32cb-154">После установки службы "возможности рабочего стола" в меню " **службы** " появится служба ввода Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e32cb-154">After you have installed the Desktop Experience service, the Tablet PC Input service will appear in the **Services** menu.</span></span> <span data-ttu-id="e32cb-155">Чтобы открыть меню " **службы** ", нажмите кнопку " **Пуск**", выберите " **Администрирование**", а затем " **службы**".</span><span class="sxs-lookup"><span data-stu-id="e32cb-155">To access the **Services** menu, click **Start**, click **Administrative Tools**, and then click **Services**.</span></span> <span data-ttu-id="e32cb-156">Чтобы запустить службу, щелкните правой кнопкой мыши элемент **служба ввода Tablet PC** и выберите команду **запустить**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-156">To start the service, right-click **Tablet PC Input Service** and then click **Start**.</span></span> <span data-ttu-id="e32cb-157">На следующем рисунке показано меню **службы** с запущенной службой ввода Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e32cb-157">The following image shows the **Services** menu with the Tablet PC Input Service started.</span></span>

<span data-ttu-id="e32cb-158">![Меню "службы" с запущенной службой ввода Tablet PC](images/setup-server-5-tablet-pc-input-service.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-158">![Services menu with the tablet pc input service started](images/setup-server-5-tablet-pc-input-service.png)</span></span><br/>
<span data-ttu-id="e32cb-159">*Меню "службы" с запущенной службой ввода Tablet PC*</span><span class="sxs-lookup"><span data-stu-id="e32cb-159">*Services menu with the tablet pc input service started*</span></span>

## <a name="performing-server-side-recognition-using-silverlight"></a><span data-ttu-id="e32cb-160">Выполнение Server-Sideного распознавания с помощью Silverlight</span><span class="sxs-lookup"><span data-stu-id="e32cb-160">Performing Server-Side Recognition Using Silverlight</span></span>

<span data-ttu-id="e32cb-161">В этом разделе показано, как создать веб-приложение, которое использует Silverlight для записи рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="e32cb-161">This section shows how to create a Web application that uses Silverlight to capture handwriting input.</span></span> <span data-ttu-id="e32cb-162">Чтобы запрограммировать распознаватель в Visual Studio 2008, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e32cb-162">Use the following steps to program the recognizer in Visual Studio 2008.</span></span>

- <span data-ttu-id="e32cb-163">Установите и обновите Visual Studio 2008, чтобы добавить поддержку Silverlight.</span><span class="sxs-lookup"><span data-stu-id="e32cb-163">Install and update Visual Studio 2008 to add support for Silverlight.</span></span>
- <span data-ttu-id="e32cb-164">Создайте новый проект Silverlight в Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="e32cb-164">Create a new Silverlight project in Visual Studio 2008.</span></span>
- <span data-ttu-id="e32cb-165">Добавьте необходимые ссылки на службы в проект.</span><span class="sxs-lookup"><span data-stu-id="e32cb-165">Add the necessary service references to your project.</span></span>
- <span data-ttu-id="e32cb-166">Создание службы WCF Silverlight для распознавания рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="e32cb-166">Create a Silverlight WCF Service for ink recognition.</span></span>
- <span data-ttu-id="e32cb-167">Добавьте ссылку на службу в клиентский проект.</span><span class="sxs-lookup"><span data-stu-id="e32cb-167">Add the service reference to your client project.</span></span>
- <span data-ttu-id="e32cb-168">Добавьте класс InkCollector в проект Инкрекогнитион.</span><span class="sxs-lookup"><span data-stu-id="e32cb-168">Add the InkCollector class to the InkRecognition project.</span></span>
- <span data-ttu-id="e32cb-169">Удалите защищенные директивы транспорта из конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="e32cb-169">Remove secure transport directives from the client configuration</span></span>

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a><span data-ttu-id="e32cb-170">Установка и обновление Visual Studio 2008 для добавления поддержки Silverlight</span><span class="sxs-lookup"><span data-stu-id="e32cb-170">Install and Update Visual Studio 2008 to Add Support for Silverlight</span></span>

<span data-ttu-id="e32cb-171">Перед началом работы необходимо выполнить следующие действия на сервере Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e32cb-171">Before you begin, you must perform the following steps on your Windows Server 2008 R2 server.</span></span>

- <span data-ttu-id="e32cb-172">Установите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="e32cb-172">Install Visual Studio 2008.</span></span>
- <span data-ttu-id="e32cb-173">Установите [Microsoft Visual Studio 2008 с пакетом обновления 1 (SP1)](https://www.microsoft.com/download/details.aspx?id=10986).</span><span class="sxs-lookup"><span data-stu-id="e32cb-173">Install [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span></span>
- <span data-ttu-id="e32cb-174">Установите [пакет SDK для Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).</span><span class="sxs-lookup"><span data-stu-id="e32cb-174">Install [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span></span>

<span data-ttu-id="e32cb-175">После установки этих приложений и обновлений можно приступать к созданию веб-приложения для распознавания на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="e32cb-175">After you have installed these applications and updates, you are ready to create your server-side recognition Web application.</span></span>

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a><span data-ttu-id="e32cb-176">Создание нового веб-проекта Silverlight в Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="e32cb-176">Create a new Silverlight Web Project in Visual Studio 2008</span></span>

<span data-ttu-id="e32cb-177">В меню **Файл** выберите **Новый проект**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-177">From the **File** menu, click **New Project**.</span></span> <span data-ttu-id="e32cb-178">Выберите шаблон приложения Silverlight из списка проектов Visual C \# .</span><span class="sxs-lookup"><span data-stu-id="e32cb-178">Select the Silverlight Application template from the Visual C\# project list.</span></span> <span data-ttu-id="e32cb-179">Присвойте проекту имя Инкрекогнитион и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-179">Name your project InkRecognition and click **OK**.</span></span> <span data-ttu-id="e32cb-180">На следующем рисунке показан проект C \# Silverlight, выбранный с именем инкрекогнитион.</span><span class="sxs-lookup"><span data-stu-id="e32cb-180">The following image shows the C\# Silverlight project selected and named InkRecognition.</span></span>

<span data-ttu-id="e32cb-181">![\#выбранный проект c Silverlight с именем инкрекогнитион](images/project-1-new-project.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-181">![c\# silverlight project selected, with the name inkrecognition](images/project-1-new-project.png)</span></span><br/>
<span data-ttu-id="e32cb-182">*\#выбранный проект c Silverlight с именем инкрекогнитион*</span><span class="sxs-lookup"><span data-stu-id="e32cb-182">*c\# silverlight project selected, with the name inkrecognition*</span></span>

<span data-ttu-id="e32cb-183">После нажатия кнопки **ОК** появится диалоговое окно, предлагающее добавить в проект приложение Silverlight.</span><span class="sxs-lookup"><span data-stu-id="e32cb-183">After you click **OK**, a dialog box prompts you to add a Silverlight application to your project.</span></span> <span data-ttu-id="e32cb-184">Выберите **Добавить новый веб-проект ASP.NET в решение для размещения Silverlight** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-184">Select **Add a new ASP.NET Web project to the solution to host Silverlight** and click **OK**.</span></span> <span data-ttu-id="e32cb-185">На следующем рисунке показано, как настроить пример проекта перед нажатием кнопки **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-185">The following image shows how to set up the example project before you click **OK**.</span></span>

<span data-ttu-id="e32cb-186">![Диалоговое окно с запросом на Добавление приложения Silverlight в проект](images/project-2-add-a-new-aspnetproject.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-186">![Dialog box with prompt for adding a silverlight application to a project](images/project-2-add-a-new-aspnetproject.png)</span></span><br/>
<span data-ttu-id="e32cb-187">*Диалоговое окно с запросом на Добавление приложения Silverlight в проект*</span><span class="sxs-lookup"><span data-stu-id="e32cb-187">*Dialog box with prompt for adding a silverlight application to a project*</span></span>

### <a name="add-the-necessary-service-references-to-your-project"></a><span data-ttu-id="e32cb-188">Добавление необходимых ссылок на службы в проект</span><span class="sxs-lookup"><span data-stu-id="e32cb-188">Add the Necessary Service References to your Project</span></span>

<span data-ttu-id="e32cb-189">Теперь у вас есть универсальный клиентский проект Silverlight (Инкрекогнитион) с веб-проектом (Инкрекогнитион. Web), настроенным в решении.</span><span class="sxs-lookup"><span data-stu-id="e32cb-189">Now you have your generic Silverlight client project (InkRecognition) with a Web project (InkRecognition.Web) set up in your solution.</span></span> <span data-ttu-id="e32cb-190">Проект откроется с помощью Page. XAML и Open. aspx по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e32cb-190">The project will open with Page.xaml and Default.aspx open.</span></span> <span data-ttu-id="e32cb-191">Закройте эти окна и добавьте ссылки System. Runtime. Serialization и System. ServiceModel в проект Инкрекогнитион, щелкнув правой кнопкой мыши папку References в проекте Инкрекогнитион и выбрав пункт **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-191">Close these windows and add the System.Runtime.Serialization and System.ServiceModel references to the InkRecognition project by right-clicking on the references folder in the InkRecognition project and selecting **Add Reference**.</span></span> <span data-ttu-id="e32cb-192">На следующем рисунке показано диалоговое окно с выбранными ссылками на реквизиты.</span><span class="sxs-lookup"><span data-stu-id="e32cb-192">The following image shows the dialog box with the requisite references selected.</span></span>

<span data-ttu-id="e32cb-193">![Диалоговое окно «Добавление ссылок» с выбранным System. Runtime. Serialization и System. ServiceModel](images/project-3a-add-references-to-inkreco.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-193">![Add references dialog box with system.runtime.serialization and system.servicemodel selected](images/project-3a-add-references-to-inkreco.png)</span></span><br/>
<span data-ttu-id="e32cb-194">*Диалоговое окно «Добавление ссылок» с выбранным System. Runtime. Serialization и System. ServiceModel*</span><span class="sxs-lookup"><span data-stu-id="e32cb-194">*Add references dialog box with system.runtime.serialization and system.servicemodel selected*</span></span>

<span data-ttu-id="e32cb-195">Далее необходимо добавить ссылки System. ServiceModel и Microsoft. Ink в проект Инкрекогнитион. Web.</span><span class="sxs-lookup"><span data-stu-id="e32cb-195">Next, you need to add the System.ServiceModel and Microsoft.Ink references to the InkRecognition.Web project.</span></span> <span data-ttu-id="e32cb-196">Ссылка Microsoft. Ink не будет отображаться в ссылках на .NET по умолчанию, поэтому выполните поиск Microsoft.Ink.dll в папке Windows.</span><span class="sxs-lookup"><span data-stu-id="e32cb-196">The Microsoft.Ink reference will not appear in the .NET references by default, so search your Windows folder for Microsoft.Ink.dll.</span></span> <span data-ttu-id="e32cb-197">После того как библиотека DLL будет найдена, добавьте сборку в ссылки проекта: выберите вкладку **Обзор** , перейдите в папку, содержащую Microsoft.Ink.dll, выберите Microsoft.Ink.dll и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-197">After you have located the DLL, add the assembly to the project references: select the **Browse** tab, change to the folder containing Microsoft.Ink.dll, select Microsoft.Ink.dll, and then click **OK**.</span></span> <span data-ttu-id="e32cb-198">На следующем рисунке показано решение проекта в проводнике Windows со всеми добавленными эталонными сборками.</span><span class="sxs-lookup"><span data-stu-id="e32cb-198">The following image shows the project's solution in Windows Explorer with all of the reference assemblies added.</span></span>

<span data-ttu-id="e32cb-199">![проект инкрекогнитион в проводнике Windows со всеми добавленными эталонными сборками](images/project-3b-with-reference-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-199">![inkrecognition project in windows explorer with all reference assemblies added](images/project-3b-with-reference-assemblies.png)</span></span><br/>
<span data-ttu-id="e32cb-200">*проект инкрекогнитион в проводнике Windows со всеми добавленными эталонными сборками*</span><span class="sxs-lookup"><span data-stu-id="e32cb-200">*inkrecognition project in windows explorer with all reference assemblies added*</span></span>

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a><span data-ttu-id="e32cb-201">Создание службы WCF Silverlight для распознавания рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="e32cb-201">Create a Silverlight WCF Service for Ink Recognition</span></span>

<span data-ttu-id="e32cb-202">Далее предстоит добавить службу WCF для распознавания рукописного текста в проект.</span><span class="sxs-lookup"><span data-stu-id="e32cb-202">Next, you will add a WCF service for ink recognition to the project.</span></span> <span data-ttu-id="e32cb-203">Щелкните правой кнопкой мыши проект Инкрекогнитион. Web, выберите **Добавить**, а затем — **новый элемент**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-203">Right-click your InkRecognition.Web project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="e32cb-204">Выберите шаблон службы WCF Silverlight, измените имя на Инкрекогитионсервице и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-204">Select the WCF Silverlight Service template, change the name to InkRecogitionService, and then click **Add**.</span></span> <span data-ttu-id="e32cb-205">На следующем рисунке показано диалоговое окно **Добавление нового элемента** со службой WCF Silverlight и именем.</span><span class="sxs-lookup"><span data-stu-id="e32cb-205">The following image shows the **Add New Item** dialog box with the Silverlight WCF service selected and named.</span></span>

<span data-ttu-id="e32cb-206">![Диалоговое окно "Добавление нового элемента" с выбранной и именованной службой WCF Silverlight](images/project-4-add-wcf-service.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-206">![Add new item dialog box with silverlight wcf service selected and named](images/project-4-add-wcf-service.png)</span></span><br/>
<span data-ttu-id="e32cb-207&quot;>*Диалоговое окно &quot;Добавление нового элемента&quot; с выбранной и именованной службой WCF Silverlight*</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e32cb-207&quot;>*Add new item dialog box with silverlight wcf service selected and named*</span></span>

<span data-ttu-id=&quot;e32cb-208&quot;>После добавления службы WCF Silverlight будет открыт код службы, Инкрекогнитионсервице. cs.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e32cb-208&quot;>After you add the WCF Silverlight service, the service code behind, InkRecognitionService.cs, will open.</span></span> <span data-ttu-id=&quot;e32cb-209&quot;>Замените код службы следующим кодом.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e32cb-209&quot;>Replace the service code with the following code.</span></span>

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = &quot;")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a><span data-ttu-id="e32cb-210">Добавление ссылки на службу в клиентский проект</span><span class="sxs-lookup"><span data-stu-id="e32cb-210">Add the Service Reference to your Client Project</span></span>

<span data-ttu-id="e32cb-211">Теперь, когда у вас есть служба Silverlight WCF для Инкрекогнитион, вы будете использовать службу из клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e32cb-211">Now that you have your Silverlight WCF service for InkRecognition, you will consume the service from your client application.</span></span> <span data-ttu-id="e32cb-212">Щелкните правой кнопкой мыши проект Инкрекогнитион и выберите **Добавление ссылки на службу**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-212">Right-click the InkRecognition project and select **Add Service Reference**.</span></span> <span data-ttu-id="e32cb-213">В появившемся диалоговом окне **Добавление ссылки на службу** выберите **обнаружить** , чтобы найти службы из текущего решения.</span><span class="sxs-lookup"><span data-stu-id="e32cb-213">From the **Add Service Reference** dialog box that appears, select **Discover** to discover services from the current solution.</span></span> <span data-ttu-id="e32cb-214">Инкрекогнитионсервице появится в области службы.</span><span class="sxs-lookup"><span data-stu-id="e32cb-214">InkRecognitionService will appear in the Services pane.</span></span> <span data-ttu-id="e32cb-215">Дважды щелкните Инкрекогнитионсервице в области службы, измените пространство имен на Инкрекогнитионсервицереференце и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-215">Double-click InkRecognitionService from the Services pane, change the namespace to InkRecognitionServiceReference, and then click **OK**.</span></span> <span data-ttu-id="e32cb-216">На следующем рисунке показано диалоговое окно **Добавление ссылки на службу** с выбранным инкрекогнитионсервице и измененным пространством имен.</span><span class="sxs-lookup"><span data-stu-id="e32cb-216">The following image shows the **Add Service Reference** dialog box with InkRecognitionService selected and the namespace changed.</span></span>

<span data-ttu-id="e32cb-217">![Диалоговое окно "Добавление ссылки на службу" с выбранным инкрекогнитионсервице и измененным пространством имен](images/project-5-discover-service-reference.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-217">![Add service reference dialog box with inkrecognitionservice selected and namespace changed](images/project-5-discover-service-reference.png)</span></span><br/>
<span data-ttu-id="e32cb-218">*Диалоговое окно "Добавление ссылки на службу" с выбранным инкрекогнитионсервице и измененным пространством имен*</span><span class="sxs-lookup"><span data-stu-id="e32cb-218">*Add service reference dialog box with inkrecognitionservice selected and namespace changed*</span></span>

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a><span data-ttu-id="e32cb-219">Добавление класса InkCollector в проект Инкрекогнитион</span><span class="sxs-lookup"><span data-stu-id="e32cb-219">Add the InkCollector Class to the InkRecognition Project</span></span>

<span data-ttu-id="e32cb-220">Щелкните правой кнопкой мыши проект Инкрекогнитион, выберите **Добавить**, а затем щелкните **новый элемент**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-220">Right-click the InkRecognition project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="e32cb-221">В меню **Visual C \#** выберите **\# класс c**.</span><span class="sxs-lookup"><span data-stu-id="e32cb-221">From the **Visual C\#** menu, select **C\# class**.</span></span> <span data-ttu-id="e32cb-222">Присвойте классу имя InkCollector.</span><span class="sxs-lookup"><span data-stu-id="e32cb-222">Name the class InkCollector.</span></span> <span data-ttu-id="e32cb-223">На следующем рисунке показано диалоговое окно с \# выбранным классом C и именем.</span><span class="sxs-lookup"><span data-stu-id="e32cb-223">The following image shows the dialog box with the C\# class selected and named.</span></span>

<span data-ttu-id="e32cb-224">![Диалоговое окно "Добавление нового элемента" с \# выбранным классом c и именем](images/project-6-add-ink-collector.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-224">![Add new item dialog box with c\# class selected and named](images/project-6-add-ink-collector.png)</span></span><br/>
<span data-ttu-id="e32cb-225">*Диалоговое окно "Добавление нового элемента" с \# выбранным классом c и именем*</span><span class="sxs-lookup"><span data-stu-id="e32cb-225">*Add new item dialog box with c\# class selected and named*</span></span>

<span data-ttu-id="e32cb-226">После добавления класса InkCollector будет открыто определение класса.</span><span class="sxs-lookup"><span data-stu-id="e32cb-226">After you add the InkCollector class, the class definition will open.</span></span> <span data-ttu-id="e32cb-227">Замените код в сборщике рукописного ввода на следующий код.</span><span class="sxs-lookup"><span data-stu-id="e32cb-227">Replace the code in the Ink Collector with the following code.</span></span>

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a><span data-ttu-id="e32cb-228">Обновление XAML для страницы по умолчанию и добавление кода программной части для распознавания рукописного текста</span><span class="sxs-lookup"><span data-stu-id="e32cb-228">Update the XAML for the Default Page and Add a Code Behind for Handwriting Recognition</span></span>

<span data-ttu-id="e32cb-229">Теперь, когда у вас есть класс, собирающий рукописный ввод, необходимо обновить XAML в Page. XAML, используя следующий код XAML.</span><span class="sxs-lookup"><span data-stu-id="e32cb-229">Now that you have a class that collects ink, you will need to update the XAML in page.xaml with the following XAML.</span></span> <span data-ttu-id="e32cb-230">Следующий код добавляет желтый градиент к области ввода, элементу управления InkCanvas и кнопку, запускающую распознавание.</span><span class="sxs-lookup"><span data-stu-id="e32cb-230">The following code adds a yellow gradient to the input area, an InkCanvas control, and a button that will trigger recognition.</span></span>

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

<span data-ttu-id="e32cb-231">Замените страницу кода программной части Page. XAML. cs следующим кодом, который добавит обработчик событий для кнопки **распознать** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-231">Replace the code behind page, Page.xaml.cs, with the following code that will add an event handler for the **Recognize** button.</span></span>

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a><span data-ttu-id="e32cb-232">Удалите защищенные директивы транспорта из конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="e32cb-232">Remove Secure Transport Directives from the Client Configuration</span></span>

<span data-ttu-id="e32cb-233">Прежде чем можно будет использовать службу WCF, необходимо удалить все параметры безопасного транспорта из конфигурации службы, так как в настоящее время защищенные транспортные протоколы не поддерживаются в службах WCF Silverlight 2,0.</span><span class="sxs-lookup"><span data-stu-id="e32cb-233">Before you can consume the WCF service, you must remove all secure transport options from the service configuration because secure transports are not currently supported in Silverlight 2.0 WCF services.</span></span> <span data-ttu-id="e32cb-234">В проекте Инкрекогнитион обновите параметры безопасности в Сервицереференцес. Клиентконфиг.</span><span class="sxs-lookup"><span data-stu-id="e32cb-234">From the InkRecognition project, update the security settings in ServiceReferences.ClientConfig.</span></span> <span data-ttu-id="e32cb-235">Изменение XML-кода безопасности с</span><span class="sxs-lookup"><span data-stu-id="e32cb-235">Change the security XML from</span></span>

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

<span data-ttu-id="e32cb-236">значение</span><span class="sxs-lookup"><span data-stu-id="e32cb-236">to</span></span>

```XML
       <security mode="None"/>
```

<span data-ttu-id="e32cb-237">Теперь приложение должно работать.</span><span class="sxs-lookup"><span data-stu-id="e32cb-237">Now, your application should run.</span></span> <span data-ttu-id="e32cb-238">На следующем рисунке показано, как приложение выглядит в пределах авебпажевис рукописного ввода, указанного в поле распознавания.</span><span class="sxs-lookup"><span data-stu-id="e32cb-238">The following image shows how the application looks within awebpagewith some handwriting entered into the recognition box.</span></span>

<span data-ttu-id="e32cb-239">![Приложение в авебпажевис. Некоторые рукописные данные, указанные в поле распознавания](images/demo-1.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-239">![Application within awebpagewith some handwriting entered into recognition box](images/demo-1.png)</span></span><br/>
<span data-ttu-id="e32cb-240">*Приложение в авебпажевис. Некоторые рукописные данные, указанные в поле распознавания*</span><span class="sxs-lookup"><span data-stu-id="e32cb-240">*Application within awebpagewith some handwriting entered into recognition box*</span></span>

<span data-ttu-id="e32cb-241">На следующем рисунке показан распознанный текст в раскрывающемся списке **результатов** .</span><span class="sxs-lookup"><span data-stu-id="e32cb-241">The following image shows the recognized text in the **Result** drop-down list.</span></span>

<span data-ttu-id="e32cb-242">![Приложение внутри авебпажевис распознанного текста в раскрывающемся списке результатов](images/demo-2.png)</span><span class="sxs-lookup"><span data-stu-id="e32cb-242">![Application within awebpagewith recognized text in result drop-down list](images/demo-2.png)</span></span><br/>
<span data-ttu-id="e32cb-243">*Приложение внутри авебпажевис распознанного текста в раскрывающемся списке результатов*</span><span class="sxs-lookup"><span data-stu-id="e32cb-243">*Application within awebpagewith recognized text in result drop-down list*</span></span>

 

 



