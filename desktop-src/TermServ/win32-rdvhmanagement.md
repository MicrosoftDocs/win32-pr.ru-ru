---
title: Класс Win32_RdvhManagement
description: Описание службы управления удаленный рабочий стол виртуального узла (РДВХ).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Класс Win32_RdvhManagement службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RdvhManagement, описание
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672675"
---
# <a name="win32_rdvhmanagement-class"></a><span data-ttu-id="2c1ba-105">\_Класс Win32 рдвхманажемент</span><span class="sxs-lookup"><span data-stu-id="2c1ba-105">Win32\_RdvhManagement class</span></span>

<span data-ttu-id="2c1ba-106">Описание службы управления удаленный рабочий стол виртуального узла (РДВХ).</span><span class="sxs-lookup"><span data-stu-id="2c1ba-106">Describes a Remote Desktop Virtual Host (RDVH) management service.</span></span>

<span data-ttu-id="2c1ba-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1ba-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c1ba-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a><span data-ttu-id="2c1ba-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2c1ba-109">Members</span></span>

<span data-ttu-id="2c1ba-110">Класс **Win32 \_ рдвхманажемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2c1ba-110">The **Win32\_RdvhManagement** class has these types of members:</span></span>

-   [<span data-ttu-id="2c1ba-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2c1ba-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2c1ba-112">Методы</span><span class="sxs-lookup"><span data-stu-id="2c1ba-112">Methods</span></span>

<span data-ttu-id="2c1ba-113">Класс **Win32 \_ рдвхманажемент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-113">The **Win32\_RdvhManagement** class has these methods.</span></span>



| <span data-ttu-id="2c1ba-114">Метод</span><span class="sxs-lookup"><span data-stu-id="2c1ba-114">Method</span></span>                                                                                  | <span data-ttu-id="2c1ba-115">Описание</span><span class="sxs-lookup"><span data-stu-id="2c1ba-115">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c1ba-116">**рдвкреатеусердисктемплате**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-116">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="2c1ba-117">Создает пользовательский шаблон диска с указанным максимальным размером и в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-117">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="2c1ba-118">Все созданные диски пользователей будут иметь максимальные размеры, соответствующие максимальному размеру шаблона.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-118">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="2c1ba-119">**рдвмигратевмтодифференсост**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-119">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="2c1ba-120">Инициирует динамическую миграцию виртуальной машины в сценариях VDI.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-120">Initiates a live migration of virtual machine in VDI scenarios</span></span><br/>                                                                                               |
| [<span data-ttu-id="2c1ba-121">**рдвкопибасевмлокалли**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-121">**RdvCopyBaseVmLocally**</span></span>](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | <span data-ttu-id="2c1ba-122">Локальное копирование расположения базовой виртуальной машины в Узел RDV Server</span><span class="sxs-lookup"><span data-stu-id="2c1ba-122">Copies Base VM location locally to RDV Host server</span></span><br/>                                                                                                           |
| [<span data-ttu-id="2c1ba-123">**рдвкреатеусердисктемплате**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-123">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="2c1ba-124">Создает пользовательский шаблон диска с указанным максимальным размером и в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-124">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="2c1ba-125">Все созданные диски пользователей будут иметь максимальные размеры, соответствующие максимальному размеру шаблона.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-125">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="2c1ba-126">**рдвмигратевмтодифференсост**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-126">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="2c1ba-127">Инициирует динамическую миграцию виртуальной машины в сценариях VDI.</span><span class="sxs-lookup"><span data-stu-id="2c1ba-127">Initiates a live migration of virtual machine in VDI scenarios.</span></span><br/>                                                                                              |
| [<span data-ttu-id="2c1ba-128">**рдвсетупвмпермиссионс**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-128">**RdvSetupVMPermissions**</span></span>](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | <span data-ttu-id="2c1ba-129">Задает разрешения в виртуальной машине для вызывающего объекта</span><span class="sxs-lookup"><span data-stu-id="2c1ba-129">Sets permissions in VM for the caller</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="2c1ba-130">**рдвундовмпермиссионс**</span><span class="sxs-lookup"><span data-stu-id="2c1ba-130">**RdvUndoVMPermissions**</span></span>](rdvundovmpermissions-win32-rdvhmanagement.md)               | <span data-ttu-id="2c1ba-131">Отмена разрешений в наборе виртуальных машин с помощью Рдвсетупвмпермиссионс</span><span class="sxs-lookup"><span data-stu-id="2c1ba-131">Reverts permissions in VM set by RdvSetupVMPermissions</span></span><br/>                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="2c1ba-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2c1ba-132">Requirements</span></span>



| <span data-ttu-id="2c1ba-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2c1ba-133">Requirement</span></span> | <span data-ttu-id="2c1ba-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2c1ba-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1ba-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c1ba-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2c1ba-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2c1ba-136">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="2c1ba-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c1ba-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2c1ba-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c1ba-138">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="2c1ba-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2c1ba-139">Namespace</span></span><br/>                | <span data-ttu-id="2c1ba-140">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="2c1ba-140">Root\\cimv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="2c1ba-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2c1ba-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c1ba-142"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ba-142"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2c1ba-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2c1ba-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c1ba-144"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ba-144"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





