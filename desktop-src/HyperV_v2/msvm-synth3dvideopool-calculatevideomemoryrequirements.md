---
description: Вычисляет объем видеопамяти, необходимый для виртуальной машины RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Метод Калкулатевидеомеморирекуирементс класса Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154591"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a><span data-ttu-id="92761-103">Метод Калкулатевидеомеморирекуирементс \_ класса Synth3dVideoPool мсвм</span><span class="sxs-lookup"><span data-stu-id="92761-103">CalculateVideoMemoryRequirements method of the Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="92761-104">Вычисляет объем видеопамяти, необходимый для виртуальной машины RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="92761-104">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="92761-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92761-105">Syntax</span></span>


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a><span data-ttu-id="92761-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92761-107">*monitorResolution* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92761-107">*monitorResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92761-108">Максимальное разрешение монитора для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92761-108">The maximum monitor resolution for the virtual machine.</span></span> <span data-ttu-id="92761-109">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="92761-109">This must be one of the following values.</span></span>



| <span data-ttu-id="92761-110">Значение</span><span class="sxs-lookup"><span data-stu-id="92761-110">Value</span></span>                                                                        | <span data-ttu-id="92761-111">Значение</span><span class="sxs-lookup"><span data-stu-id="92761-111">Meaning</span></span>                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="92761-112"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="92761-112"><dt>0</dt></span></span> </dl> | <span data-ttu-id="92761-113">Максимальное разрешение составляет 1024 768.</span><span class="sxs-lookup"><span data-stu-id="92761-113">The maximum resolution is 1024   768.</span></span><br/>  |
| <dl> <span data-ttu-id="92761-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="92761-114"><dt>1</dt></span></span> </dl> | <span data-ttu-id="92761-115">Максимальное разрешение составляет 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="92761-115">The maximum resolution is 1280   1024.</span></span><br/> |
| <dl> <span data-ttu-id="92761-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="92761-116"><dt>2</dt></span></span> </dl> | <span data-ttu-id="92761-117">Максимальное разрешение составляет 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="92761-117">The maximum resolution is 1600   1200.</span></span><br/> |
| <dl> <span data-ttu-id="92761-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="92761-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="92761-119">Максимальное разрешение составляет 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="92761-119">The maximum resolution is 1920   1200.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="92761-120">*нумберофмониторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92761-120">*numberOfMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92761-121">Максимальное число мониторов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="92761-121">The maximum number of monitors for the virtual machine.</span></span> <span data-ttu-id="92761-122">Минимальное число мониторов — один, а максимальное зависит от максимального разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="92761-122">The minimum number of monitors is one and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="92761-123">В следующей таблице определяется максимальное число мониторов, разрешенных для различных способов разрешения.</span><span class="sxs-lookup"><span data-stu-id="92761-123">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="92761-124">Решение</span><span class="sxs-lookup"><span data-stu-id="92761-124">Resolution</span></span>             | <span data-ttu-id="92761-125">Максимальное число мониторов</span><span class="sxs-lookup"><span data-stu-id="92761-125">Maximum monitors</span></span> |
|------------------------|------------------|
| <span data-ttu-id="92761-126">1024 768</span><span class="sxs-lookup"><span data-stu-id="92761-126">1024   768</span></span><br/>  | <span data-ttu-id="92761-127">4</span><span class="sxs-lookup"><span data-stu-id="92761-127">4</span></span><br/>     |
| <span data-ttu-id="92761-128">1280 1024</span><span class="sxs-lookup"><span data-stu-id="92761-128">1280   1024</span></span><br/> | <span data-ttu-id="92761-129">4</span><span class="sxs-lookup"><span data-stu-id="92761-129">4</span></span><br/>     |
| <span data-ttu-id="92761-130">1600 1200</span><span class="sxs-lookup"><span data-stu-id="92761-130">1600   1200</span></span><br/> | <span data-ttu-id="92761-131">3</span><span class="sxs-lookup"><span data-stu-id="92761-131">3</span></span><br/>     |
| <span data-ttu-id="92761-132">1920 1200</span><span class="sxs-lookup"><span data-stu-id="92761-132">1920   1200</span></span><br/> | <span data-ttu-id="92761-133">2</span><span class="sxs-lookup"><span data-stu-id="92761-133">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="92761-134">*рекуиредвидеомемори* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92761-134">*requiredVideoMemory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92761-135">Получает требуемый объем видеопамяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="92761-135">Receives the required amount of video memory, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92761-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92761-136">Return value</span></span>

<span data-ttu-id="92761-137">Возвращает код состояния, который может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="92761-137">Returns a status code, which can be one of the following values.</span></span>



| <span data-ttu-id="92761-138">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="92761-138">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="92761-139">Описание</span><span class="sxs-lookup"><span data-stu-id="92761-139">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="92761-140"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="92761-140"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="92761-141">Удалось.</span><span class="sxs-lookup"><span data-stu-id="92761-141">Successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="92761-142"><dt>**Параметры метода проверены — задание запущено**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="92761-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="92761-143">Задание запущено.</span><span class="sxs-lookup"><span data-stu-id="92761-143">Job started.</span></span><br/>                               |
| <dl> <span data-ttu-id="92761-144"><dt>**Сбой**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="92761-144"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="92761-145">сбой.</span><span class="sxs-lookup"><span data-stu-id="92761-145">Failed.</span></span><br/>                                    |
| <dl> <span data-ttu-id="92761-146"><dt>**Отказано в доступе**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="92761-146"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="92761-147">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="92761-147">Access denied.</span></span><br/>                             |
| <dl> <span data-ttu-id="92761-148"><dt>**Не поддерживается**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="92761-148"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="92761-149">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="92761-149">Not supported.</span></span><br/>                             |
| <dl> <span data-ttu-id="92761-150"><dt>**Состояние неизвестно**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="92761-150"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="92761-151">Состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="92761-151">Status is unknown.</span></span><br/>                         |
| <dl> <span data-ttu-id="92761-152"><dt>**Время ожидания**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="92761-152"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="92761-153">Превышено время ожидания.</span><span class="sxs-lookup"><span data-stu-id="92761-153">Timeout.</span></span><br/>                                   |
| <dl> <span data-ttu-id="92761-154"><dt>**Недопустимый параметр**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="92761-154"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="92761-155">Недействительный параметр.</span><span class="sxs-lookup"><span data-stu-id="92761-155">A parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="92761-156"><dt>**Система используется**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="92761-156"><dt>**System is in used**</dt> <dt>32774</dt></span></span> </dl>                      | <span data-ttu-id="92761-157">Система используется.</span><span class="sxs-lookup"><span data-stu-id="92761-157">System is in use.</span></span><br/>                          |
| <dl> <span data-ttu-id="92761-158"><dt>**Недопустимое состояние для этой операции**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="92761-158"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="92761-159">Состояние недопустимо для этой операции.</span><span class="sxs-lookup"><span data-stu-id="92761-159">The state is not valid for this operation.</span></span><br/> |
| <dl> <span data-ttu-id="92761-160"><dt>**Недопустимый тип данных**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="92761-160"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="92761-161">Неверный тип данных.</span><span class="sxs-lookup"><span data-stu-id="92761-161">Incorrect data type.</span></span><br/>                       |
| <dl> <span data-ttu-id="92761-162"><dt>**Система недоступна**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="92761-162"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="92761-163">Система недоступна.</span><span class="sxs-lookup"><span data-stu-id="92761-163">System is not available.</span></span><br/>                   |
| <dl> <span data-ttu-id="92761-164"><dt>**Недостаточно памяти**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="92761-164"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="92761-165">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="92761-165">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="92761-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92761-166">Remarks</span></span>

<span data-ttu-id="92761-167">Этот метод обычно вызывается в системе узла, чтобы определить, достаточно ли памяти на узле для размещения виртуальной машины RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="92761-167">This method is typically called on the host system to determine if the host has enough available video memory to host a RemoteFX virtual machine.</span></span> <span data-ttu-id="92761-168">Для этого сравните объем видеопамяти, вычисленный этим методом, с помощью свойства [**мсвм \_ Фисикалгпуинфо. аваилаблевидеомемори**](msvm-physicalgpuinfo.md) , чтобы определить, достаточно ли памяти на размещающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="92761-168">To do this, you compare the amount of video memory calculated by this method with the [**Msvm\_PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) property to determine if the host machine has enough available video memory.</span></span> <span data-ttu-id="92761-169">Эти сведения можно использовать, чтобы определить, можно ли переместить виртуальную машину в систему узла.</span><span class="sxs-lookup"><span data-stu-id="92761-169">You can use this information to determine if a virtual machine can be moved to the host system.</span></span>

## <a name="requirements"></a><span data-ttu-id="92761-170">Требования</span><span class="sxs-lookup"><span data-stu-id="92761-170">Requirements</span></span>



| <span data-ttu-id="92761-171">Требование</span><span class="sxs-lookup"><span data-stu-id="92761-171">Requirement</span></span> | <span data-ttu-id="92761-172">Значение</span><span class="sxs-lookup"><span data-stu-id="92761-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92761-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92761-173">Minimum supported client</span></span><br/> | <span data-ttu-id="92761-174">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="92761-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="92761-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92761-175">Minimum supported server</span></span><br/> | <span data-ttu-id="92761-176">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="92761-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92761-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92761-177">Namespace</span></span><br/>                | <span data-ttu-id="92761-178">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="92761-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="92761-179">MOF</span><span class="sxs-lookup"><span data-stu-id="92761-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92761-180"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92761-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92761-181">DLL</span><span class="sxs-lookup"><span data-stu-id="92761-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92761-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92761-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="92761-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92761-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92761-184">**Мсвм \_ фисикалгпуинфо**</span><span class="sxs-lookup"><span data-stu-id="92761-184">**Msvm\_PhysicalGPUInfo**</span></span>](msvm-physicalgpuinfo.md)
</dt> <dt>

[<span data-ttu-id="92761-185">**Мсвм \_ Synth3dVideoPool**</span><span class="sxs-lookup"><span data-stu-id="92761-185">**Msvm\_Synth3dVideoPool**</span></span>](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




