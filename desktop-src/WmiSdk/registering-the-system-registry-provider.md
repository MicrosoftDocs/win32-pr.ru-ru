---
description: Поставщик системного реестра регистрируется как часть процесса установки WMI в Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Регистрация поставщика системного реестра
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702003"
---
# <a name="registering-the-system-registry-provider"></a><span data-ttu-id="fe81f-103">Регистрация поставщика системного реестра</span><span class="sxs-lookup"><span data-stu-id="fe81f-103">Registering the System Registry Provider</span></span>

<span data-ttu-id="fe81f-104">Поставщик системного реестра регистрируется как часть процесса установки WMI в Windows.</span><span class="sxs-lookup"><span data-stu-id="fe81f-104">The System Registry provider is registered as part of the WMI installation process on Windows.</span></span> <span data-ttu-id="fe81f-105">Если вы используете другую платформу и хотите использовать поставщик системного реестра, необходимо сначала зарегистрировать поставщик, выполнив описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fe81f-105">If you are using another platform and want to use the System Registry provider, you must first register the provider yourself following the steps described below.</span></span>

<span data-ttu-id="fe81f-106">В следующей процедуре описывается регистрация поставщика системного реестра.</span><span class="sxs-lookup"><span data-stu-id="fe81f-106">The following procedure describes how to register the System Registry provider.</span></span>

<span data-ttu-id="fe81f-107">**Регистрация поставщика системного реестра**</span><span class="sxs-lookup"><span data-stu-id="fe81f-107">**To register the System Registry provider**</span></span>

1.  <span data-ttu-id="fe81f-108">Зарегистрируйте поставщик в качестве сервера COM.</span><span class="sxs-lookup"><span data-stu-id="fe81f-108">Register the provider as a COM server.</span></span>

    <span data-ttu-id="fe81f-109">При необходимости может потребоваться создать записи реестра.</span><span class="sxs-lookup"><span data-stu-id="fe81f-109">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="fe81f-110">Этот процесс применяется ко всем COM-серверам и не связан с WMI.</span><span class="sxs-lookup"><span data-stu-id="fe81f-110">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="fe81f-111">Дополнительные сведения см. в документации по [com](https://msdn.microsoft.com/library/aa139695.aspx) в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fe81f-111">For more information, see the [COM](https://msdn.microsoft.com/library/aa139695.aspx) documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

2.  <span data-ttu-id="fe81f-112">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) для описания реализации поставщика системного реестра.</span><span class="sxs-lookup"><span data-stu-id="fe81f-112">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the System Registry provider.</span></span>

    <span data-ttu-id="fe81f-113">Экземпляр [**\_ \_ Win32Provider**](--win32provider.md) описывает имя поставщика и его идентификатор класса (**CLSID**).</span><span class="sxs-lookup"><span data-stu-id="fe81f-113">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (**CLSID**).</span></span>

    <span data-ttu-id="fe81f-114">В следующем примере показано, как зарегистрировать [**\_ \_ Win32Provider**](--win32provider.md) в качестве свойства экземпляра, события или поставщика метода.</span><span class="sxs-lookup"><span data-stu-id="fe81f-114">The following example describes how to register [**\_\_Win32Provider**](--win32provider.md) as an instance property, event, or method provider.</span></span>

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  <span data-ttu-id="fe81f-115">Создайте один или несколько экземпляров классов, производных от класса [**\_ \_ провидеррегистратион**](--providerregistration.md) , чтобы описать логическую реализацию поставщика системного реестра.</span><span class="sxs-lookup"><span data-stu-id="fe81f-115">Create one or more instances of classes derived from the [**\_\_ProviderRegistration**](--providerregistration.md) class to describe the logical implementation of the System Registry provider.</span></span>

    <span data-ttu-id="fe81f-116">В зависимости от цели регистрации поставщика системного реестра можно создать один или несколько следующих классов.</span><span class="sxs-lookup"><span data-stu-id="fe81f-116">Depending on the purpose for which you are registering the System Registry provider, you can create one or more of the following classes.</span></span>

    [<span data-ttu-id="fe81f-117">**\_\_инстанцепровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="fe81f-117">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

    [<span data-ttu-id="fe81f-118">**\_\_пропертипровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="fe81f-118">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

    [<span data-ttu-id="fe81f-119">**\_\_евентпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="fe81f-119">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

    [<span data-ttu-id="fe81f-120">**\_\_месодпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="fe81f-120">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

    <span data-ttu-id="fe81f-121">В следующем примере кода MOF описывается, как можно зарегистрировать поставщик системного реестра в качестве экземпляра, свойства, события или поставщика метода.</span><span class="sxs-lookup"><span data-stu-id="fe81f-121">The following MOF code example describes how you can register the System Registry provider as an instance, property, event, or method provider.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  <span data-ttu-id="fe81f-122">Скомпилируйте MOF-файл с помощью компилятора MOF или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="fe81f-122">Compile the MOF file using the MOF compiler or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

<span data-ttu-id="fe81f-123">Файл режевент. mof, указанный в разделе WMI Windows SDK, содержит экземпляры [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) , необходимые для регистрации поставщика системных реестров в качестве поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="fe81f-123">The RegEvent.mof file provided in the WMI section of the Windows SDK contains the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) instances necessary to register the System Registry provider as an event provider.</span></span> <span data-ttu-id="fe81f-124">Дополнительные сведения о регистрации поставщика см. в статьях [Регистрация поставщика](registering-a-provider.md) и [Получение события WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="fe81f-124">For more information about registering a provider, see [Registering a Provider](registering-a-provider.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 



