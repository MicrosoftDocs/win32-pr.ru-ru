---
description: Представляет параметры пропускной способности порта.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Класс Msvm_EthernetSwitchPortBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684265"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a><span data-ttu-id="26dc6-103">\_Класс мсвм есернетсвитчпортбандвидссеттингдата</span><span class="sxs-lookup"><span data-stu-id="26dc6-103">Msvm\_EthernetSwitchPortBandwidthSettingData class</span></span>

<span data-ttu-id="26dc6-104">Представляет параметры пропускной способности порта.</span><span class="sxs-lookup"><span data-stu-id="26dc6-104">Represents the port bandwidth settings.</span></span>

<span data-ttu-id="26dc6-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="26dc6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26dc6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26dc6-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a><span data-ttu-id="26dc6-107">Члены</span><span class="sxs-lookup"><span data-stu-id="26dc6-107">Members</span></span>

<span data-ttu-id="26dc6-108">Класс **мсвм \_ есернетсвитчпортбандвидссеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="26dc6-108">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="26dc6-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="26dc6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26dc6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="26dc6-110">Properties</span></span>

<span data-ttu-id="26dc6-111">Класс **мсвм \_ есернетсвитчпортбандвидссеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="26dc6-111">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26dc6-112">**бурстлимит**</span><span class="sxs-lookup"><span data-stu-id="26dc6-112">**BurstLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-113">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26dc6-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26dc6-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-115">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="26dc6-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-116">Пиковая пропускная способность, разрешенная из порта во время пакетов.</span><span class="sxs-lookup"><span data-stu-id="26dc6-116">The peak bandwidth allowed from the port during bursts.</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-117">**бурстсизе**</span><span class="sxs-lookup"><span data-stu-id="26dc6-117">**BurstSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-118">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26dc6-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26dc6-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-120">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="26dc6-120">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-121">Максимально допустимый размер пакета.</span><span class="sxs-lookup"><span data-stu-id="26dc6-121">The maximum burst size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-122">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="26dc6-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26dc6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26dc6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-125">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="26dc6-125">A short description of the object.</span></span> <span data-ttu-id="26dc6-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры пропускной способности порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="26dc6-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="26dc6-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26dc6-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26dc6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-130">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="26dc6-130">A description of the object.</span></span> <span data-ttu-id="26dc6-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет параметры пропускной способности порта".</span><span class="sxs-lookup"><span data-stu-id="26dc6-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="26dc6-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26dc6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26dc6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-135">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="26dc6-135">A display name for the object.</span></span> <span data-ttu-id="26dc6-136">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры пропускной способности порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="26dc6-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26dc6-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26dc6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26dc6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-140">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="26dc6-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-141">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="26dc6-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="26dc6-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="26dc6-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-143">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="26dc6-143">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-144">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26dc6-144">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26dc6-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-146">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="26dc6-146">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-147">Ограничение пропускной способности, разрешенное для порта.</span><span class="sxs-lookup"><span data-stu-id="26dc6-147">The bandwidth limit allowed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-148">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="26dc6-148">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-149">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26dc6-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26dc6-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-151">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="26dc6-151">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-152">Минимальная абсолютная пропускная способность, гарантированная для порта.</span><span class="sxs-lookup"><span data-stu-id="26dc6-152">The minimum absolute bandwidth guaranteed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="26dc6-153">**Weight**</span><span class="sxs-lookup"><span data-stu-id="26dc6-153">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26dc6-154">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26dc6-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26dc6-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26dc6-156">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="26dc6-156">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="26dc6-157">Минимальная пропускная способность, гарантированная для порта.</span><span class="sxs-lookup"><span data-stu-id="26dc6-157">The minimum bandwidth in weight guaranteed for the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26dc6-158">Требования</span><span class="sxs-lookup"><span data-stu-id="26dc6-158">Requirements</span></span>



| <span data-ttu-id="26dc6-159">Требование</span><span class="sxs-lookup"><span data-stu-id="26dc6-159">Requirement</span></span> | <span data-ttu-id="26dc6-160">Значение</span><span class="sxs-lookup"><span data-stu-id="26dc6-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26dc6-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26dc6-161">Minimum supported client</span></span><br/> | <span data-ttu-id="26dc6-162">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="26dc6-162">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="26dc6-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26dc6-163">Minimum supported server</span></span><br/> | <span data-ttu-id="26dc6-164">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="26dc6-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26dc6-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26dc6-165">Namespace</span></span><br/>                | <span data-ttu-id="26dc6-166">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="26dc6-166">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="26dc6-167">MOF</span><span class="sxs-lookup"><span data-stu-id="26dc6-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26dc6-168"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26dc6-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26dc6-169">DLL</span><span class="sxs-lookup"><span data-stu-id="26dc6-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26dc6-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26dc6-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

