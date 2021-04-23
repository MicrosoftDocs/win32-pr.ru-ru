---
description: Извлекает сведения о файле набора виртуальных жестких дисков.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Метод Жетвхдсетинформатион класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682847"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="d01ff-103">Метод Жетвхдсетинформатион \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="d01ff-103">GetVHDSetInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="d01ff-104">Извлекает сведения о файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="d01ff-104">Retrieves information about a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d01ff-105">Syntax</span></span>


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d01ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d01ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d01ff-107">*Вхдсетпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d01ff-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d01ff-108">Полный путь, указывающий расположение файла набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="d01ff-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="d01ff-109">*Аддитионалинформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d01ff-109">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d01ff-110">Массив, указывающий, какие дополнительные сведения следует собрать о файле набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="d01ff-110">An array specifying what additional information should be gathered about the VHD Set file.</span></span> <span data-ttu-id="d01ff-111">Каждая запись в массиве является типом дополнительной информации.</span><span class="sxs-lookup"><span data-stu-id="d01ff-111">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="d01ff-112">Если этот параметр имеет значение NULL, дополнительные сведения не извлекаются.</span><span class="sxs-lookup"><span data-stu-id="d01ff-112">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d01ff-113">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d01ff-113">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d01ff-114">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d01ff-114">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

<span data-ttu-id="d01ff-115">**Пути** (2)</span><span class="sxs-lookup"><span data-stu-id="d01ff-115">**Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d01ff-116">*Сведения о* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d01ff-116">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d01ff-117">В случае успеха этот объект содержит сведения для запрошенного файла набора виртуальных жестких дисков.</span><span class="sxs-lookup"><span data-stu-id="d01ff-117">If successful, this object contains the information for the requested VHD Set file.</span></span> <span data-ttu-id="d01ff-118">Это встроенный экземпляр [**мсвм \_ вхдсетинформатион**](msvm-vhdsetinformation.md).</span><span class="sxs-lookup"><span data-stu-id="d01ff-118">This is an embedded instance of [**Msvm\_VHDSetInformation**](msvm-vhdsetinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01ff-119">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d01ff-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d01ff-120">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="d01ff-120">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d01ff-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d01ff-121">Return value</span></span>

<span data-ttu-id="d01ff-122">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d01ff-122">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d01ff-123">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d01ff-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d01ff-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-125">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="d01ff-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-126">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="d01ff-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-127">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="d01ff-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-128">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="d01ff-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-129">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="d01ff-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-130">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="d01ff-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-131">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="d01ff-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-132">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="d01ff-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-133">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="d01ff-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-134">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="d01ff-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-135">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="d01ff-135">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d01ff-136">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="d01ff-136">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d01ff-137">Требования</span><span class="sxs-lookup"><span data-stu-id="d01ff-137">Requirements</span></span>



| <span data-ttu-id="d01ff-138">Требование</span><span class="sxs-lookup"><span data-stu-id="d01ff-138">Requirement</span></span> | <span data-ttu-id="d01ff-139">Значение</span><span class="sxs-lookup"><span data-stu-id="d01ff-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01ff-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d01ff-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d01ff-141">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d01ff-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d01ff-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d01ff-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d01ff-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d01ff-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d01ff-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d01ff-144">Namespace</span></span><br/>                | <span data-ttu-id="d01ff-145">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d01ff-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d01ff-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d01ff-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d01ff-147"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d01ff-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d01ff-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d01ff-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d01ff-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d01ff-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d01ff-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d01ff-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01ff-151">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="d01ff-151">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




