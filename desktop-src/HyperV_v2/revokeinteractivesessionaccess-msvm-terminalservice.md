---
description: Отменяет доступ к интерактивному сеансу виртуальной машины из указанного списка доверенных лиц.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Метод Ревокеинтерактивесессионакцесс класса Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813689"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="d0ddc-103">Метод Ревокеинтерактивесессионакцесс \_ класса Терминалсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="d0ddc-103">RevokeInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="d0ddc-104">Отменяет доступ к интерактивному сеансу виртуальной машины из указанного списка доверенных лиц.</span><span class="sxs-lookup"><span data-stu-id="d0ddc-104">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ddc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0ddc-105">Syntax</span></span>


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d0ddc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0ddc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ddc-107">*ComputerSystem* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0ddc-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ddc-108">Ссылка на экземпляр класса платформы [**CIM \_**](cim-computersystem.md) , представляющий виртуальную машину, к которой будет отозван доступ.</span><span class="sxs-lookup"><span data-stu-id="d0ddc-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to which access will be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="d0ddc-109">*Доверенные лица* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0ddc-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ddc-110">Массив строк, каждый из которых определяет доверенное лицо, права доступа которого будут отозваны.</span><span class="sxs-lookup"><span data-stu-id="d0ddc-110">An array of strings, each identifying a trustee whose access rights will be revoked.</span></span> <span data-ttu-id="d0ddc-111">Идентификаторы доверенного лица должны быть указаны в формате, совместимом с Windows SAM, или в формате строки идентификатора безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="d0ddc-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="d0ddc-112">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d0ddc-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ddc-113">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d0ddc-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ddc-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0ddc-114">Return value</span></span>

<span data-ttu-id="d0ddc-115">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d0ddc-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d0ddc-116">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-117">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-118">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-119">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-120">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-121">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-122">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-125">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d0ddc-126">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="d0ddc-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d0ddc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d0ddc-127">Requirements</span></span>



| <span data-ttu-id="d0ddc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d0ddc-128">Requirement</span></span> | <span data-ttu-id="d0ddc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d0ddc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ddc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0ddc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ddc-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d0ddc-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d0ddc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0ddc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ddc-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d0ddc-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d0ddc-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d0ddc-134">Namespace</span></span><br/>                | <span data-ttu-id="d0ddc-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d0ddc-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d0ddc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d0ddc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0ddc-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0ddc-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0ddc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d0ddc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0ddc-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d0ddc-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d0ddc-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0ddc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ddc-141">**Мсвм \_ терминалсервице**</span><span class="sxs-lookup"><span data-stu-id="d0ddc-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

