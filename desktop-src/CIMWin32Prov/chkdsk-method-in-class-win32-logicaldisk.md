---
description: Вызывает операцию chkdsk на диске.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Метод chkdsk класса Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142112"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="1ff6e-103">Метод chkdsk \_ класса LogicalDisk Win32</span><span class="sxs-lookup"><span data-stu-id="1ff6e-103">Chkdsk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="1ff6e-104">Метод экземпляра **chkdsk** вызывает операцию **chkdsk** на диске.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-104">The **Chkdsk** instance method invokes the **chkdsk** operation on the disk.</span></span>

<span data-ttu-id="1ff6e-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="1ff6e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1ff6e-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1ff6e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff6e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ff6e-107">Syntax</span></span>


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a><span data-ttu-id="1ff6e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ff6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff6e-109">*Фиксеррорс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff6e-109">*FixErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-110">Указывает, что следует сделать с ошибками, обнаруженными на диске.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-110">Indicates what should be done to errors found on the disk.</span></span> <span data-ttu-id="1ff6e-111">Если **значение равно true**, ошибки исправлены.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-111">If **true**, then errors are fixed.</span></span> <span data-ttu-id="1ff6e-112">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-112">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-113">*Вигораусиндексчекк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff6e-113">*VigorousIndexCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-114">Если **значение — true**, необходимо выполнить менее тщательные проверку записей индекса.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-114">If **true**, a less vigorous check of index entries should be performed.</span></span> <span data-ttu-id="1ff6e-115">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-115">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-116">*Скипфолдерцикле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff6e-116">*SkipFolderCycle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-117">Если **значение равно true**, проверка цикла папок должна быть пропущена.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-117">If **true**, the folder cycle checking should be skipped.</span></span> <span data-ttu-id="1ff6e-118">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-118">The default is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-119">*Форцедисмаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff6e-119">*ForceDismount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-120">Если **значение — true**, перед проверкой диск должен быть принудительно отключен.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-120">If **true**, the drive should be forced to dismount before checking.</span></span> <span data-ttu-id="1ff6e-121">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-121">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-122">*Рековербадсекторс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff6e-122">*RecoverBadSectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-123">Если **значение равно true**, то должны быть найдены поврежденные секторы и данные для чтения должны быть восстановлены из этих секторов.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-123">If **true**, the bad sectors should be located and the readable information should be recovered from these sectors.</span></span> <span data-ttu-id="1ff6e-124">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-124">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-125">*Окторунатбутуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ff6e-125">*OKToRunAtBootUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-126">Если **значение — true**, операция **chkdsk** должна выполняться при следующей загрузке, если операция не может быть выполнена, так как диск заблокирован во время вызова этого метода.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-126">If **true**, the **chkdsk** operation should be performed at next boot up time, in case the operation could not be performed because the disk is locked at time this method is called.</span></span> <span data-ttu-id="1ff6e-127">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-127">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff6e-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ff6e-128">Return value</span></span>

<span data-ttu-id="1ff6e-129">При успешном выполнении возвращает значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="1ff6e-129">Returns a value of 0 (zero) if successful.</span></span> <span data-ttu-id="1ff6e-130">Другие значения перечислены в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-130">Other values are listed in the following list.</span></span> <span data-ttu-id="1ff6e-131">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1ff6e-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1ff6e-132">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1ff6e-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1ff6e-133">**Успешно — Chkdsk завершена**</span><span class="sxs-lookup"><span data-stu-id="1ff6e-133">**Success - Chkdsk completed**</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-134">0</span><span class="sxs-lookup"><span data-stu-id="1ff6e-134">0</span></span>

<span data-ttu-id="1ff6e-135">Успешно — [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) завершена</span><span class="sxs-lookup"><span data-stu-id="1ff6e-135">Success - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) Completed</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-136">**Успешно — заблокировано и chkdsk запланировано при перезагрузке**</span><span class="sxs-lookup"><span data-stu-id="1ff6e-136">**Success - Locked and chkdsk scheduled on reboot**</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-137">1</span><span class="sxs-lookup"><span data-stu-id="1ff6e-137">1</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-138">**Сбой — неизвестная файловая система**</span><span class="sxs-lookup"><span data-stu-id="1ff6e-138">**Failure - Unknown file system**</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-139">2</span><span class="sxs-lookup"><span data-stu-id="1ff6e-139">2</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-140">**Сбой-неизвестная ошибка**</span><span class="sxs-lookup"><span data-stu-id="1ff6e-140">**Failure - Unknown error**</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-141">3</span><span class="sxs-lookup"><span data-stu-id="1ff6e-141">3</span></span>

</dd> <dt>

<span data-ttu-id="1ff6e-142">**Сбой-неподдерживаемая файловая система**</span><span class="sxs-lookup"><span data-stu-id="1ff6e-142">**Failure - Unsupported File System**</span></span>
</dt> <dd>

<span data-ttu-id="1ff6e-143">4</span><span class="sxs-lookup"><span data-stu-id="1ff6e-143">4</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ff6e-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ff6e-144">Remarks</span></span>

<span data-ttu-id="1ff6e-145">Этот метод применим только к тем экземплярам логического диска, которые представляют физический диск на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-145">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="1ff6e-146">Он неприменим к сопоставленным логическим дискам.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-146">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="1ff6e-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="1ff6e-147">Examples</span></span>

<span data-ttu-id="1ff6e-148">В образце кода PowerShell[для сервера выполняется](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) проверка удаленной системы и возвращается значение true или false, если установлен флаг chkdsk/f.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-148">The[Is CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell code sample examines the remote system and returns a true or false if the chkdsk /f flag was set.</span></span>

<span data-ttu-id="1ff6e-149">Пример кода PowerShell для [удаленной проверки](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) запускается удаленно или планирует проверку диска.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-149">The [Remotely scan disk](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell code sample remotely starts or schedules Scan Disk.</span></span>

<span data-ttu-id="1ff6e-150">Следующий пример кода VBScript выполняется ChkDsk.exe на диске D на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1ff6e-150">The following VBScript code sample Runs ChkDsk.exe against drive D on a computer.</span></span>


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a><span data-ttu-id="1ff6e-151">Требования</span><span class="sxs-lookup"><span data-stu-id="1ff6e-151">Requirements</span></span>



| <span data-ttu-id="1ff6e-152">Требование</span><span class="sxs-lookup"><span data-stu-id="1ff6e-152">Requirement</span></span> | <span data-ttu-id="1ff6e-153">Значение</span><span class="sxs-lookup"><span data-stu-id="1ff6e-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff6e-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ff6e-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff6e-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ff6e-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ff6e-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ff6e-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff6e-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ff6e-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ff6e-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ff6e-158">Namespace</span></span><br/>                | <span data-ttu-id="1ff6e-159">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1ff6e-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1ff6e-160">MOF</span><span class="sxs-lookup"><span data-stu-id="1ff6e-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ff6e-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ff6e-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ff6e-162">DLL</span><span class="sxs-lookup"><span data-stu-id="1ff6e-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ff6e-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ff6e-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff6e-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ff6e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff6e-165">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="1ff6e-165">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="1ff6e-166">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1ff6e-166">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

