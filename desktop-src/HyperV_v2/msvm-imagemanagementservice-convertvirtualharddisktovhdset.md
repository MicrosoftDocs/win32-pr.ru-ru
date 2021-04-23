---
description: Преобразование файла виртуального жесткого диска путем создания нового файла набора ВИРТУАЛЬНЫХ жестких дисков вместе с существующим виртуальным жестким диском.
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Метод Конвертвиртуалхарддисктовхдсет класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6113a14f321ff7319f8be15767621db3a7e833de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999476"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ab299-103">Метод Конвертвиртуалхарддисктовхдсет \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="ab299-103">ConvertVirtualHardDiskToVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ab299-104">Преобразование файла виртуального жесткого диска путем создания нового файла набора ВИРТУАЛЬНЫХ жестких дисков вместе с существующим виртуальным жестким диском.</span><span class="sxs-lookup"><span data-stu-id="ab299-104">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab299-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab299-105">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ab299-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab299-107">*Виртуалхарддискпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab299-107">*VirtualHardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab299-108">Строка, содержащая путь к файлу виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="ab299-108">String containing the path to the virtual hard disk file.</span></span> <span data-ttu-id="ab299-109">Новый файл набора виртуальных жестких дисков будет иметь то же имя файла, но с. Расширение VHD.</span><span class="sxs-lookup"><span data-stu-id="ab299-109">The new VHD Set file will have the same filename but with the .VHDS extension.</span></span>

</dd> <dt>

<span data-ttu-id="ab299-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ab299-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab299-111">Ссылка на задание (может иметь значение null, если задача завершена).</span><span class="sxs-lookup"><span data-stu-id="ab299-111">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab299-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab299-112">Return value</span></span>

<span data-ttu-id="ab299-113">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ab299-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ab299-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="ab299-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="ab299-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="ab299-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="ab299-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ab299-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="ab299-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="ab299-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="ab299-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="ab299-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="ab299-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="ab299-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="ab299-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="ab299-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ab299-127">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="ab299-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ab299-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ab299-128">Requirements</span></span>



| <span data-ttu-id="ab299-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ab299-129">Requirement</span></span> | <span data-ttu-id="ab299-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ab299-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab299-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab299-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ab299-132">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ab299-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ab299-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab299-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ab299-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ab299-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ab299-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ab299-135">Namespace</span></span><br/>                | <span data-ttu-id="ab299-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ab299-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ab299-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ab299-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab299-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab299-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab299-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ab299-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab299-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab299-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab299-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab299-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab299-142">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="ab299-142">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




