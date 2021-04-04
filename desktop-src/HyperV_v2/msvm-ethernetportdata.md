---
description: Абстрактный класс, представляющий данные времени выполнения порта, собираемые расширением коммутатора Ethernet.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Класс Msvm_EthernetPortData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910155"
---
# <a name="msvm_ethernetportdata-class"></a><span data-ttu-id="1d89b-103">\_Класс мсвм есернетпортдата</span><span class="sxs-lookup"><span data-stu-id="1d89b-103">Msvm\_EthernetPortData class</span></span>

<span data-ttu-id="1d89b-104">Абстрактный класс, представляющий данные времени выполнения порта, собираемые расширением коммутатора Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1d89b-104">An abstract class that represents port runtime data collected by an Ethernet switch extension.</span></span> <span data-ttu-id="1d89b-105">Все классы данных портов Ethernet должны быть производными от этого абстрактного класса.</span><span class="sxs-lookup"><span data-stu-id="1d89b-105">All Ethernet port data classes must derive from this abstract class.</span></span>

<span data-ttu-id="1d89b-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1d89b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d89b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d89b-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="1d89b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1d89b-108">Members</span></span>

<span data-ttu-id="1d89b-109">Класс **мсвм \_ есернетпортдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1d89b-109">The **Msvm\_EthernetPortData** class has these types of members:</span></span>

-   [<span data-ttu-id="1d89b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d89b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d89b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d89b-111">Properties</span></span>

<span data-ttu-id="1d89b-112">Класс **мсвм \_ есернетпортдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1d89b-112">The **Msvm\_EthernetPortData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d89b-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1d89b-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-116">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1d89b-116">A short description of the object.</span></span> <span data-ttu-id="1d89b-117">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d89b-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-118">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d89b-118">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-121">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d89b-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-122">Имя подкласса, используемого при создании этого экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="1d89b-122">The name of the subclass used in the creation of this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1d89b-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-126">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1d89b-126">A description of the object.</span></span> <span data-ttu-id="1d89b-127">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d89b-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-128">**девицекреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1d89b-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-131">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-[**код \_ модели**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d89b-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-132">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="1d89b-132">The scoping system's creation class name.</span></span> <span data-ttu-id="1d89b-133">Для этого свойства всегда задано значение "Мсвм \_ есернетсвитчпорт".</span><span class="sxs-lookup"><span data-stu-id="1d89b-133">This property is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d89b-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-137">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM-[**код \_ модели**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1d89b-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-138">ИДЕНТИФИКАТОР устройства, определяющего область данного экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="1d89b-138">The Device ID of the port that scopes this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-139">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1d89b-139">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-142">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1d89b-142">A display name for the object.</span></span> <span data-ttu-id="1d89b-143">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d89b-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d89b-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-147">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="1d89b-147">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-148">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="1d89b-148">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1d89b-149">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d89b-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-150">**Name**</span><span class="sxs-lookup"><span data-stu-id="1d89b-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-153">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d89b-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-154">Строка, уникально идентифицирующая этот экземпляр данных порта в области действия коммутатора и порта.</span><span class="sxs-lookup"><span data-stu-id="1d89b-154">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-155">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1d89b-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-158">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d89b-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-159">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="1d89b-159">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="1d89b-160">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d89b-160">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d89b-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1d89b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d89b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d89b-163">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier) [**распространен**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d89b-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d89b-164">Имя виртуального коммутатора, который ограничивает область данного экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="1d89b-164">The name of the virtual switch that scopes this port data instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d89b-165">Требования</span><span class="sxs-lookup"><span data-stu-id="1d89b-165">Requirements</span></span>



| <span data-ttu-id="1d89b-166">Требование</span><span class="sxs-lookup"><span data-stu-id="1d89b-166">Requirement</span></span> | <span data-ttu-id="1d89b-167">Значение</span><span class="sxs-lookup"><span data-stu-id="1d89b-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d89b-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d89b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="1d89b-169">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1d89b-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1d89b-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d89b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="1d89b-171">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1d89b-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d89b-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d89b-172">Namespace</span></span><br/>                | <span data-ttu-id="1d89b-173">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1d89b-173">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d89b-174">MOF</span><span class="sxs-lookup"><span data-stu-id="1d89b-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d89b-175"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d89b-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d89b-176">DLL</span><span class="sxs-lookup"><span data-stu-id="1d89b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d89b-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d89b-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

