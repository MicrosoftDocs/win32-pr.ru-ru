---
description: Планирует запуск Autochk на диске, представленном консолью Win32 LogicalDisk при \_ следующей перезагрузке, если установлен бит "грязный".
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Метод Счедулеауточк класса Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990454"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="da693-103">Метод Счедулеауточк \_ класса LogicalDisk Win32</span><span class="sxs-lookup"><span data-stu-id="da693-103">ScheduleAutoChk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="da693-104">Метод класса **счедулеауточк** планирует выполнение Autochk на диске, представленном в [**Win32 \_ LogicalDisk**](win32-logicaldisk.md) при следующей перезагрузке, если установлен бит "грязный".</span><span class="sxs-lookup"><span data-stu-id="da693-104">The **ScheduleAutoChk** class method schedules Autochk to be run on the disk drive represented by the [**Win32\_LogicalDisk**](win32-logicaldisk.md) at the next reboot if the dirty bit is set.</span></span>

<span data-ttu-id="da693-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="da693-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da693-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="da693-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da693-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da693-107">Syntax</span></span>


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="da693-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="da693-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da693-109">*Логический* \[ диск окне\]</span><span class="sxs-lookup"><span data-stu-id="da693-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da693-110">Указывает список дисков, которые нужно запланировать для выполнения Autochk при следующей перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="da693-110">Specifies the list of drives to schedule for Autochk at the next reboot.</span></span> <span data-ttu-id="da693-111">Строковый синтаксис состоит из буквы диска, за которой следует двоеточие для логического диска, например: "C:"</span><span class="sxs-lookup"><span data-stu-id="da693-111">The string syntax consists of the drive letter followed by a colon for the logical disk, for example: "C:"</span></span>

> [!Note]  
> <span data-ttu-id="da693-112">Всегда проверяйте допустимость букв дисков в массиве *LogicalDisk* , когда данные поступают из неизвестного источника или ненадежного источника.</span><span class="sxs-lookup"><span data-stu-id="da693-112">Always check the validity of the drive letters in the *LogicalDisk* array when the data comes from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da693-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da693-113">Return value</span></span>

<span data-ttu-id="da693-114">Возвращает значение 0 (нуль) в случае успеха и другое значение, если возникает какая-либо другая ошибка.</span><span class="sxs-lookup"><span data-stu-id="da693-114">Returns a value of 0 (zero) if successful, and some other value if any other error occurs.</span></span> <span data-ttu-id="da693-115">Значения перечислены в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="da693-115">Values are listed in the following list.</span></span> <span data-ttu-id="da693-116">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="da693-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="da693-117">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="da693-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="da693-118">**Без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="da693-118">**No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da693-119">**Ошибка-удаленный диск** (1)</span><span class="sxs-lookup"><span data-stu-id="da693-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="da693-120">**Ошибка — съемный накопитель** (2)</span><span class="sxs-lookup"><span data-stu-id="da693-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da693-121">**Ошибка-диск не является корневым каталогом** (3)</span><span class="sxs-lookup"><span data-stu-id="da693-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da693-122">**Ошибка-неизвестный диск** (4)</span><span class="sxs-lookup"><span data-stu-id="da693-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="da693-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da693-123">Remarks</span></span>

<span data-ttu-id="da693-124">Этот метод применим только к тем экземплярам логического диска, которые представляют физический диск на компьютере.</span><span class="sxs-lookup"><span data-stu-id="da693-124">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="da693-125">Этот метод неприменим к сопоставленным логическим дискам.</span><span class="sxs-lookup"><span data-stu-id="da693-125">This method is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="da693-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="da693-126">Examples</span></span>

<span data-ttu-id="da693-127">Следующие примеры VBScript и PowerShell планируются Autochk.exe для запуска на диске C при следующем перезагрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="da693-127">The following VBScript and PowerShell samples schedule Autochk.exe to run against drive C the next time the computer reboots.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a><span data-ttu-id="da693-128">Требования</span><span class="sxs-lookup"><span data-stu-id="da693-128">Requirements</span></span>



| <span data-ttu-id="da693-129">Требование</span><span class="sxs-lookup"><span data-stu-id="da693-129">Requirement</span></span> | <span data-ttu-id="da693-130">Значение</span><span class="sxs-lookup"><span data-stu-id="da693-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da693-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da693-131">Minimum supported client</span></span><br/> | <span data-ttu-id="da693-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da693-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da693-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da693-133">Minimum supported server</span></span><br/> | <span data-ttu-id="da693-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da693-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da693-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="da693-135">Namespace</span></span><br/>                | <span data-ttu-id="da693-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="da693-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da693-137">MOF</span><span class="sxs-lookup"><span data-stu-id="da693-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da693-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da693-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da693-139">DLL</span><span class="sxs-lookup"><span data-stu-id="da693-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da693-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da693-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da693-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da693-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da693-142">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="da693-142">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> </dl>

 

