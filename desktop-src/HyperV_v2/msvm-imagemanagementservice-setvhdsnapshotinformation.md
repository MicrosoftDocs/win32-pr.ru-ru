---
description: Изменяет запись моментального снимка виртуального жесткого диска в файле набора виртуальных жестких дисков. Если идентификатор моментального снимка в вопросе уже существует, существующая запись моментального снимка будет перезаписана новой записью. В противном случае новая запись будет добавлена в файл набора виртуальных жестких дисков.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Метод Сетвхдснапшотинформатион класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 54f5ac23cdf8f49532a05eee3fd23293715cd02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662515"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="07e04-105">Метод Сетвхдснапшотинформатион \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="07e04-105">SetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="07e04-106">Изменяет запись моментального снимка виртуального жесткого диска в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="07e04-106">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="07e04-107">Если идентификатор моментального снимка в вопросе уже существует, существующая запись моментального снимка будет перезаписана новой записью.</span><span class="sxs-lookup"><span data-stu-id="07e04-107">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="07e04-108">В противном случае новая запись будет добавлена в файл набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="07e04-108">Otherwise, the new entry will be added to the VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e04-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07e04-109">Syntax</span></span>


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="07e04-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="07e04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e04-111">*Сведения о* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07e04-111">*Information* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07e04-112">Сведения о моментальном снимке VHD, которые необходимо изменить или добавить в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="07e04-112">VHD Snapshot Information to be changed or added in the VHD Set file.</span></span> <span data-ttu-id="07e04-113">Строка является внедренным экземпляром [**мсвм \_ вхдснапшотинформатион**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="07e04-113">The string is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="07e04-114">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07e04-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07e04-115">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="07e04-115">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07e04-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07e04-116">Return value</span></span>

<span data-ttu-id="07e04-117">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="07e04-117">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="07e04-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="07e04-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-119">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="07e04-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-120">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="07e04-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-121">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="07e04-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-122">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="07e04-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-123">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="07e04-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-124">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="07e04-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-125">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="07e04-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-126">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="07e04-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-127">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="07e04-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-128">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="07e04-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-129">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="07e04-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-130">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="07e04-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="07e04-131">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="07e04-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="07e04-132">Требования</span><span class="sxs-lookup"><span data-stu-id="07e04-132">Requirements</span></span>



| <span data-ttu-id="07e04-133">Требование</span><span class="sxs-lookup"><span data-stu-id="07e04-133">Requirement</span></span> | <span data-ttu-id="07e04-134">Значение</span><span class="sxs-lookup"><span data-stu-id="07e04-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07e04-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07e04-135">Minimum supported client</span></span><br/> | <span data-ttu-id="07e04-136">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="07e04-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="07e04-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07e04-137">Minimum supported server</span></span><br/> | <span data-ttu-id="07e04-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="07e04-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="07e04-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="07e04-139">Namespace</span></span><br/>                | <span data-ttu-id="07e04-140">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="07e04-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="07e04-141">MOF</span><span class="sxs-lookup"><span data-stu-id="07e04-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07e04-142"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07e04-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="07e04-143">DLL</span><span class="sxs-lookup"><span data-stu-id="07e04-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07e04-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07e04-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="07e04-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07e04-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e04-146">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="07e04-146">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




