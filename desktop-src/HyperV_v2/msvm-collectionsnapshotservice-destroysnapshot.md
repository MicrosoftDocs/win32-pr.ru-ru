---
description: Уничтожает существующий моментальный снимок коллекции виртуальных систем. Этот метод может оказаться побочным действием уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Метод Дестройснапшот класса Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662744"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="53147-104">Метод Дестройснапшот \_ класса Коллектионснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="53147-104">DestroySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="53147-105">Уничтожает существующий моментальный снимок коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="53147-105">Destroys an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="53147-106">Этот метод может оказаться побочным действием уничтожить другие моментальные снимки, зависящие от затронутого моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="53147-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="53147-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53147-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="53147-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53147-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53147-109">*Аффектедснапшотколлектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53147-109">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53147-110">Ссылка на [**\_ коллекцию CIM**](cim-collection.md) , описывающую затронутую коллекцию моментальных снимков виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="53147-110">Reference to a [**CIM\_Collection**](cim-collection.md) that describes the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="53147-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="53147-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53147-112">Необязательная ссылка, которая возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="53147-112">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="53147-113">При наличии возвращаемой ссылки на экземпляр [**CIM \_ конкретежоб**](cim-concretejob.md) можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="53147-113">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53147-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53147-114">Return value</span></span>

<span data-ttu-id="53147-115">При успешном выполнении возвращает значение 0 (завершено) или 4096 (задание запущено); в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="53147-115">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="53147-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="53147-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53147-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="53147-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="53147-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="53147-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="53147-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="53147-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="53147-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="53147-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="53147-121">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="53147-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="53147-122">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="53147-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="53147-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="53147-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="53147-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="53147-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="53147-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="53147-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="53147-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="53147-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="53147-127">Требования</span><span class="sxs-lookup"><span data-stu-id="53147-127">Requirements</span></span>



| <span data-ttu-id="53147-128">Требование</span><span class="sxs-lookup"><span data-stu-id="53147-128">Requirement</span></span> | <span data-ttu-id="53147-129">Значение</span><span class="sxs-lookup"><span data-stu-id="53147-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53147-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53147-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53147-131">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="53147-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="53147-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53147-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53147-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="53147-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="53147-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="53147-134">Namespace</span></span><br/>                | <span data-ttu-id="53147-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="53147-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53147-136">MOF</span><span class="sxs-lookup"><span data-stu-id="53147-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53147-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53147-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53147-138">DLL</span><span class="sxs-lookup"><span data-stu-id="53147-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53147-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53147-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53147-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53147-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53147-141">**Мсвм \_ коллектионснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="53147-141">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




