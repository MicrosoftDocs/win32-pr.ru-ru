---
description: Представляет сеть, в которой служба миграции виртуальной системы прослушивает входящую миграцию виртуальной системы.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Класс Msvm_VirtualSystemMigrationNetworkSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896826"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a><span data-ttu-id="58619-103">\_Класс мсвм виртуалсистеммигратионнетворксеттингдата</span><span class="sxs-lookup"><span data-stu-id="58619-103">Msvm\_VirtualSystemMigrationNetworkSettingData class</span></span>

<span data-ttu-id="58619-104">Представляет сеть, в которой служба миграции виртуальной системы прослушивает входящую миграцию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="58619-104">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span>

<span data-ttu-id="58619-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="58619-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58619-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58619-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a><span data-ttu-id="58619-107">Члены</span><span class="sxs-lookup"><span data-stu-id="58619-107">Members</span></span>

<span data-ttu-id="58619-108">Класс **мсвм \_ виртуалсистеммигратионнетворксеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="58619-108">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="58619-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="58619-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58619-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="58619-110">Properties</span></span>

<span data-ttu-id="58619-111">Класс **мсвм \_ виртуалсистеммигратионнетворксеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="58619-111">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58619-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="58619-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58619-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58619-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58619-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="58619-115">A short description of the object.</span></span> <span data-ttu-id="58619-116">Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="58619-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="58619-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58619-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58619-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58619-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58619-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="58619-120">A description of the object.</span></span> <span data-ttu-id="58619-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58619-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58619-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="58619-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58619-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58619-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58619-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="58619-125">A display name for the object.</span></span> <span data-ttu-id="58619-126">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58619-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58619-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="58619-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58619-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58619-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58619-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="58619-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="58619-131">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="58619-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="58619-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58619-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58619-133">**Метрика**</span><span class="sxs-lookup"><span data-stu-id="58619-133">**Metric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58619-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58619-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58619-136">Метрика приоритета этой сети для миграции.</span><span class="sxs-lookup"><span data-stu-id="58619-136">The priority metric of this network for migration.</span></span> <span data-ttu-id="58619-137">Более низкие значения имеют более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="58619-137">Lower values are higher in priority.</span></span>

</dd> <dt>

<span data-ttu-id="58619-138">**PrefixLength**</span><span class="sxs-lookup"><span data-stu-id="58619-138">**PrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-139">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="58619-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="58619-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58619-141">Длина префикса подсети для миграции.</span><span class="sxs-lookup"><span data-stu-id="58619-141">The migration network subnet prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="58619-142">**субнетнумбер**</span><span class="sxs-lookup"><span data-stu-id="58619-142">**SubnetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58619-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58619-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58619-145">Номер подсети сети миграции.</span><span class="sxs-lookup"><span data-stu-id="58619-145">The migration network subnet number.</span></span>

</dd> <dt>

<span data-ttu-id="58619-146">**Теги**</span><span class="sxs-lookup"><span data-stu-id="58619-146">**Tags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58619-147">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="58619-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58619-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58619-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58619-149">Массив тегов для представления системы управления, которая установила эту сеть для службы миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="58619-149">An array of tags to represent which management system has set this network for virtual system migration service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58619-150">Требования</span><span class="sxs-lookup"><span data-stu-id="58619-150">Requirements</span></span>



| <span data-ttu-id="58619-151">Требование</span><span class="sxs-lookup"><span data-stu-id="58619-151">Requirement</span></span> | <span data-ttu-id="58619-152">Значение</span><span class="sxs-lookup"><span data-stu-id="58619-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58619-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58619-153">Minimum supported client</span></span><br/> | <span data-ttu-id="58619-154">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="58619-154">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58619-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58619-155">Minimum supported server</span></span><br/> | <span data-ttu-id="58619-156">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="58619-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58619-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58619-157">Namespace</span></span><br/>                | <span data-ttu-id="58619-158">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="58619-158">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="58619-159">MOF</span><span class="sxs-lookup"><span data-stu-id="58619-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58619-160"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58619-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58619-161">DLL</span><span class="sxs-lookup"><span data-stu-id="58619-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58619-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58619-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58619-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58619-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58619-164">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="58619-164">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="58619-165">**модифинетворксеттингс**</span><span class="sxs-lookup"><span data-stu-id="58619-165">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

