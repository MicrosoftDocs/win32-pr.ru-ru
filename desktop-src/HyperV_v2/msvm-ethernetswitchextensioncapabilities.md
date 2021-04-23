---
description: Представляет ассоциацию между расширениями Ethernet и их возможностями.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Класс Msvm_EthernetSwitchExtensionCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819497"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a><span data-ttu-id="c1dec-103">\_Класс мсвм есернетсвитчекстенсионкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="c1dec-103">Msvm\_EthernetSwitchExtensionCapabilities class</span></span>

<span data-ttu-id="c1dec-104">Представляет ассоциацию между расширениями Ethernet и их возможностями.</span><span class="sxs-lookup"><span data-stu-id="c1dec-104">Represents the association between Ethernet extensions and their capabilities.</span></span>

<span data-ttu-id="c1dec-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c1dec-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1dec-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="c1dec-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c1dec-107">Members</span></span>

<span data-ttu-id="c1dec-108">Класс **мсвм \_ есернетсвитчекстенсионкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c1dec-108">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="c1dec-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1dec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1dec-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1dec-110">Properties</span></span>

<span data-ttu-id="c1dec-111">Класс **мсвм \_ есернетсвитчекстенсионкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c1dec-111">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1dec-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c1dec-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1dec-113">Тип данных: **[ **мсвм \_ есернетсвитчфеатурекапабилитиес**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="c1dec-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c1dec-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1dec-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1dec-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("возможности")</span><span class="sxs-lookup"><span data-stu-id="c1dec-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="c1dec-116">Ссылка на экземпляр класса [**мсвм \_ есернетсвитчфеатурекапабилитиес**](msvm-ethernetswitchfeaturecapabilities.md) , представляющий объект capabilities, связанный с параметром.</span><span class="sxs-lookup"><span data-stu-id="c1dec-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the capabilities object associated with the switch.</span></span> <span data-ttu-id="c1dec-117">Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="c1dec-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="c1dec-118">**Характеристики**</span><span class="sxs-lookup"><span data-stu-id="c1dec-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1dec-119">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c1dec-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c1dec-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1dec-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1dec-121">Содержит описательные сведения о возможностях.</span><span class="sxs-lookup"><span data-stu-id="c1dec-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="c1dec-122">Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="c1dec-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="c1dec-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c1dec-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="c1dec-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c1dec-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="c1dec-125"><dt>**По умолчанию**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c1dec-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="c1dec-126">Связанные возможности представляют возможности управляемого элемента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1dec-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="c1dec-127"><dt>**Текущие**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c1dec-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="c1dec-128">Связанные возможности представляют текущие возможности управляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="c1dec-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c1dec-129">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="c1dec-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1dec-130">Тип данных: **[ **мсвм \_ инсталледесернетсвитчекстенсион**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="c1dec-130">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c1dec-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1dec-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1dec-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("манажеделемент")</span><span class="sxs-lookup"><span data-stu-id="c1dec-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="c1dec-133">Ссылка на экземпляр класса [**мсвм \_ инсталледесернетсвитчекстенсион**](msvm-installedethernetswitchextension.md) , представляющий установленное расширение.</span><span class="sxs-lookup"><span data-stu-id="c1dec-133">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents the installed extension.</span></span> <span data-ttu-id="c1dec-134">Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="c1dec-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1dec-135">Требования</span><span class="sxs-lookup"><span data-stu-id="c1dec-135">Requirements</span></span>



| <span data-ttu-id="c1dec-136">Требование</span><span class="sxs-lookup"><span data-stu-id="c1dec-136">Requirement</span></span> | <span data-ttu-id="c1dec-137">Значение</span><span class="sxs-lookup"><span data-stu-id="c1dec-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dec-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1dec-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c1dec-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c1dec-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1dec-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1dec-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c1dec-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c1dec-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1dec-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1dec-142">Namespace</span></span><br/>                | <span data-ttu-id="c1dec-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c1dec-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1dec-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c1dec-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1dec-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1dec-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1dec-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c1dec-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1dec-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1dec-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

