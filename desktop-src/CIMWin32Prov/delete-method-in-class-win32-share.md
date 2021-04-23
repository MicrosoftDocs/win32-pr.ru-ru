---
description: Удаляет имя общего ресурса из списка общих ресурсов сервера, отключая подключения к общему ресурсу.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Метод Delete класса Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141659"
---
# <a name="delete-method-of-the-win32_share-class"></a><span data-ttu-id="21028-103">Метод DELETE \_ класса общего ресурса Win32</span><span class="sxs-lookup"><span data-stu-id="21028-103">Delete method of the Win32\_Share class</span></span>

<span data-ttu-id="21028-104">Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет имя общего ресурса из списка общих ресурсов сервера, отключая подключения к общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="21028-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span>

<span data-ttu-id="21028-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="21028-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="21028-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="21028-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="21028-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21028-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="21028-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="21028-108">Parameters</span></span>

<span data-ttu-id="21028-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="21028-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21028-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21028-110">Return value</span></span>

<span data-ttu-id="21028-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="21028-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="21028-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="21028-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="21028-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="21028-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="21028-114">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="21028-114">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="21028-115">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="21028-115">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="21028-116">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="21028-116">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="21028-117">**Недопустимое имя** (9)</span><span class="sxs-lookup"><span data-stu-id="21028-117">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="21028-118">**Недопустимый уровень** (10)</span><span class="sxs-lookup"><span data-stu-id="21028-118">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="21028-119">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="21028-119">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="21028-120">**Повторяющаяся общая папка** (22)</span><span class="sxs-lookup"><span data-stu-id="21028-120">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="21028-121">**Путь перенаправления** (23)</span><span class="sxs-lookup"><span data-stu-id="21028-121">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="21028-122">**Неизвестное устройство или каталог** (24)</span><span class="sxs-lookup"><span data-stu-id="21028-122">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="21028-123">**Не найдено сетевое имя** (25)</span><span class="sxs-lookup"><span data-stu-id="21028-123">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="21028-124">**Другие** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="21028-124">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="21028-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21028-125">Remarks</span></span>

<span data-ttu-id="21028-126">Метод **Delete** является методом объекта и используется в экземпляре класса.</span><span class="sxs-lookup"><span data-stu-id="21028-126">The **Delete** method is an object method and is used on an instance of a class.</span></span>

<span data-ttu-id="21028-127">Только члены локальной группы "Администраторы" или "Операторы учетных записей", а также участники группы операторов связи, печати или сервера могут успешно выполнять метод.</span><span class="sxs-lookup"><span data-stu-id="21028-127">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute the method.</span></span> <span data-ttu-id="21028-128">Оператор Print может удалять только очереди принтера.</span><span class="sxs-lookup"><span data-stu-id="21028-128">The Print operator can delete only printer queues.</span></span> <span data-ttu-id="21028-129">Оператор связи может удалять только очереди устройств связи.</span><span class="sxs-lookup"><span data-stu-id="21028-129">The Communication operator can delete only communication-device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="21028-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="21028-130">Examples</span></span>

<span data-ttu-id="21028-131">В следующем примере кода VBScript удаляется указанная общая папка.</span><span class="sxs-lookup"><span data-stu-id="21028-131">The following VBScript code sample deletes the specified share.</span></span>


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



<span data-ttu-id="21028-132">В следующем примере кода PowerShell удаляются пустые общие папки.</span><span class="sxs-lookup"><span data-stu-id="21028-132">The following PowerShell code sample deletes blank shares.</span></span>


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a><span data-ttu-id="21028-133">Требования</span><span class="sxs-lookup"><span data-stu-id="21028-133">Requirements</span></span>



| <span data-ttu-id="21028-134">Требование</span><span class="sxs-lookup"><span data-stu-id="21028-134">Requirement</span></span> | <span data-ttu-id="21028-135">Значение</span><span class="sxs-lookup"><span data-stu-id="21028-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21028-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21028-136">Minimum supported client</span></span><br/> | <span data-ttu-id="21028-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21028-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21028-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21028-138">Minimum supported server</span></span><br/> | <span data-ttu-id="21028-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21028-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21028-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="21028-140">Namespace</span></span><br/>                | <span data-ttu-id="21028-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="21028-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21028-142">MOF</span><span class="sxs-lookup"><span data-stu-id="21028-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21028-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21028-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21028-144">DLL</span><span class="sxs-lookup"><span data-stu-id="21028-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21028-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21028-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21028-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21028-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="21028-147">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21028-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="21028-148">**\_Общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="21028-148">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

