---
description: Иногда может потребоваться обновить только часть экземпляра.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Обновление части экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701934"
---
# <a name="updating-part-of-an-instance"></a><span data-ttu-id="d16de-103">Обновление части экземпляра</span><span class="sxs-lookup"><span data-stu-id="d16de-103">Updating Part of an Instance</span></span>

<span data-ttu-id="d16de-104">Иногда может потребоваться обновить только часть экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d16de-104">Occasionally, you may want to update only part of an instance.</span></span> <span data-ttu-id="d16de-105">Например, некоторые экземпляры имеют большое количество свойств.</span><span class="sxs-lookup"><span data-stu-id="d16de-105">For example, some instances have a large number of properties.</span></span> <span data-ttu-id="d16de-106">Если вам пришлось обновлять большое количество этих экземпляров, производительность системы может снизиться.</span><span class="sxs-lookup"><span data-stu-id="d16de-106">If you had to update a large number of these instances, you may reduce system performance.</span></span> <span data-ttu-id="d16de-107">Таким образом, можно обновить только часть экземпляра и, таким образом, сократить объем информации, которую необходимо отправить и получить из WMI.</span><span class="sxs-lookup"><span data-stu-id="d16de-107">Therefore, you can choose to update only part of the instance, and thus reduce the amount of information you must send and retrieve to and from WMI.</span></span> <span data-ttu-id="d16de-108">Однако Инструментарий WMI напрямую не поддерживает операции с частичным экземпляром и большинство поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d16de-108">However, WMI does not directly support partial-instance operations, nor do most providers.</span></span> <span data-ttu-id="d16de-109">Таким образом, при написании приложения, использующего операции с частичным экземпляром, необходимо подготовиться к сбою вызовов с помощью **\_ \_ \_ неподдерживаемого** поставщика WBEM e или WBEM e, не **\_ \_ \_ \_ поддерживающего** код ошибки в C++.</span><span class="sxs-lookup"><span data-stu-id="d16de-109">Therefore, if you write an application that uses partial-instance operations, be prepared for your calls to fail with either the **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** or **WBEM\_E\_NOT\_SUPPORTED** error code in C++.</span></span> <span data-ttu-id="d16de-110">В языках сценариев коды ошибок могут быть либо **вбемеррпровидерноткапабле** , либо **вбемеррнотсуппортед**.</span><span class="sxs-lookup"><span data-stu-id="d16de-110">In scripting languages the error codes are either **wbemErrProviderNotCapable** or **wbemErrNotSupported**.</span></span>

<span data-ttu-id="d16de-111">В сценариях эта операция необходима только для повышения производительности при обновлении одного или двух записываемых свойств в очень большом количестве объектов на предприятии.</span><span class="sxs-lookup"><span data-stu-id="d16de-111">In scripting, this operation is only necessary to aid performance when updating one or two writeable properties in a very large number of objects over an enterprise.</span></span> <span data-ttu-id="d16de-112">В противном случае стандартный вызов VBScript к [**SWbemObject. \_**](swbemobject-put-.md) WHERE или [**SWbemObject. \_ путасинк**](swbemobject-putasync-.md), в то время как записывает весь объект, фактически обновляет только те свойства, для которых у поставщика есть доступ на запись.</span><span class="sxs-lookup"><span data-stu-id="d16de-112">Otherwise, the normal VBScript calls to [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md), while seeming to write the entire object, are actually only updating the properties which the provider has write-enabled.</span></span>

<span data-ttu-id="d16de-113">Следующая процедура описывает, как запросить обновление частичного экземпляра с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d16de-113">The following procedure describes how to request a partial-instance update using PowerShell.</span></span>

<span data-ttu-id="d16de-114">**Запрос обновления частичного экземпляра с помощью PowerShell**</span><span class="sxs-lookup"><span data-stu-id="d16de-114">**To request a partial-instance update using PowerShell**</span></span>

1.  <span data-ttu-id="d16de-115">Получите путь к объекту, который вы хотите обновить.</span><span class="sxs-lookup"><span data-stu-id="d16de-115">Retrieve the path of the object you wish to update.</span></span>

    <span data-ttu-id="d16de-116">Путь можно описать вручную или, в противном случае, запросить объект и получить свойство **\_ \_ path** .</span><span class="sxs-lookup"><span data-stu-id="d16de-116">You can describe the path either manually, or else query the object and then retrieve the **\_\_Path** property.</span></span>

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  <span data-ttu-id="d16de-117">Настройте хэш-таблицу, в которой перечислены имена обновляемых свойств, и используйте эту хэш-таблицу в вызове [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="d16de-117">Set up a hash table listing the names of the properties to be updated, and use this hash table in a call to [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

<span data-ttu-id="d16de-118">Следующая процедура описывает, как запросить обновление частичного экземпляра с помощью C#.</span><span class="sxs-lookup"><span data-stu-id="d16de-118">The following procedure describes how to request a partial-instance update using C#.</span></span>

> [!Note]  
> <span data-ttu-id="d16de-119">**System. Management** является исходным пространством имен .NET, используемым для доступа к WMI; Однако интерфейсы API в этом пространстве имен обычно выполняются медленнее и не масштабируются по сравнению с более современными аналогами **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="d16de-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="d16de-120">**Запрос обновления частичного экземпляра с помощью C #**</span><span class="sxs-lookup"><span data-stu-id="d16de-120">**To request a partial-instance update using C#**</span></span>

1.  <span data-ttu-id="d16de-121">Создайте новый объект [ManagementObject](/dotnet/api/system.management.managementobject) , представляющий конкретный экземпляр для обновления.</span><span class="sxs-lookup"><span data-stu-id="d16de-121">Create a new [ManagementObject](/dotnet/api/system.management.managementobject) object that represents the specific instance to update.</span></span>

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  <span data-ttu-id="d16de-122">Задайте значение свойства с помощью вызова [ManagementObject. сетпропертивалуе](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span><span class="sxs-lookup"><span data-stu-id="d16de-122">Set the property value with a call to [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span></span>

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

<span data-ttu-id="d16de-123">Следующая процедура описывает, как запросить обновление частичного экземпляра с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="d16de-123">The following procedure describes how to request a partial-instance update using VBScript.</span></span>

<span data-ttu-id="d16de-124">**Запрос обновления частичного экземпляра с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="d16de-124">**To request a partial-instance update using VBScript**</span></span>

1.  <span data-ttu-id="d16de-125">Создайте объект контекста [**свбемнамедвалуесет**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="d16de-125">Create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object.</span></span>

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  <span data-ttu-id="d16de-126">Добавьте значения расширения " \_ \_ Размещение \_ расширений" и " \_ \_ разместить запрос на \_ \_ клиенте ext \_ " в объект контекста с помощью метода [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="d16de-126">Add the Put extension values "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" to the context object using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span>

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  <span data-ttu-id="d16de-127">Настройте массив, в котором перечислены имена обновляемых свойств, и добавьте этот массив в объект контекста [**свбемнамедвалуесет**](swbemnamedvalueset.md) с помощью параметра размещения расширения " \_ \_ Вставить \_ ext \_ Properties".</span><span class="sxs-lookup"><span data-stu-id="d16de-127">Set up an array listing the names of the properties to be updated and add this array to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object with the Put extension value "\_\_PUT\_EXT\_PROPERTIES".</span></span>

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  <span data-ttu-id="d16de-128">Задайте параметр *ифлагс* вызова [**SWbemObject \_ .**](swbemobject-put-.md) Set в **вбемчанжефлагупдатеонли**.</span><span class="sxs-lookup"><span data-stu-id="d16de-128">Set the *iFlags* parameter of the [**SWbemObject.Put\_**](swbemobject-put-.md) call to **wbemChangeFlagUpdateOnly**.</span></span> <span data-ttu-id="d16de-129">Без этого флага вызов завершится ошибкой с недопустимым контекстом.</span><span class="sxs-lookup"><span data-stu-id="d16de-129">Without this flag the call will fail with an invalid context.</span></span>

5.  <span data-ttu-id="d16de-130">Передайте объект флага и контекст поставщику в параметре *обжвбемнамедвалуесет* либо [**SWbemObject \_ .**](swbemobject-put-.md) WHERE, либо [**SWbemObject. путасинк \_**](swbemobject-putasync-.md).</span><span class="sxs-lookup"><span data-stu-id="d16de-130">Pass your flag and context object to the provider in the *objwbemNamedValueSet* parameter of either [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md).</span></span>

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

<span data-ttu-id="d16de-131">Следующая процедура описывает, как запросить обновление частичного экземпляра с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="d16de-131">The following procedure describes how to request a partial-instance update using C++.</span></span>

<span data-ttu-id="d16de-132">**Запрос обновления частичного экземпляра с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="d16de-132">**To request a partial-instance update using C++**</span></span>

1.  <span data-ttu-id="d16de-133">Создайте объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) с вызовом [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="d16de-133">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="d16de-134">Объект контекста — это объект, который WMI использует для передачи дополнительных сведений поставщику WMI.</span><span class="sxs-lookup"><span data-stu-id="d16de-134">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="d16de-135">В этом случае вы используете объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , чтобы дать поставщику возможность принимать обновления частичного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d16de-135">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to accept partial-instance updates.</span></span>

2.  <span data-ttu-id="d16de-136">Добавьте \_ \_ \_ именованные значения "помещает расширения" и " \_ \_ поместить \_ ext \_ Client \_ request" в объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) с помощью вызова [**ивбемконтекст:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="d16de-136">Add the "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" named values to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="d16de-137">В следующей таблице перечислены значения " \_ \_ Размещение \_ расширений" и " \_ \_ Размещение \_ ext \_ \_ WebRequest Client".</span><span class="sxs-lookup"><span data-stu-id="d16de-137">The following table lists the meaning of "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST".</span></span>

    

    | <span data-ttu-id="d16de-138">Именованное значение</span><span class="sxs-lookup"><span data-stu-id="d16de-138">Named value</span></span>                     | <span data-ttu-id="d16de-139">Описание</span><span class="sxs-lookup"><span data-stu-id="d16de-139">Description</span></span>                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d16de-140">" \_ \_ Размещение \_ расширений"</span><span class="sxs-lookup"><span data-stu-id="d16de-140">"\_\_PUT\_EXTENSIONS"</span></span>           | <span data-ttu-id="d16de-141">**VT \_ Для BOOL** задано значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d16de-141">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="d16de-142">Значение, указывающее, что было указано одно или несколько других значений контекста.</span><span class="sxs-lookup"><span data-stu-id="d16de-142">A value indicating that one or more of the other context values has been specified.</span></span> <span data-ttu-id="d16de-143">Это позволяет быстро проверить объект контекста в поставщике, чтобы определить, используются ли обновления частичного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d16de-143">This allows a quick check of the context object inside the provider to determine if partial-instance updates are being used.</span></span> |
    | <span data-ttu-id="d16de-144">" \_ \_ Размещение \_ ext \_ Client \_ request"</span><span class="sxs-lookup"><span data-stu-id="d16de-144">"\_\_PUT\_EXT\_CLIENT\_REQUEST"</span></span> | <span data-ttu-id="d16de-145">**VT \_ Для BOOL** задано значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d16de-145">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="d16de-146">Задается клиентом во время первоначального запроса.</span><span class="sxs-lookup"><span data-stu-id="d16de-146">Set by the client during the initial request.</span></span> <span data-ttu-id="d16de-147">Это значение используется для предотвращения ошибок повторного входа.</span><span class="sxs-lookup"><span data-stu-id="d16de-147">This value is used to prevent reentrancy errors.</span></span>                                                                                                                   |

    

     

3.  <span data-ttu-id="d16de-148">Добавьте к \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ объекту [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) в любом сочетании с другим вызовом метода [**ивбемконтекст:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue), добавить свойства "поместить ext", "разместить ВДЛ", "вставить ext" или "вставить ext Atomic".</span><span class="sxs-lookup"><span data-stu-id="d16de-148">Add the \_\_PUT\_EXT\_STRICT\_NULLS, \_\_PUT\_EXT\_PROPERTIES, or \_\_PUT\_EXT\_ATOMIC in any combination as needed to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with another call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="d16de-149">В следующей таблице перечислены значения именованных значений.</span><span class="sxs-lookup"><span data-stu-id="d16de-149">The following table lists the meaning of the named values.</span></span>

    

    | <span data-ttu-id="d16de-150">Именованное значение</span><span class="sxs-lookup"><span data-stu-id="d16de-150">Named value</span></span>                   | <span data-ttu-id="d16de-151">Описание</span><span class="sxs-lookup"><span data-stu-id="d16de-151">Description</span></span>                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d16de-152">" \_ \_ поставьте \_ ext в \_ \_ значения NULL"</span><span class="sxs-lookup"><span data-stu-id="d16de-152">"\_\_PUT\_EXT\_STRICT\_NULLS"</span></span> | <span data-ttu-id="d16de-153">**VT \_ Для BOOL** задано значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d16de-153">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="d16de-154">Указывает, что клиент намеренно установил свойства **VT \_ null** и ждет, что операция записи будет выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d16de-154">Indicates that the client has intentionally set properties to **VT\_NULL** and expects the write operation to succeed.</span></span> <span data-ttu-id="d16de-155">Если поставщик не может присвоить значения **null**, следует сообщить об ошибке.</span><span class="sxs-lookup"><span data-stu-id="d16de-155">If the provider cannot set the values to **NULL**, an error should be reported.</span></span> |
    | <span data-ttu-id="d16de-156">" \_ \_ Вставить \_ ext \_ Properties"</span><span class="sxs-lookup"><span data-stu-id="d16de-156">"\_\_PUT\_EXT\_PROPERTIES"</span></span>    | <span data-ttu-id="d16de-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) строк, содержащих список обновляемых имен свойств.</span><span class="sxs-lookup"><span data-stu-id="d16de-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings containing a list of property names to be updated.</span></span> <span data-ttu-id="d16de-158">Может использоваться отдельно или в сочетании со \_ \_ \_ свойством "вставить ext \_ ".</span><span class="sxs-lookup"><span data-stu-id="d16de-158">May be used alone or in combination with "\_\_PUT\_EXT\_PROPERTIES".</span></span> <span data-ttu-id="d16de-159">Значения находятся в записываемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="d16de-159">The values are in the instance being written.</span></span>                           |
    | <span data-ttu-id="d16de-160">" \_ \_ помещает \_ ext \_ Atomic"</span><span class="sxs-lookup"><span data-stu-id="d16de-160">"\_\_PUT\_EXT\_ATOMIC"</span></span>        | <span data-ttu-id="d16de-161">**VT \_ Для BOOL** задано значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d16de-161">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="d16de-162">Указывает, что все обновления должны выполняться одновременно (атомарная семантика) или поставщик должен вернуться обратно.</span><span class="sxs-lookup"><span data-stu-id="d16de-162">Indicates that all updates must succeed simultaneously (atomic semantics) or the provider must revert back.</span></span> <span data-ttu-id="d16de-163">Частичный результат не может быть успешным.</span><span class="sxs-lookup"><span data-stu-id="d16de-163">There can be no partial success.</span></span> <span data-ttu-id="d16de-164">Может использоваться отдельно или в сочетании с другими флагами.</span><span class="sxs-lookup"><span data-stu-id="d16de-164">May be used alone or in combination with other flags.</span></span>     |

    

     

4.  <span data-ttu-id="d16de-165">Установите параметр *ифлагс* в значение **\_ \_ \_ только обновление флагов WBEM**.</span><span class="sxs-lookup"><span data-stu-id="d16de-165">Set the *iFlags* parameter to **WBEM\_FLAG\_UPDATE\_ONLY**.</span></span> <span data-ttu-id="d16de-166">Без этого флага вызов завершится ошибкой с недопустимым контекстом.</span><span class="sxs-lookup"><span data-stu-id="d16de-166">Without this flag the call will fail with an invalid context.</span></span>
5.  <span data-ttu-id="d16de-167">Передайте объект контекста [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) в любые вызовы [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) в параметре *пкткс* .</span><span class="sxs-lookup"><span data-stu-id="d16de-167">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) in the *pCtx* parameter.</span></span>

    <span data-ttu-id="d16de-168">Передача объекта [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) дает поставщику разрешение на обновление частичного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d16de-168">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance updates.</span></span> <span data-ttu-id="d16de-169">В обновлении с полным экземпляром необходимо установить *пкткс* в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d16de-169">In a full-instance update, you would set *pCtx* to **NULL**.</span></span>

    <span data-ttu-id="d16de-170">Поставщик может записать все необходимые свойства, если объект контекста, находящиеся в вызове, не содержит " \_ \_ размещать \_ расширения".</span><span class="sxs-lookup"><span data-stu-id="d16de-170">The provider may write any necessary properties if the context object present in the call does not contain "\_\_PUT\_EXTENSIONS".</span></span> <span data-ttu-id="d16de-171">Если \_ \_ \_ в объекте контекста есть "постановка расширений", Инструментарий WMI требует, чтобы поставщик либо приложил к семантике операции точно, либо в случае сбоя вызова.</span><span class="sxs-lookup"><span data-stu-id="d16de-171">If "\_\_PUT\_EXTENSIONS" is present in the context object, WMI requires the provider to either obey the semantics of the operation exactly or else fail the call.</span></span> <span data-ttu-id="d16de-172">Дополнительные сведения см. [в разделе Обработка сообщений с запретом доступа в поставщике](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="d16de-172">For more information, see [Handling Access Denied Messages in a Provider](impersonating-a-client.md).</span></span>

 

 
