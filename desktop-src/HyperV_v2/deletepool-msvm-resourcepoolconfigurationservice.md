---
description: Удаляет пул ресурсов.
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: Метод DeletePool класса Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84273daa0aa30dca8722d90d4fcec22b88325bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663991"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="61be0-103">Метод DeletePool \_ класса Ресаурцепулконфигуратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="61be0-103">DeletePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="61be0-104">Удаляет пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61be0-104">Deletes a resource pool.</span></span> <span data-ttu-id="61be0-105">Для успешного удаления пула ресурсов выделение не может быть завершено, а удаление завершится с ошибкой 32774 (используется).</span><span class="sxs-lookup"><span data-stu-id="61be0-105">To successfully delete a resource pool, no allocations can be outstanding or the delete will fail with 32774 (In Use).</span></span> <span data-ttu-id="61be0-106">Если пул ресурсов является корневым пулом ресурсов, все ресурсы узла возвращаются к базовой системе.</span><span class="sxs-lookup"><span data-stu-id="61be0-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="61be0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61be0-107">Syntax</span></span>


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="61be0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="61be0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61be0-109">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61be0-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61be0-110">Ссылка на экземпляр класса [**CIM \_ ResourcePool**](cim-resourcepool.md) , представляющий удаляемый пул.</span><span class="sxs-lookup"><span data-stu-id="61be0-110">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="61be0-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61be0-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61be0-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61be0-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61be0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61be0-113">Return value</span></span>

<span data-ttu-id="61be0-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="61be0-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="61be0-115">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="61be0-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-116">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="61be0-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="61be0-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-118">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="61be0-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="61be0-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="61be0-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="61be0-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-122">**Неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="61be0-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="61be0-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="61be0-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-125">**Используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="61be0-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-126">**Недопустимое состояние** (32775)</span><span class="sxs-lookup"><span data-stu-id="61be0-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-127">**Неверный тип ресурса для пула** (32776)</span><span class="sxs-lookup"><span data-stu-id="61be0-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-128">**Недоступно** (32777)</span><span class="sxs-lookup"><span data-stu-id="61be0-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="61be0-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-130">**Поставщик зарезервирован** (32779)</span><span class="sxs-lookup"><span data-stu-id="61be0-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-131">**Недостаточно ресурсов** (32780)</span><span class="sxs-lookup"><span data-stu-id="61be0-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-132">**Объект не найден** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="61be0-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-133">**Объект существует** (32788)</span><span class="sxs-lookup"><span data-stu-id="61be0-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="61be0-134">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="61be0-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="61be0-135">Требования</span><span class="sxs-lookup"><span data-stu-id="61be0-135">Requirements</span></span>



| <span data-ttu-id="61be0-136">Требование</span><span class="sxs-lookup"><span data-stu-id="61be0-136">Requirement</span></span> | <span data-ttu-id="61be0-137">Значение</span><span class="sxs-lookup"><span data-stu-id="61be0-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61be0-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61be0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="61be0-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61be0-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61be0-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61be0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="61be0-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61be0-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61be0-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61be0-142">Namespace</span></span><br/>                | <span data-ttu-id="61be0-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="61be0-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61be0-144">MOF</span><span class="sxs-lookup"><span data-stu-id="61be0-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61be0-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61be0-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61be0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="61be0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61be0-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61be0-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61be0-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61be0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61be0-149">**Мсвм \_ ресаурцепулконфигуратионсервице**</span><span class="sxs-lookup"><span data-stu-id="61be0-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

