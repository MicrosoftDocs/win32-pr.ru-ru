---
description: Представляет параметры для службы виртуализации, имеющейся в одной системе узла.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Класс Msvm_VirtualSystemManagementServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682485"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a><span data-ttu-id="e752f-103">\_Класс мсвм виртуалсистемманажементсервицесеттингдата</span><span class="sxs-lookup"><span data-stu-id="e752f-103">Msvm\_VirtualSystemManagementServiceSettingData class</span></span>

<span data-ttu-id="e752f-104">Представляет параметры для службы виртуализации, имеющейся в одной системе узла.</span><span class="sxs-lookup"><span data-stu-id="e752f-104">Represents the settings for the virtualization service present on a single host system.</span></span> <span data-ttu-id="e752f-105">Свойства этого класса нельзя изменить напрямую.</span><span class="sxs-lookup"><span data-stu-id="e752f-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="e752f-106">Клиент должен вызвать метод [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) , чтобы изменить любое из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="e752f-106">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify any of these properties.</span></span>

<span data-ttu-id="e752f-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e752f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e752f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e752f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a><span data-ttu-id="e752f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e752f-109">Members</span></span>

<span data-ttu-id="e752f-110">Класс **мсвм \_ виртуалсистемманажементсервицесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e752f-110">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e752f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e752f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e752f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e752f-112">Properties</span></span>

<span data-ttu-id="e752f-113">Класс **мсвм \_ виртуалсистемманажементсервицесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e752f-113">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e752f-114">**биослоккстринг**</span><span class="sxs-lookup"><span data-stu-id="e752f-114">**BiosLockString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e752f-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span><span class="sxs-lookup"><span data-stu-id="e752f-117">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span></span>
</dt> </dl>

<span data-ttu-id="e752f-118">Используется изготовителями оборудования для разрешения запуска операционных систем Windows, заблокированных BIOS, на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e752f-118">Used by OEMs to allow BIOS-locked Windows operating systems to run in the virtual machine.</span></span> <span data-ttu-id="e752f-119">Длина этой строки должна составлять ровно 32 символов.</span><span class="sxs-lookup"><span data-stu-id="e752f-119">This string must be exactly 32 characters in length.</span></span>

<span data-ttu-id="e752f-120">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-120">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e752f-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-124">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e752f-124">A short description of the object.</span></span> <span data-ttu-id="e752f-125">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e752f-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="e752f-126">**куррентввннаддресс**</span><span class="sxs-lookup"><span data-stu-id="e752f-126">**CurrentWWNNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-129">Имя узла в Интернете для динамически создаваемых адресов WWN-имен, используемых для виртуальных адаптеров шины.</span><span class="sxs-lookup"><span data-stu-id="e752f-129">The world wide node name (WWNN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="e752f-130">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-130">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-131">**дефаултекстерналдатарут**</span><span class="sxs-lookup"><span data-stu-id="e752f-131">**DefaultExternalDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e752f-134">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md).**Конфигуратиондатарут**")</span><span class="sxs-lookup"><span data-stu-id="e752f-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span></span>
</dt> </dl>

<span data-ttu-id="e752f-135">Корневой каталог внешних данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e752f-135">The default external data root.</span></span> <span data-ttu-id="e752f-136">По умолчанию "*root* \\ папка ProgramData \\ \\ \\ виртуализация Microsoft Windows".</span><span class="sxs-lookup"><span data-stu-id="e752f-136">By default, "*root*\\ProgramData\\Microsoft\\Windows\\Virtualization".</span></span>

<span data-ttu-id="e752f-137">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-137">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-138">**дефаултвиртуалхарддисккачингмоде**</span><span class="sxs-lookup"><span data-stu-id="e752f-138">**DefaultVirtualHardDiskCachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e752f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-141">Указывает, следует ли использовать кэширование файлов в памяти по умолчанию для дисков.</span><span class="sxs-lookup"><span data-stu-id="e752f-141">Indicates whether in-memory file caching should be used for disks by default.</span></span> <span data-ttu-id="e752f-142">Это значение может быть переопределено отдельно для каждого диска в поле **качингмоде** класса [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-142">This value can be overridden on a per-disk basis in the **CachingMode** field of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="e752f-143">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e752f-143">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e752f-144">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e752f-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="e752f-145">**Без кэширования** (3)</span><span class="sxs-lookup"><span data-stu-id="e752f-145">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="e752f-146">**Кэшировать родители-предки** (4)</span><span class="sxs-lookup"><span data-stu-id="e752f-146">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e752f-147">**дефаултвиртуалхарддискпас**</span><span class="sxs-lookup"><span data-stu-id="e752f-147">**DefaultVirtualHardDiskPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-150">Путь к виртуальному жесткому диску по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e752f-150">The default virtual hard disk path.</span></span> <span data-ttu-id="e752f-151">По умолчанию "*корневые* \\ Пользователи \\ общедоступные \\ документы — \\ виртуальные жесткие диски".</span><span class="sxs-lookup"><span data-stu-id="e752f-151">By default, "*root*\\Users\\Public\\Documents\\Virtual Hard Disks".</span></span>

<span data-ttu-id="e752f-152">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-152">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-153">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e752f-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-156">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e752f-156">A description of the object.</span></span> <span data-ttu-id="e752f-157">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Settings для службы управления виртуальными системами".</span><span class="sxs-lookup"><span data-stu-id="e752f-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="e752f-158">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e752f-158">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-161">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e752f-161">A display name for the object.</span></span> <span data-ttu-id="e752f-162">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e752f-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span> <span data-ttu-id="e752f-163">Изменение этого свойства приведет к изменению свойства **ElementName** связанного производного класса [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="e752f-163">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-164">**енханцедсессионмодинаблед**</span><span class="sxs-lookup"><span data-stu-id="e752f-164">**EnhancedSessionModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-165">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e752f-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-167">Указывает, разрешен ли режим расширенного сеанса на сервере.</span><span class="sxs-lookup"><span data-stu-id="e752f-167">Indicates whether enhanced session mode is permitted on the server.</span></span> <span data-ttu-id="e752f-168">**Значение true** указывает, что разрешено; в противном случае **false**.</span><span class="sxs-lookup"><span data-stu-id="e752f-168">**True** indicates permitted, otherwise **False**.</span></span>

<span data-ttu-id="e752f-169">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e752f-169">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-170">**хбалунтимеаут**</span><span class="sxs-lookup"><span data-stu-id="e752f-170">**HbaLunTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e752f-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-173">Указывает время, в течение которого виртуальное устройство искусственного Fibre Channel будет ожидать отображения логического номера устройства (LUN) перед запуском виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e752f-173">Specifies the amount of time that the synthetic Fibre Channel virtual device will wait for a logical unit number (LUN) to appear before starting a virtual machine.</span></span>

<span data-ttu-id="e752f-174">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-174">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-175">**хипервисоррутсчедулеренаблед**</span><span class="sxs-lookup"><span data-stu-id="e752f-175">**HypervisorRootSchedulerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-176">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e752f-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-178">Включен ли корневой планировщик низкоуровневой оболочки.</span><span class="sxs-lookup"><span data-stu-id="e752f-178">Whether or not the hypervisor root scheduler is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="e752f-179">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="e752f-179">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e752f-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e752f-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e752f-183">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e752f-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e752f-184">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e752f-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e752f-185">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "Microsoft:*Host*", где *Host* — это NetBIOS-имя системы размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="e752f-185">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*host*", where *host* is the NetBIOS name of the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-186">**максимуммакаддресс**</span><span class="sxs-lookup"><span data-stu-id="e752f-186">**MaximumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-189">Максимальный MAC-адрес для динамически создаваемых MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="e752f-189">The maximum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="e752f-190">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-190">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-191">**максимумввпнаддресс**</span><span class="sxs-lookup"><span data-stu-id="e752f-191">**MaximumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-194">Максимальный WWN-адрес для динамически создаваемых адресов WWN-имен, используемых для виртуальных адаптеров шины.</span><span class="sxs-lookup"><span data-stu-id="e752f-194">The maximum world wide port name (WWPN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="e752f-195">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-195">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-196">**минимуммакаддресс**</span><span class="sxs-lookup"><span data-stu-id="e752f-196">**MinimumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-199">Минимальный MAC-адрес для динамически создаваемых MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="e752f-199">The minimum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="e752f-200">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-200">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-201">**минимумввпнаддресс**</span><span class="sxs-lookup"><span data-stu-id="e752f-201">**MinimumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-204">Минимальный адрес WWN имени порта для динамически создаваемых адресов WWN, используемых для виртуальных адаптеров шины.</span><span class="sxs-lookup"><span data-stu-id="e752f-204">The minimum world wide port name address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="e752f-205">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-205">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-206">**нумаспаннинженаблед**</span><span class="sxs-lookup"><span data-stu-id="e752f-206">**NumaSpanningEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-207">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e752f-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e752f-209">Указывает, может ли память выделяться из узлов удаленного доступа к памяти неоднородным доступом (NUMA) при запуске виртуальной машины или при назначении памяти виртуальной машине с помощью динамической памяти.</span><span class="sxs-lookup"><span data-stu-id="e752f-209">Specifies whether memory can be allocated from remote nonuniform memory access (NUMA) nodes when starting a virtual machine or when assigning memory to a virtual machine by dynamic memory.</span></span> <span data-ttu-id="e752f-210">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e752f-210">This can be one of the following values.</span></span>



| <span data-ttu-id="e752f-211">Значение</span><span class="sxs-lookup"><span data-stu-id="e752f-211">Value</span></span>                                                                                | <span data-ttu-id="e752f-212">Значение</span><span class="sxs-lookup"><span data-stu-id="e752f-212">Meaning</span></span>                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e752f-213"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="e752f-213"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="e752f-214">Память может выделяться как с локального, так и с удаленного узла NUMA.</span><span class="sxs-lookup"><span data-stu-id="e752f-214">Memory can be allocated from both local and remote NUMA nodes.</span></span><br/>                   |
| <dl> <span data-ttu-id="e752f-215"><dt>**Неверно**</dt></span><span class="sxs-lookup"><span data-stu-id="e752f-215"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="e752f-216">Память может быть выделена только из узла NUMA, назначенного виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e752f-216">Memory can be allocated only from the NUMA node assigned to the virtual machine.</span></span><br/> |



 

<span data-ttu-id="e752f-217">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-217">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-218">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="e752f-218">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e752f-221">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="e752f-221">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="e752f-222">Описывает, как можно достичь основного владельца системы (например, номер телефона или адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="e752f-222">Describes how the primary system owner can be reached (for example, phone number or email address).</span></span> <span data-ttu-id="e752f-223">По умолчанию пусто.</span><span class="sxs-lookup"><span data-stu-id="e752f-223">By default, empty.</span></span> <span data-ttu-id="e752f-224">Длина имени не может превышать 256 символов.</span><span class="sxs-lookup"><span data-stu-id="e752f-224">This name may not exceed 256 characters in length.</span></span>

<span data-ttu-id="e752f-225">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-225">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e752f-226">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="e752f-226">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e752f-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e752f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e752f-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e752f-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e752f-229">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="e752f-229">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="e752f-230">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="e752f-230">The name of the primary system owner.</span></span> <span data-ttu-id="e752f-231">По умолчанию «администраторы».</span><span class="sxs-lookup"><span data-stu-id="e752f-231">By default, "Administrators".</span></span> <span data-ttu-id="e752f-232">Длина этого значения не может превышать 64 символов.</span><span class="sxs-lookup"><span data-stu-id="e752f-232">This value may not exceed 64 characters in length.</span></span>

<span data-ttu-id="e752f-233">Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e752f-233">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e752f-234">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e752f-234">Remarks</span></span>

<span data-ttu-id="e752f-235">Доступ к классу **\_ виртуалсистемманажементсервицесеттингдата мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="e752f-235">Access to the **Msvm\_VirtualSystemManagementServiceSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e752f-236">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e752f-236">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e752f-237">Требования</span><span class="sxs-lookup"><span data-stu-id="e752f-237">Requirements</span></span>



| <span data-ttu-id="e752f-238">Требование</span><span class="sxs-lookup"><span data-stu-id="e752f-238">Requirement</span></span> | <span data-ttu-id="e752f-239">Значение</span><span class="sxs-lookup"><span data-stu-id="e752f-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e752f-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e752f-240">Minimum supported client</span></span><br/> | <span data-ttu-id="e752f-241">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e752f-241">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e752f-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e752f-242">Minimum supported server</span></span><br/> | <span data-ttu-id="e752f-243">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e752f-243">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e752f-244">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e752f-244">Namespace</span></span><br/>                | <span data-ttu-id="e752f-245">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e752f-245">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e752f-246">MOF</span><span class="sxs-lookup"><span data-stu-id="e752f-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e752f-247"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e752f-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e752f-248">DLL</span><span class="sxs-lookup"><span data-stu-id="e752f-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e752f-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e752f-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e752f-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e752f-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e752f-251">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="e752f-251">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="e752f-252">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="e752f-252">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="e752f-253">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e752f-253">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e752f-254">Классы управления виртуальной системой</span><span class="sxs-lookup"><span data-stu-id="e752f-254">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

