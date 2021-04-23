---
description: Исключает диски из операции Autochk для выполнения при следующей перезагрузке.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Метод Ексклудефромауточк класса Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655799"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="db943-103">Метод Ексклудефромауточк \_ класса LogicalDisk Win32</span><span class="sxs-lookup"><span data-stu-id="db943-103">ExcludeFromAutochk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="db943-104">Метод **ексклудефромауточк** исключает диски из операции **Autochk** для выполнения при следующей перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="db943-104">The **ExcludeFromAutochk** method excludes disks from the **autochk** operation to be run at the next reboot.</span></span>

<span data-ttu-id="db943-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="db943-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="db943-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="db943-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="db943-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db943-107">Syntax</span></span>


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="db943-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="db943-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db943-109">*Логический* \[ диск окне\]</span><span class="sxs-lookup"><span data-stu-id="db943-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db943-110">Список дисков, которые следует исключить из **Autochk** при следующей перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="db943-110">List of drives that should be excluded from **autochk** at the next reboot.</span></span> <span data-ttu-id="db943-111">Строковый синтаксис состоит из буквы диска, за которой следует двоеточие для логического диска.</span><span class="sxs-lookup"><span data-stu-id="db943-111">The string syntax consists of the drive letter followed by a colon for the logical disk.</span></span>

<span data-ttu-id="db943-112">Пример: "C:"</span><span class="sxs-lookup"><span data-stu-id="db943-112">Example: "C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db943-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db943-113">Return value</span></span>

<span data-ttu-id="db943-114">Возвращает значение 0 (ноль), если ошибка не возникает.</span><span class="sxs-lookup"><span data-stu-id="db943-114">Returns a value of 0 (zero) when no error occurs.</span></span> <span data-ttu-id="db943-115">Значения перечислены в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="db943-115">Values are listed in the following list.</span></span> <span data-ttu-id="db943-116">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="db943-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="db943-117">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="db943-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="db943-118">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="db943-118">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="db943-119">**Ошибка-удаленный диск** (1)</span><span class="sxs-lookup"><span data-stu-id="db943-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="db943-120">**Ошибка — съемный накопитель** (2)</span><span class="sxs-lookup"><span data-stu-id="db943-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="db943-121">**Ошибка-диск не является корневым каталогом** (3)</span><span class="sxs-lookup"><span data-stu-id="db943-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="db943-122">**Ошибка-неизвестный диск** (4)</span><span class="sxs-lookup"><span data-stu-id="db943-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="db943-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db943-123">Remarks</span></span>

<span data-ttu-id="db943-124">Если этот параметр не исключен, на диске выполняется **Autochk** , если для диска задан бит "грязный".</span><span class="sxs-lookup"><span data-stu-id="db943-124">If not excluded, **autochk** is performed on the disk when the dirty bit is set for the disk.</span></span> <span data-ttu-id="db943-125">Обратите внимание, что вызовы для исключения дисков не являются кумулятивными.</span><span class="sxs-lookup"><span data-stu-id="db943-125">Note that the calls to exclude disks are not cumulative.</span></span> <span data-ttu-id="db943-126">Если выполняется вызов для исключения некоторых дисков, новый список не добавляется в список дисков, которые уже отмечены для исключения.</span><span class="sxs-lookup"><span data-stu-id="db943-126">If a call is made to exclude some disks, then the new list is not added to the list of disks that are already marked for exclusion.</span></span> <span data-ttu-id="db943-127">Новый список дисков перезаписывает предыдущий список.</span><span class="sxs-lookup"><span data-stu-id="db943-127">The new list of disks overwrites the previous list.</span></span> <span data-ttu-id="db943-128">Этот метод применим только к тем экземплярам логического диска, которые представляют физический диск на компьютере.</span><span class="sxs-lookup"><span data-stu-id="db943-128">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="db943-129">Он неприменим к сопоставленным логическим дискам.</span><span class="sxs-lookup"><span data-stu-id="db943-129">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="db943-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="db943-130">Examples</span></span>

<span data-ttu-id="db943-131">Следующий пример кода VBScript гарантирует, что Autochk.exe не будет выполняться для диска C при следующем перезагрузке компьютера, даже если на диске C установлен "грязный бит".</span><span class="sxs-lookup"><span data-stu-id="db943-131">The following VBScript code sample ensures that Autochk.exe will not run against drive C the next time the computer reboots, even if the "dirty bit" has been set on drive C.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a><span data-ttu-id="db943-132">Требования</span><span class="sxs-lookup"><span data-stu-id="db943-132">Requirements</span></span>



| <span data-ttu-id="db943-133">Требование</span><span class="sxs-lookup"><span data-stu-id="db943-133">Requirement</span></span> | <span data-ttu-id="db943-134">Значение</span><span class="sxs-lookup"><span data-stu-id="db943-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db943-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db943-135">Minimum supported client</span></span><br/> | <span data-ttu-id="db943-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db943-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db943-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db943-137">Minimum supported server</span></span><br/> | <span data-ttu-id="db943-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db943-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db943-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db943-139">Namespace</span></span><br/>                | <span data-ttu-id="db943-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="db943-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db943-141">MOF</span><span class="sxs-lookup"><span data-stu-id="db943-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db943-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db943-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db943-143">DLL</span><span class="sxs-lookup"><span data-stu-id="db943-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db943-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db943-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db943-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db943-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db943-146">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="db943-146">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="db943-147">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="db943-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

