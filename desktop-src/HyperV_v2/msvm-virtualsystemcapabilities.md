---
description: Описывает возможности связанной Мсвм \_ ComputerSystem.
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Класс Msvm_VirtualSystemCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262895"
---
# <a name="msvm_virtualsystemcapabilities-class"></a><span data-ttu-id="6d2eb-103">\_Класс мсвм виртуалсистемкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="6d2eb-103">Msvm\_VirtualSystemCapabilities class</span></span>

<span data-ttu-id="6d2eb-104">Описывает возможности связанной [**мсвм \_ ComputerSystem**](msvm-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="6d2eb-104">Describes the capabilities of the associated [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="6d2eb-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2eb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d2eb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="6d2eb-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6d2eb-107">Members</span></span>

<span data-ttu-id="6d2eb-108">Класс **мсвм \_ виртуалсистемкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6d2eb-108">The **Msvm\_VirtualSystemCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="6d2eb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d2eb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d2eb-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d2eb-110">Properties</span></span>

<span data-ttu-id="6d2eb-111">Класс **мсвм \_ виртуалсистемкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-111">The **Msvm\_VirtualSystemCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d2eb-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-115">A short description of the object.</span></span> <span data-ttu-id="6d2eb-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6d2eb-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6d2eb-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-120">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-120">A description of the object.</span></span> <span data-ttu-id="6d2eb-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6d2eb-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6d2eb-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-125">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-125">A display name for the object.</span></span> <span data-ttu-id="6d2eb-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6d2eb-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6d2eb-127">**елементнамидитсуппортед**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-127">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-130">Указывает, можно ли изменить свойство **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="6d2eb-130">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="6d2eb-131">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-131">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="6d2eb-132">**елементнамемаск**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-132">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-135">Задает ограничения для **ElementName**, выраженные в виде регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-135">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="6d2eb-136">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-136">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="6d2eb-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-140">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-141">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6d2eb-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6d2eb-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6d2eb-143">**макселементнамелен**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-143">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-144">Тип данных: **unit16**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-144">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-146">Квалификаторы: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="6d2eb-146">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-147">Задает максимальную поддерживаемую длину свойства **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="6d2eb-147">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="6d2eb-148">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-148">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="6d2eb-149">**рекуестедстатессуппортед**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-149">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d2eb-150">Тип данных: массив **unit16**</span><span class="sxs-lookup"><span data-stu-id="6d2eb-150">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="6d2eb-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d2eb-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d2eb-152">Указывает возможные состояния, которые могут быть запрошены при использовании метода **RequestStateChange** для включенного логического элемента.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-152">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="6d2eb-153">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="6d2eb-153">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="6d2eb-154">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2eb-154">Value</span></span>                                                                         | <span data-ttu-id="6d2eb-155">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2eb-155">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="6d2eb-156"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-156"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="6d2eb-157">Активировано</span><span class="sxs-lookup"><span data-stu-id="6d2eb-157">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="6d2eb-158"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-158"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="6d2eb-159">Отключит</span><span class="sxs-lookup"><span data-stu-id="6d2eb-159">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="6d2eb-160"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-160"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="6d2eb-161">Завершение работы</span><span class="sxs-lookup"><span data-stu-id="6d2eb-161">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="6d2eb-162"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-162"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="6d2eb-163">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="6d2eb-163">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="6d2eb-164"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-164"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="6d2eb-165">Тест</span><span class="sxs-lookup"><span data-stu-id="6d2eb-165">Test</span></span><br/>      |
| <dl> <span data-ttu-id="6d2eb-166"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-166"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="6d2eb-167">Которого</span><span class="sxs-lookup"><span data-stu-id="6d2eb-167">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="6d2eb-168"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-168"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="6d2eb-169">Замораживани</span><span class="sxs-lookup"><span data-stu-id="6d2eb-169">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="6d2eb-170"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-170"><dt>10</dt></span></span> </dl> | <span data-ttu-id="6d2eb-171">Перезагрузка</span><span class="sxs-lookup"><span data-stu-id="6d2eb-171">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="6d2eb-172"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-172"><dt>11</dt></span></span> </dl> | <span data-ttu-id="6d2eb-173">Reset</span><span class="sxs-lookup"><span data-stu-id="6d2eb-173">Reset</span></span><br/>     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d2eb-174">Требования</span><span class="sxs-lookup"><span data-stu-id="6d2eb-174">Requirements</span></span>



| <span data-ttu-id="6d2eb-175">Требование</span><span class="sxs-lookup"><span data-stu-id="6d2eb-175">Requirement</span></span> | <span data-ttu-id="6d2eb-176">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2eb-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2eb-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d2eb-177">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2eb-178">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6d2eb-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6d2eb-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d2eb-179">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2eb-180">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6d2eb-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d2eb-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d2eb-181">Namespace</span></span><br/>                | <span data-ttu-id="6d2eb-182">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6d2eb-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6d2eb-183">MOF</span><span class="sxs-lookup"><span data-stu-id="6d2eb-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d2eb-184"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d2eb-185">DLL</span><span class="sxs-lookup"><span data-stu-id="6d2eb-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d2eb-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d2eb-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

