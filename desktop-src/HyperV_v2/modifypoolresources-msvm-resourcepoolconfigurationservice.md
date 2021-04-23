---
description: Изменяет параметры ресурсов родительского пула для ресурсов, назначенных дочернему пулу.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Метод Модифипулресаурцес класса Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911688"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="75473-103">Метод Модифипулресаурцес \_ класса Ресаурцепулконфигуратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="75473-103">ModifyPoolResources method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="75473-104">Изменяет параметры ресурсов родительского пула для ресурсов, назначенных дочернему пулу.</span><span class="sxs-lookup"><span data-stu-id="75473-104">Changes the parent pool resource settings for resources assigned to a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="75473-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75473-105">Syntax</span></span>


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="75473-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75473-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75473-107">*Чилдпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75473-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75473-108">Ссылка на экземпляр класса [**CIM \_ ResourcePool**](cim-resourcepool.md) , представляющий дочерний пул, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="75473-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="75473-109">*Парентпулс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75473-109">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75473-110">Массив ссылок [**\_ ResourcePool CIM**](cim-resourcepool.md) , представляющих новые родительские пулы, которые нужно назначить дочернему пулу.</span><span class="sxs-lookup"><span data-stu-id="75473-110">An array of [**CIM\_ResourcePool**](cim-resourcepool.md) references that represent the new parent pools to assign to the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="75473-111">*Аллокатионсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="75473-111">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75473-112">Необязательный массив из одного или нескольких внедренных экземпляров класса [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) , которые используются для указания параметров, связанных с выделением пула.</span><span class="sxs-lookup"><span data-stu-id="75473-112">An optional array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span>

</dd> <dt>

<span data-ttu-id="75473-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="75473-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75473-114">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="75473-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75473-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75473-115">Return value</span></span>

<span data-ttu-id="75473-116">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="75473-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="75473-117">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="75473-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75473-118">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="75473-118">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="75473-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="75473-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="75473-120">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="75473-120">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="75473-121">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="75473-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="75473-122">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="75473-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="75473-123">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="75473-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="75473-124">**Неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="75473-124">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="75473-125">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="75473-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="75473-126">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="75473-126">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="75473-127">**Используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="75473-127">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="75473-128">**Недопустимое состояние** (32775)</span><span class="sxs-lookup"><span data-stu-id="75473-128">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="75473-129">**Неверный тип ресурса для пула** (32776)</span><span class="sxs-lookup"><span data-stu-id="75473-129">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="75473-130">**Недоступно** (32777)</span><span class="sxs-lookup"><span data-stu-id="75473-130">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="75473-131">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="75473-131">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="75473-132">**Поставщик зарезервирован** (32779)</span><span class="sxs-lookup"><span data-stu-id="75473-132">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="75473-133">**Недостаточно ресурсов** (32780)</span><span class="sxs-lookup"><span data-stu-id="75473-133">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="75473-134">**Объект не найден** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="75473-134">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="75473-135">**Объект существует** (32788)</span><span class="sxs-lookup"><span data-stu-id="75473-135">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="75473-136">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="75473-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75473-137">Требования</span><span class="sxs-lookup"><span data-stu-id="75473-137">Requirements</span></span>



| <span data-ttu-id="75473-138">Требование</span><span class="sxs-lookup"><span data-stu-id="75473-138">Requirement</span></span> | <span data-ttu-id="75473-139">Значение</span><span class="sxs-lookup"><span data-stu-id="75473-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75473-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75473-140">Minimum supported client</span></span><br/> | <span data-ttu-id="75473-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="75473-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75473-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75473-142">Minimum supported server</span></span><br/> | <span data-ttu-id="75473-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="75473-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75473-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="75473-144">Namespace</span></span><br/>                | <span data-ttu-id="75473-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="75473-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75473-146">MOF</span><span class="sxs-lookup"><span data-stu-id="75473-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75473-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75473-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75473-148">DLL</span><span class="sxs-lookup"><span data-stu-id="75473-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75473-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75473-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75473-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75473-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75473-151">**Мсвм \_ ресаурцепулконфигуратионсервице**</span><span class="sxs-lookup"><span data-stu-id="75473-151">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

