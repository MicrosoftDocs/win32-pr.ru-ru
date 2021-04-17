---
description: Абстрактный класс, представляющий ресурс для заданного экземпляра коммутатора Ethernet.
ms.assetid: 5ae1be2a-8d59-4efe-a4ae-7cac1727cfa2
title: Класс Msvm_EthernetSwitchData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchData
- Msvm_EthernetSwitchData.InstanceID
- Msvm_EthernetSwitchData.Caption
- Msvm_EthernetSwitchData.Description
- Msvm_EthernetSwitchData.ElementName
- Msvm_EthernetSwitchData.SystemCreationClassName
- Msvm_EthernetSwitchData.SystemName
- Msvm_EthernetSwitchData.CreationClassName
- Msvm_EthernetSwitchData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca2e4e01266a0a7da0f3ec85a86615406625f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663469"
---
# <a name="msvm_ethernetswitchdata-class"></a><span data-ttu-id="f7a34-103">\_Класс мсвм есернетсвитчдата</span><span class="sxs-lookup"><span data-stu-id="f7a34-103">Msvm\_EthernetSwitchData class</span></span>

<span data-ttu-id="f7a34-104">Абстрактный класс, представляющий ресурс для заданного экземпляра коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="f7a34-104">Abstract class that represents a resource for a given instance of an Ethernet switch.</span></span>

<span data-ttu-id="f7a34-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f7a34-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a34-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7a34-106">Syntax</span></span>

``` syntax
[Abstract, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchData : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchBandwidthData";
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="f7a34-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f7a34-107">Members</span></span>

<span data-ttu-id="f7a34-108">Класс **мсвм \_ есернетсвитчдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f7a34-108">The **Msvm\_EthernetSwitchData** class has these types of members:</span></span>

-   [<span data-ttu-id="f7a34-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7a34-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7a34-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f7a34-110">Properties</span></span>

<span data-ttu-id="f7a34-111">Класс **мсвм \_ есернетсвитчдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f7a34-111">The **Msvm\_EthernetSwitchData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7a34-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f7a34-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f7a34-115">A short description of the object.</span></span> <span data-ttu-id="f7a34-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f7a34-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f7a34-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f7a34-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-120">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f7a34-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-121">Имя класса или подкласса, используемого при создании этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f7a34-121">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="f7a34-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f7a34-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-125">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f7a34-125">A description of the object.</span></span> <span data-ttu-id="f7a34-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f7a34-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f7a34-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f7a34-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-130">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f7a34-130">A display name for the object.</span></span> <span data-ttu-id="f7a34-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f7a34-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f7a34-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f7a34-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-135">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="f7a34-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-136">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="f7a34-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f7a34-137">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f7a34-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f7a34-138">**Name**</span><span class="sxs-lookup"><span data-stu-id="f7a34-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-141">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f7a34-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-142">Уникальное имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7a34-142">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f7a34-143">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f7a34-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-146">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f7a34-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-147">Имя класса создания системы размещения.</span><span class="sxs-lookup"><span data-stu-id="f7a34-147">The hosting system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f7a34-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f7a34-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7a34-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f7a34-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f7a34-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7a34-151">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f7a34-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7a34-152">Имя виртуального коммутатора, к которому привязан связанный экземпляр ресурса.</span><span class="sxs-lookup"><span data-stu-id="f7a34-152">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7a34-153">Требования</span><span class="sxs-lookup"><span data-stu-id="f7a34-153">Requirements</span></span>



| <span data-ttu-id="f7a34-154">Требование</span><span class="sxs-lookup"><span data-stu-id="f7a34-154">Requirement</span></span> | <span data-ttu-id="f7a34-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f7a34-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a34-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7a34-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a34-157">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f7a34-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f7a34-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7a34-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a34-159">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f7a34-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7a34-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7a34-160">Namespace</span></span><br/>                | <span data-ttu-id="f7a34-161">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f7a34-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f7a34-162">MOF</span><span class="sxs-lookup"><span data-stu-id="f7a34-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7a34-163"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7a34-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7a34-164">DLL</span><span class="sxs-lookup"><span data-stu-id="f7a34-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7a34-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7a34-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

