---
description: Запускает задание по удалению ресурсов из пула ресурсов.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: Метод Ремовересаурцесфромресаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41c8a7d1608b9c4d5ea629aa9c053e022d59d9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542402"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="13572-103">Метод Ремовересаурцесфромресаурцепул \_ класса CIM ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="13572-103">RemoveResourcesFromResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="13572-104">Запускает задание по удалению ресурсов из пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13572-104">Starts a job to remove resources from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="13572-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13572-105">Syntax</span></span>


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="13572-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13572-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13572-107">*Хостресаурцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13572-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13572-108">Массив экземпляров [**CIM \_**](cim-logicaldevice.md) , которые необходимо удалить из пула.</span><span class="sxs-lookup"><span data-stu-id="13572-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to remove from the pool.</span></span>

</dd> <dt>

<span data-ttu-id="13572-109">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13572-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13572-110">[**\_ ResourcePool CIM**](cim-resourcepool.md) , представляющий пул, из которого удаляются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="13572-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) representing the pool to remove the resources from.</span></span>

</dd> <dt>

<span data-ttu-id="13572-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="13572-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13572-112">[**\_ Конкретежоб CIM**](cim-concretejob.md) , который ссылается на задание (может иметь **значение NULL** , если задание завершено).</span><span class="sxs-lookup"><span data-stu-id="13572-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13572-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13572-113">Return value</span></span>

<span data-ttu-id="13572-114">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="13572-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="13572-115">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="13572-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13572-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="13572-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="13572-117">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="13572-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="13572-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="13572-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="13572-119">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="13572-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="13572-120">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="13572-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="13572-121">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="13572-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="13572-122">**Неверный ResourceType для пула** (7)</span><span class="sxs-lookup"><span data-stu-id="13572-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="13572-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="13572-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="13572-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="13572-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="13572-125">**Размер не поддерживается** (4097)</span><span class="sxs-lookup"><span data-stu-id="13572-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="13572-126">**Метод зарезервирован** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="13572-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="13572-127">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="13572-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="13572-128">Требования</span><span class="sxs-lookup"><span data-stu-id="13572-128">Requirements</span></span>



| <span data-ttu-id="13572-129">Требование</span><span class="sxs-lookup"><span data-stu-id="13572-129">Requirement</span></span> | <span data-ttu-id="13572-130">Значение</span><span class="sxs-lookup"><span data-stu-id="13572-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13572-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13572-131">Minimum supported client</span></span><br/> | <span data-ttu-id="13572-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13572-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="13572-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13572-133">Minimum supported server</span></span><br/> | <span data-ttu-id="13572-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13572-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="13572-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="13572-135">Namespace</span></span><br/>                | <span data-ttu-id="13572-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="13572-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13572-137">MOF</span><span class="sxs-lookup"><span data-stu-id="13572-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13572-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13572-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13572-139">DLL</span><span class="sxs-lookup"><span data-stu-id="13572-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13572-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13572-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13572-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13572-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13572-142">**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="13572-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




