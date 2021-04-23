---
description: Конкретная версия \_ класса заданий CIM. Этот класс представляет собой универсальную выполняемую единицу работы, выполняющую создание экземпляров, например пакет или задание печати.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: Класс CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682952"
---
# <a name="cim_concretejob-class"></a><span data-ttu-id="24026-104">\_Класс CIM конкретежоб</span><span class="sxs-lookup"><span data-stu-id="24026-104">CIM\_ConcreteJob class</span></span>

<span data-ttu-id="24026-105">Конкретная версия класса [**\_ заданий CIM**](cim-job.md) .</span><span class="sxs-lookup"><span data-stu-id="24026-105">A concrete version of the [**CIM\_Job**](cim-job.md) class.</span></span> <span data-ttu-id="24026-106">Этот класс представляет собой универсальную выполняемую единицу работы, выполняющую создание экземпляров, например пакет или задание печати.</span><span class="sxs-lookup"><span data-stu-id="24026-106">This class represent a generic instantiable unit of work to run, such as a batch or a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="24026-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24026-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a><span data-ttu-id="24026-108">Члены</span><span class="sxs-lookup"><span data-stu-id="24026-108">Members</span></span>

<span data-ttu-id="24026-109">Класс **CIM \_ конкретежоб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="24026-109">The **CIM\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="24026-110">Методы</span><span class="sxs-lookup"><span data-stu-id="24026-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="24026-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="24026-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="24026-112">Методы</span><span class="sxs-lookup"><span data-stu-id="24026-112">Methods</span></span>

<span data-ttu-id="24026-113">Класс **CIM \_ конкретежоб** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="24026-113">The **CIM\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="24026-114">Метод</span><span class="sxs-lookup"><span data-stu-id="24026-114">Method</span></span>                                                           | <span data-ttu-id="24026-115">Описание</span><span class="sxs-lookup"><span data-stu-id="24026-115">Description</span></span>                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="24026-116">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="24026-116">**GetError**</span></span>](cim-concretejob-geterror.md)                     | <span data-ttu-id="24026-117">Извлекает сведения об ошибке для рабочего состояния конкретного задания.</span><span class="sxs-lookup"><span data-stu-id="24026-117">Retrieves error information for the operational status of a concrete job.</span></span><br/> |
| [<span data-ttu-id="24026-118">**Равен**</span><span class="sxs-lookup"><span data-stu-id="24026-118">**RequestStateChange**</span></span>](cim-concretejob-requeststatechange.md) | <span data-ttu-id="24026-119">Запрашивает указанное изменение состояния для конкретного задания.</span><span class="sxs-lookup"><span data-stu-id="24026-119">Requests the specified state change to a concrete job.</span></span><br/>                    |



 

### <a name="properties"></a><span data-ttu-id="24026-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="24026-120">Properties</span></span>

<span data-ttu-id="24026-121">Класс **CIM \_ конкретежоб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="24026-121">The **CIM\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24026-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="24026-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24026-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24026-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24026-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24026-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24026-125">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="24026-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="24026-126">Уникально и непрозрачно определяет экземпляр этого класса в области содержащего его пространства имен.</span><span class="sxs-lookup"><span data-stu-id="24026-126">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="24026-127">Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="24026-127">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="24026-128">*OrgID* должен включать в себя запись с правом или иным именем, которая принадлежит бизнес-сущности, определяющей **InstanceId**, или быть зарегистрированным идентификатором, который назначается распознанным глобальным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="24026-128">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="24026-129">Этот шаблон похож на структуру имен классов схемы.</span><span class="sxs-lookup"><span data-stu-id="24026-129">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="24026-130">Кроме того, чтобы обеспечить уникальность, первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="24026-130">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="24026-131">Поэтому *OrgID* не должен содержать двоеточие (":").</span><span class="sxs-lookup"><span data-stu-id="24026-131">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="24026-132">*LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.</span><span class="sxs-lookup"><span data-stu-id="24026-132">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="24026-133">Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="24026-133">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="24026-134">Для экземпляров распределенного управления Task Force (DMTF) необходимо использовать шаблон с *OrgID* , для которого задано значение CIM.</span><span class="sxs-lookup"><span data-stu-id="24026-134">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="24026-135">**JobState**</span><span class="sxs-lookup"><span data-stu-id="24026-135">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24026-136">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24026-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24026-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24026-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24026-138">Рабочее состояние задания и переход между этими состояниями.</span><span class="sxs-lookup"><span data-stu-id="24026-138">The operational state of the job, and the transition between those states.</span></span>

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span data-ttu-id="24026-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**Создать** (2)</span><span class="sxs-lookup"><span data-stu-id="24026-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**New** (2)</span></span>


</dt> <dd>

<span data-ttu-id="24026-140">Задание никогда не запускалось.</span><span class="sxs-lookup"><span data-stu-id="24026-140">the job has never been started.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="24026-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="24026-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="24026-142">Задание переходит с состояния "новое", "приостановлено" или "служба" в состояние "работает".</span><span class="sxs-lookup"><span data-stu-id="24026-142">The job is moving from the 'New', 'Suspended', or 'Service' states into the 'Running' state.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="24026-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (4)</span><span class="sxs-lookup"><span data-stu-id="24026-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (4)</span></span>


</dt> <dd>

<span data-ttu-id="24026-144">Задание работает.</span><span class="sxs-lookup"><span data-stu-id="24026-144">The Job is running.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="24026-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="24026-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (5)</span></span>


</dt> <dd>

<span data-ttu-id="24026-146">Задание остановлено, но может быть перезапущено без проблем.</span><span class="sxs-lookup"><span data-stu-id="24026-146">The Job is stopped, but can be restarted in a seamless manner.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="24026-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (6)</span><span class="sxs-lookup"><span data-stu-id="24026-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (6)</span></span>


</dt> <dd>

<span data-ttu-id="24026-148">Задание переходит в состояние "завершено", "завершено" или "уничтожено".</span><span class="sxs-lookup"><span data-stu-id="24026-148">The job is moving to a 'Completed', 'Terminated', or 'Killed' state.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="24026-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (7)</span><span class="sxs-lookup"><span data-stu-id="24026-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (7)</span></span>


</dt> <dd>

<span data-ttu-id="24026-150">Задание выполнено нормально.</span><span class="sxs-lookup"><span data-stu-id="24026-150">The job has completed normally.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="24026-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="24026-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (8)</span></span>


</dt> <dd>

<span data-ttu-id="24026-152">Задание остановлено запросом на изменение состояния завершения.</span><span class="sxs-lookup"><span data-stu-id="24026-152">The job has been stopped by a 'Terminate' state change request.</span></span> <span data-ttu-id="24026-153">Задание и все его базовые процессы завершены и могут быть перезапущены (это зависит от задания) только в качестве нового задания.</span><span class="sxs-lookup"><span data-stu-id="24026-153">The job and all its underlying processes are ended and can be restarted (this is job-specific) only as a new job.</span></span>

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span data-ttu-id="24026-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Уничтожено** (9)</span><span class="sxs-lookup"><span data-stu-id="24026-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)</span></span>


</dt> <dd>

<span data-ttu-id="24026-155">Задание остановлено запросом на изменение состояния "Kill".</span><span class="sxs-lookup"><span data-stu-id="24026-155">The job has been stopped by a 'Kill' state change request.</span></span> <span data-ttu-id="24026-156">Базовые процессы могли быть запущены, а для освобождения ресурсов может потребоваться очистка.</span><span class="sxs-lookup"><span data-stu-id="24026-156">Underlying processes might have been left running, and cleanup might be required to free up resources.</span></span>

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span data-ttu-id="24026-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Исключение** (10)</span><span class="sxs-lookup"><span data-stu-id="24026-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span></span>


</dt> <dd>

<span data-ttu-id="24026-158">Задание находится в ненормальном состоянии, что может указывать на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="24026-158">The Job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="24026-159">Фактическое состояние может отображаться при наличии объектов, относящихся к определенному заданию.</span><span class="sxs-lookup"><span data-stu-id="24026-159">Actual status might be displayed though job-specific objects.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="24026-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (11)</span><span class="sxs-lookup"><span data-stu-id="24026-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="24026-161">Задание находится в состоянии, зависящем от поставщика, которое поддерживает обнаружение проблем, разрешение или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="24026-161">The Job is in a vendor-specific state that supports problem discovery, or resolution, or both</span></span>

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span data-ttu-id="24026-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Ожидание запроса** (12)</span><span class="sxs-lookup"><span data-stu-id="24026-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query Pending** (12)</span></span>


</dt> <dd>

<span data-ttu-id="24026-163">Ожидание разрешения запроса клиентом.</span><span class="sxs-lookup"><span data-stu-id="24026-163">Waiting for a client to resolve a query.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="24026-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (13.. 32767)</span><span class="sxs-lookup"><span data-stu-id="24026-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (13..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="24026-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="24026-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24026-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="24026-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24026-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24026-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24026-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24026-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24026-169">Квалификаторы: [**обязательный**](/windows/desktop/WmiSdk/standard-qualifiers), [**переопределенный**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="24026-169">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="24026-170">Понятное имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="24026-170">The user-friendly name of the instance.</span></span> <span data-ttu-id="24026-171">Кроме того, понятное имя можно использовать в качестве свойства для поиска или запроса.</span><span class="sxs-lookup"><span data-stu-id="24026-171">In addition, the user-friendly name can be used as a property for a search or query.</span></span>

> [!Note]  
> <span data-ttu-id="24026-172">Имя не обязательно должно быть уникальным в пределах пространства имен.</span><span class="sxs-lookup"><span data-stu-id="24026-172">The name does not have to be unique within the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="24026-173">**тимебефореремовал**</span><span class="sxs-lookup"><span data-stu-id="24026-173">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24026-174">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="24026-174">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24026-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="24026-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="24026-176">Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24026-176">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24026-177">Указывает время хранения завершенного задания.</span><span class="sxs-lookup"><span data-stu-id="24026-177">Indicates how long a completed job is retained.</span></span> <span data-ttu-id="24026-178">Значение по умолчанию — "00000000000500.000000:000" (5 минут).</span><span class="sxs-lookup"><span data-stu-id="24026-178">The default value is "00000000000500.000000:000" (five minutes).</span></span>

</dd> <dt>

<span data-ttu-id="24026-179">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="24026-179">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24026-180">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="24026-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24026-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24026-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24026-182">Дата или время последнего изменения состояния задания.</span><span class="sxs-lookup"><span data-stu-id="24026-182">The date or time when the state of the job last changed.</span></span>

> [!Note]  
> <span data-ttu-id="24026-183">Если состояние задания не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="24026-183">If the state of the Job has not changed and this property is populated, then it must be set to a zero interval value.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24026-184">Требования</span><span class="sxs-lookup"><span data-stu-id="24026-184">Requirements</span></span>



| <span data-ttu-id="24026-185">Требование</span><span class="sxs-lookup"><span data-stu-id="24026-185">Requirement</span></span> | <span data-ttu-id="24026-186">Значение</span><span class="sxs-lookup"><span data-stu-id="24026-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24026-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24026-187">Minimum supported client</span></span><br/> | <span data-ttu-id="24026-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="24026-188">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="24026-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24026-189">Minimum supported server</span></span><br/> | <span data-ttu-id="24026-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24026-190">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="24026-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="24026-191">Namespace</span></span><br/>                | <span data-ttu-id="24026-192">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="24026-192">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24026-193">MOF</span><span class="sxs-lookup"><span data-stu-id="24026-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24026-194"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24026-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24026-195">DLL</span><span class="sxs-lookup"><span data-stu-id="24026-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24026-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24026-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24026-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24026-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24026-198">**\_Задание CIM**</span><span class="sxs-lookup"><span data-stu-id="24026-198">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

