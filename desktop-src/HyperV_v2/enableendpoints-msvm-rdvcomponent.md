---
description: Запрашивает службы удаленных рабочих столов виртуальное устройство для запуска канала подключения к виртуальной машине.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Метод Енаблиндпоинтс класса Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263226"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a><span data-ttu-id="6222a-103">Метод Енаблиндпоинтс \_ класса Рдвкомпонент мсвм</span><span class="sxs-lookup"><span data-stu-id="6222a-103">EnableEndPoints method of the Msvm\_RdvComponent class</span></span>

<span data-ttu-id="6222a-104">Запрашивает службы удаленных рабочих столов виртуальное устройство для запуска канала подключения к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6222a-104">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6222a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6222a-105">Syntax</span></span>


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a><span data-ttu-id="6222a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6222a-106">Parameters</span></span>

<span data-ttu-id="6222a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6222a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6222a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6222a-108">Return value</span></span>

<span data-ttu-id="6222a-109">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6222a-109">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6222a-110">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="6222a-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-111">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="6222a-111">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-112">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="6222a-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-113">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="6222a-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-114">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="6222a-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-115">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="6222a-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-116">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="6222a-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-117">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="6222a-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-118">**Недостаточно памяти** (32774)</span><span class="sxs-lookup"><span data-stu-id="6222a-118">**Out of memory** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6222a-119">**Файл не найден** (32775)</span><span class="sxs-lookup"><span data-stu-id="6222a-119">**File not found** (32775)</span></span>
</dt> <dt>

 <span data-ttu-id="6222a-120">(32776)</span><span class="sxs-lookup"><span data-stu-id="6222a-120">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="6222a-121">(32777)</span><span class="sxs-lookup"><span data-stu-id="6222a-121">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="6222a-122">(32778)</span><span class="sxs-lookup"><span data-stu-id="6222a-122">(32778)</span></span>
</dt> <dt>

 <span data-ttu-id="6222a-123">(32779)</span><span class="sxs-lookup"><span data-stu-id="6222a-123">(32779)</span></span>
</dt> <dt>

 <span data-ttu-id="6222a-124">(32780)</span><span class="sxs-lookup"><span data-stu-id="6222a-124">(32780)</span></span>
</dt> <dt>

 <span data-ttu-id="6222a-125">(32781)</span><span class="sxs-lookup"><span data-stu-id="6222a-125">(32781)</span></span>
</dt> <dt>

 <span data-ttu-id="6222a-126">(32782)</span><span class="sxs-lookup"><span data-stu-id="6222a-126">(32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6222a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6222a-127">Requirements</span></span>



| <span data-ttu-id="6222a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6222a-128">Requirement</span></span> | <span data-ttu-id="6222a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6222a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6222a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6222a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6222a-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6222a-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6222a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6222a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6222a-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6222a-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6222a-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6222a-134">Namespace</span></span><br/>                | <span data-ttu-id="6222a-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6222a-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6222a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6222a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6222a-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6222a-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6222a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6222a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6222a-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6222a-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6222a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6222a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6222a-141">**Мсвм \_ рдвкомпонент**</span><span class="sxs-lookup"><span data-stu-id="6222a-141">**Msvm\_RdvComponent**</span></span>](msvm-rdvcomponent.md)
</dt> </dl>

 

 




