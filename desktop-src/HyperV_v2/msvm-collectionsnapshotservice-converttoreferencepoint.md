---
description: Преобразование существующего моментального снимка коллекции в коллекцию опорных точек. Коллекция моментальных снимков удаляется как побочный результат. В контрольные точки можно преобразовать только моментальные снимки восстановления.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Метод Конверттореференцепоинт класса Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913703"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="63723-105">Метод Конверттореференцепоинт \_ класса Коллектионснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="63723-105">ConvertToReferencePoint method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="63723-106">Преобразование существующего моментального снимка коллекции в коллекцию опорных точек.</span><span class="sxs-lookup"><span data-stu-id="63723-106">Convert an existing collection snapshot to a reference point collection.</span></span> <span data-ttu-id="63723-107">Коллекция моментальных снимков удаляется как побочный результат.</span><span class="sxs-lookup"><span data-stu-id="63723-107">The snapshot collection gets deleted as a side effect.</span></span> <span data-ttu-id="63723-108">В контрольные точки можно преобразовать только моментальные снимки восстановления.</span><span class="sxs-lookup"><span data-stu-id="63723-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="63723-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63723-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="63723-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="63723-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63723-111">*Аффектедснапшотколлектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63723-111">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63723-112">Ссылка на [**\_ снапшотколлектион мсвм**](msvm-snapshotcollection.md) , содержащий затронутую коллекцию моментальных снимков виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="63723-112">Reference to a [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) containing the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="63723-113">*Ресултингреференцепоинтколлектион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="63723-113">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63723-114">Ссылка на [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) , содержащий результирующую коллекцию опорных точек виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="63723-114">Reference to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) containing the resulting virtual system reference point collection</span></span>

</dd> <dt>

<span data-ttu-id="63723-115">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63723-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63723-116">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="63723-116">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63723-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63723-117">Return value</span></span>

<span data-ttu-id="63723-118">При успешном выполнении возвращает значение 0 (завершено) или 4096 (задание запущено); в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="63723-118">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="63723-119">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="63723-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63723-120">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="63723-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="63723-121">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="63723-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="63723-122">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="63723-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="63723-123">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="63723-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="63723-124">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="63723-124">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="63723-125">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="63723-125">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="63723-126">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="63723-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="63723-127">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="63723-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="63723-128">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="63723-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="63723-129">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="63723-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="63723-130">Требования</span><span class="sxs-lookup"><span data-stu-id="63723-130">Requirements</span></span>



| <span data-ttu-id="63723-131">Требование</span><span class="sxs-lookup"><span data-stu-id="63723-131">Requirement</span></span> | <span data-ttu-id="63723-132">Значение</span><span class="sxs-lookup"><span data-stu-id="63723-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63723-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63723-133">Minimum supported client</span></span><br/> | <span data-ttu-id="63723-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="63723-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="63723-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63723-135">Minimum supported server</span></span><br/> | <span data-ttu-id="63723-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="63723-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="63723-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="63723-137">Namespace</span></span><br/>                | <span data-ttu-id="63723-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="63723-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="63723-139">MOF</span><span class="sxs-lookup"><span data-stu-id="63723-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63723-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63723-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63723-141">DLL</span><span class="sxs-lookup"><span data-stu-id="63723-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63723-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63723-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="63723-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63723-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63723-144">**Мсвм \_ коллектионснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="63723-144">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




