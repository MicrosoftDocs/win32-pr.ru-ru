---
title: Класс Win32_TSNetworkAdapterSetting
description: Определяет различные параметры конфигурации для \_ класса терминала Win32, включая свойства, связанные с сетевым адаптером, и максимальное разрешенное число подключений.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSNetworkAdapterSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSNetworkAdapterSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2f2f1ac7d6bf4b1fd3fb5f5a92fc4fd5260a92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491592"
---
# <a name="win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="983c2-105">\_Класс Win32 тснетворкадаптерсеттинг</span><span class="sxs-lookup"><span data-stu-id="983c2-105">Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="983c2-106">Класс **WMI \_ тснетворкадаптерсеттинг** инструментария Win32 определяет различные параметры конфигурации для [**класса \_ терминала Win32**](win32-terminal.md) , включая свойства, связанные с сетевым адаптером, и максимальное разрешенное число подключений.</span><span class="sxs-lookup"><span data-stu-id="983c2-106">The **Win32\_TSNetworkAdapterSetting** WMI class defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

<span data-ttu-id="983c2-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="983c2-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="983c2-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="983c2-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="983c2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="983c2-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a><span data-ttu-id="983c2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="983c2-110">Members</span></span>

<span data-ttu-id="983c2-111">Класс **Win32 \_ тснетворкадаптерсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="983c2-111">The **Win32\_TSNetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="983c2-112">Методы</span><span class="sxs-lookup"><span data-stu-id="983c2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="983c2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="983c2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="983c2-114">Методы</span><span class="sxs-lookup"><span data-stu-id="983c2-114">Methods</span></span>

<span data-ttu-id="983c2-115">Класс **Win32 \_ тснетворкадаптерсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="983c2-115">The **Win32\_TSNetworkAdapterSetting** class has these methods.</span></span>



| <span data-ttu-id="983c2-116">Метод</span><span class="sxs-lookup"><span data-stu-id="983c2-116">Method</span></span>                                                                                     | <span data-ttu-id="983c2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="983c2-117">Description</span></span>                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="983c2-118">**селекталлнетворкадаптерс**</span><span class="sxs-lookup"><span data-stu-id="983c2-118">**SelectAllNetworkAdapters**</span></span>](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | <span data-ttu-id="983c2-119">Выбирает все сетевые адаптеры.</span><span class="sxs-lookup"><span data-stu-id="983c2-119">Selects all network adapters.</span></span><br/>                                                                 |
| [<span data-ttu-id="983c2-120">**селектнетворкадаптерип**</span><span class="sxs-lookup"><span data-stu-id="983c2-120">**SelectNetworkAdapterIP**</span></span>](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | <span data-ttu-id="983c2-121">Выбирает сетевой адаптер на основе IP-адреса адаптера.</span><span class="sxs-lookup"><span data-stu-id="983c2-121">Selects a network adapter based on the adapter's IP address.</span></span><br/>                                  |
| [<span data-ttu-id="983c2-122">**сетнетворкадаптерланаид**</span><span class="sxs-lookup"><span data-stu-id="983c2-122">**SetNetworkAdapterLanaID**</span></span>](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | <span data-ttu-id="983c2-123">Указывает номер локального сетевого адаптера (LANA) NetBIOS, который нужно задать.</span><span class="sxs-lookup"><span data-stu-id="983c2-123">Specifies the NetBIOS Local Area Network Adapter (LANA) number of the network adapter to set.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="983c2-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="983c2-124">Properties</span></span>

<span data-ttu-id="983c2-125">Класс **Win32 \_ тснетворкадаптерсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="983c2-125">The **Win32\_TSNetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="983c2-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="983c2-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983c2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983c2-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="983c2-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="983c2-130">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="983c2-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="983c2-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="983c2-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="983c2-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="983c2-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983c2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-135">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="983c2-135">Description of the object.</span></span>

<span data-ttu-id="983c2-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="983c2-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="983c2-137">**девицеидлист**</span><span class="sxs-lookup"><span data-stu-id="983c2-137">**DeviceIDList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-138">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="983c2-138">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="983c2-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-140">Массив строк доступных идентификаторов устройств возвращается в порядке расположения физических сетевых адаптеров, возвращенных в массиве свойств **нетворкадаптерлист** .</span><span class="sxs-lookup"><span data-stu-id="983c2-140">String array of available device IDs returned in the order of physical network adapters returned in the **NetworkAdapterList** property array.</span></span> <span data-ttu-id="983c2-141">Значение идентификатора устройства является свойством **DeviceID** в [**Win32 \_ сетевого адаптера**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span><span class="sxs-lookup"><span data-stu-id="983c2-141">The device ID value is the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span></span>

</dd> <dt>

<span data-ttu-id="983c2-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="983c2-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-143">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="983c2-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983c2-145">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="983c2-145">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="983c2-146">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="983c2-146">The date the object was installed.</span></span> <span data-ttu-id="983c2-147">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="983c2-147">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="983c2-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="983c2-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="983c2-149">**максимумконнектионс**</span><span class="sxs-lookup"><span data-stu-id="983c2-149">**MaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983c2-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="983c2-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="983c2-152">Максимальное разрешенное число подключений.</span><span class="sxs-lookup"><span data-stu-id="983c2-152">The maximum number of connections allowed.</span></span> <span data-ttu-id="983c2-153">Значение **максинт** обозначает неограниченное количество соединений.</span><span class="sxs-lookup"><span data-stu-id="983c2-153">The value **MAXINT** denotes an unlimited number of connections.</span></span>

</dd> <dt>

<span data-ttu-id="983c2-154">**Name**</span><span class="sxs-lookup"><span data-stu-id="983c2-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983c2-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-157">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="983c2-157">The name of the object.</span></span>

<span data-ttu-id="983c2-158">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="983c2-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="983c2-159">**нетворкадаптерид**</span><span class="sxs-lookup"><span data-stu-id="983c2-159">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983c2-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-162">Идентификатор GUID, представляющий идентификатор устанавливаемого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="983c2-162">The GUID that represents the ID of the network adapter to set.</span></span> <span data-ttu-id="983c2-163">**Идентификатор GUID** , состоящий из всех нулей, означает все сетевые адаптеры.</span><span class="sxs-lookup"><span data-stu-id="983c2-163">A **GUID** that consists of all zeros denotes all network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="983c2-164">**нетворкадаптерланаид**</span><span class="sxs-lookup"><span data-stu-id="983c2-164">**NetworkAdapterLanaID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983c2-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-167">Номер локального сетевого адаптера (LANA) NetBIOS сетевого адаптера, который используется для обнаружения сетевого адаптера, назначенного терминалу.</span><span class="sxs-lookup"><span data-stu-id="983c2-167">NetBIOS Local Area Network Adapter (LANA) number of the network adapter that is used to identify the network adapter assigned to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="983c2-168">**нетворкадаптерлист**</span><span class="sxs-lookup"><span data-stu-id="983c2-168">**NetworkAdapterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-169">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="983c2-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="983c2-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-171">Строковый массив доступных физических сетевых адаптеров и соответствующих идентификаторов устройств.</span><span class="sxs-lookup"><span data-stu-id="983c2-171">String array of available physical network adapters and the corresponding device IDs.</span></span> <span data-ttu-id="983c2-172">Идентификаторами устройств являются свойства **DeviceID** в [**Win32 \_ сетевого адаптера**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span><span class="sxs-lookup"><span data-stu-id="983c2-172">The device IDs are the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span></span>

</dd> <dt>

<span data-ttu-id="983c2-173">**нетворкадаптернаме**</span><span class="sxs-lookup"><span data-stu-id="983c2-173">**NetworkAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983c2-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-176">Описание устанавливаемого сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="983c2-176">Description of the network adapter to set.</span></span> <span data-ttu-id="983c2-177">Это значение находится в [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span><span class="sxs-lookup"><span data-stu-id="983c2-177">This value is in [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span></span>

</dd> <dt>

<span data-ttu-id="983c2-178">**полицисаурцемаксимумконнектионс**</span><span class="sxs-lookup"><span data-stu-id="983c2-178">**PolicySourceMaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-179">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="983c2-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-181">Указывает, настроено ли свойство **максимумконнектионс** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="983c2-181">Indicates whether the **MaximumConnections** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="983c2-182">0</span><span class="sxs-lookup"><span data-stu-id="983c2-182">0</span></span>
</dt> <dd>

<span data-ttu-id="983c2-183">Сервер</span><span class="sxs-lookup"><span data-stu-id="983c2-183">Server</span></span>

</dd> <dt>

<span data-ttu-id="983c2-184">1</span><span class="sxs-lookup"><span data-stu-id="983c2-184">1</span></span>
</dt> <dd>

<span data-ttu-id="983c2-185">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="983c2-185">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="983c2-186">2</span><span class="sxs-lookup"><span data-stu-id="983c2-186">2</span></span>
</dt> <dd>

<span data-ttu-id="983c2-187">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="983c2-187">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="983c2-188">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="983c2-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983c2-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="983c2-191">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="983c2-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="983c2-192">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="983c2-192">Current status of the object.</span></span> <span data-ttu-id="983c2-193">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="983c2-193">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="983c2-194">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="983c2-194">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="983c2-195">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="983c2-195">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="983c2-196">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="983c2-196">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="983c2-197">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="983c2-197">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="983c2-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="983c2-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="983c2-199">("ОК")</span><span class="sxs-lookup"><span data-stu-id="983c2-199">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="983c2-200">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="983c2-200">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="983c2-201">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="983c2-201">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="983c2-202">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="983c2-202">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="983c2-203">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="983c2-203">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="983c2-204">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="983c2-204">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="983c2-205">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="983c2-205">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="983c2-206">("Служба")</span><span class="sxs-lookup"><span data-stu-id="983c2-206">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="983c2-207">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="983c2-207">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="983c2-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="983c2-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="983c2-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="983c2-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="983c2-210">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="983c2-210">The name of the terminal.</span></span>

<span data-ttu-id="983c2-211">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="983c2-211">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="983c2-212">Комментарии</span><span class="sxs-lookup"><span data-stu-id="983c2-212">Remarks</span></span>

<span data-ttu-id="983c2-213">Имейте в виду, что Винстатионс, связанный с сеансом консоли, не может получить доступ к методам и свойствам этого класса.</span><span class="sxs-lookup"><span data-stu-id="983c2-213">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="983c2-214">Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства Терминалнаме, методы этого объекта возвращают **WBEM \_ E \_ не \_ поддерживаются**.</span><span class="sxs-lookup"><span data-stu-id="983c2-214">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="983c2-215">Этот код ошибки также возвращается, если станция окна пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="983c2-215">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="983c2-216">Чтобы подключиться к \\ \\ пространству имен root cimv2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="983c2-216">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="983c2-217">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="983c2-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="983c2-218">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="983c2-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="983c2-219">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="983c2-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="983c2-220">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="983c2-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="983c2-221">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="983c2-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="983c2-222">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="983c2-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="983c2-223">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="983c2-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="983c2-224">Требования</span><span class="sxs-lookup"><span data-stu-id="983c2-224">Requirements</span></span>



| <span data-ttu-id="983c2-225">Требование</span><span class="sxs-lookup"><span data-stu-id="983c2-225">Requirement</span></span> | <span data-ttu-id="983c2-226">Значение</span><span class="sxs-lookup"><span data-stu-id="983c2-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="983c2-227">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="983c2-227">Minimum supported client</span></span><br/> | <span data-ttu-id="983c2-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="983c2-228">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="983c2-229">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="983c2-229">Minimum supported server</span></span><br/> | <span data-ttu-id="983c2-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="983c2-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="983c2-231">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="983c2-231">Namespace</span></span><br/>                | <span data-ttu-id="983c2-232">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="983c2-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="983c2-233">MOF</span><span class="sxs-lookup"><span data-stu-id="983c2-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="983c2-234"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="983c2-234"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="983c2-235">DLL</span><span class="sxs-lookup"><span data-stu-id="983c2-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="983c2-236"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="983c2-236"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="983c2-237">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="983c2-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983c2-238">**\_Сетевого адаптера Win32**</span><span class="sxs-lookup"><span data-stu-id="983c2-238">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[<span data-ttu-id="983c2-239">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="983c2-239">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[<span data-ttu-id="983c2-240">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="983c2-240">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="983c2-241">**\_Тснетворкадаптерлистсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="983c2-241">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

