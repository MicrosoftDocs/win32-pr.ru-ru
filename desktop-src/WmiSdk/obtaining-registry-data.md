---
description: Получить или изменить данные реестра можно с помощью класса Стдрегпров WMI и его методов.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Получение данных реестра
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701343"
---
# <a name="obtaining-registry-data"></a><span data-ttu-id="acb6d-103">Получение данных реестра</span><span class="sxs-lookup"><span data-stu-id="acb6d-103">Obtaining Registry Data</span></span>

<span data-ttu-id="acb6d-104">Получить или изменить данные реестра можно с помощью класса [**СТДРЕГПРОВ**](/previous-versions/windows/desktop/regprov/stdregprov) WMI и его методов.</span><span class="sxs-lookup"><span data-stu-id="acb6d-104">You can obtain or modify registry data by using the WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and its methods.</span></span> <span data-ttu-id="acb6d-105">При использовании программы Regedit для просмотра и изменения значений реестра на локальном компьютере **стдрегпров** позволяет использовать сценарий или приложение для автоматизации таких действий на локальном компьютере и на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="acb6d-105">While use the Regedit utility to view and change registry values on the local computer, **StdRegProv** allows you to use a script or application to automate such activities on the local computer and remote computers.</span></span>

<span data-ttu-id="acb6d-106">[**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) содержит методы для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="acb6d-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contains methods to do the following:</span></span>

-   <span data-ttu-id="acb6d-107">Проверка прав доступа для пользователя</span><span class="sxs-lookup"><span data-stu-id="acb6d-107">Verify the access permissions for a user</span></span>
-   <span data-ttu-id="acb6d-108">Создание, перечисление и удаление разделов реестра</span><span class="sxs-lookup"><span data-stu-id="acb6d-108">Create, enumerate, and delete registry keys</span></span>
-   <span data-ttu-id="acb6d-109">Создание, перечисление и удаление подразделов или именованных значений</span><span class="sxs-lookup"><span data-stu-id="acb6d-109">Create, enumerate, and delete subkeys or named values</span></span>
-   <span data-ttu-id="acb6d-110">Чтение, запись и удаление значений данных</span><span class="sxs-lookup"><span data-stu-id="acb6d-110">Read, write, and delete data values</span></span>

<span data-ttu-id="acb6d-111">Данные реестра упорядочены по поддеревьям, ключам и подразделам, вложенным в ключ верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="acb6d-111">Registry data is organized by subtrees, keys, and subkeys nested under a top level key.</span></span> <span data-ttu-id="acb6d-112">Фактические значения данных называются записями или именованными значениями.</span><span class="sxs-lookup"><span data-stu-id="acb6d-112">The actual data values are called entries or named values.</span></span>

<span data-ttu-id="acb6d-113">К поддеревьям относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="acb6d-113">The subtrees include the following:</span></span>

-   <span data-ttu-id="acb6d-114">**HKey \_ \_Корень классов** (сокращенно, как **HKCR**)</span><span class="sxs-lookup"><span data-stu-id="acb6d-114">**HKEY\_CLASSES\_ROOT** (abbreviated as **HKCR**)</span></span>
-   <span data-ttu-id="acb6d-115">**HKey \_ ТЕКУЩИЙ \_ пользователь** (**HKCU**)</span><span class="sxs-lookup"><span data-stu-id="acb6d-115">**HKEY\_CURRENT\_USER** (**HKCU**)</span></span>
-   <span data-ttu-id="acb6d-116">**HKey \_ ЛОКАЛЬНЫЙ \_ компьютер** (**HKLM**)</span><span class="sxs-lookup"><span data-stu-id="acb6d-116">**HKEY\_LOCAL\_MACHINE** (**HKLM**)</span></span>
-   <span data-ttu-id="acb6d-117">**\_Пользователи hKey**</span><span class="sxs-lookup"><span data-stu-id="acb6d-117">**HKEY\_USERS**</span></span>
-   <span data-ttu-id="acb6d-118">**\_Текущая \_ Конфигурация hKey**</span><span class="sxs-lookup"><span data-stu-id="acb6d-118">**HKEY\_CURRENT\_CONFIG**</span></span>

<span data-ttu-id="acb6d-119">Например, в записи реестра **hKey** \\ **Software** \\ **Microsoft** \\ **DirectX** \\ **инсталледверсион**, поддерево hKey — это **программное обеспечение**, подразделы — **Microsoft** и **DirectX**, а запись именованного значения — **инсталледверсион**.</span><span class="sxs-lookup"><span data-stu-id="acb6d-119">For example, in the registry entry **HKEY**\\**SOFTWARE**\\**Microsoft**\\**DirectX**\\**InstalledVersion**, the HKEY subtree is **SOFTWARE**; the subkeys are **Microsoft** and **DirectX**; and the named value entry is **InstalledVersion**.</span></span>

<span data-ttu-id="acb6d-120">[**Регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) возникает, когда происходит изменение определенного ключа, но запись не определяет, как изменяются значения, а это событие не активируется изменениями ниже указанного ключа.</span><span class="sxs-lookup"><span data-stu-id="acb6d-120">A [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) occurs when a change to a specific key occurs, but the entry does not identify how the values change nor will this event be triggered by changes below the specified key.</span></span> <span data-ttu-id="acb6d-121">Для определения изменений в любом месте иерархии ключевой структуры используйте [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), который не возвращает определенные значения или изменения ключа.</span><span class="sxs-lookup"><span data-stu-id="acb6d-121">To identify changes anywhere in a hierarchical key structure, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), which does not return specific values or key changes that occur.</span></span> <span data-ttu-id="acb6d-122">Чтобы получить определенное изменение значения записи, используйте [**события registryvaluechangeevent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), а затем прочтите запись, чтобы получить базовое значение.</span><span class="sxs-lookup"><span data-stu-id="acb6d-122">To obtain a specific entry value change, use the [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), and then read the entry to obtain a baseline value.</span></span>

<span data-ttu-id="acb6d-123">[**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) содержит только методы, которые могут вызываться из C++ или скрипта, который отличается от структуры классов Win32.</span><span class="sxs-lookup"><span data-stu-id="acb6d-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) only has methods that can be called from C++ or script, which is different from the Win32 class structure.</span></span>

<span data-ttu-id="acb6d-124">В следующем примере кода показано, как использовать метод [**стдрегпров. енумкэй**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) для перечисления всех подразделов программного обеспечения Майкрософт в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="acb6d-124">The following code example shows how to use the [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) method to list all of the Microsoft software subkeys under the registry key.</span></span>

<span data-ttu-id="acb6d-125">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="acb6d-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





<span data-ttu-id="acb6d-126">[**Стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) имеет различные методы для чтения различных типов данных значений записей реестра.</span><span class="sxs-lookup"><span data-stu-id="acb6d-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) has different methods for reading the various registry entry value data types.</span></span> <span data-ttu-id="acb6d-127">Если запись имеет неизвестные значения, то для их перечисления можно вызвать метод [**стдрегпров. енумвалуес**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) .</span><span class="sxs-lookup"><span data-stu-id="acb6d-127">If the entry has unknown values, then you can call [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) to list them.</span></span> <span data-ttu-id="acb6d-128">В следующей таблице перечислены соответствия между методами **стдрегпров** и типами данных.</span><span class="sxs-lookup"><span data-stu-id="acb6d-128">The following table lists the correspondence between **StdRegProv** methods and the data types.</span></span>



| <span data-ttu-id="acb6d-129">Метод</span><span class="sxs-lookup"><span data-stu-id="acb6d-129">Method</span></span>                                                                                  | <span data-ttu-id="acb6d-130">Тип данных</span><span class="sxs-lookup"><span data-stu-id="acb6d-130">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="acb6d-131">**жетбинаривалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-131">**GetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="acb6d-132">**\_двоичный файл REG**</span><span class="sxs-lookup"><span data-stu-id="acb6d-132">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="acb6d-133">**жетдвордвалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-133">**GetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="acb6d-134">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="acb6d-134">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="acb6d-135">**жетекспандедстрингвалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-135">**GetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="acb6d-136">**\_распаковать \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="acb6d-136">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="acb6d-137">**жетмултистрингвалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-137">**GetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="acb6d-138">**REG \_ Multi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="acb6d-138">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="acb6d-139">**GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="acb6d-139">**GetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="acb6d-140">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="acb6d-140">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="acb6d-141">В следующей таблице перечислены соответствующие методы для создания новых ключей или значений, а также изменения существующих.</span><span class="sxs-lookup"><span data-stu-id="acb6d-141">The following table lists the corresponding methods for creating new keys or values, or changing existing ones.</span></span>



| <span data-ttu-id="acb6d-142">Метод</span><span class="sxs-lookup"><span data-stu-id="acb6d-142">Method</span></span>                                                                                  | <span data-ttu-id="acb6d-143">Тип данных</span><span class="sxs-lookup"><span data-stu-id="acb6d-143">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="acb6d-144">**сетбинаривалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-144">**SetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="acb6d-145">**\_двоичный файл REG**</span><span class="sxs-lookup"><span data-stu-id="acb6d-145">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="acb6d-146">**сетдвордвалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-146">**SetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="acb6d-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="acb6d-147">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="acb6d-148">**сетекспандедстрингвалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-148">**SetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="acb6d-149">**\_распаковать \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="acb6d-149">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="acb6d-150">**сетмултистрингвалуе**</span><span class="sxs-lookup"><span data-stu-id="acb6d-150">**SetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="acb6d-151">**REG \_ Multi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="acb6d-151">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="acb6d-152">**SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="acb6d-152">**SetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="acb6d-153">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="acb6d-153">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="acb6d-154">В следующем примере показано, как прочитать список источников для журнала системных событий из раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="acb6d-154">The following example shows how to read the list of sources for the system event log from the registry key.</span></span>

<span data-ttu-id="acb6d-155">**HKey \_ \_** \\  \\  \\  \\ **Система журнала событий** \\  служб, установленная в системе локального компьютера</span><span class="sxs-lookup"><span data-stu-id="acb6d-155">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Services**\\**Eventlog**\\**System**</span></span>

<span data-ttu-id="acb6d-156">Обратите внимание, что элементы в многострочном значении обрабатываются как коллекция или массив.</span><span class="sxs-lookup"><span data-stu-id="acb6d-156">Note that the items in the multistring value are treated as a collection or array.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



<span data-ttu-id="acb6d-157">Поставщик реестра размещается в локальной службе, а не на LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="acb6d-157">The registry provider is hosted in LocalService—not the LocalSystem.</span></span> <span data-ttu-id="acb6d-158">Поэтому получение сведений удаленно из поддерева **hKey \_ текущий \_ пользователь** невозможно.</span><span class="sxs-lookup"><span data-stu-id="acb6d-158">Therefore, obtaining information remotely from the subtree **HKEY\_CURRENT\_USER** is not possible.</span></span> <span data-ttu-id="acb6d-159">Однако сценарии, выполняемые на локальном компьютере, по-прежнему могут обращаться к **\_ текущему \_ пользователю hKey**.</span><span class="sxs-lookup"><span data-stu-id="acb6d-159">However, scripts run on the local computer can still access **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="acb6d-160">Можно задать для модели размещения значение LocalSystem на удаленном компьютере, но это является угрозой безопасности, так как реестр на удаленном компьютере уязвим для злонамеренного доступа.</span><span class="sxs-lookup"><span data-stu-id="acb6d-160">You can set the hosting model to LocalSystem on a remote machine, but that is a security risk because the registry on the remote machine is vulnerable to hostile access.</span></span> <span data-ttu-id="acb6d-161">Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="acb6d-161">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="examples"></a><span data-ttu-id="acb6d-162">Примеры</span><span class="sxs-lookup"><span data-stu-id="acb6d-162">Examples</span></span>

<span data-ttu-id="acb6d-163">Пример кода на языке VBScript в [разделе "чтение двоичного значения реестра](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) " в коллекции TechNet использует инструментарий WMI для чтения двоичного значения реестра.</span><span class="sxs-lookup"><span data-stu-id="acb6d-163">The [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript code example on TechNet Gallery uses WMI to read a binary registry value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acb6d-164">См. также</span><span class="sxs-lookup"><span data-stu-id="acb6d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acb6d-165">Задачи WMI: реестр</span><span class="sxs-lookup"><span data-stu-id="acb6d-165">WMI Tasks: Registry</span></span>](wmi-tasks--registry.md)
</dt> </dl>

 

 
