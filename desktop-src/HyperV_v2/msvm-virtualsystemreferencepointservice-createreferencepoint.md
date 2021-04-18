---
description: Создает опорную точку виртуальной системы.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Метод Креатереференцепоинт класса Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664810"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="e92f0-103">Метод Креатереференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="e92f0-103">CreateReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="e92f0-104">Создает опорную точку виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="e92f0-104">Creates a reference point of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e92f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e92f0-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e92f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e92f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e92f0-107">*Аффектедсистем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e92f0-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e92f0-108">Объект [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , который ссылается на затронутую виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="e92f0-108">A [**Msvm\_ComputerSystem**](msvm-computersystem.md) that references the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="e92f0-109">*Референцепоинтсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e92f0-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e92f0-110">Содержит настройки параметров.</span><span class="sxs-lookup"><span data-stu-id="e92f0-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="e92f0-111">*Референцепоинттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e92f0-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e92f0-112">Тип запрошенной точки ссылки:</span><span class="sxs-lookup"><span data-stu-id="e92f0-112">Requested reference point type:</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="e92f0-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**На основе журнала** (0)</span><span class="sxs-lookup"><span data-stu-id="e92f0-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e92f0-114">На основе отслеживания журнала реплики Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e92f0-114">Based on Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="e92f0-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**На основе RCT** (1)</span><span class="sxs-lookup"><span data-stu-id="e92f0-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e92f0-116">На основе устойчивых Отслеживание изменений виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="e92f0-116">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e92f0-117">*Ресултингреференцепоинт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e92f0-117">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e92f0-118">Результирующая эталонная точка виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="e92f0-118">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="e92f0-119">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e92f0-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e92f0-120">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="e92f0-120">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="e92f0-121">В этом случае экземпляр класса [**мсвм \_ виртуалсистемреференцепоинт**](msvm-virtualsystemreferencepoint.md) , представляющий новую опорную точку виртуальной системы, представлен через ассоциацию [**CIM \_ аффектеджобелемент**](cim-affectedjobelement.md) со значением свойства **аффектеделемент** , ссылающегося на новый экземпляр класса **мсвм \_ виртуалсистемреференцепоинт** , который представляет точку ссылки на виртуальную систему, а значение **ElementEffects** установлено в 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="e92f0-121">In this case, the instance of the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) class representing the new virtual system reference point is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **Msvm\_VirtualSystemReferencePoint** class representing the virtual system reference point and the value of the **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e92f0-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e92f0-122">Return value</span></span>

<span data-ttu-id="e92f0-123">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e92f0-123">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e92f0-124">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="e92f0-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-125">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="e92f0-125">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-126">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="e92f0-126">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-127">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="e92f0-127">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-128">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="e92f0-128">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-129">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="e92f0-129">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-130">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="e92f0-130">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-131">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="e92f0-131">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-132">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="e92f0-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-133">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e92f0-133">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e92f0-134">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="e92f0-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e92f0-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e92f0-135">Requirements</span></span>



| <span data-ttu-id="e92f0-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e92f0-136">Requirement</span></span> | <span data-ttu-id="e92f0-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e92f0-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e92f0-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e92f0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e92f0-139">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e92f0-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e92f0-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e92f0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e92f0-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e92f0-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e92f0-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e92f0-142">Namespace</span></span><br/>                | <span data-ttu-id="e92f0-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e92f0-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e92f0-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e92f0-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e92f0-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e92f0-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e92f0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e92f0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e92f0-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e92f0-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e92f0-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e92f0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e92f0-149">**Мсвм \_ виртуалсистемреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="e92f0-149">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




