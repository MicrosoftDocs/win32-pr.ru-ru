---
description: Удаляет запись моментального снимка виртуального жесткого диска в файле набора виртуальных жестких дисков.
ms.assetid: 37d55a5f-209d-42ce-8f69-8b494055e263
title: Метод Делетевхдснапшот класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.DeleteVHDSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5c7f3f115825aedb3a21a8f33326a712c52e0780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682848"
---
# <a name="deletevhdsnapshot-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ced06-103">Метод Делетевхдснапшот \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="ced06-103">DeleteVHDSnapshot method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ced06-104">Удаляет запись моментального снимка виртуального жесткого диска в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="ced06-104">Deletes a VHD Snapshot entry within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced06-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ced06-105">Syntax</span></span>


```mof
uint32 DeleteVHDSnapshot(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotId,
  [in]  boolean             PersistReferenceSnapshot,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ced06-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ced06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ced06-107">*Вхдсетпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ced06-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ced06-108">Строка, содержащая путь к файлу набора виртуальных жестких дисков, содержащему рассматриваемый моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="ced06-108">String containing the path to the VHD Set file containing the snapshot in question.</span></span>

</dd> <dt>

<span data-ttu-id="ced06-109">*SnapshotId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ced06-109">*SnapshotId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ced06-110">Идентификатор GUID, представляющий идентификатор моментального снимка для удаляемого элемента моментального снимка виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="ced06-110">A GUID representing the Snapshot ID for the VHD Snapshot entry to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="ced06-111">*Персистреференцеснапшот* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ced06-111">*PersistReferenceSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ced06-112">Следует ли сохранять запись моментального снимка только для ссылок после удаления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="ced06-112">Whether or not a reference-only snapshot record should be persisted after the snapshot is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="ced06-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ced06-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ced06-114">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="ced06-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ced06-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ced06-115">Return value</span></span>

<span data-ttu-id="ced06-116">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ced06-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ced06-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ced06-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ced06-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="ced06-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="ced06-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ced06-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="ced06-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="ced06-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="ced06-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="ced06-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="ced06-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="ced06-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="ced06-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="ced06-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ced06-130">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="ced06-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ced06-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ced06-131">Requirements</span></span>



| <span data-ttu-id="ced06-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ced06-132">Requirement</span></span> | <span data-ttu-id="ced06-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ced06-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced06-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ced06-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ced06-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ced06-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ced06-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ced06-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ced06-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ced06-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ced06-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ced06-138">Namespace</span></span><br/>                | <span data-ttu-id="ced06-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ced06-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ced06-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ced06-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ced06-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ced06-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ced06-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ced06-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ced06-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ced06-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ced06-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ced06-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced06-145">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="ced06-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




