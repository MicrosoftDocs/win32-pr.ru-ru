---
description: Инструментарий WMI автоматически регистрирует библиотеку DLL поставщика представления в процессе установки WMI. Однако для каждого пространства имен, которое будет содержать классы представлений, по-прежнему необходимо зарегистрировать поставщик представления в инструментарии WMI.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Регистрация поставщика представления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703180"
---
# <a name="registering-the-view-provider"></a><span data-ttu-id="d0fe6-104">Регистрация поставщика представления</span><span class="sxs-lookup"><span data-stu-id="d0fe6-104">Registering the View Provider</span></span>

<span data-ttu-id="d0fe6-105">Инструментарий WMI автоматически регистрирует библиотеку DLL поставщика представления в процессе установки WMI.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-105">WMI automatically registers the View Provider DLL during the WMI installation process.</span></span> <span data-ttu-id="d0fe6-106">Однако для каждого пространства имен, которое будет содержать классы представлений, по-прежнему необходимо зарегистрировать поставщик представления в инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-106">However, you still need to register the View Provider with WMI for each namespace that will contain view classes.</span></span>

<span data-ttu-id="d0fe6-107">Следующая процедура описывает, как зарегистрировать поставщик представления.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-107">The following procedure describes how to register the View Provider.</span></span>

<span data-ttu-id="d0fe6-108">**Регистрация поставщика представления**</span><span class="sxs-lookup"><span data-stu-id="d0fe6-108">**To register the View Provider**</span></span>

1.  <span data-ttu-id="d0fe6-109">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) для описания реализации поставщика представления.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the View Provider.</span></span>

    <span data-ttu-id="d0fe6-110">Экземпляр [**\_ \_ Win32Provider**](--win32provider.md) описывает имя поставщика и его идентификатор класса (CLSID), а также параметры безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-110">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (CLSID), as well as the default security settings.</span></span>

    <span data-ttu-id="d0fe6-111">В следующем примере кода описывается реализация [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="d0fe6-111">The following code example describes an implementation of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  <span data-ttu-id="d0fe6-112">Создайте экземпляр класса [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="d0fe6-112">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

    <span data-ttu-id="d0fe6-113">В следующем примере кода показано, как создать экземпляр класса **\_ \_ инстанцепровидеррегистратион** .</span><span class="sxs-lookup"><span data-stu-id="d0fe6-113">The following code example shows how to create an instance of the **\_\_InstanceProviderRegistration** class.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  <span data-ttu-id="d0fe6-114">Создайте экземпляр класса [**\_ \_ месодпровидеррегистратион**](--methodproviderregistration.md) , если требуется, чтобы класс представления Union поддерживал методы.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-114">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class if you want to have your union view class support methods.</span></span>

    <span data-ttu-id="d0fe6-115">В следующем примере кода показано, как создать экземпляр класса **\_ \_ месодпровидеррегистратион** .</span><span class="sxs-lookup"><span data-stu-id="d0fe6-115">The following code example shows how to create an instance of the **\_\_MethodProviderRegistration** class.</span></span>

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  <span data-ttu-id="d0fe6-116">Скомпилируйте MOF-код с помощью компилятора MOF ([mofcomp](mofcomp.md)) или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="d0fe6-116">Compile your MOF code using the MOF compiler ([mofcomp](mofcomp.md)) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="d0fe6-117">Если вы сохраните приведенный выше пример MOF-кода в файл с именем Виевтест. mof, используйте команду mofcomp, чтобы загрузить MOF-код в целевое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-117">If you save the previously listed MOF code example into a file named Viewtest.mof, use the Mofcomp command to load the MOF code into the target namespace.</span></span> <span data-ttu-id="d0fe6-118">*Намеспацепас* — пространство имен, в котором нужно создать экземпляр класса представления.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-118">*NamespacePath* is the namespace in which you wish to create the view class instance.</span></span>

    <span data-ttu-id="d0fe6-119">Введите следующую команду в командной строке, чтобы загрузить MOF-код в целевое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-119">Type the following command at a command prompt to load the MOF code into the target namespace.</span></span>

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    <span data-ttu-id="d0fe6-120">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="d0fe6-120">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="d0fe6-121">Дополнительные сведения см. [в разделе Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d0fe6-121">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

 

 



