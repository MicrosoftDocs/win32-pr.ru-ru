---
title: Метод Думпвминфо класса Win32_TSVm
description: Этот член предназначен для внутренних целей тестирования и не должен использоваться в коде.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Думпвминфо
- Службы удаленных рабочих столов метода Думпвминфо, класс Win32_TSVm
- Класс Win32_TSVm службы удаленных рабочих столов, метод Думпвминфо
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804036"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a><span data-ttu-id="52e1f-106">Метод Думпвминфо \_ класса Win32 тсвм</span><span class="sxs-lookup"><span data-stu-id="52e1f-106">DumpVmInfo method of the Win32\_TSVm class</span></span>

<span data-ttu-id="52e1f-107">Этот член предназначен для внутренних целей тестирования и не должен использоваться в коде.</span><span class="sxs-lookup"><span data-stu-id="52e1f-107">This member is for internal testing purposes, and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e1f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52e1f-108">Syntax</span></span>


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a><span data-ttu-id="52e1f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="52e1f-109">Parameters</span></span>

<span data-ttu-id="52e1f-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="52e1f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52e1f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52e1f-111">Return value</span></span>

<span data-ttu-id="52e1f-112">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="52e1f-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="52e1f-113">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="52e1f-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="52e1f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="52e1f-114">Requirements</span></span>



| <span data-ttu-id="52e1f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="52e1f-115">Requirement</span></span> | <span data-ttu-id="52e1f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="52e1f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="52e1f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52e1f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="52e1f-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="52e1f-118">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="52e1f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52e1f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="52e1f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52e1f-120">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="52e1f-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="52e1f-121">Namespace</span></span><br/>                | <span data-ttu-id="52e1f-122">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="52e1f-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="52e1f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="52e1f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52e1f-124"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52e1f-124"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="52e1f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="52e1f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52e1f-126"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52e1f-126"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e1f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52e1f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e1f-128">**\_Тсвм Win32**</span><span class="sxs-lookup"><span data-stu-id="52e1f-128">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





