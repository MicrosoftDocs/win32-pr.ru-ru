---
description: Получает текущий размер (в байтах) свободного виртуального адресного пространства, доступного процессу.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Метод Жетаваилаблевиртуалсизе класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655796"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a><span data-ttu-id="fbbb4-103">Метод Жетаваилаблевиртуалсизе \_ класса процесса Win32</span><span class="sxs-lookup"><span data-stu-id="fbbb4-103">GetAvailableVirtualSize method of the Win32\_Process class</span></span>

<span data-ttu-id="fbbb4-104">Получает текущий размер (в байтах) свободного виртуального адресного пространства, доступного процессу.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-104">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbbb4-105">Syntax</span></span>


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a><span data-ttu-id="fbbb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbbb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbbb4-107">*Аваилаблевиртуалсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fbbb4-107">*AvailableVirtualSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-108">Параметр *аваилаблевиртуалсизе* возвращает свободное пространство виртуального адреса, доступное для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-108">The *AvailableVirtualSize* parameter returns the free virtual address space available to this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbbb4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbbb4-109">Return value</span></span>

<span data-ttu-id="fbbb4-110">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-110">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="fbbb4-111">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-111">Any other number indicates an error.</span></span> <span data-ttu-id="fbbb4-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fbbb4-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fbbb4-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fbbb4-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fbbb4-114">**Успешное завершение**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-115">0</span><span class="sxs-lookup"><span data-stu-id="fbbb4-115">0</span></span>

<span data-ttu-id="fbbb4-116">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-116">The operation completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="fbbb4-117">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-118">2</span><span class="sxs-lookup"><span data-stu-id="fbbb4-118">2</span></span>

<span data-ttu-id="fbbb4-119">У пользователя нет доступа к запрошенной информации</span><span class="sxs-lookup"><span data-stu-id="fbbb4-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="fbbb4-120">**Недостаточно прав доступа**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-121">3</span><span class="sxs-lookup"><span data-stu-id="fbbb4-121">3</span></span>

<span data-ttu-id="fbbb4-122">У пользователя недостаточно прав.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="fbbb4-123">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-124">8</span><span class="sxs-lookup"><span data-stu-id="fbbb4-124">8</span></span>

<span data-ttu-id="fbbb4-125">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="fbbb4-126">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-127">9</span><span class="sxs-lookup"><span data-stu-id="fbbb4-127">9</span></span>

<span data-ttu-id="fbbb4-128">Указанный путь не существует.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="fbbb4-129">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-130">21</span><span class="sxs-lookup"><span data-stu-id="fbbb4-130">21</span></span>

<span data-ttu-id="fbbb4-131">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="fbbb4-131">The specified parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="fbbb4-132">**Другое**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fbbb4-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="fbbb4-133">22 4294967295</span></span>

<span data-ttu-id="fbbb4-134">Для значений, отличных от перечисленных, см. документацию по [кодам системных ошибок](/windows/desktop/Debug/system-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="fbbb4-134">For values other than those listed, refer to the [System Error Codes](/windows/desktop/Debug/system-error-codes) documentation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbbb4-135">Требования</span><span class="sxs-lookup"><span data-stu-id="fbbb4-135">Requirements</span></span>



| <span data-ttu-id="fbbb4-136">Требование</span><span class="sxs-lookup"><span data-stu-id="fbbb4-136">Requirement</span></span> | <span data-ttu-id="fbbb4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="fbbb4-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbb4-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbbb4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbb4-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fbbb4-139">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="fbbb4-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbbb4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbb4-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fbbb4-141">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="fbbb4-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fbbb4-142">Namespace</span></span><br/>                | <span data-ttu-id="fbbb4-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fbbb4-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fbbb4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="fbbb4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbbb4-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbbb4-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbbb4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fbbb4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbbb4-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbbb4-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbbb4-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbbb4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbb4-149">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

