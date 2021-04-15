---
description: Создает точку ссылки для коллекции виртуальных систем.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Метод Креатереференцепоинт класса Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350315"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="346b9-103">Метод Креатереференцепоинт \_ класса Коллектионреференцепоинтсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="346b9-103">CreateReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="346b9-104">Создает точку ссылки для коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="346b9-104">Creates a reference point of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="346b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="346b9-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="346b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="346b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="346b9-107">*Коллекция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="346b9-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="346b9-108">Ссылка на затронутую коллекцию виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="346b9-108">Reference to the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="346b9-109">*Референцепоинтсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="346b9-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="346b9-110">Параметры параметров.</span><span class="sxs-lookup"><span data-stu-id="346b9-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="346b9-111">*Референцепоинттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="346b9-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="346b9-112">Указывает тип контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="346b9-112">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="346b9-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="346b9-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="346b9-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**На основе журнала** (1)</span><span class="sxs-lookup"><span data-stu-id="346b9-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="346b9-115">Отслеживание журнала реплики Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="346b9-115">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="346b9-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**На основе RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="346b9-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="346b9-117">На основе устойчивых Отслеживание изменений виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="346b9-117">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="346b9-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="346b9-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="346b9-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="346b9-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="346b9-120">*Ресултингреференцепоинтколлектион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="346b9-120">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="346b9-121">Результирующая эталонная точка коллекции виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="346b9-121">Resulting reference point of a virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="346b9-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="346b9-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="346b9-123">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="346b9-123">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="346b9-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="346b9-124">Return value</span></span>

<span data-ttu-id="346b9-125">В случае успеха возвращает 0 (без ошибок) или 4096 (задание запущено). в противном случае возвратите ошибку.</span><span class="sxs-lookup"><span data-stu-id="346b9-125">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="346b9-126">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="346b9-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-127">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="346b9-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-128">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="346b9-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-129">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="346b9-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-130">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="346b9-130">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-131">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="346b9-131">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-132">**Недопустимый тип** (6)</span><span class="sxs-lookup"><span data-stu-id="346b9-132">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-133">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="346b9-133">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-134">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="346b9-134">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-135">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="346b9-135">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="346b9-136">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="346b9-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="346b9-137">Требования</span><span class="sxs-lookup"><span data-stu-id="346b9-137">Requirements</span></span>



| <span data-ttu-id="346b9-138">Требование</span><span class="sxs-lookup"><span data-stu-id="346b9-138">Requirement</span></span> | <span data-ttu-id="346b9-139">Значение</span><span class="sxs-lookup"><span data-stu-id="346b9-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346b9-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="346b9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="346b9-141">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="346b9-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="346b9-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="346b9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="346b9-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="346b9-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="346b9-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="346b9-144">Namespace</span></span><br/>                | <span data-ttu-id="346b9-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="346b9-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="346b9-146">MOF</span><span class="sxs-lookup"><span data-stu-id="346b9-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="346b9-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="346b9-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="346b9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="346b9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="346b9-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="346b9-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="346b9-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="346b9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346b9-151">**Мсвм \_ коллектионреференцепоинтсервице**</span><span class="sxs-lookup"><span data-stu-id="346b9-151">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




