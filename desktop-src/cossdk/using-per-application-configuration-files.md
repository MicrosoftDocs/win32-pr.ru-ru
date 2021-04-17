---
description: Использование файлов конфигурации Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Использование файлов конфигурации Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692014"
---
# <a name="using-per-application-configuration-files"></a><span data-ttu-id="256bc-103">Использование файлов конфигурации Per-Application</span><span class="sxs-lookup"><span data-stu-id="256bc-103">Using Per-Application Configuration Files</span></span>

<span data-ttu-id="256bc-104">Для использования файлов конфигурации COM+ для каждого приложения необходимо выполнить следующие основные действия.</span><span class="sxs-lookup"><span data-stu-id="256bc-104">Using COM+ per-application configuration files requires the following basic steps:</span></span>

-   <span data-ttu-id="256bc-105">Настройка корневого каталога приложения для приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="256bc-105">Configure an application root directory for a COM+ application.</span></span>
-   <span data-ttu-id="256bc-106">Создайте файлы Application. manifest и application.config в корневом каталоге приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="256bc-106">Create application.manifest and application.config files in the COM+ application root directory.</span></span>

> [!Note]  
> <span data-ttu-id="256bc-107">Файлы конфигурации для каждого приложения доступны только начиная с Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="256bc-107">Per-application configuration files are only available starting with Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span>

 

<span data-ttu-id="256bc-108">**Использование файла конфигурации для каждого приложения**</span><span class="sxs-lookup"><span data-stu-id="256bc-108">**To use a per-application configuration file**</span></span>

1.  <span data-ttu-id="256bc-109">Создайте библиотеку классов .NET со ссылкой на сборку System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="256bc-109">Create a .NET class library, with a reference to the System.EnterpriseServices assembly.</span></span>

2.  <span data-ttu-id="256bc-110">Библиотека классов должна содержать следующий код:</span><span class="sxs-lookup"><span data-stu-id="256bc-110">The class library should contain the following code:</span></span>

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    <span data-ttu-id="256bc-111">Обратите внимание, что "ConfigData1" — это пример имени параметра.</span><span class="sxs-lookup"><span data-stu-id="256bc-111">Note that "ConfigData1" is a sample setting name.</span></span> <span data-ttu-id="256bc-112">Его можно заменить именем выбранного параметра.</span><span class="sxs-lookup"><span data-stu-id="256bc-112">You can replace this with the setting name of your choice.</span></span>

3.  <span data-ttu-id="256bc-113">Создайте пустое приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="256bc-113">Create an empty COM+ application.</span></span> <span data-ttu-id="256bc-114">Инструкции по выполнению этой задачи см. в разделе [Создание нового приложения COM+](creating-a-new-com--application.md).</span><span class="sxs-lookup"><span data-stu-id="256bc-114">For instructions on how to do this, see [Creating a New COM+ Application](creating-a-new-com--application.md).</span></span>
4.  <span data-ttu-id="256bc-115">Установите библиотеку классов, созданную в приложении COM+.</span><span class="sxs-lookup"><span data-stu-id="256bc-115">Install the class library you created into the COM+ application.</span></span> <span data-ttu-id="256bc-116">Инструкции по выполнению этой задачи см. в разделе [Установка новых компонентов](installing-new-components.md).</span><span class="sxs-lookup"><span data-stu-id="256bc-116">For instructions on how to do this, see [Installing New Components](installing-new-components.md).</span></span>
5.  <span data-ttu-id="256bc-117">В средстве администрирования "службы компонентов" щелкните правой кнопкой мыши созданное приложение COM+ и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="256bc-117">In the Component Services administrative tool, right-click the COM+ application you created and select **Properties**.</span></span>
6.  <span data-ttu-id="256bc-118">В диалоговом окне **Свойства** перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="256bc-118">In the **Properties** dialog box, select the **Activation** tab.</span></span>
7.  <span data-ttu-id="256bc-119">Убедитесь, что для параметра **тип активации** задано значение **серверное приложение**.</span><span class="sxs-lookup"><span data-stu-id="256bc-119">Make sure the **Activation type** is set to **Server application**.</span></span>
8.  <span data-ttu-id="256bc-120">В текстовом поле **корневой каталог приложения** введите путь или перейдите к каталогу, в котором вы хотите сохранить файлы конфигурации приложения для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="256bc-120">In the **Application Root Directory** text box, enter the path or browse to the directory where you want to store your application configuration files for this application.</span></span>
9.  <span data-ttu-id="256bc-121">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="256bc-121">Click **OK**.</span></span>

    <span data-ttu-id="256bc-122">Обратите внимание, что корневой каталог приложения COM+ можно также указать с помощью свойства Аппликатиондиректори класса [**комадминкаталогобжект**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="256bc-122">Note that you can also specify the COM+ application root directory through the ApplicationDirectory property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="256bc-123">Дополнительные сведения см. в разделе [**приложения**](applications.md).</span><span class="sxs-lookup"><span data-stu-id="256bc-123">For more information, see [**Applications**](applications.md).</span></span>

10. <span data-ttu-id="256bc-124">В каталоге, выбранном для хранения файлов конфигурации приложения, создайте файл с именем *Application*. manifest.</span><span class="sxs-lookup"><span data-stu-id="256bc-124">In the directory you chose to store your application configuration files, create a file named *application*.manifest.</span></span> <span data-ttu-id="256bc-125">В текстовом редакторе добавьте в этот файл следующий текст:</span><span class="sxs-lookup"><span data-stu-id="256bc-125">With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. <span data-ttu-id="256bc-126">В том же каталоге создайте файл с именем *Application*. config. В текстовом редакторе добавьте в этот файл следующий текст:</span><span class="sxs-lookup"><span data-stu-id="256bc-126">In the same directory, create a file named *application*.config. With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    <span data-ttu-id="256bc-127">Обратите внимание, что этот файл конфигурации является всего лишь примером.</span><span class="sxs-lookup"><span data-stu-id="256bc-127">Note that this configuration file is just an example.</span></span> <span data-ttu-id="256bc-128">Можно создать несколько ключей с разными именами и значениями.</span><span class="sxs-lookup"><span data-stu-id="256bc-128">You can create multiple keys with different names and values.</span></span> <span data-ttu-id="256bc-129">Однако обратите внимание, что "ConfigData1" соответствует имени параметра, используемого в библиотеке классов, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="256bc-129">Note, however, that "ConfigData1" matches the setting name used in the class library created earlier.</span></span>

12. <span data-ttu-id="256bc-130">Создайте консольное приложение .NET со ссылкой на созданную ранее библиотеку классов .NET и ссылку на сборку System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="256bc-130">Create a .NET console application, with a reference to the .NET class library you created earlier, and a reference to the System.EnterpriseServices assembly.</span></span>
13. <span data-ttu-id="256bc-131">Консольное приложение должно содержать следующий код:</span><span class="sxs-lookup"><span data-stu-id="256bc-131">The console application should contain the following code:</span></span>
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

<span data-ttu-id="256bc-132">Запустите консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="256bc-132">Run the console application.</span></span> <span data-ttu-id="256bc-133">Результат должен выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="256bc-133">The output should be:</span></span>

``` syntax
Configuration Data Number 1
```

 

 



