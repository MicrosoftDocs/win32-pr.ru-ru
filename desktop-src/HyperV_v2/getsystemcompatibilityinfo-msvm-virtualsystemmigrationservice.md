---
description: Создает непрозрачный большой двоичный объект данных, содержащий сведения о совместимости для указанной системы.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Метод Жетсистемкомпатибилитинфо класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682520"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="453be-103">Метод Жетсистемкомпатибилитинфо \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="453be-103">GetSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="453be-104">Создает непрозрачный большой двоичный объект данных, содержащий сведения о совместимости для указанной системы.</span><span class="sxs-lookup"><span data-stu-id="453be-104">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span> <span data-ttu-id="453be-105">Этот метод используется совместно с методом [**чекксистемкомпатибилитинфо**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) , чтобы определить, возможна ли быстрая или динамическая миграция виртуальной машины на другую компьютерную систему, без фактической попытки миграции.</span><span class="sxs-lookup"><span data-stu-id="453be-105">This method is used in conjunction with the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method to determine whether a quick or live migration of a virtual machine to another hosting computer system is possible without actually attempting the migration.</span></span>

## <a name="syntax"></a><span data-ttu-id="453be-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="453be-106">Syntax</span></span>


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a><span data-ttu-id="453be-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="453be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453be-108">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="453be-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453be-109">Ссылка на класс [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину, для которой необходимо получить сведения о совместимости.</span><span class="sxs-lookup"><span data-stu-id="453be-109">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to retrieve compatibility information for.</span></span> <span data-ttu-id="453be-110">Если этот параметр относится к системе компьютера размещения, то данные, возвращаемые в параметре *компатибилитинфо* , можно использовать, чтобы определить, можно ли быстро перенести любую из виртуальных машин на компьютере, на котором размещен компьютер, в другую систему.</span><span class="sxs-lookup"><span data-stu-id="453be-110">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityInfo* parameter can be used to determine whether any of the virtual machines on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="453be-111">*Компатибилитинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="453be-111">*CompatibilityInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="453be-112">Непрозрачный большой двоичный объект данных, который может быть передан методу [**чекксистемкомпатибилитинфо**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) на другом компьютере компьютера для подтверждения совместимости.</span><span class="sxs-lookup"><span data-stu-id="453be-112">An opaque blob of data that can be passed to the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on another hosting computer system to confirm compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="453be-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="453be-113">Return value</span></span>

<span data-ttu-id="453be-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="453be-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="453be-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="453be-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="453be-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="453be-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="453be-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="453be-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="453be-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="453be-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="453be-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="453be-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="453be-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="453be-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="453be-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="453be-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="453be-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="453be-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="453be-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="453be-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="453be-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="453be-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="453be-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="453be-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="453be-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="453be-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="453be-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="453be-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="453be-128">Требования</span><span class="sxs-lookup"><span data-stu-id="453be-128">Requirements</span></span>



| <span data-ttu-id="453be-129">Требование</span><span class="sxs-lookup"><span data-stu-id="453be-129">Requirement</span></span> | <span data-ttu-id="453be-130">Значение</span><span class="sxs-lookup"><span data-stu-id="453be-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="453be-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="453be-131">Minimum supported client</span></span><br/> | <span data-ttu-id="453be-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="453be-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="453be-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="453be-133">Minimum supported server</span></span><br/> | <span data-ttu-id="453be-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="453be-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="453be-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="453be-135">Namespace</span></span><br/>                | <span data-ttu-id="453be-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="453be-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="453be-137">MOF</span><span class="sxs-lookup"><span data-stu-id="453be-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="453be-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="453be-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="453be-139">DLL</span><span class="sxs-lookup"><span data-stu-id="453be-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="453be-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="453be-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="453be-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="453be-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="453be-142">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="453be-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




