---
title: Метод Сетвиртуалдесктопстате класса Win32_RDMSVirtualDesktop
description: Обновляет состояние виртуального рабочего стола.
ms.assetid: 8f4f3d31-0434-4018-a33a-2ffd62c09669
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуалдесктопстате
- Службы удаленных рабочих столов метода Сетвиртуалдесктопстате, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Сетвиртуалдесктопстате
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af913e29857a59cacf283bff6a1642e0ea4cef9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672711"
---
# <a name="setvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="b2eb4-106">Метод Сетвиртуалдесктопстате \_ класса Win32 рдмсвиртуалдесктоп</span><span class="sxs-lookup"><span data-stu-id="b2eb4-106">SetVirtualDesktopState method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="b2eb4-107">Обновляет состояние виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-107">Updates the state of the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2eb4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2eb4-108">Syntax</span></span>


```mof
uint32 SetVirtualDesktopState(
  [in] uint32 VMState
);
```



## <a name="parameters"></a><span data-ttu-id="b2eb4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2eb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2eb4-110">*VMState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2eb4-110">*VMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2eb4-111">Значение, указывающее новое состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-111">A value that specifies the new state of the virtual machine.</span></span>

<span data-ttu-id="b2eb4-112">Для этого параметра может быть задано одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b2eb4-112">This parameter can bet set to one of the following values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b2eb4-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0 (по умолчанию))</span><span class="sxs-lookup"><span data-stu-id="b2eb4-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Default))</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-114">Не удалось определить состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-114">The state of the virtual machine could not be determined.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b2eb4-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-116">Виртуальная машина запущена.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-116">The virtual machine is running.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b2eb4-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-118">Виртуальная машина отключена.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-118">The virtual machine is turned off.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b2eb4-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (32768)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-120">Виртуальная машина приостановлена.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-120">The virtual machine is paused.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="b2eb4-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (32769)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-122">Виртуальная машина находится в сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-122">The virtual machine is in a saved state.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b2eb4-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (32770)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-124">Виртуальная машина запускается.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-124">The virtual machine is starting.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="b2eb4-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Сохранение** (32773)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-126">Виртуальная машина сохраняет свое состояние.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-126">The virtual machine is saving its state.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b2eb4-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (32774)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (32774)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-128">Виртуальная машина отключается.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-128">The virtual machine is turning off.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="b2eb4-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Приостановка** (32776)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-130">Виртуальная машина приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-130">The virtual machine is pausing.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="b2eb4-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Возобновление** (32777)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="b2eb4-132">Виртуальная машина возобновляет работу из приостановленного состояния.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-132">The virtual machine is resuming from a paused state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2eb4-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2eb4-133">Return value</span></span>

<span data-ttu-id="b2eb4-134">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-134">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2eb4-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b2eb4-135">Requirements</span></span>



| <span data-ttu-id="b2eb4-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b2eb4-136">Requirement</span></span> | <span data-ttu-id="b2eb4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b2eb4-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2eb4-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2eb4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b2eb4-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b2eb4-139">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b2eb4-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2eb4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b2eb4-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2eb4-141">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b2eb4-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b2eb4-142">Namespace</span></span><br/>                | <span data-ttu-id="b2eb4-143">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="b2eb4-143">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b2eb4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="b2eb4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2eb4-145"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2eb4-145"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2eb4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b2eb4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2eb4-147"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2eb4-147"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b2eb4-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2eb4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2eb4-149">**\_Рдмсвиртуалдесктоп Win32**</span><span class="sxs-lookup"><span data-stu-id="b2eb4-149">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





