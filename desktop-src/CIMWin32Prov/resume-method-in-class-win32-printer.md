---
description: Возобновляет приостановленную очередь печати.
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Метод Resume класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3eca8849fd1c5c449261dac1a9530f4da42e9482
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655750"
---
# <a name="resume-method-of-the-win32_printer-class"></a><span data-ttu-id="a036a-103">Метод Resume \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="a036a-103">Resume method of the Win32\_Printer class</span></span>

<span data-ttu-id="a036a-104">Метод класса **Resume** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) Возобновляет приостановленную очередь печати.</span><span class="sxs-lookup"><span data-stu-id="a036a-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method resumes a paused print queue.</span></span>

<span data-ttu-id="a036a-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a036a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a036a-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a036a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a036a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a036a-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="a036a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a036a-108">Parameters</span></span>

<span data-ttu-id="a036a-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a036a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a036a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a036a-110">Return value</span></span>

<span data-ttu-id="a036a-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="a036a-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a036a-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a036a-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a036a-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a036a-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a036a-114">**0**</span><span class="sxs-lookup"><span data-stu-id="a036a-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a036a-115">Успешно</span><span class="sxs-lookup"><span data-stu-id="a036a-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="a036a-116">**5**</span><span class="sxs-lookup"><span data-stu-id="a036a-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a036a-117">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="a036a-117">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a036a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a036a-118">Requirements</span></span>



| <span data-ttu-id="a036a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a036a-119">Requirement</span></span> | <span data-ttu-id="a036a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a036a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a036a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a036a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a036a-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a036a-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a036a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a036a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a036a-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a036a-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a036a-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a036a-125">Namespace</span></span><br/>                | <span data-ttu-id="a036a-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a036a-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a036a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="a036a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a036a-128"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a036a-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a036a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a036a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a036a-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a036a-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a036a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a036a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a036a-132">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a036a-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a036a-133">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="a036a-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="a036a-134">**Приостановить метод**</span><span class="sxs-lookup"><span data-stu-id="a036a-134">**Pause Method**</span></span>](pause-method-in-class-win32-printer.md)
</dt> </dl>

 

