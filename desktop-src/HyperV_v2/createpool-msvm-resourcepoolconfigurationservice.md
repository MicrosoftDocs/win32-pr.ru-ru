---
description: Создает дочерний пул ресурсов.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Метод CreatePool класса Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683757"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="93d14-103">Метод CreatePool \_ класса Ресаурцепулконфигуратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="93d14-103">CreatePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="93d14-104">Создает дочерний пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93d14-104">Creates a child resource pool.</span></span> <span data-ttu-id="93d14-105">Пул ресурсов будет находиться в той же системе, что и эта служба.</span><span class="sxs-lookup"><span data-stu-id="93d14-105">The resource pool will be scoped to the same System as this Service.</span></span> <span data-ttu-id="93d14-106">Полученный пул будет дочерним пулом.</span><span class="sxs-lookup"><span data-stu-id="93d14-106">The resulting pool will be a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d14-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93d14-107">Syntax</span></span>


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="93d14-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="93d14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d14-109">*Пулсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d14-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d14-110">Встроенный экземпляр класса [**мсвм \_ ресаурцепулсеттингдата**](msvm-resourcepoolsettingdata.md) , который используется для указания параметров пула, не связанных с распределением.</span><span class="sxs-lookup"><span data-stu-id="93d14-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the pool settings that are not allocation related.</span></span>

</dd> <dt>

<span data-ttu-id="93d14-111">*Парентпулс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d14-111">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d14-112">Массив ссылок на [**мсвм \_ ResourcePool**](msvm-resourcepool.md) , представляющих пул или пулы, из которых создается новый пул.</span><span class="sxs-lookup"><span data-stu-id="93d14-112">An array of [**Msvm\_ResourcePool**](msvm-resourcepool.md) references that represent the pool or pools from which to create the new pool.</span></span>

</dd> <dt>

<span data-ttu-id="93d14-113">*Аллокатионсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d14-113">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d14-114">Массив из одного или нескольких внедренных экземпляров класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) , которые используются для указания параметров, связанных с выделением пула.</span><span class="sxs-lookup"><span data-stu-id="93d14-114">An array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span> <span data-ttu-id="93d14-115">Этот массив должен содержать либо один элемент для каждого элемента в массиве *парентпулс* , либо только один элемент.</span><span class="sxs-lookup"><span data-stu-id="93d14-115">This array must contain either one element for each element in the *ParentPools* array, or exactly one element.</span></span> <span data-ttu-id="93d14-116">Если этот массив содержит один элемент, а *парентпулс* содержит более одного элемента, *алллокатионсеттингс* указывает общее распределение емкости, которое может быть удовлетворено любым из родительских пулов.</span><span class="sxs-lookup"><span data-stu-id="93d14-116">If this array contains one element and *ParentPools* contains more than one element, *AlllocationSettings* specifies a shared capacity allocation that can be satisfied by any of the parent pools.</span></span>

<span data-ttu-id="93d14-117">Он используется для ограничения ресурсов, которые могут быть выделены от дочернего пула к пулу, до более низкого предела, чем совокупная емкость, предоставляемая его родительскими элементами.</span><span class="sxs-lookup"><span data-stu-id="93d14-117">This is used to restrict the resources that can be allocated from the child to the pool to a lower limit than the aggregate capacity provided by its parents.</span></span> <span data-ttu-id="93d14-118">Этот параметр не поддерживается всеми типами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93d14-118">This option is not supported by all resource types.</span></span> <span data-ttu-id="93d14-119">Если тип ресурса не поддерживает распределение общей емкости, этот метод возвратит 32770 (не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="93d14-119">If a resource type does not support shared capacity allocation, this method will return 32770 (Not Supported).</span></span>

</dd> <dt>

<span data-ttu-id="93d14-120">*Пул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="93d14-120">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93d14-121">Ссылка на полученный пул.</span><span class="sxs-lookup"><span data-stu-id="93d14-121">A reference to the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="93d14-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="93d14-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93d14-123">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d14-123">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d14-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93d14-124">Return value</span></span>

<span data-ttu-id="93d14-125">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="93d14-125">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="93d14-126">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="93d14-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-127">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="93d14-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-128">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="93d14-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-129">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="93d14-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-130">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="93d14-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-131">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="93d14-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-132">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="93d14-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-133">**Неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="93d14-133">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-134">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="93d14-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-135">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="93d14-135">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-136">**Используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="93d14-136">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-137">**Недопустимое состояние** (32775)</span><span class="sxs-lookup"><span data-stu-id="93d14-137">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-138">**Неверный тип ресурса для пула** (32776)</span><span class="sxs-lookup"><span data-stu-id="93d14-138">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-139">**Недоступно** (32777)</span><span class="sxs-lookup"><span data-stu-id="93d14-139">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-140">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="93d14-140">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-141">**Поставщик зарезервирован** (32779)</span><span class="sxs-lookup"><span data-stu-id="93d14-141">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-142">**Недостаточно ресурсов** (32780)</span><span class="sxs-lookup"><span data-stu-id="93d14-142">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-143">**Объект не найден** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="93d14-143">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-144">**Объект существует** (32788)</span><span class="sxs-lookup"><span data-stu-id="93d14-144">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="93d14-145">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="93d14-145">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="93d14-146">Требования</span><span class="sxs-lookup"><span data-stu-id="93d14-146">Requirements</span></span>



| <span data-ttu-id="93d14-147">Требование</span><span class="sxs-lookup"><span data-stu-id="93d14-147">Requirement</span></span> | <span data-ttu-id="93d14-148">Значение</span><span class="sxs-lookup"><span data-stu-id="93d14-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d14-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93d14-149">Minimum supported client</span></span><br/> | <span data-ttu-id="93d14-150">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="93d14-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93d14-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93d14-151">Minimum supported server</span></span><br/> | <span data-ttu-id="93d14-152">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="93d14-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93d14-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93d14-153">Namespace</span></span><br/>                | <span data-ttu-id="93d14-154">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="93d14-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93d14-155">MOF</span><span class="sxs-lookup"><span data-stu-id="93d14-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93d14-156"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93d14-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93d14-157">DLL</span><span class="sxs-lookup"><span data-stu-id="93d14-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93d14-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93d14-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93d14-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93d14-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d14-160">**Мсвм \_ ресаурцепулконфигуратионсервице**</span><span class="sxs-lookup"><span data-stu-id="93d14-160">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

