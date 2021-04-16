---
title: Класс Win32_Workspace
description: Указывает службы удаленных рабочих столов сведения о конфигурации рабочей области.
ms.assetid: 27192dca-cbb4-4620-ae52-c27aba4b4dff
ms.tgt_platform: multiple
keywords:
- Класс Win32_Workspace службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_Workspace, описание
topic_type:
- apiref
api_name:
- Win32_Workspace
- Win32_Workspace.Caption
- Win32_Workspace.Description
- Win32_Workspace.InstallDate
- Win32_Workspace.Name
- Win32_Workspace.Status
- Win32_Workspace.IsDefaultName
- Win32_Workspace.ID
- Win32_Workspace.Redirector
- Win32_Workspace.RedirectorAlternateAddress
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1153a4eb8a260e539845a9458a5c8cee4581d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672479"
---
# <a name="win32_workspace-class"></a><span data-ttu-id="a1855-105">\_Класс рабочей области Win32</span><span class="sxs-lookup"><span data-stu-id="a1855-105">Win32\_Workspace class</span></span>

<span data-ttu-id="a1855-106">Указывает службы удаленных рабочих столов сведения о конфигурации рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a1855-106">Specifies Remote Desktop Services workspace configuration information.</span></span>

<span data-ttu-id="a1855-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a1855-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1855-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1855-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov"), singleton]
class Win32_Workspace : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  IsDefaultName;
  string   ID;
  string   Redirector;
  string   RedirectorAlternateAddress;
};
```

## <a name="members"></a><span data-ttu-id="a1855-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a1855-109">Members</span></span>

<span data-ttu-id="a1855-110">Класс **\_ рабочей области Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a1855-110">The **Win32\_Workspace** class has these types of members:</span></span>

-   [<span data-ttu-id="a1855-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a1855-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1855-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a1855-112">Properties</span></span>

<span data-ttu-id="a1855-113">Класс **\_ рабочей области Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a1855-113">The **Win32\_Workspace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1855-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a1855-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a1855-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1855-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1855-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a1855-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a1855-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="a1855-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="a1855-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1855-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1855-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a1855-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a1855-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1855-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1855-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a1855-123">Description of the object.</span></span>

<span data-ttu-id="a1855-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1855-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1855-125">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="a1855-125">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a1855-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1855-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1855-128">Идентификатор рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a1855-128">The identifier of the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="a1855-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a1855-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-130">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1855-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1855-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1855-132">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="a1855-132">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a1855-133">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="a1855-133">The date the object was installed.</span></span> <span data-ttu-id="a1855-134">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="a1855-134">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a1855-135">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1855-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1855-136">**исдефаултнаме**</span><span class="sxs-lookup"><span data-stu-id="a1855-136">**IsDefaultName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a1855-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1855-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1855-139">Указывает, является ли имя рабочей области именем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1855-139">Specifies if the workspace name is the default name.</span></span> <span data-ttu-id="a1855-140">Содержит ненулевое значение, если имя является именем по умолчанию или нулем в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a1855-140">Contains nonzero if the name is a default name or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a1855-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="a1855-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a1855-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1855-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1855-144">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a1855-144">The name of the object.</span></span>

<span data-ttu-id="a1855-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1855-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1855-146">**Перенаправителя**</span><span class="sxs-lookup"><span data-stu-id="a1855-146">**Redirector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a1855-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1855-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a1855-149">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a1855-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a1855-150">Имя компьютера перенаправителя для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a1855-150">The machine name of the redirector for the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="a1855-151">**редиректоралтернатеаддресс**</span><span class="sxs-lookup"><span data-stu-id="a1855-151">**RedirectorAlternateAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a1855-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a1855-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a1855-154">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a1855-154">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a1855-155">Альтернативный адрес для перенаправителя.</span><span class="sxs-lookup"><span data-stu-id="a1855-155">The alternate address for the redirector.</span></span>

</dd> <dt>

<span data-ttu-id="a1855-156">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a1855-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1855-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a1855-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1855-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1855-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1855-159">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="a1855-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a1855-160">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a1855-160">Current status of the object.</span></span> <span data-ttu-id="a1855-161">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="a1855-161">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a1855-162">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="a1855-162">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a1855-163">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="a1855-163">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a1855-164">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="a1855-164">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a1855-165">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="a1855-165">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a1855-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a1855-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="a1855-167">("ОК")</span><span class="sxs-lookup"><span data-stu-id="a1855-167">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a1855-168">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="a1855-168">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a1855-169">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="a1855-169">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a1855-170">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a1855-170">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a1855-171">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a1855-171">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a1855-172">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a1855-172">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a1855-173">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="a1855-173">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a1855-174">("Служба")</span><span class="sxs-lookup"><span data-stu-id="a1855-174">("Service")</span></span>


<span data-ttu-id="a1855-175"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a1855-175"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a1855-176">Требования</span><span class="sxs-lookup"><span data-stu-id="a1855-176">Requirements</span></span>



| <span data-ttu-id="a1855-177">Требование</span><span class="sxs-lookup"><span data-stu-id="a1855-177">Requirement</span></span> | <span data-ttu-id="a1855-178">Значение</span><span class="sxs-lookup"><span data-stu-id="a1855-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1855-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1855-179">Minimum supported client</span></span><br/> | <span data-ttu-id="a1855-180">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a1855-180">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a1855-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1855-181">Minimum supported server</span></span><br/> | <span data-ttu-id="a1855-182">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1855-182">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="a1855-183">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a1855-183">Namespace</span></span><br/>                | <span data-ttu-id="a1855-184">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a1855-184">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a1855-185">MOF</span><span class="sxs-lookup"><span data-stu-id="a1855-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1855-186"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1855-186"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a1855-187">DLL</span><span class="sxs-lookup"><span data-stu-id="a1855-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1855-188"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1855-188"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

