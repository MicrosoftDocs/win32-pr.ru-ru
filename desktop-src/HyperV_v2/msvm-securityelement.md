---
description: Представляет параметры безопасности среды выполнения CIM \_ ComputerSystem.
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Класс Msvm_SecurityElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f0de0fe1a515db0e7b1d8d49b96b61500703480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999769"
---
# <a name="msvm_securityelement-class"></a><span data-ttu-id="ffed9-103">\_Класс SecurityElement мсвм</span><span class="sxs-lookup"><span data-stu-id="ffed9-103">Msvm\_SecurityElement class</span></span>

<span data-ttu-id="ffed9-104">Представляет параметры безопасности среды выполнения [**CIM \_ ComputerSystem**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="ffed9-104">Represents the runtime security settings of a [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="ffed9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ffed9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffed9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffed9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a><span data-ttu-id="ffed9-107">Члены</span><span class="sxs-lookup"><span data-stu-id="ffed9-107">Members</span></span>

<span data-ttu-id="ffed9-108">Класс **\_ SecurityElement мсвм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ffed9-108">The **Msvm\_SecurityElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ffed9-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffed9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffed9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffed9-110">Properties</span></span>

<span data-ttu-id="ffed9-111">Класс **\_ SecurityElement мсвм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ffed9-111">The **Msvm\_SecurityElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffed9-112">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ffed9-112">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed9-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ffed9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffed9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-115">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ffed9-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ffed9-116">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ffed9-116">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="ffed9-117">При использовании с другими ключевыми свойствами этого класса **свойство CreationClassName** позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="ffed9-117">When used with the other key properties of this class, **CreationClassName** allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="ffed9-118">**енкриптстатеандвммигратионтраффиценаблед**</span><span class="sxs-lookup"><span data-stu-id="ffed9-118">**EncryptStateAndVmMigrationTrafficEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed9-119">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ffed9-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffed9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffed9-121">Указывает, имеет ли виртуальная машина в настоящий момент трафик о состоянии и миграции.</span><span class="sxs-lookup"><span data-stu-id="ffed9-121">Indicates whether the VM is currently having its state and migration traffic encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="ffed9-122">**Экранирование**</span><span class="sxs-lookup"><span data-stu-id="ffed9-122">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed9-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ffed9-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffed9-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffed9-125">Указывает, является ли виртуальная машина в данный момент экранированной.</span><span class="sxs-lookup"><span data-stu-id="ffed9-125">Indicates whether the VM is currently shielded.</span></span>

</dd> <dt>

<span data-ttu-id="ffed9-126">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ffed9-126">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed9-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ffed9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffed9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-129">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="ffed9-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="ffed9-130">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="ffed9-130">The creation class name of the scoping system.</span></span>

</dd> <dt>

<span data-ttu-id="ffed9-131">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ffed9-131">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed9-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ffed9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffed9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffed9-134">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="ffed9-134">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="ffed9-135">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="ffed9-135">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffed9-136">Требования</span><span class="sxs-lookup"><span data-stu-id="ffed9-136">Requirements</span></span>



| <span data-ttu-id="ffed9-137">Требование</span><span class="sxs-lookup"><span data-stu-id="ffed9-137">Requirement</span></span> | <span data-ttu-id="ffed9-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ffed9-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffed9-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffed9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ffed9-140">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="ffed9-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ffed9-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffed9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ffed9-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ffed9-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ffed9-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ffed9-143">Namespace</span></span><br/>                | <span data-ttu-id="ffed9-144">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ffed9-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffed9-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ffed9-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffed9-146"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffed9-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffed9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ffed9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffed9-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffed9-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffed9-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffed9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffed9-150">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ffed9-150">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

