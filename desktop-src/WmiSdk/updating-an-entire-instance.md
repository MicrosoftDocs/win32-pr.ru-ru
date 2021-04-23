---
description: Наиболее распространенным способом обновления экземпляра класса WMI является обновление всего экземпляра.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Обновление всего экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265594"
---
# <a name="updating-an-entire-instance"></a><span data-ttu-id="fa551-103">Обновление всего экземпляра</span><span class="sxs-lookup"><span data-stu-id="fa551-103">Updating an Entire Instance</span></span>

<span data-ttu-id="fa551-104">Наиболее распространенным способом обновления экземпляра класса WMI является обновление всего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fa551-104">The most common means of updating a WMI class instance is to update the entire instance at once.</span></span> <span data-ttu-id="fa551-105">При обновлении всего экземпляра Инструментарий WMI не нужно анализировать экземпляр в отдельные свойства и передавать его в приложение.</span><span class="sxs-lookup"><span data-stu-id="fa551-105">By updating an entire instance, WMI does not have to parse the instance into individual properties and send them to your application.</span></span> <span data-ttu-id="fa551-106">Вместо этого инструментарий WMI может просто отправить вам весь экземпляр.</span><span class="sxs-lookup"><span data-stu-id="fa551-106">Instead, WMI can simply send you the entire instance.</span></span> <span data-ttu-id="fa551-107">По завершении Инструментарий WMI может скопировать весь измененный экземпляр по исходному экземпляру.</span><span class="sxs-lookup"><span data-stu-id="fa551-107">When you finish, WMI can then copy your entire changed instance over the original instance.</span></span>

<span data-ttu-id="fa551-108">Следующая процедура описывает, как изменить или обновить экземпляр с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fa551-108">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

<span data-ttu-id="fa551-109">**Изменение или обновление экземпляра с помощью PowerShell**</span><span class="sxs-lookup"><span data-stu-id="fa551-109">**To modify or update an instance using PowerShell**</span></span>

1.  <span data-ttu-id="fa551-110">Получите локальную копию объекта с помощью вызова Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="fa551-110">Retrieve a local copy of the object with a call to Get-WmiObject.</span></span>

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  <span data-ttu-id="fa551-111">При необходимости просмотрите свойства объекта, вызвав коллекцию Properties.</span><span class="sxs-lookup"><span data-stu-id="fa551-111">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="fa551-112">Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.</span><span class="sxs-lookup"><span data-stu-id="fa551-112">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  <span data-ttu-id="fa551-113">Внесите любые изменения в свойства локального объекта.</span><span class="sxs-lookup"><span data-stu-id="fa551-113">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="fa551-114">Это изменит только локальную копию.</span><span class="sxs-lookup"><span data-stu-id="fa551-114">Doing so changes only the local copy.</span></span> <span data-ttu-id="fa551-115">Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="fa551-115">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  <span data-ttu-id="fa551-116">Поместите объект обратно в репозиторий WMI, используя вызов метода размещения.</span><span class="sxs-lookup"><span data-stu-id="fa551-116">Place the object back into the WMI repository using a call to the Put method.</span></span>

    ```PowerShell
    $mySettings.Put()
    ```

    

<span data-ttu-id="fa551-117">Следующая процедура описывает, как изменить или обновить экземпляр с помощью C#.</span><span class="sxs-lookup"><span data-stu-id="fa551-117">The following procedure describes how to modify or update an instance using C#.</span></span>

<span data-ttu-id="fa551-118">**Изменение или обновление экземпляра с помощью C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="fa551-118">**To modify or update an instance using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="fa551-119">Получите локальную копию объекта с помощью вызова [CimSession.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85))GetObject, как описано в статье [Получение экземпляра WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="fa551-119">Retrieve a local copy of the object with a call to [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), as described in [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  <span data-ttu-id="fa551-120">При необходимости просмотрите свойства объекта, вызвав коллекцию Properties.</span><span class="sxs-lookup"><span data-stu-id="fa551-120">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="fa551-121">Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.</span><span class="sxs-lookup"><span data-stu-id="fa551-121">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="fa551-122">Внесите любые изменения в свойства локального объекта.</span><span class="sxs-lookup"><span data-stu-id="fa551-122">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="fa551-123">Это изменит только локальную копию.</span><span class="sxs-lookup"><span data-stu-id="fa551-123">Doing so changes only the local copy.</span></span> <span data-ttu-id="fa551-124">Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="fa551-124">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  <span data-ttu-id="fa551-125">Поместите объект обратно в репозиторий WMI с помощью вызова [CimSession. модифинстанце](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa551-125">Place the object back into the WMI repository using a call to [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span></span>

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

<span data-ttu-id="fa551-126">Следующая процедура описывает, как изменить или обновить экземпляр с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fa551-126">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

> [!Note]  
> <span data-ttu-id="fa551-127">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="fa551-127">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="fa551-128">**Изменение или обновление экземпляра с помощью C# (Microsoft. Management)**</span><span class="sxs-lookup"><span data-stu-id="fa551-128">**To modify or update an instance using C# (Microsoft.Management)**</span></span>

1.  <span data-ttu-id="fa551-129">Получите локальную копию объекта с помощью вызова [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="fa551-129">Retrieve a local copy of the object with a call to [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  <span data-ttu-id="fa551-130">При необходимости просмотрите свойства объекта, вызвав коллекцию Properties.</span><span class="sxs-lookup"><span data-stu-id="fa551-130">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="fa551-131">Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.</span><span class="sxs-lookup"><span data-stu-id="fa551-131">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="fa551-132">Внесите любые изменения в свойства локального объекта.</span><span class="sxs-lookup"><span data-stu-id="fa551-132">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="fa551-133">Это изменит только локальную копию.</span><span class="sxs-lookup"><span data-stu-id="fa551-133">Doing so changes only the local copy.</span></span> <span data-ttu-id="fa551-134">Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="fa551-134">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  <span data-ttu-id="fa551-135">Поместите объект обратно в репозиторий WMI, используя вызов метода [ManagementObject.](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) Place или.</span><span class="sxs-lookup"><span data-stu-id="fa551-135">Place the object back into the WMI repository using a call to the [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) or method.</span></span>

    ```CSharp
    myDisk.Put();
    ```

    

<span data-ttu-id="fa551-136">Следующая процедура описывает, как изменить или обновить экземпляр с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="fa551-136">The following procedure describes how to modify or update an instance using VBScript.</span></span>

<span data-ttu-id="fa551-137">**Изменение или обновление экземпляра с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="fa551-137">**To modify or update an instance using VBScript**</span></span>

1.  <span data-ttu-id="fa551-138">Получите локальную копию объекта с помощью вызова **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="fa551-138">Retrieve a local copy of the object with a call to **GetObject**.</span></span>
2.  <span data-ttu-id="fa551-139">При необходимости просмотрите свойства объекта, вызвав метод [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="fa551-139">If necessary, view the properties of the object with a call to the [**Properties\_**](swbemobject-properties-.md) method.</span></span>

    <span data-ttu-id="fa551-140">Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.</span><span class="sxs-lookup"><span data-stu-id="fa551-140">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="fa551-141">Внесите любые изменения в свойства объекта с помощью вызова метода [**SWbemProperty. Value**](swbemproperty-value.md) .</span><span class="sxs-lookup"><span data-stu-id="fa551-141">Make any changes to the object properties with a call to the [**SWbemProperty.Value**](swbemproperty-value.md) method.</span></span>

    <span data-ttu-id="fa551-142">Метод **value** изменяет только локальную копию.</span><span class="sxs-lookup"><span data-stu-id="fa551-142">The **Value** method changes only the local copy.</span></span> <span data-ttu-id="fa551-143">Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="fa551-143">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="fa551-144">Поместите объект обратно в репозиторий WMI, вызвав методы [**SWbemObject. \_**](swbemobject-put-.md) Place или [**SWbemObject. путасинк \_**](swbemobject-putasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="fa551-144">Place the object back into the WMI repository with a call the [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md) methods.</span></span>

<span data-ttu-id="fa551-145">Как предполагается в именах, [**помещайте \_**](swbemobject-put-.md) обновления синхронно, а обновления [**путасинк \_**](swbemobject-putasync-.md) асинхронно.</span><span class="sxs-lookup"><span data-stu-id="fa551-145">As the names imply, [**Put\_**](swbemobject-put-.md) updates synchronously while [**PutAsync\_**](swbemobject-putasync-.md) updates asynchronously.</span></span> <span data-ttu-id="fa551-146">Любой метод копирует поверх исходного экземпляра с измененным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="fa551-146">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="fa551-147">Однако, чтобы воспользоваться преимуществами асинхронной обработки, необходимо создать объект [**свбемсинк**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="fa551-147">However, to take advantage of asynchronous processing, you must create an [**SWbemSink**](swbemsink.md) object.</span></span> <span data-ttu-id="fa551-148">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa551-148">For more information, see [Calling a method](calling-a-method.md).</span></span>

<span data-ttu-id="fa551-149">Следующая процедура описывает, как изменить или обновить экземпляр с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="fa551-149">The following procedure describes how to modify or update an instance using C++.</span></span>

<span data-ttu-id="fa551-150">**Изменение или обновление экземпляра с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="fa551-150">**To modify or update an instance using C++**</span></span>

1.  <span data-ttu-id="fa551-151">Получите локальную копию экземпляра с вызовом [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="fa551-151">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>
2.  <span data-ttu-id="fa551-152">При необходимости просмотрите свойства объекта, вызвав метод [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span><span class="sxs-lookup"><span data-stu-id="fa551-152">If necessary, view the properties of the object with a call to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span></span>

    <span data-ttu-id="fa551-153">Хотя это и не является обязательным, может потребоваться знание значения свойства перед его изменением.</span><span class="sxs-lookup"><span data-stu-id="fa551-153">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="fa551-154">Внесите необходимые изменения в копию с помощью вызова [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="fa551-154">Make any necessary changes to the copy with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="fa551-155">Метод **размещения** изменяет только локальную копию.</span><span class="sxs-lookup"><span data-stu-id="fa551-155">The **Put** method changes only the local copy.</span></span> <span data-ttu-id="fa551-156">Чтобы сохранить изменения в инструментарии WMI, необходимо поместить всю копию обратно в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="fa551-156">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="fa551-157">Поместите копию обратно в репозиторий WMI, вызвав методы [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="fa551-157">Place your copy back into the WMI repository with a call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) methods.</span></span>

    <span data-ttu-id="fa551-158">Как предполагается в именах, **PutInstance** обновляется синхронно, а [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) обновляется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="fa551-158">As the names imply, **PutInstance** updates synchronously while [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) updates asynchronously.</span></span> <span data-ttu-id="fa551-159">Любой метод копирует поверх исходного экземпляра с измененным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="fa551-159">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="fa551-160">Однако, чтобы воспользоваться преимуществами асинхронной обработки, необходимо реализовать интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="fa551-160">However, to take advantage of asynchronous processing, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="fa551-161">Следует иметь в виду, что операция обновления экземпляра, принадлежащего к иерархии классов, может не быть выполнена из-за ошибки, связанной с другим классом в иерархии.</span><span class="sxs-lookup"><span data-stu-id="fa551-161">You should be aware that an update operation on an instance belonging to a class hierarchy might not succeed due to an error involving another class in the hierarchy.</span></span> <span data-ttu-id="fa551-162">Инструментарий WMI вызывает метод [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) каждого из поставщиков, ответственных за классы, от которых наследуется исходный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="fa551-162">WMI calls the [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method of each of the providers responsible for the classes from which the class owning the original instance derives.</span></span> <span data-ttu-id="fa551-163">В случае сбоя любого из этих поставщиков исходный запрос на обновление завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fa551-163">If any of these providers fail, the original update request fails.</span></span> <span data-ttu-id="fa551-164">Дополнительные сведения см. в подразделе "Примечания" раздела [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="fa551-164">For more information, see the Remarks section of [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

<span data-ttu-id="fa551-165">Дополнительные сведения см. [в разделе вызов метода поставщика](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa551-165">For more information, see [Calling a Provider Method](calling-a-provider-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="fa551-166">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="fa551-166">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="fa551-167">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa551-167">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 
