---
description: Уничтожает существующую коллекцию опорных точек. Этот метод может в качестве побочного действия уничтожить другие опорные точки, зависящие от затронутой коллекции опорных точек.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Метод Дестройреференцепоинт класса Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156862"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="f1f5d-104">Метод Дестройреференцепоинт \_ класса Коллектионреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="f1f5d-104">DestroyReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="f1f5d-105">Уничтожает существующую коллекцию опорных точек.</span><span class="sxs-lookup"><span data-stu-id="f1f5d-105">Destroys an existing reference point collection.</span></span> <span data-ttu-id="f1f5d-106">Этот метод может в качестве побочного действия уничтожить другие опорные точки, зависящие от затронутой коллекции опорных точек.</span><span class="sxs-lookup"><span data-stu-id="f1f5d-106">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f5d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1f5d-107">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f1f5d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1f5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f5d-109">*Аффектедреференцепоинтколлектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1f5d-109">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f5d-110">Ссылка на затронутую коллекцию опорных точек виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f1f5d-110">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="f1f5d-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1f5d-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f5d-112">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="f1f5d-112">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f5d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1f5d-113">Return value</span></span>

<span data-ttu-id="f1f5d-114">В случае успеха возвращает 0 (без ошибок) или 4096 (задание запущено). в противном случае возвратите ошибку.</span><span class="sxs-lookup"><span data-stu-id="f1f5d-114">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="f1f5d-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-117">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-119">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-120">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-121">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-121">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-122">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-123">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-124">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f1f5d-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="f1f5d-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f1f5d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f1f5d-126">Requirements</span></span>



| <span data-ttu-id="f1f5d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f1f5d-127">Requirement</span></span> | <span data-ttu-id="f1f5d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f1f5d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f5d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1f5d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f5d-130">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f1f5d-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f1f5d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1f5d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f5d-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f1f5d-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f1f5d-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1f5d-133">Namespace</span></span><br/>                | <span data-ttu-id="f1f5d-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f1f5d-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1f5d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f1f5d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1f5d-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1f5d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1f5d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f1f5d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1f5d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1f5d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1f5d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1f5d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f5d-140">**Мсвм \_ коллектионреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="f1f5d-140">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




