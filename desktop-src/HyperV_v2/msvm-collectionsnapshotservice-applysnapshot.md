---
description: Применяет коллекцию моментальных снимков к коллекции виртуальных компьютеров.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Метод Апплиснапшот класса Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682649"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="1df50-103">Метод Апплиснапшот \_ класса Коллектионснапшотсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="1df50-103">ApplySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="1df50-104">Применяет коллекцию моментальных снимков к коллекции виртуальных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="1df50-104">Applies a snapshot collection to the collection of virtual computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1df50-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1df50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1df50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1df50-107">*Снапшотколлектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1df50-107">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df50-108">Ссылка на [**\_ коллекцию CIM**](cim-collection.md) , представляющую коллекцию моментальных снимков, которую необходимо применить.</span><span class="sxs-lookup"><span data-stu-id="1df50-108">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="1df50-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1df50-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1df50-110">Необязательная ссылка, которая возвращается, если операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="1df50-110">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="1df50-111">При наличии возвращаемой ссылки на экземпляр [**CIM \_ конкретежоб**](cim-concretejob.md) можно использовать для отслеживания хода выполнения и получения результата метода.</span><span class="sxs-lookup"><span data-stu-id="1df50-111">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1df50-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1df50-112">Return value</span></span>

<span data-ttu-id="1df50-113">При успешном выполнении возвращает 0; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1df50-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1df50-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="1df50-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="1df50-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="1df50-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="1df50-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="1df50-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="1df50-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-120">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="1df50-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1df50-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-122">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="1df50-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-123">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1df50-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1df50-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="1df50-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1df50-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1df50-125">Requirements</span></span>



| <span data-ttu-id="1df50-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1df50-126">Requirement</span></span> | <span data-ttu-id="1df50-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1df50-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df50-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1df50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1df50-129">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="1df50-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1df50-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1df50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1df50-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1df50-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1df50-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1df50-132">Namespace</span></span><br/>                | <span data-ttu-id="1df50-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1df50-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1df50-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1df50-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1df50-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1df50-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1df50-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1df50-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1df50-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1df50-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1df50-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1df50-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df50-139">**Мсвм \_ коллектионснапшотсервице**</span><span class="sxs-lookup"><span data-stu-id="1df50-139">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




