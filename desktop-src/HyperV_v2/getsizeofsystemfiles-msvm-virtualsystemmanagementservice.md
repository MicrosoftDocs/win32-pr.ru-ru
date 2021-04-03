---
description: Получает общий размер системных файлов виртуальной машины.
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Метод Жетсизеофсистемфилес класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9fcf93093e17c2989121bf33ee5f5fbf09bab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810313"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="47f3e-103">Метод Жетсизеофсистемфилес \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="47f3e-103">GetSizeOfSystemFiles method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="47f3e-104">Получает общий размер системных файлов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="47f3e-104">Retrieves the total size of the system files of virtual machine.</span></span> <span data-ttu-id="47f3e-105">К ним относятся файлы конфигурации и сохраненного состояния.</span><span class="sxs-lookup"><span data-stu-id="47f3e-105">These include the configuration and saved state files.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f3e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47f3e-106">Syntax</span></span>


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a><span data-ttu-id="47f3e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="47f3e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f3e-108">*ВССД* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="47f3e-108">*Vssd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f3e-109">Ссылка на экземпляр [**\_ виртуалсистемсеттингдата CIM**](/previous-versions//cc136954(v=vs.85)) , для которого необходимо получить размер системных файлов.</span><span class="sxs-lookup"><span data-stu-id="47f3e-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose system files size are to be retrieved.</span></span> <span data-ttu-id="47f3e-110">Этот экземпляр может представлять либо текущий экземпляр виртуальной машины, либо экземпляр моментального снимка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="47f3e-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="47f3e-111">*Размер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="47f3e-111">*Size* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f3e-112">Общий размер системных файлов (в байтах).</span><span class="sxs-lookup"><span data-stu-id="47f3e-112">The total size, in bytes, of system files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f3e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47f3e-113">Return value</span></span>

<span data-ttu-id="47f3e-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="47f3e-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="47f3e-115">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="47f3e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-116">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="47f3e-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-117">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="47f3e-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-118">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="47f3e-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-119">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="47f3e-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-120">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="47f3e-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-121">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="47f3e-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-122">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="47f3e-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-123">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="47f3e-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-124">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="47f3e-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-125">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="47f3e-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-126">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="47f3e-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="47f3e-127">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="47f3e-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="47f3e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="47f3e-128">Requirements</span></span>



| <span data-ttu-id="47f3e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="47f3e-129">Requirement</span></span> | <span data-ttu-id="47f3e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="47f3e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f3e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47f3e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="47f3e-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="47f3e-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="47f3e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47f3e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="47f3e-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="47f3e-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47f3e-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="47f3e-135">Namespace</span></span><br/>                | <span data-ttu-id="47f3e-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="47f3e-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="47f3e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="47f3e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47f3e-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47f3e-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47f3e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="47f3e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f3e-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47f3e-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47f3e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47f3e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f3e-142">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="47f3e-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

