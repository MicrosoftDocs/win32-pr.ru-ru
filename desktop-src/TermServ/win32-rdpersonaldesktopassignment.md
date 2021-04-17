---
title: Класс Win32_RDPersonalDesktopAssignment
description: Список назначений персональных рабочих столов.
ms.assetid: 3abf773d-8dc3-44ae-8887-1a1f38e29fbb
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDPersonalDesktopAssignment службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDPersonalDesktopAssignment, описание
topic_type:
- apiref
api_name:
- Win32_RDPersonalDesktopAssignment
- Win32_RDPersonalDesktopAssignment.Caption
- Win32_RDPersonalDesktopAssignment.Description
- Win32_RDPersonalDesktopAssignment.InstallDate
- Win32_RDPersonalDesktopAssignment.Name
- Win32_RDPersonalDesktopAssignment.Status
- Win32_RDPersonalDesktopAssignment.UserName
- Win32_RDPersonalDesktopAssignment.DomainName
- Win32_RDPersonalDesktopAssignment.FarmAlias
- Win32_RDPersonalDesktopAssignment.VMName
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088e7be5da0a62a0f5b7ed72f8a439661cc41c80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681802"
---
# <a name="win32_rdpersonaldesktopassignment-class"></a><span data-ttu-id="b207a-105">\_Класс Win32 рдперсоналдесктопассигнмент</span><span class="sxs-lookup"><span data-stu-id="b207a-105">Win32\_RDPersonalDesktopAssignment class</span></span>

<span data-ttu-id="b207a-106">Список назначений персональных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b207a-106">The list of personal desktop assignments.</span></span>

<span data-ttu-id="b207a-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b207a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b207a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b207a-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDPersonalDesktopAssignment : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   UserName;
  string   DomainName;
  string   FarmAlias;
  string   VMName;
};
```

## <a name="members"></a><span data-ttu-id="b207a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b207a-109">Members</span></span>

<span data-ttu-id="b207a-110">Класс **Win32 \_ рдперсоналдесктопассигнмент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b207a-110">The **Win32\_RDPersonalDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="b207a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b207a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b207a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b207a-112">Properties</span></span>

<span data-ttu-id="b207a-113">Класс **Win32 \_ рдперсоналдесктопассигнмент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b207a-113">The **Win32\_RDPersonalDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b207a-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b207a-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b207a-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b207a-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b207a-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b207a-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="b207a-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b207a-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b207a-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b207a-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b207a-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b207a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b207a-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b207a-123">Description of the object.</span></span>

<span data-ttu-id="b207a-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b207a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b207a-125">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="b207a-125">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b207a-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b207a-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b207a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b207a-129">Доменное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="b207a-129">Domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="b207a-130">**фармалиас**</span><span class="sxs-lookup"><span data-stu-id="b207a-130">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b207a-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b207a-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b207a-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b207a-134">Ферма, в которой назначен личный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="b207a-134">Farm in which personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="b207a-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b207a-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-136">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b207a-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b207a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b207a-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="b207a-138">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b207a-139">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b207a-139">The date the object was installed.</span></span> <span data-ttu-id="b207a-140">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="b207a-140">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b207a-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b207a-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b207a-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="b207a-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b207a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b207a-145">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="b207a-145">The name of the object.</span></span>

<span data-ttu-id="b207a-146">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b207a-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b207a-147">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b207a-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b207a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b207a-150">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b207a-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b207a-151">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b207a-151">Current status of the object.</span></span> <span data-ttu-id="b207a-152">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="b207a-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b207a-153">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="b207a-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b207a-154">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="b207a-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b207a-155">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="b207a-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b207a-156">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b207a-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b207a-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b207a-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b207a-158">("ОК")</span><span class="sxs-lookup"><span data-stu-id="b207a-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b207a-159">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="b207a-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b207a-160">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="b207a-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b207a-161">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b207a-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b207a-162">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b207a-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b207a-163">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b207a-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b207a-164">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="b207a-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b207a-165">("Служба")</span><span class="sxs-lookup"><span data-stu-id="b207a-165">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b207a-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="b207a-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b207a-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b207a-169">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b207a-169">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b207a-170">Имя пользователя, которому назначен личный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="b207a-170">User name to whom personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="b207a-171">**VMName**</span><span class="sxs-lookup"><span data-stu-id="b207a-171">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b207a-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b207a-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b207a-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b207a-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b207a-174">Имя назначенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b207a-174">Assigned VM name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b207a-175">Требования</span><span class="sxs-lookup"><span data-stu-id="b207a-175">Requirements</span></span>



| <span data-ttu-id="b207a-176">Требование</span><span class="sxs-lookup"><span data-stu-id="b207a-176">Requirement</span></span> | <span data-ttu-id="b207a-177">Значение</span><span class="sxs-lookup"><span data-stu-id="b207a-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b207a-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b207a-178">Minimum supported client</span></span><br/> | <span data-ttu-id="b207a-179">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b207a-179">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b207a-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b207a-180">Minimum supported server</span></span><br/> | <span data-ttu-id="b207a-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b207a-181">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="b207a-182">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b207a-182">Namespace</span></span><br/>                | <span data-ttu-id="b207a-183">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b207a-183">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b207a-184">MOF</span><span class="sxs-lookup"><span data-stu-id="b207a-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b207a-185"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b207a-185"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="b207a-186">DLL</span><span class="sxs-lookup"><span data-stu-id="b207a-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b207a-187"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b207a-187"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

