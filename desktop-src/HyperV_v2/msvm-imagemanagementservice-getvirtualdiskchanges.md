---
description: Извлекает список изменений в заданной области виртуального диска, начиная с предоставленного ИД отказоустойчивого Отслеживание изменений или идентификатора моментального снимка Вхдсет.
ms.assetid: c1dac403-96e0-4c0d-ad71-858f04bf07cd
title: Метод Жетвиртуалдискчанжес класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualDiskChanges
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55a9cb9a63e05e002f99984a306566c50d9e1d7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682846"
---
# <a name="getvirtualdiskchanges-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="f3318-103">Метод Жетвиртуалдискчанжес \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="f3318-103">GetVirtualDiskChanges method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="f3318-104">Извлекает список изменений в заданной области виртуального диска, начиная с предоставленного ИД отказоустойчивого Отслеживание изменений или идентификатора моментального снимка Вхдсет.</span><span class="sxs-lookup"><span data-stu-id="f3318-104">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3318-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3318-105">Syntax</span></span>


```mof
uint32 GetVirtualDiskChanges(
  [in]  string              Path,
  [in]  string              LimitId,
  [in]  string              TargetSnapshotId,
  [in]  uint64              ByteOffset,
  [in]  uint64              ByteLength,
  [out] uint64              ProcessedByteLength,
  [out] uint64              ChangedByteOffsets[],
  [out] uint64              ChangedByteLengths[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f3318-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3318-107">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3318-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-108">Полный путь, указывающий расположение файла виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="f3318-108">A fully-qualified path that specifies the location of the Virtual Hard Disk file.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-109">*Лимитид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3318-109">*LimitId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-110">Устойчивый идентификатор Отслеживание изменений или идентификатор моментального снимка набора виртуальных жестких дисков, указывающий базовый план для изменений на виртуальном диске.</span><span class="sxs-lookup"><span data-stu-id="f3318-110">A Resilient Change Tracking Id or VHD Set Snapshot Id indicating the baseline for changes in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-111">*Таржетснапшотид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3318-111">*TargetSnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-112">Идентификатор моментального снимка Вхдсет, указывающий моментальный снимок, который необходимо сравнить с базовыми показателями при обходе изменений на виртуальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="f3318-112">A VHDSet Snapshot Id indicating the snapshot to compare to the baseline when determing changes in the virtual hard disk.</span></span> <span data-ttu-id="f3318-113">Этот параметр допустим только для файлов набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="f3318-113">This parameter is only valid for VHD Set files.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-114">*ByteOffset* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3318-114">*ByteOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-115">Смещение в байтах для региона на виртуальном диске, для которого необходимо запросить изменения.</span><span class="sxs-lookup"><span data-stu-id="f3318-115">The byte offset of the region in the virtual disk to query changes for.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-116">*ByteLength* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3318-116">*ByteLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-117">Длина в байтах области на виртуальном диске для запроса изменений.</span><span class="sxs-lookup"><span data-stu-id="f3318-117">The byte length of the region in the virtual disk to query changes for.</span></span> <span data-ttu-id="f3318-118">Размер должен быть меньше размера виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="f3318-118">This must be less than the size of the Virtual Disk.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-119">*Процесседбителенгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3318-119">*ProcessedByteLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-120">Общая длина обработанного байта.</span><span class="sxs-lookup"><span data-stu-id="f3318-120">The total byte length that was processed.</span></span> <span data-ttu-id="f3318-121">Это значение может быть равно ByteLength или меньше.</span><span class="sxs-lookup"><span data-stu-id="f3318-121">This may be equal to ByteLength or less.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-122">*Чанжедбитеоффсетс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3318-122">*ChangedByteOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-123">Список смещений байтов в виртуальном диске, указывающий начало каждого измененного диапазона.</span><span class="sxs-lookup"><span data-stu-id="f3318-123">The list of byte offsets into the virtual disk indicating the beginning of each changed range.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-124">*Чанжедбителенгсс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3318-124">*ChangedByteLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-125">Список длин байт измененных диапазонов на виртуальном диске.</span><span class="sxs-lookup"><span data-stu-id="f3318-125">The list of byte lengths of the changed ranges in the virtual disk.</span></span>

</dd> <dt>

<span data-ttu-id="f3318-126">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f3318-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3318-127">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="f3318-127">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3318-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3318-128">Return value</span></span>

<span data-ttu-id="f3318-129">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f3318-129">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f3318-130">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f3318-130">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-131">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f3318-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-132">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f3318-132">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-133">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f3318-133">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-134">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f3318-134">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-135">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f3318-135">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-136">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f3318-136">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-137">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f3318-137">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-138">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f3318-138">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-139">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f3318-139">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-140">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f3318-140">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-141">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f3318-141">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-142">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f3318-142">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f3318-143">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="f3318-143">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f3318-144">Требования</span><span class="sxs-lookup"><span data-stu-id="f3318-144">Requirements</span></span>



| <span data-ttu-id="f3318-145">Требование</span><span class="sxs-lookup"><span data-stu-id="f3318-145">Requirement</span></span> | <span data-ttu-id="f3318-146">Значение</span><span class="sxs-lookup"><span data-stu-id="f3318-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3318-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3318-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f3318-148">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f3318-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f3318-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3318-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f3318-150">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f3318-150">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f3318-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3318-151">Namespace</span></span><br/>                | <span data-ttu-id="f3318-152">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f3318-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f3318-153">MOF</span><span class="sxs-lookup"><span data-stu-id="f3318-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3318-154"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3318-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3318-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f3318-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3318-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3318-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3318-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3318-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3318-158">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="f3318-158">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




