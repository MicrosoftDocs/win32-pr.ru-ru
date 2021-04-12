---
title: Класс Win32_RDCentralPublishedFarm
description: Список ферм, из которых были опубликованы настольные компьютеры или приложения.
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDCentralPublishedFarm службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDCentralPublishedFarm, описание
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490104"
---
# <a name="win32_rdcentralpublishedfarm-class"></a><span data-ttu-id="93c9f-105">\_Класс Win32 рдцентралпублишедфарм</span><span class="sxs-lookup"><span data-stu-id="93c9f-105">Win32\_RDCentralPublishedFarm class</span></span>

<span data-ttu-id="93c9f-106">Список ферм, из которых были опубликованы настольные компьютеры или приложения.</span><span class="sxs-lookup"><span data-stu-id="93c9f-106">The list of farms from which desktops or applications have been published.</span></span>

<span data-ttu-id="93c9f-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="93c9f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c9f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93c9f-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="93c9f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="93c9f-109">Members</span></span>

<span data-ttu-id="93c9f-110">Класс **Win32 \_ рдцентралпублишедфарм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93c9f-110">The **Win32\_RDCentralPublishedFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="93c9f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="93c9f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93c9f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="93c9f-112">Properties</span></span>

<span data-ttu-id="93c9f-113">Класс **Win32 \_ рдцентралпублишедфарм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93c9f-113">The **Win32\_RDCentralPublishedFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93c9f-114">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="93c9f-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93c9f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="93c9f-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="93c9f-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-118">Имя фермы, из которой были опубликованы настольные компьютеры или приложения.</span><span class="sxs-lookup"><span data-stu-id="93c9f-118">The name of the farm from which desktops or applications have been published.</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="93c9f-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93c9f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93c9f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="93c9f-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-123">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="93c9f-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="93c9f-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93c9f-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93c9f-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93c9f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93c9f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-128">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="93c9f-128">Description of the object.</span></span>

<span data-ttu-id="93c9f-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93c9f-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-130">**фармтипе**</span><span class="sxs-lookup"><span data-stu-id="93c9f-130">**FarmType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93c9f-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="93c9f-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-133">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93c9f-133">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-134">Тип фермы:</span><span class="sxs-lookup"><span data-stu-id="93c9f-134">The kind of farm:</span></span>

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

<span data-ttu-id="93c9f-135">**Узлов сеансов удаленных рабочих столов** (0)</span><span class="sxs-lookup"><span data-stu-id="93c9f-135">**RDSH** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="93c9f-136">**Темпвм** (1)</span><span class="sxs-lookup"><span data-stu-id="93c9f-136">**TempVM** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="93c9f-137">**Мануалперсоналвм** (2)</span><span class="sxs-lookup"><span data-stu-id="93c9f-137">**ManualPersonalVM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="93c9f-138">**Аутоперсоналвм** (3)</span><span class="sxs-lookup"><span data-stu-id="93c9f-138">**AutoPersonalVM** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93c9f-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93c9f-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93c9f-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93c9f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-142">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="93c9f-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-143">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="93c9f-143">The date the object was installed.</span></span> <span data-ttu-id="93c9f-144">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="93c9f-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="93c9f-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93c9f-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-146">**исусерадмин**</span><span class="sxs-lookup"><span data-stu-id="93c9f-146">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-147">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="93c9f-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="93c9f-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-149">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93c9f-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-150">**значение true** , если пользователь должен быть добавлен в локальную группу администраторов при подключении. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="93c9f-150">**true** if a user needs to be added to local administrator group upon connection; otherwise, **false**.</span></span> <span data-ttu-id="93c9f-151">Применяется только к типам ферм Мануалперсоналвм и Аутоперсоналвм.</span><span class="sxs-lookup"><span data-stu-id="93c9f-151">Applicable only to ManualPersonalVm and AutoPersonalVM farm types.</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="93c9f-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93c9f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93c9f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-155">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="93c9f-155">The name of the object.</span></span>

<span data-ttu-id="93c9f-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93c9f-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-157">**роллбаккенаблед**</span><span class="sxs-lookup"><span data-stu-id="93c9f-157">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-158">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="93c9f-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="93c9f-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-160">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93c9f-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-161">**true** для автоматического отката виртуальной машины до моментального снимка после выхода пользователя из системы; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="93c9f-161">**true** to auto rollback VM to a snapshot after user logoff; otherwise, **false**.</span></span> <span data-ttu-id="93c9f-162">Применимо только к типам ферм Темпвм.</span><span class="sxs-lookup"><span data-stu-id="93c9f-162">Applicable only to TempVm farm types.</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="93c9f-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93c9f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="93c9f-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-166">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93c9f-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-167">Имя дескриптора безопасности, управляющего доступом к приложению, в формате SDDL.</span><span class="sxs-lookup"><span data-stu-id="93c9f-167">The name of the security descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="93c9f-168">Использование пустой строки подразумевает разрешение любой доступ.</span><span class="sxs-lookup"><span data-stu-id="93c9f-168">Using an empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="93c9f-169">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="93c9f-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93c9f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93c9f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-172">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="93c9f-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-173">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="93c9f-173">Current status of the object.</span></span> <span data-ttu-id="93c9f-174">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="93c9f-174">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="93c9f-175">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="93c9f-175">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="93c9f-176">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="93c9f-176">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="93c9f-177">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="93c9f-177">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="93c9f-178">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="93c9f-178">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="93c9f-179">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93c9f-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="93c9f-180">("ОК")</span><span class="sxs-lookup"><span data-stu-id="93c9f-180">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="93c9f-181">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="93c9f-181">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="93c9f-182">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="93c9f-182">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="93c9f-183">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="93c9f-183">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="93c9f-184">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="93c9f-184">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="93c9f-185">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="93c9f-185">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="93c9f-186">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="93c9f-186">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="93c9f-187">("Служба")</span><span class="sxs-lookup"><span data-stu-id="93c9f-187">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93c9f-188">**вмфармсеттингс**</span><span class="sxs-lookup"><span data-stu-id="93c9f-188">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c9f-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93c9f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="93c9f-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93c9f-191">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93c9f-191">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93c9f-192">Параметры фермы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="93c9f-192">The virtual machine farm settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93c9f-193">Требования</span><span class="sxs-lookup"><span data-stu-id="93c9f-193">Requirements</span></span>



| <span data-ttu-id="93c9f-194">Требование</span><span class="sxs-lookup"><span data-stu-id="93c9f-194">Requirement</span></span> | <span data-ttu-id="93c9f-195">Значение</span><span class="sxs-lookup"><span data-stu-id="93c9f-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c9f-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93c9f-196">Minimum supported client</span></span><br/> | <span data-ttu-id="93c9f-197">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="93c9f-197">None supported</span></span><br/>                                                                |
| <span data-ttu-id="93c9f-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93c9f-198">Minimum supported server</span></span><br/> | <span data-ttu-id="93c9f-199">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93c9f-199">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="93c9f-200">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93c9f-200">Namespace</span></span><br/>                | <span data-ttu-id="93c9f-201">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="93c9f-201">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="93c9f-202">MOF</span><span class="sxs-lookup"><span data-stu-id="93c9f-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93c9f-203"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93c9f-203"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="93c9f-204">DLL</span><span class="sxs-lookup"><span data-stu-id="93c9f-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c9f-205"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c9f-205"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

