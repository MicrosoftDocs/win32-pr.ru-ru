---
description: Запускает отладчик, зарегистрированный в данный момент для этого процесса.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Метод Аттачдебугжер класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895537"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a><span data-ttu-id="fd27b-103">Метод Аттачдебугжер \_ класса процесса Win32</span><span class="sxs-lookup"><span data-stu-id="fd27b-103">AttachDebugger method of the Win32\_Process class</span></span>

<span data-ttu-id="fd27b-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) аттачдебугжер запускает отладчик, который в настоящее время зарегистрирован для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="fd27b-104">The **AttachDebugger** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method starts the debugger that is currently registered for this process.</span></span>

<span data-ttu-id="fd27b-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="fd27b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fd27b-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fd27b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd27b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd27b-107">Syntax</span></span>


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a><span data-ttu-id="fd27b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd27b-108">Parameters</span></span>

<span data-ttu-id="fd27b-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fd27b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd27b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd27b-110">Return value</span></span>

<span data-ttu-id="fd27b-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="fd27b-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="fd27b-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fd27b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fd27b-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fd27b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fd27b-114">**Успешное завершение**</span><span class="sxs-lookup"><span data-stu-id="fd27b-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="fd27b-115">0</span><span class="sxs-lookup"><span data-stu-id="fd27b-115">0</span></span>

<span data-ttu-id="fd27b-116">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="fd27b-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="fd27b-117">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="fd27b-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="fd27b-118">2</span><span class="sxs-lookup"><span data-stu-id="fd27b-118">2</span></span>

<span data-ttu-id="fd27b-119">У пользователя нет доступа к запрошенной информации.</span><span class="sxs-lookup"><span data-stu-id="fd27b-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="fd27b-120">**Недостаточно прав доступа**</span><span class="sxs-lookup"><span data-stu-id="fd27b-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="fd27b-121">3</span><span class="sxs-lookup"><span data-stu-id="fd27b-121">3</span></span>

<span data-ttu-id="fd27b-122">У пользователя недостаточно прав.</span><span class="sxs-lookup"><span data-stu-id="fd27b-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="fd27b-123">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="fd27b-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="fd27b-124">8</span><span class="sxs-lookup"><span data-stu-id="fd27b-124">8</span></span>

<span data-ttu-id="fd27b-125">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="fd27b-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="fd27b-126">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="fd27b-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="fd27b-127">9</span><span class="sxs-lookup"><span data-stu-id="fd27b-127">9</span></span>

<span data-ttu-id="fd27b-128">Указанный путь не существует.</span><span class="sxs-lookup"><span data-stu-id="fd27b-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="fd27b-129">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="fd27b-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fd27b-130">21</span><span class="sxs-lookup"><span data-stu-id="fd27b-130">21</span></span>

<span data-ttu-id="fd27b-131">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="fd27b-131">The specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fd27b-132">**Другое**</span><span class="sxs-lookup"><span data-stu-id="fd27b-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fd27b-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="fd27b-133">22 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd27b-134">Требования</span><span class="sxs-lookup"><span data-stu-id="fd27b-134">Requirements</span></span>



| <span data-ttu-id="fd27b-135">Требование</span><span class="sxs-lookup"><span data-stu-id="fd27b-135">Requirement</span></span> | <span data-ttu-id="fd27b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="fd27b-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd27b-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd27b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fd27b-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd27b-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd27b-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd27b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fd27b-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd27b-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd27b-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fd27b-141">Namespace</span></span><br/>                | <span data-ttu-id="fd27b-142">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fd27b-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd27b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fd27b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd27b-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd27b-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd27b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fd27b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd27b-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd27b-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd27b-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd27b-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd27b-148">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd27b-148">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fd27b-149">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="fd27b-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

