---
description: Запускает задание для создания корневого ResourcePool. Область ResourcePool будет соответствовать той же системе, что и эта служба.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Метод CreateResourcePool класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810336"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="10270-104">Метод CreateResourcePool \_ класса CIM ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="10270-104">CreateResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="10270-105">Запускает задание для создания корневого ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="10270-105">Starts a job to create a root ResourcePool.</span></span> <span data-ttu-id="10270-106">Область ResourcePool будет соответствовать той же системе, что и эта служба.</span><span class="sxs-lookup"><span data-stu-id="10270-106">The ResourcePool will be scoped to the same System as this Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="10270-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10270-107">Syntax</span></span>


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="10270-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10270-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10270-109">*ElementName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10270-109">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10270-110">Имя, соответствующее конечному пользователю для создаваемого пула.</span><span class="sxs-lookup"><span data-stu-id="10270-110">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="10270-111">Если **значение равно NULL**, можно использовать имя по умолчанию, предоставляемое системой.</span><span class="sxs-lookup"><span data-stu-id="10270-111">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="10270-112">Значение будет храниться в свойстве **ElementName** для созданного пула.</span><span class="sxs-lookup"><span data-stu-id="10270-112">The value will be stored in the **ElementName** property for the created pool.</span></span>

</dd> <dt>

<span data-ttu-id="10270-113">*Хостресаурцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10270-113">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10270-114">Массив из нуля или более [**устройств \_ типа CIM**](cim-logicaldevice.md) , которые используются для создания пула или изменения исходных экстентов.</span><span class="sxs-lookup"><span data-stu-id="10270-114">Array of zero or more [**CIM\_LogicalDevice**](cim-logicaldevice.md) devices that are used to create the Pool or modify the source extents.</span></span> <span data-ttu-id="10270-115">Все элементы в массиве должны быть одного типа.</span><span class="sxs-lookup"><span data-stu-id="10270-115">All elements in the array must be of the same type.</span></span>

</dd> <dt>

<span data-ttu-id="10270-116">*ResourceType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10270-116">*ResourceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10270-117">Тип ресурсов, которыми будет управлять созданный пул.</span><span class="sxs-lookup"><span data-stu-id="10270-117">The type of resources the created pool will manage.</span></span> <span data-ttu-id="10270-118">Если *хостресаурцес* содержит элементы, это свойство должно иметь свой тип.</span><span class="sxs-lookup"><span data-stu-id="10270-118">If *HostResources* contains elements, this property must mach their type.</span></span>

</dd> <dt>

<span data-ttu-id="10270-119">*Пул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="10270-119">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10270-120">При успешном выполнении возвращает ссылку на полученный [**\_ ResourcePool CIM**](cim-resourcepool.md).</span><span class="sxs-lookup"><span data-stu-id="10270-120">On success, returns a reference to the resulting [**CIM\_ResourcePool**](cim-resourcepool.md).</span></span> <span data-ttu-id="10270-121">При возвращении задания это может быть **значение NULL**. в этом случае клиент должен использовать задание, чтобы найти результирующий ResourcePool после завершения задания.</span><span class="sxs-lookup"><span data-stu-id="10270-121">When a Job is returned, this may be **NULL**, in which case, the client must use the Job to find the resulting ResourcePool once the Job completes.</span></span>

</dd> <dt>

<span data-ttu-id="10270-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="10270-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10270-123">Ссылка на [**CIM \_ конкретежоб**](cim-concretejob.md) , представляющий задание (может иметь значение null, если задание завершено).</span><span class="sxs-lookup"><span data-stu-id="10270-123">Reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) that represents the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10270-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10270-124">Return value</span></span>

<span data-ttu-id="10270-125">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="10270-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="10270-126">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="10270-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="10270-127">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="10270-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="10270-128">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10270-128">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="10270-129">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="10270-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="10270-130">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="10270-130">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="10270-131">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="10270-131">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="10270-132">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="10270-132">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="10270-133">**Неверный ResourceType для пула** (7)</span><span class="sxs-lookup"><span data-stu-id="10270-133">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="10270-134">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="10270-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="10270-135">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="10270-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="10270-136">**Размер не поддерживается** (4097)</span><span class="sxs-lookup"><span data-stu-id="10270-136">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="10270-137">**Метод зарезервирован** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="10270-137">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="10270-138">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="10270-138">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="10270-139">Требования</span><span class="sxs-lookup"><span data-stu-id="10270-139">Requirements</span></span>



| <span data-ttu-id="10270-140">Требование</span><span class="sxs-lookup"><span data-stu-id="10270-140">Requirement</span></span> | <span data-ttu-id="10270-141">Значение</span><span class="sxs-lookup"><span data-stu-id="10270-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10270-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10270-142">Minimum supported client</span></span><br/> | <span data-ttu-id="10270-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="10270-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="10270-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10270-144">Minimum supported server</span></span><br/> | <span data-ttu-id="10270-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="10270-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="10270-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="10270-146">Namespace</span></span><br/>                | <span data-ttu-id="10270-147">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="10270-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="10270-148">MOF</span><span class="sxs-lookup"><span data-stu-id="10270-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10270-149"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10270-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10270-150">DLL</span><span class="sxs-lookup"><span data-stu-id="10270-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10270-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10270-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10270-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10270-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10270-153">**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="10270-153">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




