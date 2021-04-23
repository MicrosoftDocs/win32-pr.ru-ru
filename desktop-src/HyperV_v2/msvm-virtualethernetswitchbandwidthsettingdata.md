---
description: Представляет параметры пропускной способности для виртуального коммутатора.
ms.assetid: bc6f8cd3-f74a-4f4a-9ffe-a88def3966d9
title: Класс Msvm_VirtualEthernetSwitchBandwidthSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchBandwidthSettingData
- Msvm_VirtualEthernetSwitchBandwidthSettingData.InstanceID
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Caption
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Description
- Msvm_VirtualEthernetSwitchBandwidthSettingData.ElementName
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowReservation
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec94409366761ee208d3e8a6af59a4d07527d82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650956"
---
# <a name="msvm_virtualethernetswitchbandwidthsettingdata-class"></a><span data-ttu-id="c8fb5-103">\_Класс мсвм виртуалесернетсвитчбандвидссеттингдата</span><span class="sxs-lookup"><span data-stu-id="c8fb5-103">Msvm\_VirtualEthernetSwitchBandwidthSettingData class</span></span>

<span data-ttu-id="c8fb5-104">Представляет параметры пропускной способности для виртуального коммутатора.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-104">Represents the bandwidth settings for a virtual switch.</span></span>

<span data-ttu-id="c8fb5-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8fb5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8fb5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("3EB2B8E8-4ABF-4DBF-9071-16DD47481FBE"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchBandwidthSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  string InstanceID = "Microsoft:Definition\GUID\Default";
  string Caption = "Ethernet Switch Bandwidth Settings";
  string Description = "Represents the switch bandwidth settings.";
  string ElementName = "Ethernet Switch Bandwidth Settings";
  UINT64 DefaultFlowReservation = 0;
  UINT64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="c8fb5-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c8fb5-107">Members</span></span>

<span data-ttu-id="c8fb5-108">Класс **мсвм \_ виртуалесернетсвитчбандвидссеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c8fb5-108">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c8fb5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8fb5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8fb5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8fb5-110">Properties</span></span>

<span data-ttu-id="c8fb5-111">Класс **мсвм \_ виртуалесернетсвитчбандвидссеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-111">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8fb5-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8fb5-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8fb5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8fb5-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-115">A short description of the object.</span></span> <span data-ttu-id="c8fb5-116">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и всегда имеет значение "Параметры пропускной способности коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="c8fb5-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="c8fb5-117">**дефаултфловресерватион**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-117">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8fb5-118">Тип данных: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-118">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c8fb5-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-120">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="c8fb5-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c8fb5-121">Указывает абсолютное резервирование пропускной способности для неклассифицированных потоков на базовом адаптере.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-121">Specifies the absolute bandwidth reservation for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c8fb5-122">**дефаултфловвеигхт**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-122">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8fb5-123">Тип данных: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-123">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c8fb5-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-125">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="c8fb5-125">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c8fb5-126">Указывает зарезервированную пропускную способность для неклассифицированных потоков на базовом адаптере.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-126">Specifies the bandwidth reservation in weight for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c8fb5-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8fb5-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8fb5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8fb5-130">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-130">A description of the object.</span></span> <span data-ttu-id="c8fb5-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет параметры пропускной способности коммутатора".</span><span class="sxs-lookup"><span data-stu-id="c8fb5-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the switch bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="c8fb5-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8fb5-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8fb5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8fb5-135">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-135">A display name for the object.</span></span> <span data-ttu-id="c8fb5-136">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "Параметры пропускной способности коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="c8fb5-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="c8fb5-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8fb5-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8fb5-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8fb5-140">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c8fb5-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8fb5-141">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c8fb5-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c8fb5-142">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)) и всегда имеет значение "Microsoft: определение \\ *GUID* \\ по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="c8fb5-142">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:Definition\\*GUID*\\Default".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8fb5-143">Требования</span><span class="sxs-lookup"><span data-stu-id="c8fb5-143">Requirements</span></span>



| <span data-ttu-id="c8fb5-144">Требование</span><span class="sxs-lookup"><span data-stu-id="c8fb5-144">Requirement</span></span> | <span data-ttu-id="c8fb5-145">Значение</span><span class="sxs-lookup"><span data-stu-id="c8fb5-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8fb5-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8fb5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c8fb5-147">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c8fb5-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c8fb5-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8fb5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c8fb5-149">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c8fb5-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8fb5-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c8fb5-150">Namespace</span></span><br/>                | <span data-ttu-id="c8fb5-151">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c8fb5-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c8fb5-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c8fb5-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8fb5-153"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8fb5-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8fb5-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c8fb5-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8fb5-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8fb5-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

