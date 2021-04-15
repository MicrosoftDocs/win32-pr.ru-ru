---
description: Извлекает сведения о моментальном снимке виртуального жесткого диска в файле набора виртуальных жестких дисков.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Метод Жетвхдснапшотинформатион класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 85ea18e2be5329345ba49f4956307c4b29134ed6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662519"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="db503-103">Метод Жетвхдснапшотинформатион \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="db503-103">GetVHDSnapshotInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="db503-104">Извлекает сведения о моментальном снимке виртуального жесткого диска в файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="db503-104">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="db503-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db503-105">Syntax</span></span>


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="db503-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db503-107">*Вхдсетпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db503-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db503-108">Полный путь, указывающий расположение файла набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="db503-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="db503-109">*Снапшотидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db503-109">*SnapshotIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db503-110">Список идентификаторов GUID, представляющих идентификаторы моментальных снимков каждого моментального снимка, для которого запрашиваются сведения.</span><span class="sxs-lookup"><span data-stu-id="db503-110">A list of GUIDs representing the Snapshot Ids of each Snapshot for which information is being requested.</span></span> <span data-ttu-id="db503-111">Если этот параметр имеет значение NULL, то будут получены сведения обо всех моментальных снимках.</span><span class="sxs-lookup"><span data-stu-id="db503-111">If this parameter is NULL, information for all Snapshots will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="db503-112">*Аддитионалинформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db503-112">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db503-113">Массив, указывающий, какие дополнительные сведения следует собрать о каждом моментальном снимке виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="db503-113">An array specifying what additional information should be gathered about each VHD Snapshot.</span></span> <span data-ttu-id="db503-114">Каждая запись в массиве является типом дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="db503-114">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="db503-115">Если этот параметр имеет значение NULL, дополнительные сведения не извлекаются.</span><span class="sxs-lookup"><span data-stu-id="db503-115">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db503-116">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="db503-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db503-117">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="db503-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

<span data-ttu-id="db503-118">**Родительские пути** (2)</span><span class="sxs-lookup"><span data-stu-id="db503-118">**Parent Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="db503-119">*Снапшотинформатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db503-119">*SnapshotInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db503-120">В случае успеха массив сведений о каждом запрошенном моментальном снимке.</span><span class="sxs-lookup"><span data-stu-id="db503-120">If successful, an array of information about each requested snapshot.</span></span> <span data-ttu-id="db503-121">Каждый элемент является внедренным экземпляром [**мсвм \_ вхдснапшотинформатион**](msvm-vhdsnapshotinformation.md).</span><span class="sxs-lookup"><span data-stu-id="db503-121">Each element is an embedded instance of [**Msvm\_VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="db503-122">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db503-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db503-123">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="db503-123">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db503-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db503-124">Return value</span></span>

<span data-ttu-id="db503-125">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="db503-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="db503-126">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="db503-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="db503-127">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="db503-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="db503-128">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="db503-128">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="db503-129">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="db503-129">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="db503-130">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="db503-130">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="db503-131">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="db503-131">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="db503-132">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="db503-132">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="db503-133">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="db503-133">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="db503-134">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="db503-134">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="db503-135">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="db503-135">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="db503-136">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="db503-136">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="db503-137">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="db503-137">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="db503-138">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="db503-138">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="db503-139">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="db503-139">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="db503-140">Требования</span><span class="sxs-lookup"><span data-stu-id="db503-140">Requirements</span></span>



| <span data-ttu-id="db503-141">Требование</span><span class="sxs-lookup"><span data-stu-id="db503-141">Requirement</span></span> | <span data-ttu-id="db503-142">Значение</span><span class="sxs-lookup"><span data-stu-id="db503-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db503-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db503-143">Minimum supported client</span></span><br/> | <span data-ttu-id="db503-144">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="db503-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="db503-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db503-145">Minimum supported server</span></span><br/> | <span data-ttu-id="db503-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="db503-146">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="db503-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db503-147">Namespace</span></span><br/>                | <span data-ttu-id="db503-148">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="db503-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="db503-149">MOF</span><span class="sxs-lookup"><span data-stu-id="db503-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db503-150"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db503-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="db503-151">DLL</span><span class="sxs-lookup"><span data-stu-id="db503-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db503-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="db503-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="db503-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db503-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db503-154">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="db503-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




