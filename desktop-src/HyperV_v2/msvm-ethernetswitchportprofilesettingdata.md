---
description: Представляет параметры профиля порта.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Класс Msvm_EthernetSwitchPortProfileSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684696"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a><span data-ttu-id="fc98e-103">\_Класс мсвм есернетсвитчпортпрофилесеттингдата</span><span class="sxs-lookup"><span data-stu-id="fc98e-103">Msvm\_EthernetSwitchPortProfileSettingData class</span></span>

<span data-ttu-id="fc98e-104">Представляет параметры профиля порта.</span><span class="sxs-lookup"><span data-stu-id="fc98e-104">Represents the port profile settings.</span></span>

<span data-ttu-id="fc98e-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fc98e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc98e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc98e-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a><span data-ttu-id="fc98e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fc98e-107">Members</span></span>

<span data-ttu-id="fc98e-108">Класс **мсвм \_ есернетсвитчпортпрофилесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fc98e-108">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fc98e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc98e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc98e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc98e-110">Properties</span></span>

<span data-ttu-id="fc98e-111">Класс **мсвм \_ есернетсвитчпортпрофилесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fc98e-111">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc98e-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="fc98e-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc98e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fc98e-115">A short description of the object.</span></span> <span data-ttu-id="fc98e-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры профиля порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="fc98e-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-117">**кднлабелид**</span><span class="sxs-lookup"><span data-stu-id="fc98e-117">**CdnLabelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc98e-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-120">Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-120">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-121">Идентификатор метки CDN.</span><span class="sxs-lookup"><span data-stu-id="fc98e-121">The CDN label identifier.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-122">**кднлабелстринг**</span><span class="sxs-lookup"><span data-stu-id="fc98e-122">**CdnLabelString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-125">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (12), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-126">Строка метки CDN.</span><span class="sxs-lookup"><span data-stu-id="fc98e-126">The CDN label string.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc98e-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc98e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-130">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fc98e-130">A description of the object.</span></span> <span data-ttu-id="fc98e-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет параметры профиля порта".</span><span class="sxs-lookup"><span data-stu-id="fc98e-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port profile settings.".</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fc98e-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc98e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-135">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="fc98e-135">A display name for the object.</span></span> <span data-ttu-id="fc98e-136">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры профиля порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="fc98e-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fc98e-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc98e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-140">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="fc98e-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-141">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="fc98e-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fc98e-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc98e-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-143">**NetCfgInstanceId**</span><span class="sxs-lookup"><span data-stu-id="fc98e-143">**NetCfgInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-146">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (6), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-147">Уникальный идентификатор устройства для подинтерфейса.</span><span class="sxs-lookup"><span data-stu-id="fc98e-147">An unique device identifier of the subinterface.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-148">**пЦибуснумбер**</span><span class="sxs-lookup"><span data-stu-id="fc98e-148">**PciBusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc98e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-151">Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-151">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-152">Номер шины PCI.</span><span class="sxs-lookup"><span data-stu-id="fc98e-152">The PCI bus number.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-153">**пЦидевиценумбер**</span><span class="sxs-lookup"><span data-stu-id="fc98e-153">**PciDeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc98e-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-156">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-156">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-157">Номер устройства PCI.</span><span class="sxs-lookup"><span data-stu-id="fc98e-157">The PCI device number.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-158">**пЦифунктионнумбер**</span><span class="sxs-lookup"><span data-stu-id="fc98e-158">**PciFunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc98e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-161">Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-161">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-162">Номер функции PCI.</span><span class="sxs-lookup"><span data-stu-id="fc98e-162">The PCI function number.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-163">**пЦисегментнумбер**</span><span class="sxs-lookup"><span data-stu-id="fc98e-163">**PciSegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-164">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc98e-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-166">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-166">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-167">Номер сегмента PCI.</span><span class="sxs-lookup"><span data-stu-id="fc98e-167">The PCI segment number.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-168">**профиледата**</span><span class="sxs-lookup"><span data-stu-id="fc98e-168">**ProfileData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-169">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc98e-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-171">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-171">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-172">Дополнительные данные для профиля порта.</span><span class="sxs-lookup"><span data-stu-id="fc98e-172">Additional data for the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-173">**ProfileId**</span><span class="sxs-lookup"><span data-stu-id="fc98e-173">**ProfileId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-176">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (2), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-177">Идентификатор профиля порта.</span><span class="sxs-lookup"><span data-stu-id="fc98e-177">The identifier of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-178">**ProfileName**</span><span class="sxs-lookup"><span data-stu-id="fc98e-178">**ProfileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-181">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-182">Имя профиля порта.</span><span class="sxs-lookup"><span data-stu-id="fc98e-182">The name of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-183">**Поставщика**</span><span class="sxs-lookup"><span data-stu-id="fc98e-183">**VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-186">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (4), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-187">Идентификатор поставщика, определяющего профиль.</span><span class="sxs-lookup"><span data-stu-id="fc98e-187">The identifier of the vendor defining the profile.</span></span>

</dd> <dt>

<span data-ttu-id="fc98e-188">**ИмяПоставщика**</span><span class="sxs-lookup"><span data-stu-id="fc98e-188">**VendorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc98e-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc98e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fc98e-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fc98e-191">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (3), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="fc98e-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="fc98e-192">Имя поставщика, определяющего профиль.</span><span class="sxs-lookup"><span data-stu-id="fc98e-192">The name of the vendor defining the profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc98e-193">Требования</span><span class="sxs-lookup"><span data-stu-id="fc98e-193">Requirements</span></span>



| <span data-ttu-id="fc98e-194">Требование</span><span class="sxs-lookup"><span data-stu-id="fc98e-194">Requirement</span></span> | <span data-ttu-id="fc98e-195">Значение</span><span class="sxs-lookup"><span data-stu-id="fc98e-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc98e-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc98e-196">Minimum supported client</span></span><br/> | <span data-ttu-id="fc98e-197">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fc98e-197">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fc98e-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc98e-198">Minimum supported server</span></span><br/> | <span data-ttu-id="fc98e-199">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fc98e-199">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc98e-200">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fc98e-200">Namespace</span></span><br/>                | <span data-ttu-id="fc98e-201">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fc98e-201">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc98e-202">MOF</span><span class="sxs-lookup"><span data-stu-id="fc98e-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc98e-203"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc98e-203"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc98e-204">DLL</span><span class="sxs-lookup"><span data-stu-id="fc98e-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc98e-205"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc98e-205"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

