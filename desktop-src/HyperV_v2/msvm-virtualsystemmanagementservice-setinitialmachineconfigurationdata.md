---
description: Задает данные конфигурации исходного компьютера для виртуальных машин.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Метод Сетинитиалмачинеконфигуратиондата класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808783"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="78bde-103">Метод Сетинитиалмачинеконфигуратиондата \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="78bde-103">SetInitialMachineConfigurationData method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="78bde-104">Задает исходные данные конфигурации ВИРТУАЛЬНОЙ машины.</span><span class="sxs-lookup"><span data-stu-id="78bde-104">Sets a VM's initial machine configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="78bde-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78bde-105">Syntax</span></span>


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="78bde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78bde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78bde-107">*Параметра targetsystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78bde-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78bde-108">Ссылка на виртуальную систему компьютера, на которой будут установлены данные ИМК.</span><span class="sxs-lookup"><span data-stu-id="78bde-108">A reference to the virtual computer system on which the IMC data will be set.</span></span>

</dd> <dt>

<span data-ttu-id="78bde-109">*CDATA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78bde-109">*ImcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78bde-110">Устанавливаемые данные ИМК.</span><span class="sxs-lookup"><span data-stu-id="78bde-110">The IMC data to set.</span></span> <span data-ttu-id="78bde-111">Первые четыре байта должны быть длиной массива в порядке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="78bde-111">The first four bytes must be the length of the array in big-endian order</span></span>

</dd> <dt>

<span data-ttu-id="78bde-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="78bde-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78bde-113">Необязательный параметр для отслеживания хода выполнения операции, который используется, если метод не может быть выполнен синхронно.</span><span class="sxs-lookup"><span data-stu-id="78bde-113">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="78bde-114">Если операция выполняется асинхронно, возвращается значение 4096.</span><span class="sxs-lookup"><span data-stu-id="78bde-114">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78bde-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78bde-115">Return value</span></span>

<span data-ttu-id="78bde-116">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="78bde-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="78bde-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="78bde-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-118">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="78bde-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="78bde-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="78bde-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="78bde-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-122">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="78bde-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="78bde-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="78bde-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-125">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="78bde-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-126">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="78bde-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-127">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="78bde-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-128">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="78bde-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="78bde-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="78bde-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="78bde-130">Требования</span><span class="sxs-lookup"><span data-stu-id="78bde-130">Requirements</span></span>



| <span data-ttu-id="78bde-131">Требование</span><span class="sxs-lookup"><span data-stu-id="78bde-131">Requirement</span></span> | <span data-ttu-id="78bde-132">Значение</span><span class="sxs-lookup"><span data-stu-id="78bde-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78bde-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78bde-133">Minimum supported client</span></span><br/> | <span data-ttu-id="78bde-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="78bde-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="78bde-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78bde-135">Minimum supported server</span></span><br/> | <span data-ttu-id="78bde-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="78bde-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="78bde-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="78bde-137">Namespace</span></span><br/>                | <span data-ttu-id="78bde-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="78bde-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="78bde-139">MOF</span><span class="sxs-lookup"><span data-stu-id="78bde-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78bde-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78bde-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78bde-141">DLL</span><span class="sxs-lookup"><span data-stu-id="78bde-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78bde-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78bde-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="78bde-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78bde-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78bde-144">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="78bde-144">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




