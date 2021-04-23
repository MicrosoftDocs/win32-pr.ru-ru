---
title: Класс Win32_TSGetIcon
description: Возвращает содержимое значка, указанного в параметре путь к файлу и индекс.
ms.assetid: c0ab50f1-f5a9-4f5e-8280-40c638f09e1c
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGetIcon службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGetIcon, описание
topic_type:
- apiref
api_name:
- Win32_TSGetIcon
- Win32_TSGetIcon.Caption
- Win32_TSGetIcon.Description
- Win32_TSGetIcon.InstallDate
- Win32_TSGetIcon.Name
- Win32_TSGetIcon.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0186e158f025be8e8a5e6cf3e87f3ad5d8b296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988753"
---
# <a name="win32_tsgeticon-class"></a><span data-ttu-id="bd57c-105">\_Класс Win32 тсжетикон</span><span class="sxs-lookup"><span data-stu-id="bd57c-105">Win32\_TSGetIcon class</span></span>

<span data-ttu-id="bd57c-106">Возвращает содержимое значка, указанного по пути к файлу и индексу</span><span class="sxs-lookup"><span data-stu-id="bd57c-106">Returns the contents of the icon specified by file path and index</span></span>

<span data-ttu-id="bd57c-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bd57c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd57c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd57c-108">Syntax</span></span>

``` syntax
class Win32_TSGetIcon : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="bd57c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="bd57c-109">Members</span></span>

<span data-ttu-id="bd57c-110">Класс **Win32 \_ тсжетикон** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bd57c-110">The **Win32\_TSGetIcon** class has these types of members:</span></span>

-   [<span data-ttu-id="bd57c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="bd57c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="bd57c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd57c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bd57c-113">Методы</span><span class="sxs-lookup"><span data-stu-id="bd57c-113">Methods</span></span>

<span data-ttu-id="bd57c-114">Класс **Win32 \_ тсжетикон** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bd57c-114">The **Win32\_TSGetIcon** class has these methods.</span></span>



| <span data-ttu-id="bd57c-115">Метод</span><span class="sxs-lookup"><span data-stu-id="bd57c-115">Method</span></span>                                     | <span data-ttu-id="bd57c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bd57c-116">Description</span></span>                                            |
|:-------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="bd57c-117">**Значок**</span><span class="sxs-lookup"><span data-stu-id="bd57c-117">**GetIcon**</span></span>](geticon-win32-tsgeticon.md) | <span data-ttu-id="bd57c-118">Возвращает содержимое указанного значка.</span><span class="sxs-lookup"><span data-stu-id="bd57c-118">Returns the contents of the specified icon.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bd57c-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd57c-119">Properties</span></span>

<span data-ttu-id="bd57c-120">Класс **Win32 \_ тсжетикон** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bd57c-120">The **Win32\_TSGetIcon** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd57c-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="bd57c-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd57c-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd57c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd57c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-124">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bd57c-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bd57c-125">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="bd57c-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="bd57c-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd57c-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd57c-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd57c-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd57c-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd57c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd57c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd57c-130">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="bd57c-130">Description of the object.</span></span>

<span data-ttu-id="bd57c-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd57c-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd57c-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bd57c-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd57c-133">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bd57c-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd57c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-135">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="bd57c-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="bd57c-136">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="bd57c-136">The date the object was installed.</span></span> <span data-ttu-id="bd57c-137">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="bd57c-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bd57c-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd57c-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd57c-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="bd57c-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd57c-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd57c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd57c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd57c-142">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="bd57c-142">The name of the object.</span></span>

<span data-ttu-id="bd57c-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd57c-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd57c-144">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="bd57c-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd57c-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd57c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd57c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd57c-147">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="bd57c-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="bd57c-148">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="bd57c-148">Current status of the object.</span></span> <span data-ttu-id="bd57c-149">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="bd57c-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bd57c-150">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="bd57c-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bd57c-151">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="bd57c-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bd57c-152">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="bd57c-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bd57c-153">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="bd57c-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bd57c-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd57c-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="bd57c-155">("ОК")</span><span class="sxs-lookup"><span data-stu-id="bd57c-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bd57c-156">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="bd57c-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bd57c-157">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="bd57c-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bd57c-158">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="bd57c-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bd57c-159">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="bd57c-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bd57c-160">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="bd57c-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bd57c-161">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="bd57c-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bd57c-162">("Служба")</span><span class="sxs-lookup"><span data-stu-id="bd57c-162">("Service")</span></span>


<span data-ttu-id="bd57c-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bd57c-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bd57c-164">Требования</span><span class="sxs-lookup"><span data-stu-id="bd57c-164">Requirements</span></span>



| <span data-ttu-id="bd57c-165">Требование</span><span class="sxs-lookup"><span data-stu-id="bd57c-165">Requirement</span></span> | <span data-ttu-id="bd57c-166">Значение</span><span class="sxs-lookup"><span data-stu-id="bd57c-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd57c-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd57c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="bd57c-168">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bd57c-168">None supported</span></span><br/>                                                               |
| <span data-ttu-id="bd57c-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd57c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="bd57c-170">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bd57c-170">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="bd57c-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bd57c-171">Namespace</span></span><br/>                | <span data-ttu-id="bd57c-172">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="bd57c-172">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bd57c-173">MOF</span><span class="sxs-lookup"><span data-stu-id="bd57c-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd57c-174"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd57c-174"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="bd57c-175">DLL</span><span class="sxs-lookup"><span data-stu-id="bd57c-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd57c-176"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd57c-176"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

