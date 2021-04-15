---
description: Запуск задания для удаления пула ресурсов.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Метод Делетересаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662475"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="c3ee3-103">Метод Делетересаурцепул \_ класса CIM ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="c3ee3-103">DeleteResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="c3ee3-104">Запуск задания для удаления пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c3ee3-104">Start a job to delete a resource pool.</span></span> <span data-ttu-id="c3ee3-105">Нет невыполненных выделений, или операция удаления завершится с ошибкой "используется".</span><span class="sxs-lookup"><span data-stu-id="c3ee3-105">No allocations may be outstanding or the delete will fail with "In Use."</span></span> <span data-ttu-id="c3ee3-106">Если пул ресурсов является корневым пулом ресурсов, все ресурсы узла возвращаются к базовой системе.</span><span class="sxs-lookup"><span data-stu-id="c3ee3-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ee3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3ee3-107">Syntax</span></span>


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c3ee3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3ee3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ee3-109">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3ee3-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ee3-110">[**\_ ResourcePool CIM**](cim-resourcepool.md) , ссылающийся на удаляемый пул.</span><span class="sxs-lookup"><span data-stu-id="c3ee3-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references to the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="c3ee3-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c3ee3-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ee3-112">[**\_ Конкретежоб CIM**](cim-concretejob.md) , который ссылается на задание (может иметь **значение NULL** , если задание завершено).</span><span class="sxs-lookup"><span data-stu-id="c3ee3-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ee3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3ee3-113">Return value</span></span>

<span data-ttu-id="c3ee3-114">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c3ee3-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c3ee3-115">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-117">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-119">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-120">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-121">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-122">**Неверный ResourceType для пула** (7)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c3ee3-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="c3ee3-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c3ee3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c3ee3-127">Requirements</span></span>



| <span data-ttu-id="c3ee3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c3ee3-128">Requirement</span></span> | <span data-ttu-id="c3ee3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ee3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ee3-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3ee3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ee3-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c3ee3-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c3ee3-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3ee3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ee3-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c3ee3-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c3ee3-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c3ee3-134">Namespace</span></span><br/>                | <span data-ttu-id="c3ee3-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c3ee3-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c3ee3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c3ee3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3ee3-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3ee3-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3ee3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c3ee3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3ee3-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3ee3-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c3ee3-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3ee3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ee3-141">**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="c3ee3-141">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




