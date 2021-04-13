---
description: Представляет операционные параметры коммутатора.
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Класс Msvm_EthernetSwitchOperationalData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350662"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a><span data-ttu-id="ef59f-103">\_Класс мсвм есернетсвитчоператионалдата</span><span class="sxs-lookup"><span data-stu-id="ef59f-103">Msvm\_EthernetSwitchOperationalData class</span></span>

<span data-ttu-id="ef59f-104">Представляет операционные параметры коммутатора.</span><span class="sxs-lookup"><span data-stu-id="ef59f-104">Represents switch operational parameters.</span></span>

<span data-ttu-id="ef59f-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ef59f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef59f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef59f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a><span data-ttu-id="ef59f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ef59f-107">Members</span></span>

<span data-ttu-id="ef59f-108">Класс **мсвм \_ есернетсвитчоператионалдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ef59f-108">The **Msvm\_EthernetSwitchOperationalData** class has these types of members:</span></span>

-   [<span data-ttu-id="ef59f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef59f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef59f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef59f-110">Properties</span></span>

<span data-ttu-id="ef59f-111">Класс **мсвм \_ есернетсвитчоператионалдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ef59f-111">The **Msvm\_EthernetSwitchOperationalData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef59f-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ef59f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ef59f-115">A short description of the object.</span></span> <span data-ttu-id="ef59f-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ef59f-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ef59f-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-120">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ef59f-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-121">Имя класса или подкласса, используемого при создании этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ef59f-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="ef59f-122">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ef59f-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-123">**куррентсвитчингмоде**</span><span class="sxs-lookup"><span data-stu-id="ef59f-123">**CurrentSwitchingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef59f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-126">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ef59f-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-127">Текущий режим переключения на коммутатор.</span><span class="sxs-lookup"><span data-stu-id="ef59f-127">The current switching mode on the switch.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef59f-128">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ef59f-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

<span data-ttu-id="ef59f-129">**802.1 q** (1)</span><span class="sxs-lookup"><span data-stu-id="ef59f-129">**802.1Q** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

<span data-ttu-id="ef59f-130">**802.1 КБГ** (2)</span><span class="sxs-lookup"><span data-stu-id="ef59f-130">**802.1Qbg** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

<span data-ttu-id="ef59f-131">**802.1 КБХ** (3)</span><span class="sxs-lookup"><span data-stu-id="ef59f-131">**802.1Qbh** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef59f-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef59f-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-135">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ef59f-135">A description of the object.</span></span> <span data-ttu-id="ef59f-136">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ef59f-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ef59f-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-140">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ef59f-140">A display name for the object.</span></span> <span data-ttu-id="ef59f-141">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ef59f-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ef59f-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-145">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ef59f-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-146">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ef59f-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ef59f-147">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ef59f-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-148">**Name**</span><span class="sxs-lookup"><span data-stu-id="ef59f-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-151">Квалификаторы: **ключ**, **Переопределение**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ef59f-151">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-152">Уникальное имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef59f-152">The unique name of the resource.</span></span> <span data-ttu-id="ef59f-153">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ef59f-153">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-154">**суппортедсвитчингмодес**</span><span class="sxs-lookup"><span data-stu-id="ef59f-154">**SupportedSwitchingModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-155">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef59f-155">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-157">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="ef59f-157">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-158">Режимы переключения, поддерживаемые параметром.</span><span class="sxs-lookup"><span data-stu-id="ef59f-158">The switching modes supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-159">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ef59f-159">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-162">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ef59f-162">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-163">Имя класса создания системы размещения.</span><span class="sxs-lookup"><span data-stu-id="ef59f-163">The hosting system's creation class name.</span></span> <span data-ttu-id="ef59f-164">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ef59f-164">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef59f-165">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ef59f-165">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef59f-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef59f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef59f-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef59f-168">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ef59f-168">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef59f-169">Имя виртуального коммутатора, к которому привязан связанный экземпляр ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef59f-169">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="ef59f-170">Это свойство наследуется от [**мсвм \_ есернетсвитчдата**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="ef59f-170">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef59f-171">Требования</span><span class="sxs-lookup"><span data-stu-id="ef59f-171">Requirements</span></span>



| <span data-ttu-id="ef59f-172">Требование</span><span class="sxs-lookup"><span data-stu-id="ef59f-172">Requirement</span></span> | <span data-ttu-id="ef59f-173">Значение</span><span class="sxs-lookup"><span data-stu-id="ef59f-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef59f-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef59f-174">Minimum supported client</span></span><br/> | <span data-ttu-id="ef59f-175">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef59f-175">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef59f-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef59f-176">Minimum supported server</span></span><br/> | <span data-ttu-id="ef59f-177">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef59f-177">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef59f-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef59f-178">Namespace</span></span><br/>                | <span data-ttu-id="ef59f-179">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ef59f-179">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef59f-180">MOF</span><span class="sxs-lookup"><span data-stu-id="ef59f-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef59f-181"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef59f-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef59f-182">DLL</span><span class="sxs-lookup"><span data-stu-id="ef59f-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef59f-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef59f-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

