---
description: Удаление&\# 8194; Метод класса WMI удаляет запланированное задание.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Метод Delete класса Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142916"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="da8e3-103">Метод DELETE \_ класса ScheduledJob Win32</span><span class="sxs-lookup"><span data-stu-id="da8e3-103">Delete method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="da8e3-104">Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет запланированное задание.</span><span class="sxs-lookup"><span data-stu-id="da8e3-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a scheduled job.</span></span>

<span data-ttu-id="da8e3-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="da8e3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da8e3-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="da8e3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da8e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da8e3-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="da8e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="da8e3-108">Parameters</span></span>

<span data-ttu-id="da8e3-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="da8e3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da8e3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da8e3-110">Return value</span></span>

<span data-ttu-id="da8e3-111">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="da8e3-111">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="da8e3-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="da8e3-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="da8e3-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="da8e3-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="da8e3-114">**Успешное завершение**</span><span class="sxs-lookup"><span data-stu-id="da8e3-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-115">0</span><span class="sxs-lookup"><span data-stu-id="da8e3-115">0</span></span>

<span data-ttu-id="da8e3-116">Запрос принят.</span><span class="sxs-lookup"><span data-stu-id="da8e3-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="da8e3-117">**Не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="da8e3-117">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-118">1</span><span class="sxs-lookup"><span data-stu-id="da8e3-118">1</span></span>

<span data-ttu-id="da8e3-119">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="da8e3-119">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="da8e3-120">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="da8e3-120">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-121">2</span><span class="sxs-lookup"><span data-stu-id="da8e3-121">2</span></span>

<span data-ttu-id="da8e3-122">У пользователя нет необходимых прав доступа.</span><span class="sxs-lookup"><span data-stu-id="da8e3-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="da8e3-123">**Неизвестный сбой**</span><span class="sxs-lookup"><span data-stu-id="da8e3-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-124">8</span><span class="sxs-lookup"><span data-stu-id="da8e3-124">8</span></span>

<span data-ttu-id="da8e3-125">Интерактивный процесс.</span><span class="sxs-lookup"><span data-stu-id="da8e3-125">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="da8e3-126">**Путь не найден**</span><span class="sxs-lookup"><span data-stu-id="da8e3-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-127">9</span><span class="sxs-lookup"><span data-stu-id="da8e3-127">9</span></span>

<span data-ttu-id="da8e3-128">Не найден путь к каталогу исполняемого файла службы.</span><span class="sxs-lookup"><span data-stu-id="da8e3-128">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="da8e3-129">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="da8e3-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-130">21</span><span class="sxs-lookup"><span data-stu-id="da8e3-130">21</span></span>

<span data-ttu-id="da8e3-131">Службе переданы недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="da8e3-131">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="da8e3-132">**Служба не запущена**</span><span class="sxs-lookup"><span data-stu-id="da8e3-132">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-133">22</span><span class="sxs-lookup"><span data-stu-id="da8e3-133">22</span></span>

<span data-ttu-id="da8e3-134">Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.</span><span class="sxs-lookup"><span data-stu-id="da8e3-134">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="da8e3-135">**Другое**</span><span class="sxs-lookup"><span data-stu-id="da8e3-135">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="da8e3-136">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="da8e3-136">23 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da8e3-137">Требования</span><span class="sxs-lookup"><span data-stu-id="da8e3-137">Requirements</span></span>



| <span data-ttu-id="da8e3-138">Требование</span><span class="sxs-lookup"><span data-stu-id="da8e3-138">Requirement</span></span> | <span data-ttu-id="da8e3-139">Значение</span><span class="sxs-lookup"><span data-stu-id="da8e3-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da8e3-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da8e3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="da8e3-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da8e3-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da8e3-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da8e3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="da8e3-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da8e3-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da8e3-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="da8e3-144">Namespace</span></span><br/>                | <span data-ttu-id="da8e3-145">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="da8e3-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da8e3-146">MOF</span><span class="sxs-lookup"><span data-stu-id="da8e3-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da8e3-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da8e3-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da8e3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="da8e3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da8e3-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da8e3-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8e3-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da8e3-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="da8e3-151">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da8e3-151">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="da8e3-152">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="da8e3-152">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

