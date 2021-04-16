---
description: Перед реализацией поставщика необходимо сначала зарегистрировать поставщик в WMI. Регистрация поставщика определяет тип поставщика и классы, которые поддерживает поставщик. Инструментарий WMI может обращаться только к зарегистрированным поставщикам.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Регистрация поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702560"
---
# <a name="registering-a-provider"></a><span data-ttu-id="75c76-105">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="75c76-105">Registering a Provider</span></span>

<span data-ttu-id="75c76-106">Перед реализацией поставщика необходимо сначала зарегистрировать поставщик в WMI.</span><span class="sxs-lookup"><span data-stu-id="75c76-106">Before implementing your provider, you should first register your provider with WMI.</span></span> <span data-ttu-id="75c76-107">Регистрация поставщика определяет тип поставщика и классы, которые поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="75c76-107">Registering the provider defines the type of the provider and the classes that the provider supports.</span></span> <span data-ttu-id="75c76-108">Инструментарий WMI может обращаться только к зарегистрированным поставщикам.</span><span class="sxs-lookup"><span data-stu-id="75c76-108">WMI can only access registered providers.</span></span>

> [!Note]  
> <span data-ttu-id="75c76-109">Дополнительные сведения о регистрации поставщика MI см. в разделе [практические руководства. Регистрация поставщика MI](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="75c76-109">For more information on registering an MI provider, see [How to: Register an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span></span>

 

<span data-ttu-id="75c76-110">Вы можете написать свой код поставщика перед регистрацией поставщика.</span><span class="sxs-lookup"><span data-stu-id="75c76-110">You can write your provider code before you register the provider.</span></span> <span data-ttu-id="75c76-111">Однако очень сложно отлаживать поставщик, не зарегистрированный в WMI.</span><span class="sxs-lookup"><span data-stu-id="75c76-111">However, it is very difficult to debug a provider that is not registered with WMI.</span></span> <span data-ttu-id="75c76-112">Определение интерфейсов для поставщика также помогает структурировать назначение и структуру поставщика.</span><span class="sxs-lookup"><span data-stu-id="75c76-112">Determining the interfaces for your provider also helps to outline the purpose and structure of a provider.</span></span> <span data-ttu-id="75c76-113">Поэтому регистрация поставщика помогает в проектировании поставщика.</span><span class="sxs-lookup"><span data-stu-id="75c76-113">Therefore, registering your provider helps you design your provider.</span></span>

<span data-ttu-id="75c76-114">Только администраторы могут регистрировать или удалять поставщик.</span><span class="sxs-lookup"><span data-stu-id="75c76-114">Only administrators can register or delete a provider.</span></span>

<span data-ttu-id="75c76-115">Поставщик должен быть зарегистрирован для всех различных типов функций поставщика, которые он выполняет.</span><span class="sxs-lookup"><span data-stu-id="75c76-115">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="75c76-116">Почти все поставщики предоставляют экземпляры классов, которые они определяют, но они также могут предоставлять данные свойств, методы, события или классы.</span><span class="sxs-lookup"><span data-stu-id="75c76-116">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="75c76-117">Поставщик также может быть зарегистрирован в качестве поставщика объекта события или поставщика счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="75c76-117">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span> <span data-ttu-id="75c76-118">Рекомендуется объединить все функциональные возможности поставщика в одном поставщике, а не иметь много отдельных поставщиков для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="75c76-118">It is recommended that you combine all provider functionality in one provider rather than having many separate providers for each type.</span></span> <span data-ttu-id="75c76-119">Примером является [поставщик системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider), предоставляющий методы и экземпляры, а также [поставщик дисковых квот](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), предоставляющий экземпляры, методы и события.</span><span class="sxs-lookup"><span data-stu-id="75c76-119">An example is the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which provides methods and instances, and the [Disk Quota provider](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), which supplies instances, methods, and events.</span></span>

<span data-ttu-id="75c76-120">Поставщик должен быть зарегистрирован для всех различных типов функций поставщика, которые он выполняет.</span><span class="sxs-lookup"><span data-stu-id="75c76-120">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="75c76-121">Почти все поставщики предоставляют экземпляры классов, которые они определяют, но они также могут предоставлять данные свойств, методы, события или классы.</span><span class="sxs-lookup"><span data-stu-id="75c76-121">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="75c76-122">Поставщик также может быть зарегистрирован в качестве поставщика объекта события или поставщика счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="75c76-122">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span>

<span data-ttu-id="75c76-123">Для каждого типа регистрации используется один и тот же экземпляр [**\_ \_ Win32Provider**](--win32provider.md) :</span><span class="sxs-lookup"><span data-stu-id="75c76-123">The same instance of [**\_\_Win32Provider**](--win32provider.md) is used for each type of registration:</span></span>

-   [<span data-ttu-id="75c76-124">Регистрация поставщика экземпляра</span><span class="sxs-lookup"><span data-stu-id="75c76-124">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
-   [<span data-ttu-id="75c76-125">Регистрация поставщика класса</span><span class="sxs-lookup"><span data-stu-id="75c76-125">Registering a Class Provider</span></span>](registering-a-class-provider.md)
-   [<span data-ttu-id="75c76-126">Регистрация поставщика методов</span><span class="sxs-lookup"><span data-stu-id="75c76-126">Registering a Method Provider</span></span>](registering-a-method-provider.md)
-   [<span data-ttu-id="75c76-127">Регистрация поставщика событий</span><span class="sxs-lookup"><span data-stu-id="75c76-127">Registering an Event Provider</span></span>](registering-an-event-provider.md)
-   [<span data-ttu-id="75c76-128">Регистрация поставщика событий-получателя</span><span class="sxs-lookup"><span data-stu-id="75c76-128">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
-   [<span data-ttu-id="75c76-129">Создание поставщика экземпляров в поставщике High-Performance</span><span class="sxs-lookup"><span data-stu-id="75c76-129">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a><span data-ttu-id="75c76-130">Пример. Создание и регистрация экземпляра поставщика</span><span class="sxs-lookup"><span data-stu-id="75c76-130">Example: Creating and Registering an Instance of a Provider</span></span>

<span data-ttu-id="75c76-131">В следующем примере показан MOF-файл, который создает и регистрирует экземпляр [поставщика системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="75c76-131">The following example shows a MOF file that creates and registers an instance of the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="75c76-132">Он назначает поставщику $Reg псевдонима, чтобы избежать длинного пути, необходимого для регистрации экземпляра и метода.</span><span class="sxs-lookup"><span data-stu-id="75c76-132">It assigns the alias $Reg to the provider to avoid the long pathname required in the instance and method registrations.</span></span> <span data-ttu-id="75c76-133">Дополнительные сведения см. в разделе [Создание псевдонима](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-133">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a><span data-ttu-id="75c76-134">Пример. Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="75c76-134">Example: Registering a Provider</span></span>

<span data-ttu-id="75c76-135">В следующей процедуре описывается регистрация поставщика.</span><span class="sxs-lookup"><span data-stu-id="75c76-135">The following procedure describes how to register a provider.</span></span>

<span data-ttu-id="75c76-136">**Регистрация поставщика**</span><span class="sxs-lookup"><span data-stu-id="75c76-136">**To register a provider**</span></span>

1.  <span data-ttu-id="75c76-137">Зарегистрируйте поставщик в качестве сервера COM.</span><span class="sxs-lookup"><span data-stu-id="75c76-137">Register the provider as a COM server.</span></span>

    <span data-ttu-id="75c76-138">При необходимости может потребоваться создать записи реестра.</span><span class="sxs-lookup"><span data-stu-id="75c76-138">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="75c76-139">Этот процесс применяется ко всем COM-серверам и не связан с WMI.</span><span class="sxs-lookup"><span data-stu-id="75c76-139">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="75c76-140">Дополнительные сведения см. в разделе COM документации по пакету Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="75c76-140">For more information, see the COM section in the Microsoft Windows Software Development Kit (SDK) documentation.</span></span>

2.  <span data-ttu-id="75c76-141">Создайте MOF-файл, содержащий экземпляры [**\_ \_ Win32Provider**](--win32provider.md) и экземпляр класса, производный непосредственно или косвенно от [**\_ \_ провидеррегистратион**](--providerregistration.md), например [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-141">Create a MOF file that contains instances of [**\_\_Win32Provider**](--win32provider.md) and an instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), such as [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="75c76-142">Только администраторы могут регистрировать или удалять поставщик, создавая экземпляры классов, производных от **\_ \_ Win32Provider** или [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-142">Only administrators can register or delete a provider by creating instances of classes derived from **\_\_Win32Provider** or [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>
3.  <span data-ttu-id="75c76-143">Задайте [**хостингмодел**](--win32provider.md) в экземпляре **\_ \_ Win32Provider** в соответствии со значениями в [моделях размещения](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-143">Set the [**HostingModel**](--win32provider.md) in the instance of **\_\_Win32Provider** according to the values in [Hosting models](provider-hosting-and-security.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="75c76-144">Если поставщик не требует высокой привилегий учетной записи LocalSystem, свойство [**\_ \_ Win32Provider. хостингмодел**](--win32provider.md) должно иметь значение "нетворксервицехост".</span><span class="sxs-lookup"><span data-stu-id="75c76-144">Unless the provider requires the high privileges of the LocalSystem account, the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property should be set to "NetworkServiceHost".</span></span> <span data-ttu-id="75c76-145">Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-145">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

     

    <span data-ttu-id="75c76-146">В следующем примере MOF из полного примера показан код, создающий экземпляр [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-146">The following MOF example from the full example shows the code that creates an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  <span data-ttu-id="75c76-147">Экземпляр класса, производного непосредственно или косвенно от [**\_ \_ провидеррегистратион**](--providerregistration.md), для описания логической реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="75c76-147">An instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), to describe the logical implementation of the provider.</span></span> <span data-ttu-id="75c76-148">Поставщик может быть зарегистрирован для нескольких различных типов функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="75c76-148">A provider can be registered for several different types of functionality.</span></span> <span data-ttu-id="75c76-149">В приведенном выше примере Регпров регистрируется как экземпляр и поставщик метода.</span><span class="sxs-lookup"><span data-stu-id="75c76-149">The example above registers RegProv as an instance and method provider.</span></span> <span data-ttu-id="75c76-150">Но если Регпров поддерживает функциональность, ее также можно зарегистрировать в качестве свойства или поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="75c76-150">But if RegProv supports the functionality, it could also be registered as a property or event provider.</span></span> <span data-ttu-id="75c76-151">В следующей таблице перечислены классы, которые регистрируют функциональность поставщика.</span><span class="sxs-lookup"><span data-stu-id="75c76-151">The following table lists the classes that register provider functionality.</span></span>

    

    | <span data-ttu-id="75c76-152">Классы регистрации поставщика</span><span class="sxs-lookup"><span data-stu-id="75c76-152">Provider registration classes</span></span>                                                        | <span data-ttu-id="75c76-153">Описание</span><span class="sxs-lookup"><span data-stu-id="75c76-153">Description</span></span>                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [<span data-ttu-id="75c76-154">**\_\_инстанцепровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="75c76-154">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)           | <span data-ttu-id="75c76-155">Регистрирует [поставщик экземпляра](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-155">Registers an [instance provider](registering-an-instance-provider.md).</span></span>             |
    | [<span data-ttu-id="75c76-156">**\_\_евентпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="75c76-156">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)                 | <span data-ttu-id="75c76-157">Регистрирует [поставщик событий](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-157">Registers an [event provider](registering-an-event-provider.md).</span></span>                   |
    | [<span data-ttu-id="75c76-158">**\_\_евентконсумерпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="75c76-158">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md) | <span data-ttu-id="75c76-159">Регистрирует [поставщик потребителей событий](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-159">Registers an [event consumer provider](registering-an-event-consumer-provider.md).</span></span> |
    | [<span data-ttu-id="75c76-160">**\_\_месодпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="75c76-160">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)               | <span data-ttu-id="75c76-161">Регистрирует [поставщик метода](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-161">Registers a [method provider](registering-an-event-consumer-provider.md).</span></span>          |
    | [<span data-ttu-id="75c76-162">**\_\_пропертипровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="75c76-162">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)           | <span data-ttu-id="75c76-163">Регистрирует [поставщик свойств](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-163">Registers a [property provider](registering-a-property-provider.md).</span></span>               |

    

     

5.  <span data-ttu-id="75c76-164">Поместите MOF-файл в постоянный каталог.</span><span class="sxs-lookup"><span data-stu-id="75c76-164">Place the MOF file into a permanent directory.</span></span>

    <span data-ttu-id="75c76-165">Как правило, файл следует поместить в каталог установки поставщика.</span><span class="sxs-lookup"><span data-stu-id="75c76-165">Typically, you should place the file in the installation directory of the provider.</span></span>

6.  <span data-ttu-id="75c76-166">Скомпилируйте MOF-файл с помощью [mofcomp](mofcomp.md) или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="75c76-166">Compile the MOF file using [mofcomp](mofcomp.md) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="75c76-167">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="75c76-167">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

    <span data-ttu-id="75c76-168">**Windows 8 и Windows Server 2012:** При установке поставщиков и [**mofcomp**](mofcomp.md) , и интерфейс [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) рассматривают \[ ключ \] и \[ статические \] Квалификаторы как true, если они есть, независимо от их реальных значений.</span><span class="sxs-lookup"><span data-stu-id="75c76-168">**Windows 8 and Windows Server 2012:** When installing providers, both [**mofcomp**](mofcomp.md) and the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface treat the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="75c76-169">Другие квалификаторы обрабатываются как false, если они есть, но не имеют явного значения true.</span><span class="sxs-lookup"><span data-stu-id="75c76-169">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75c76-170">См. также</span><span class="sxs-lookup"><span data-stu-id="75c76-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c76-171">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="75c76-171">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="75c76-172">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="75c76-172">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="75c76-173">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="75c76-173">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
