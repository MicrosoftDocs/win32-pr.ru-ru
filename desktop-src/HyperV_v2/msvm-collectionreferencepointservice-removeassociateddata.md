---
description: Удаляет журнал данных, связанный с точкой ссылки.
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Метод РемовеассоЦиатеддата класса Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aec1ac249616c08c6abf1f156ad5a3416c8afaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664332"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="711ea-103">Метод РемовеассоЦиатеддата \_ класса Коллектионреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="711ea-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="711ea-104">Удаляет журнал данных, связанный с точкой ссылки.</span><span class="sxs-lookup"><span data-stu-id="711ea-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="711ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="711ea-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="711ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="711ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711ea-107">*Аффектедреференцепоинтколлектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="711ea-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="711ea-108">Ссылка на затронутую коллекцию опорных точек виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="711ea-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="711ea-109">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="711ea-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="711ea-110">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="711ea-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711ea-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="711ea-111">Return value</span></span>

<span data-ttu-id="711ea-112">В случае успеха возвращает 0 (без ошибок) или 4096 (задание запущено). в противном случае возвратите ошибку.</span><span class="sxs-lookup"><span data-stu-id="711ea-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="711ea-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="711ea-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-114">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="711ea-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-115">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="711ea-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-116">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="711ea-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-117">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="711ea-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-118">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="711ea-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-119">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="711ea-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="711ea-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="711ea-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-122">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="711ea-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="711ea-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="711ea-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="711ea-124">Требования</span><span class="sxs-lookup"><span data-stu-id="711ea-124">Requirements</span></span>



| <span data-ttu-id="711ea-125">Требование</span><span class="sxs-lookup"><span data-stu-id="711ea-125">Requirement</span></span> | <span data-ttu-id="711ea-126">Значение</span><span class="sxs-lookup"><span data-stu-id="711ea-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="711ea-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="711ea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="711ea-128">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="711ea-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="711ea-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="711ea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="711ea-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="711ea-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="711ea-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="711ea-131">Namespace</span></span><br/>                | <span data-ttu-id="711ea-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="711ea-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="711ea-133">MOF</span><span class="sxs-lookup"><span data-stu-id="711ea-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="711ea-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="711ea-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="711ea-135">DLL</span><span class="sxs-lookup"><span data-stu-id="711ea-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="711ea-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="711ea-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="711ea-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="711ea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711ea-138">**Мсвм \_ коллектионреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="711ea-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




