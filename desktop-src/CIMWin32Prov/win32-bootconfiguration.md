---
description: '\_Класс WMI бутконфигуратион для Win32 представляет конфигурацию загрузки компьютерной системы под Windows.'
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Класс Win32_BootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656024"
---
# <a name="win32_bootconfiguration-class"></a><span data-ttu-id="de8c2-103">\_Класс Win32 бутконфигуратион</span><span class="sxs-lookup"><span data-stu-id="de8c2-103">Win32\_BootConfiguration class</span></span>

<span data-ttu-id="de8c2-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ бутконфигуратион для Win32** представляет конфигурацию загрузки компьютерной системы под Windows.</span><span class="sxs-lookup"><span data-stu-id="de8c2-104">The **Win32\_BootConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the boot configuration of a computer system running Windows.</span></span>

<span data-ttu-id="de8c2-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="de8c2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="de8c2-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="de8c2-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8c2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de8c2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a><span data-ttu-id="de8c2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="de8c2-108">Members</span></span>

<span data-ttu-id="de8c2-109">Класс **Win32 \_ бутконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="de8c2-109">The **Win32\_BootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="de8c2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="de8c2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de8c2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="de8c2-111">Properties</span></span>

<span data-ttu-id="de8c2-112">Класс **Win32 \_ бутконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="de8c2-112">The **Win32\_BootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de8c2-113">**бутдиректори**</span><span class="sxs-lookup"><span data-stu-id="de8c2-113">**BootDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-116">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| процесс Win32API и функции потока \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| винбутдир")</span><span class="sxs-lookup"><span data-stu-id="de8c2-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-117">Путь к системным файлам, необходимым для загрузки системы.</span><span class="sxs-lookup"><span data-stu-id="de8c2-117">Path to the system files required for booting the system.</span></span>

<span data-ttu-id="de8c2-118">Пример: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="de8c2-118">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="de8c2-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de8c2-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-123">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="de8c2-123">Short textual description of the current object.</span></span>

<span data-ttu-id="de8c2-124">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="de8c2-124">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-125">**ConfigurationPath**</span><span class="sxs-lookup"><span data-stu-id="de8c2-125">**ConfigurationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| процесс Win32API и функции потока \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| винбутдир")</span><span class="sxs-lookup"><span data-stu-id="de8c2-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-129">Путь к файлам конфигурации.</span><span class="sxs-lookup"><span data-stu-id="de8c2-129">Path to the configuration files.</span></span> <span data-ttu-id="de8c2-130">Это значение может быть аналогично значению свойства **бутдиректори** .</span><span class="sxs-lookup"><span data-stu-id="de8c2-130">This value may be similar to the value in the **BootDirectory** property.</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de8c2-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-134">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="de8c2-134">Textual description of the current object.</span></span>

<span data-ttu-id="de8c2-135">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="de8c2-135">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-136">**ластдриве**</span><span class="sxs-lookup"><span data-stu-id="de8c2-136">**LastDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жетдриветипе")</span><span class="sxs-lookup"><span data-stu-id="de8c2-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-140">Последняя буква диска, к которой назначен физический диск.</span><span class="sxs-lookup"><span data-stu-id="de8c2-140">Last drive letter to which a physical drive is assigned.</span></span>

<span data-ttu-id="de8c2-141">Пример: "E:"</span><span class="sxs-lookup"><span data-stu-id="de8c2-141">Example: "E:"</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="de8c2-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-145">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="de8c2-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-146">Имя конфигурации загрузки.</span><span class="sxs-lookup"><span data-stu-id="de8c2-146">Name of the boot configuration.</span></span> <span data-ttu-id="de8c2-147">Это идентификатор конфигурации загрузки.</span><span class="sxs-lookup"><span data-stu-id="de8c2-147">It is an identifier for the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-148">**скратчдиректори**</span><span class="sxs-lookup"><span data-stu-id="de8c2-148">**ScratchDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-151">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жеттемппас")</span><span class="sxs-lookup"><span data-stu-id="de8c2-151">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-152">Каталог, в котором временные файлы могут находиться во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="de8c2-152">Directory where temporary files can reside during boot time.</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-153">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="de8c2-153">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-156">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="de8c2-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-157">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="de8c2-157">Identifier by which the current object is known.</span></span>

<span data-ttu-id="de8c2-158">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="de8c2-158">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="de8c2-159">**TempDirectory**</span><span class="sxs-lookup"><span data-stu-id="de8c2-159">**TempDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de8c2-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de8c2-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de8c2-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de8c2-162">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| жеттемппас")</span><span class="sxs-lookup"><span data-stu-id="de8c2-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="de8c2-163">Каталог, в котором хранятся временные файлы.</span><span class="sxs-lookup"><span data-stu-id="de8c2-163">Directory where temporary files are stored.</span></span>

<span data-ttu-id="de8c2-164">Пример: "C: \\ TEMP"</span><span class="sxs-lookup"><span data-stu-id="de8c2-164">Example: "C:\\TEMP"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de8c2-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de8c2-165">Remarks</span></span>

<span data-ttu-id="de8c2-166">Класс **Win32 \_ бутконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="de8c2-166">The **Win32\_BootConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="de8c2-167">Примеры</span><span class="sxs-lookup"><span data-stu-id="de8c2-167">Examples</span></span>

<span data-ttu-id="de8c2-168">[Список свойств конфигурации загрузки для компьютера](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl возвращает сведения о конфигурации загрузки для компьютера.</span><span class="sxs-lookup"><span data-stu-id="de8c2-168">The [List the Boot Configuration Properties of a Computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl sample returns boot configuration information for a computer.</span></span>

<span data-ttu-id="de8c2-169">Следующий пример сценария VBScript возвращает сведения о конфигурации загрузки для компьютера.</span><span class="sxs-lookup"><span data-stu-id="de8c2-169">The following VBScript sample returns boot configuration information for a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



<span data-ttu-id="de8c2-170">В следующем примере кода показано использование класса WMI **\_ Бутконфигуратион для Win32** .</span><span class="sxs-lookup"><span data-stu-id="de8c2-170">The following code sample demonstrates the use of the **Win32\_BootConfiguration** WMI class.</span></span>


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



<span data-ttu-id="de8c2-171">В предыдущем примере кода создаются следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="de8c2-171">The previous code sample creates the following output:</span></span>

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a><span data-ttu-id="de8c2-172">Требования</span><span class="sxs-lookup"><span data-stu-id="de8c2-172">Requirements</span></span>



| <span data-ttu-id="de8c2-173">Требование</span><span class="sxs-lookup"><span data-stu-id="de8c2-173">Requirement</span></span> | <span data-ttu-id="de8c2-174">Значение</span><span class="sxs-lookup"><span data-stu-id="de8c2-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de8c2-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de8c2-175">Minimum supported client</span></span><br/> | <span data-ttu-id="de8c2-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de8c2-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de8c2-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de8c2-177">Minimum supported server</span></span><br/> | <span data-ttu-id="de8c2-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de8c2-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de8c2-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="de8c2-179">Namespace</span></span><br/>                | <span data-ttu-id="de8c2-180">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="de8c2-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="de8c2-181">MOF</span><span class="sxs-lookup"><span data-stu-id="de8c2-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de8c2-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de8c2-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de8c2-183">DLL</span><span class="sxs-lookup"><span data-stu-id="de8c2-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de8c2-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de8c2-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de8c2-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de8c2-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8c2-186">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="de8c2-186">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="de8c2-187">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de8c2-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

