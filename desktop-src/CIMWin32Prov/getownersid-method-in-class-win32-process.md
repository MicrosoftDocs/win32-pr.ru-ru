---
description: Жетовнерсид&\# 8194; Метод класса WMI получает идентификатор безопасности (SID) для владельца этого процесса.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Метод Жетовнерсид класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655790"
---
# <a name="getownersid-method-of-the-win32_process-class"></a><span data-ttu-id="d81c6-103">Метод Жетовнерсид \_ класса процесса Win32</span><span class="sxs-lookup"><span data-stu-id="d81c6-103">GetOwnerSid method of the Win32\_Process class</span></span>

<span data-ttu-id="d81c6-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) жетовнерсид ИЗВЛЕКАЕТ идентификатор безопасности (SID) для владельца этого процесса.</span><span class="sxs-lookup"><span data-stu-id="d81c6-104">The **GetOwnerSid** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the security identifier (SID) for the owner of this process.</span></span>

<span data-ttu-id="d81c6-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d81c6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d81c6-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d81c6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d81c6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d81c6-107">Syntax</span></span>


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a><span data-ttu-id="d81c6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d81c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d81c6-109">*Идентификатор безопасности* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d81c6-109">*Sid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d81c6-110">Возвращает дескриптор идентификатора безопасности для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="d81c6-110">Returns the security identifier descriptor for this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d81c6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d81c6-111">Return value</span></span>

<span data-ttu-id="d81c6-112">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="d81c6-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="d81c6-113">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d81c6-113">Any other number indicates an error.</span></span> <span data-ttu-id="d81c6-114">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d81c6-114">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d81c6-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d81c6-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d81c6-116">**Успешное завершение** (0)</span><span class="sxs-lookup"><span data-stu-id="d81c6-116">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d81c6-117">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="d81c6-117">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d81c6-118">**Недостаточно прав доступа** (3)</span><span class="sxs-lookup"><span data-stu-id="d81c6-118">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d81c6-119">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="d81c6-119">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d81c6-120">**Путь не найден** (9)</span><span class="sxs-lookup"><span data-stu-id="d81c6-120">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d81c6-121">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="d81c6-121">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="d81c6-122">**Другие** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="d81c6-122">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="d81c6-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="d81c6-123">Examples</span></span>

<span data-ttu-id="d81c6-124">Пример кода PowerShell для [поиска пользователей, вошедших в систему на удаленном компьютере с версией 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) , запрашивает удаленные компьютеры, чтобы узнать, кто вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="d81c6-124">The [Find the logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell code example queries remote machines to see who is logged on.</span></span>

## <a name="requirements"></a><span data-ttu-id="d81c6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d81c6-125">Requirements</span></span>



| <span data-ttu-id="d81c6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d81c6-126">Requirement</span></span> | <span data-ttu-id="d81c6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d81c6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d81c6-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d81c6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d81c6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d81c6-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d81c6-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d81c6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d81c6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d81c6-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d81c6-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d81c6-132">Namespace</span></span><br/>                | <span data-ttu-id="d81c6-133">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d81c6-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d81c6-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d81c6-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d81c6-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d81c6-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d81c6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d81c6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d81c6-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d81c6-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d81c6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d81c6-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="d81c6-139">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d81c6-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d81c6-140">**\_Процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="d81c6-140">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

