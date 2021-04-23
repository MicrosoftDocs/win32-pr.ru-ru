---
title: Класс Win32_TSVirtualIP
description: Определяет параметры виртуализации IP для сервера узла сеансов удаленный рабочий стол.
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVirtualIP службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVirtualIP, описание
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801288"
---
# <a name="win32_tsvirtualip-class"></a><span data-ttu-id="c0952-105">\_Класс Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="c0952-105">Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="c0952-106">Определяет параметры виртуализации IP для сервера узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="c0952-106">Defines Internet protocol (IP) virtualization settings for a Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="c0952-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c0952-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0952-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0952-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a><span data-ttu-id="c0952-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c0952-109">Members</span></span>

<span data-ttu-id="c0952-110">Класс **Win32 \_ тсвиртуалип** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0952-110">The **Win32\_TSVirtualIP** class has these types of members:</span></span>

-   [<span data-ttu-id="c0952-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c0952-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0952-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0952-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0952-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c0952-113">Methods</span></span>

<span data-ttu-id="c0952-114">Класс **Win32 \_ тсвиртуалип** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c0952-114">The **Win32\_TSVirtualIP** class has these methods.</span></span>



| <span data-ttu-id="c0952-115">Метод</span><span class="sxs-lookup"><span data-stu-id="c0952-115">Method</span></span>                                                                                                   | <span data-ttu-id="c0952-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c0952-116">Description</span></span>                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0952-117">**аддпрограм**</span><span class="sxs-lookup"><span data-stu-id="c0952-117">**AddProgram**</span></span>](addprogram-win32-tsvirtualip.md)                                                       | <span data-ttu-id="c0952-118">Добавляет программу в список программ, использующих виртуализацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c0952-118">Adds a program to the list of programs that use IP virtualization.</span></span><br/>                                                                                                |
| [<span data-ttu-id="c0952-119">**ремовепрограм**</span><span class="sxs-lookup"><span data-stu-id="c0952-119">**RemoveProgram**</span></span>](removeprogram-win32-tsvirtualip.md)                                                 | <span data-ttu-id="c0952-120">Удаляет программу из списка программ, использующих виртуализацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c0952-120">Removes a program from the list of programs that use IP virtualization.</span></span><br/>                                                                                           |
| [<span data-ttu-id="c0952-121">**селектнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="c0952-121">**SelectNetworkAdapter**</span></span>](selectnetworkadapter-win32-tsvirtualip.md)                                   | <span data-ttu-id="c0952-122">Задает MAC-адрес сетевого адаптера, используемого для виртуализации IP.</span><span class="sxs-lookup"><span data-stu-id="c0952-122">Sets the MAC address of the network adapter to use for IP virtualization.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c0952-123">**сетпрограмлист**</span><span class="sxs-lookup"><span data-stu-id="c0952-123">**SetProgramList**</span></span>](setprogramlist-win32-tsvirtualip.md)                                               | <span data-ttu-id="c0952-124">Перезаписывает список программ, использующих виртуализацию IP.</span><span class="sxs-lookup"><span data-stu-id="c0952-124">Overwrites the list of programs that use IP virtualization.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c0952-125">**сетвиртуалипактиве**</span><span class="sxs-lookup"><span data-stu-id="c0952-125">**SetVirtualIPActive**</span></span>](setvirtualipactive-win32-tsvirtualip.md)                                       | <span data-ttu-id="c0952-126">Задает значение свойства **виртуалипактиве** .</span><span class="sxs-lookup"><span data-stu-id="c0952-126">Sets the **VirtualIPActive** property value.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="c0952-127">**сетвиртуалипмоде**</span><span class="sxs-lookup"><span data-stu-id="c0952-127">**SetVirtualIPMode**</span></span>](setvirtualipmode-win32-tsvirtualip.md)                                           | <span data-ttu-id="c0952-128">Задает значение свойства **виртуалипмоде** .</span><span class="sxs-lookup"><span data-stu-id="c0952-128">Sets the **VirtualIPMode** property value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="c0952-129">**сетвиртуализелупбаккаддрессесенаблед**</span><span class="sxs-lookup"><span data-stu-id="c0952-129">**SetVirtualizeLoopbackAddressesEnabled**</span></span>](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | <span data-ttu-id="c0952-130">Задает значение свойства **виртуализелупбаккаддрессесенаблед** .</span><span class="sxs-lookup"><span data-stu-id="c0952-130">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span><br/> <span data-ttu-id="c0952-131">**Windows Server 2008 R2:** Этот метод недоступен до выхода Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c0952-131">**Windows Server 2008 R2:** This method is not available prior to Windows Server 2012.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c0952-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0952-132">Properties</span></span>

<span data-ttu-id="c0952-133">Класс **Win32 \_ тсвиртуалип** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0952-133">The **Win32\_TSVirtualIP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0952-134">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c0952-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0952-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0952-137">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c0952-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c0952-138">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="c0952-138">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c0952-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0952-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0952-140">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0952-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0952-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-143">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c0952-143">Description of the object.</span></span>

<span data-ttu-id="c0952-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0952-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0952-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c0952-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-146">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0952-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0952-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="c0952-148">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c0952-149">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c0952-149">The date the object was installed.</span></span> <span data-ttu-id="c0952-150">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c0952-150">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c0952-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0952-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0952-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0952-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0952-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-155">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c0952-155">The name of the object.</span></span>

<span data-ttu-id="c0952-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0952-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0952-157">**нетворкадаптердескриптион**</span><span class="sxs-lookup"><span data-stu-id="c0952-157">**NetworkAdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0952-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-160">Описание сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="c0952-160">The description for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c0952-161">**нетворкадаптердескриптионлист**</span><span class="sxs-lookup"><span data-stu-id="c0952-161">**NetworkAdapterDescriptionList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-162">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c0952-162">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0952-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-164">Список описаний доступных физических сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="c0952-164">The list of descriptions of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="c0952-165">**нетворкадаптермакаддресс**</span><span class="sxs-lookup"><span data-stu-id="c0952-165">**NetworkAdapterMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0952-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-168">MAC-адрес сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="c0952-168">The MAC address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c0952-169">**нетворкадаптермаклист**</span><span class="sxs-lookup"><span data-stu-id="c0952-169">**NetworkAdapterMacList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-170">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c0952-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0952-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-172">Список MAC-адресов доступных физических сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="c0952-172">The list of MAC addresses of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="c0952-173">**полицисаурценетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="c0952-173">**PolicySourceNetworkAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-174">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0952-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-176">Указывает, настроен ли сетевой адаптер сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="c0952-176">Indicates whether the network adapter is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c0952-177">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c0952-177">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-178">Сервер</span><span class="sxs-lookup"><span data-stu-id="c0952-178">Server</span></span>

</dd> <dt>

<span data-ttu-id="c0952-179">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c0952-179">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-180">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="c0952-180">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0952-181">**полицисаурцепрограмлист**</span><span class="sxs-lookup"><span data-stu-id="c0952-181">**PolicySourceProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0952-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-184">Указывает, настроено ли свойство **програмлист** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="c0952-184">Indicates whether the **ProgramList** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c0952-185">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c0952-185">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-186">Сервер</span><span class="sxs-lookup"><span data-stu-id="c0952-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="c0952-187">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c0952-187">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-188">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="c0952-188">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0952-189">**полицисаурцевиртуалипактиве**</span><span class="sxs-lookup"><span data-stu-id="c0952-189">**PolicySourceVirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-190">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0952-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-192">Указывает, настроено ли свойство **виртуалипактиве** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="c0952-192">Indicates if the **VirtualIPActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c0952-193">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c0952-193">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-194">Сервер</span><span class="sxs-lookup"><span data-stu-id="c0952-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="c0952-195">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c0952-195">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-196">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="c0952-196">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0952-197">**полицисаурцевиртуалипмоде**</span><span class="sxs-lookup"><span data-stu-id="c0952-197">**PolicySourceVirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-198">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0952-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-200">Указывает, настроено ли свойство **виртуалипмоде** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="c0952-200">Indicates if the **VirtualIPMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="c0952-201">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="c0952-201">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-202">Сервер</span><span class="sxs-lookup"><span data-stu-id="c0952-202">Server</span></span>

</dd> <dt>

<span data-ttu-id="c0952-203">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c0952-203">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="c0952-204">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="c0952-204">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0952-205">**програмлист**</span><span class="sxs-lookup"><span data-stu-id="c0952-205">**ProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-206">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c0952-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0952-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-208">Указывает программы, настроенные для использования виртуализации IP.</span><span class="sxs-lookup"><span data-stu-id="c0952-208">Specifies the programs that are configured to use IP virtualization.</span></span> <span data-ttu-id="c0952-209">Это может быть имя программы или полный путь.</span><span class="sxs-lookup"><span data-stu-id="c0952-209">This may a program name or the full path.</span></span>

</dd> <dt>

<span data-ttu-id="c0952-210">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c0952-210">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0952-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0952-213">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c0952-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c0952-214">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c0952-214">Current status of the object.</span></span> <span data-ttu-id="c0952-215">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="c0952-215">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c0952-216">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="c0952-216">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c0952-217">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="c0952-217">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c0952-218">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="c0952-218">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c0952-219">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="c0952-219">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c0952-220">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0952-220">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c0952-221">("ОК")</span><span class="sxs-lookup"><span data-stu-id="c0952-221">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0952-222">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="c0952-222">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0952-223">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="c0952-223">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0952-224">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c0952-224">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0952-225">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c0952-225">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0952-226">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c0952-226">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0952-227">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="c0952-227">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0952-228">("Служба")</span><span class="sxs-lookup"><span data-stu-id="c0952-228">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0952-229">**виртуалипактиве**</span><span class="sxs-lookup"><span data-stu-id="c0952-229">**VirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-230">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0952-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0952-232">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0952-232">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0952-233">Указывает, активна ли на сервере виртуализация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c0952-233">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="c0952-234">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c0952-234">This can be one of the following values.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c0952-235"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c0952-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0952-236">Виртуализация IP-адресов неактивна.</span><span class="sxs-lookup"><span data-stu-id="c0952-236">IP virtualization is not active.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c0952-237"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c0952-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0952-238">Виртуализация IP-адресов активна.</span><span class="sxs-lookup"><span data-stu-id="c0952-238">IP virtualization is active.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0952-239">**виртуалипмоде**</span><span class="sxs-lookup"><span data-stu-id="c0952-239">**VirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-240">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0952-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-242">Указывает, какой режим виртуализации IP используется на сервере.</span><span class="sxs-lookup"><span data-stu-id="c0952-242">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="c0952-243">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c0952-243">This can be one of the following values.</span></span>

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span data-ttu-id="c0952-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**За сеанс** (0)</span><span class="sxs-lookup"><span data-stu-id="c0952-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per-Session** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0952-245">Режим виртуализации IP — для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="c0952-245">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span data-ttu-id="c0952-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**На программу** (1)</span><span class="sxs-lookup"><span data-stu-id="c0952-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per-Program** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0952-247">Режим виртуализации IP-адресов — "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="c0952-247">The IP virtualization mode is per-user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0952-248">**виртуализелупбаккаддрессесенаблед**</span><span class="sxs-lookup"><span data-stu-id="c0952-248">**VirtualizeLoopbackAddressesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0952-249">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0952-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0952-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0952-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0952-251">Указывает, включена ли виртуализация адресов замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="c0952-251">Specifies whether loopback address virtualization is enabled.</span></span>

<span data-ttu-id="c0952-252">**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c0952-252">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="c0952-253"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c0952-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0952-254">Не включено</span><span class="sxs-lookup"><span data-stu-id="c0952-254">Not enabled</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="c0952-255"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c0952-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0952-256">Активировано</span><span class="sxs-lookup"><span data-stu-id="c0952-256">Enabled</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0952-257">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0952-257">Remarks</span></span>

<span data-ttu-id="c0952-258">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c0952-258">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c0952-259">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="c0952-259">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c0952-260">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c0952-260">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c0952-261">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c0952-261">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0952-262">Требования</span><span class="sxs-lookup"><span data-stu-id="c0952-262">Requirements</span></span>



| <span data-ttu-id="c0952-263">Требование</span><span class="sxs-lookup"><span data-stu-id="c0952-263">Requirement</span></span> | <span data-ttu-id="c0952-264">Значение</span><span class="sxs-lookup"><span data-stu-id="c0952-264">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0952-265">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0952-265">Minimum supported client</span></span><br/> | <span data-ttu-id="c0952-266">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0952-266">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c0952-267">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0952-267">Minimum supported server</span></span><br/> | <span data-ttu-id="c0952-268">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0952-268">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c0952-269">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0952-269">Namespace</span></span><br/>                | <span data-ttu-id="c0952-270">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c0952-270">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c0952-271">MOF</span><span class="sxs-lookup"><span data-stu-id="c0952-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0952-272"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0952-272"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0952-273">DLL</span><span class="sxs-lookup"><span data-stu-id="c0952-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0952-274"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0952-274"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

