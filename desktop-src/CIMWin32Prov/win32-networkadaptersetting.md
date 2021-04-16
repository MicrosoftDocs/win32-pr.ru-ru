---
description: '\_Класс WMI взаимосвязей Win32 нетворкадаптерсеттинг связывает сетевой адаптер и его параметры конфигурации.'
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Класс Win32_NetworkAdapterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656019"
---
# <a name="win32_networkadaptersetting-class"></a><span data-ttu-id="e7e5a-103">\_Класс Win32 нетворкадаптерсеттинг</span><span class="sxs-lookup"><span data-stu-id="e7e5a-103">Win32\_NetworkAdapterSetting class</span></span>

<span data-ttu-id="e7e5a-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ нетворкадаптерсеттинг** связывает сетевой адаптер и его параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-104">The **Win32\_NetworkAdapterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network adapter and its configuration settings.</span></span>

<span data-ttu-id="e7e5a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e7e5a-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e5a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7e5a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="e7e5a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e7e5a-108">Members</span></span>

<span data-ttu-id="e7e5a-109">Класс **Win32 \_ нетворкадаптерсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e7e5a-109">The **Win32\_NetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e7e5a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7e5a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7e5a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7e5a-111">Properties</span></span>

<span data-ttu-id="e7e5a-112">Класс **Win32 \_ нетворкадаптерсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-112">The **Win32\_NetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7e5a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e5a-114">Тип данных: **Win32 \_ сетевого адаптера**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-114">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="e7e5a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7e5a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7e5a-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ сетевого адаптера")</span><span class="sxs-lookup"><span data-stu-id="e7e5a-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="e7e5a-117">[**\_ Сетевого адаптера Win32**](win32-networkadapter.md) , описывающий свойства сетевого адаптера, использующего определенный параметр сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-117">A [**Win32\_NetworkAdapter**](win32-networkadapter.md) that describes the properties of the network adapter that is using a particular network adapter setting.</span></span>

</dd> <dt>

<span data-ttu-id="e7e5a-118">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7e5a-119">Тип данных: **Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-119">Data type: **Win32\_NetworkAdapterConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="e7e5a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7e5a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7e5a-121">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")</span><span class="sxs-lookup"><span data-stu-id="e7e5a-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="e7e5a-122">[**\_ NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) , описывающий параметры конфигурации, используемые сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-122">A [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) that describes the configuration settings used on the network adapter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7e5a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7e5a-123">Remarks</span></span>

<span data-ttu-id="e7e5a-124">Класс **Win32 \_ нетворкадаптерсеттинг** является производным от [**Win32 \_ девицесеттингс**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="e7e5a-124">The **Win32\_NetworkAdapterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

<span data-ttu-id="e7e5a-125">Сведения о том, как использовать классы ассоциаций, см. в разделе [соединители оператора](../wmisdk/associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="e7e5a-125">For information on how to use association classes, see [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e7e5a-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="e7e5a-126">Examples</span></span>

<span data-ttu-id="e7e5a-127">Следующий пример VBScript использует **Win32 \_ нетворкадаптерсеттинг** для задания IP-адреса подключения по локальной сети.</span><span class="sxs-lookup"><span data-stu-id="e7e5a-127">The following VBScript sample uses **Win32\_NetworkAdapterSetting** to identify the IP Address on the Local Area Connection.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="e7e5a-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e7e5a-128">Requirements</span></span>



| <span data-ttu-id="e7e5a-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e7e5a-129">Requirement</span></span> | <span data-ttu-id="e7e5a-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e5a-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7e5a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e5a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7e5a-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7e5a-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7e5a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e5a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7e5a-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7e5a-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7e5a-135">Namespace</span></span><br/>                | <span data-ttu-id="e7e5a-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7e5a-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7e5a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e7e5a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7e5a-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7e5a-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7e5a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e5a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e5a-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e5a-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e5a-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7e5a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e5a-142">**\_Девицесеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="e7e5a-142">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="e7e5a-143">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="e7e5a-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e7e5a-144">Задачи WMI: Сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="e7e5a-144">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
