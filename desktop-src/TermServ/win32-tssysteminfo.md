---
title: Класс Win32_TSSystemInfo
description: Представляет информационную службу сервера централизованной публикации.
ms.assetid: fd8155dc-63bf-4001-ab93-dc87a6c91284
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSSystemInfo службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSSystemInfo, описание
topic_type:
- apiref
api_name:
- Win32_TSSystemInfo
- Win32_TSSystemInfo.Caption
- Win32_TSSystemInfo.Description
- Win32_TSSystemInfo.InstallDate
- Win32_TSSystemInfo.Name
- Win32_TSSystemInfo.Status
- Win32_TSSystemInfo.RDUGroup
- Win32_TSSystemInfo.ProviderVersion
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 188761bd06a32e0c6f246dfe41f354adf1e06332
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490086"
---
# <a name="win32_tssysteminfo-class"></a><span data-ttu-id="c408c-105">\_Класс Win32 тссистеминфо</span><span class="sxs-lookup"><span data-stu-id="c408c-105">Win32\_TSSystemInfo class</span></span>

<span data-ttu-id="c408c-106">Представляет информационную службу сервера централизованной публикации.</span><span class="sxs-lookup"><span data-stu-id="c408c-106">Represents the Centralized Publishing Server Information Service</span></span>

<span data-ttu-id="c408c-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c408c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c408c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c408c-108">Syntax</span></span>

``` syntax
class Win32_TSSystemInfo : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   RDUGroup;
  uint32   ProviderVersion;
};
```

## <a name="members"></a><span data-ttu-id="c408c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c408c-109">Members</span></span>

<span data-ttu-id="c408c-110">Класс **Win32 \_ тссистеминфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c408c-110">The **Win32\_TSSystemInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="c408c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c408c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c408c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c408c-112">Properties</span></span>

<span data-ttu-id="c408c-113">Класс **Win32 \_ тссистеминфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c408c-113">The **Win32\_TSSystemInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c408c-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c408c-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c408c-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c408c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c408c-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c408c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c408c-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c408c-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c408c-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="c408c-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c408c-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c408c-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c408c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c408c-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c408c-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c408c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c408c-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c408c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c408c-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c408c-123">Description of the object.</span></span>

<span data-ttu-id="c408c-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c408c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c408c-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c408c-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c408c-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c408c-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c408c-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c408c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c408c-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="c408c-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c408c-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c408c-129">The date the object was installed.</span></span> <span data-ttu-id="c408c-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c408c-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c408c-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c408c-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c408c-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="c408c-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c408c-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c408c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c408c-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c408c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c408c-135">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c408c-135">The name of the object.</span></span>

<span data-ttu-id="c408c-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c408c-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c408c-137">**провидерверсион**</span><span class="sxs-lookup"><span data-stu-id="c408c-137">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c408c-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c408c-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c408c-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c408c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c408c-140">Номер версии этого поставщика WMI.</span><span class="sxs-lookup"><span data-stu-id="c408c-140">The version number of this WMI Provider.</span></span>

</dd> <dt>

<span data-ttu-id="c408c-141">**рдуграуп**</span><span class="sxs-lookup"><span data-stu-id="c408c-141">**RDUGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c408c-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c408c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c408c-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c408c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c408c-144">Группа пользователей удаленный рабочий стол в формате языка определения дескрипторов безопасности (SDDL).</span><span class="sxs-lookup"><span data-stu-id="c408c-144">The Remote Desktop Users group, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="c408c-145">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c408c-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c408c-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c408c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c408c-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c408c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c408c-148">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c408c-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c408c-149">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c408c-149">Current status of the object.</span></span> <span data-ttu-id="c408c-150">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="c408c-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c408c-151">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="c408c-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c408c-152">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="c408c-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c408c-153">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="c408c-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c408c-154">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="c408c-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c408c-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c408c-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c408c-156">("ОК")</span><span class="sxs-lookup"><span data-stu-id="c408c-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c408c-157">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="c408c-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c408c-158">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="c408c-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c408c-159">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c408c-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c408c-160">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c408c-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c408c-161">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c408c-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c408c-162">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="c408c-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c408c-163">("Служба")</span><span class="sxs-lookup"><span data-stu-id="c408c-163">("Service")</span></span>


<span data-ttu-id="c408c-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c408c-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c408c-165">Требования</span><span class="sxs-lookup"><span data-stu-id="c408c-165">Requirements</span></span>



| <span data-ttu-id="c408c-166">Требование</span><span class="sxs-lookup"><span data-stu-id="c408c-166">Requirement</span></span> | <span data-ttu-id="c408c-167">Значение</span><span class="sxs-lookup"><span data-stu-id="c408c-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c408c-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c408c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c408c-169">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c408c-169">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c408c-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c408c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c408c-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c408c-171">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="c408c-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c408c-172">Namespace</span></span><br/>                | <span data-ttu-id="c408c-173">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c408c-173">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c408c-174">MOF</span><span class="sxs-lookup"><span data-stu-id="c408c-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c408c-175"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c408c-175"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="c408c-176">DLL</span><span class="sxs-lookup"><span data-stu-id="c408c-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c408c-177"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c408c-177"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

