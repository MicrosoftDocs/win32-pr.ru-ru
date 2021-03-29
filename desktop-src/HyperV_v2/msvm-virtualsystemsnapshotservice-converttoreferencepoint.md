---
description: Преобразование существующего моментального снимка виртуальной системы в точку ссылки. Моментальный снимок удаляется как побочный результат. В контрольные точки можно преобразовать только моментальные снимки восстановления.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Метод Конверттореференцепоинт класса Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662226"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="6cb57-105">Метод Конверттореференцепоинт \_ класса Виртуалсистемснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="6cb57-105">ConvertToReferencePoint method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="6cb57-106">Преобразование существующего моментального снимка виртуальной системы в точку ссылки.</span><span class="sxs-lookup"><span data-stu-id="6cb57-106">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="6cb57-107">Моментальный снимок удаляется как побочный результат.</span><span class="sxs-lookup"><span data-stu-id="6cb57-107">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="6cb57-108">В контрольные точки можно преобразовать только моментальные снимки восстановления.</span><span class="sxs-lookup"><span data-stu-id="6cb57-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb57-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cb57-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6cb57-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cb57-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb57-111">*Аффектедснапшот* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cb57-111">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb57-112">Ссылка на затронутый моментальный снимок виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="6cb57-112">Reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="6cb57-113">*Референцепоинтсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6cb57-113">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb57-114">Параметры параметров.</span><span class="sxs-lookup"><span data-stu-id="6cb57-114">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="6cb57-115">*Ресултингреференцепоинт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6cb57-115">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb57-116">Результирующая эталонная точка виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="6cb57-116">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="6cb57-117">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6cb57-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb57-118">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="6cb57-118">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb57-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cb57-119">Return value</span></span>

<span data-ttu-id="6cb57-120">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6cb57-120">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6cb57-121">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6cb57-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-122">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="6cb57-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-123">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="6cb57-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-124">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="6cb57-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-125">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="6cb57-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-126">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="6cb57-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-127">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="6cb57-127">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-128">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="6cb57-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-129">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="6cb57-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-130">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6cb57-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6cb57-131">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="6cb57-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6cb57-132">Требования</span><span class="sxs-lookup"><span data-stu-id="6cb57-132">Requirements</span></span>



| <span data-ttu-id="6cb57-133">Требование</span><span class="sxs-lookup"><span data-stu-id="6cb57-133">Requirement</span></span> | <span data-ttu-id="6cb57-134">Значение</span><span class="sxs-lookup"><span data-stu-id="6cb57-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb57-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cb57-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb57-136">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6cb57-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6cb57-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cb57-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb57-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6cb57-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6cb57-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6cb57-139">Namespace</span></span><br/>                | <span data-ttu-id="6cb57-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6cb57-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6cb57-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6cb57-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cb57-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cb57-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cb57-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6cb57-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cb57-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6cb57-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6cb57-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cb57-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb57-146">**Мсвм \_ виртуалсистемснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="6cb57-146">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




