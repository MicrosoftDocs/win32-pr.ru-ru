---
description: Проверяет сведения о совместимости для обеспечения совместимости с системой размещающего компьютера.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Метод Чекксистемкомпатибилитинфо класса Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896849"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="877cf-103">Метод Чекксистемкомпатибилитинфо \_ класса Виртуалсистеммигратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="877cf-103">CheckSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="877cf-104">Проверяет сведения о совместимости для обеспечения совместимости с системой размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="877cf-104">Checks the compatibility information for compatibility with the hosting computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="877cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="877cf-105">Syntax</span></span>


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a><span data-ttu-id="877cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="877cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="877cf-107">*Компатибилитинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="877cf-107">*CompatibilityInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="877cf-108">Большой двоичный объект данных, полученный путем вызова метода [**жетсистемкомпатибилитинфо**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) в системе размещающего компьютера.</span><span class="sxs-lookup"><span data-stu-id="877cf-108">A blob of data obtained by calling the [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="877cf-109">*Причины* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="877cf-109">*Reasons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="877cf-110">Массив строк, получающих внедренные экземпляры класса [**\_ ошибок мсвм**](msvm-error.md) , которые представляют все предупреждения или ошибки.</span><span class="sxs-lookup"><span data-stu-id="877cf-110">An array of strings that receives the embedded instances of the [**Msvm\_Error**](msvm-error.md) class that represent any warnings or errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="877cf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="877cf-111">Return value</span></span>

<span data-ttu-id="877cf-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="877cf-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="877cf-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="877cf-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="877cf-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="877cf-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="877cf-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="877cf-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="877cf-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="877cf-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="877cf-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="877cf-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="877cf-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="877cf-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="877cf-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="877cf-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="877cf-126">**Не совместимо** (32784)</span><span class="sxs-lookup"><span data-stu-id="877cf-126">**Not compatible** (32784)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="877cf-127">Требования</span><span class="sxs-lookup"><span data-stu-id="877cf-127">Requirements</span></span>



| <span data-ttu-id="877cf-128">Требование</span><span class="sxs-lookup"><span data-stu-id="877cf-128">Requirement</span></span> | <span data-ttu-id="877cf-129">Значение</span><span class="sxs-lookup"><span data-stu-id="877cf-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="877cf-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="877cf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="877cf-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="877cf-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="877cf-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="877cf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="877cf-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="877cf-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="877cf-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="877cf-134">Namespace</span></span><br/>                | <span data-ttu-id="877cf-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="877cf-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="877cf-136">MOF</span><span class="sxs-lookup"><span data-stu-id="877cf-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="877cf-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="877cf-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="877cf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="877cf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="877cf-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="877cf-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="877cf-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="877cf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="877cf-141">**Мсвм \_ виртуалсистеммигратионсервице**</span><span class="sxs-lookup"><span data-stu-id="877cf-141">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




