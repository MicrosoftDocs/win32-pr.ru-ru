---
description: Сетдатетиме&\# 8194; Метод класса WMI задает текущее системное время на компьютере.
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Метод Сетдатетиме класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655706"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="6e1ec-103">Метод Сетдатетиме \_ класса операционной системы Win32</span><span class="sxs-lookup"><span data-stu-id="6e1ec-103">SetDateTime method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="6e1ec-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сетдатетиме задает текущее системное время на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6e1ec-104">The **SetDateTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the current system time on the computer.</span></span>

<span data-ttu-id="6e1ec-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="6e1ec-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6e1ec-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6e1ec-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1ec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e1ec-107">Syntax</span></span>


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a><span data-ttu-id="6e1ec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e1ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e1ec-109">*LocalDatetime* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e1ec-109">*LocalDatetime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e1ec-110">Значение текущего времени.</span><span class="sxs-lookup"><span data-stu-id="6e1ec-110">Value of the current time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e1ec-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e1ec-111">Return value</span></span>

<span data-ttu-id="6e1ec-112">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="6e1ec-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="6e1ec-113">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e1ec-113">Any other number indicates an error.</span></span> <span data-ttu-id="6e1ec-114">Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6e1ec-114">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6e1ec-115">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6e1ec-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6e1ec-116">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="6e1ec-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e1ec-117">**Другие** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="6e1ec-117">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6e1ec-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e1ec-118">Remarks</span></span>

<span data-ttu-id="6e1ec-119">Вызывающий процесс должен иметь \_ \_ привилегию SE для имен SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="6e1ec-119">The calling process must have the SE\_SYSTEMTIME\_NAME privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1ec-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6e1ec-120">Requirements</span></span>



| <span data-ttu-id="6e1ec-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6e1ec-121">Requirement</span></span> | <span data-ttu-id="6e1ec-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6e1ec-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1ec-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e1ec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1ec-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e1ec-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e1ec-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e1ec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1ec-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e1ec-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e1ec-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e1ec-127">Namespace</span></span><br/>                | <span data-ttu-id="6e1ec-128">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6e1ec-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e1ec-129">MOF</span><span class="sxs-lookup"><span data-stu-id="6e1ec-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e1ec-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e1ec-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e1ec-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6e1ec-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e1ec-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1ec-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e1ec-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e1ec-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e1ec-134">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e1ec-134">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6e1ec-135">**Win32, \_ Операционная система**</span><span class="sxs-lookup"><span data-stu-id="6e1ec-135">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="6e1ec-136">Задачи WMI: управление рабочим столом</span><span class="sxs-lookup"><span data-stu-id="6e1ec-136">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

