---
description: Приостанавливает очередь печати.
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Метод Pause класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12d7e84351d77730b580242a58b38d7506af451a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423470"
---
# <a name="pause-method-of-the-win32_printer-class"></a><span data-ttu-id="db253-103">Метод Pause \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="db253-103">Pause method of the Win32\_Printer class</span></span>

<span data-ttu-id="db253-104">Метод класса **Pause** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) приостанавливает очередь печати.</span><span class="sxs-lookup"><span data-stu-id="db253-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method pauses the print queue.</span></span> <span data-ttu-id="db253-105">Никакие задания не могут печататься, пока очередь не будет возобновлена.</span><span class="sxs-lookup"><span data-stu-id="db253-105">No jobs can print until the queue is resumed.</span></span>

<span data-ttu-id="db253-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="db253-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="db253-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="db253-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="db253-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db253-108">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="db253-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="db253-109">Parameters</span></span>

<span data-ttu-id="db253-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="db253-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db253-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db253-111">Return value</span></span>

<span data-ttu-id="db253-112">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="db253-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="db253-113">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="db253-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="db253-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="db253-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="db253-115">**0**</span><span class="sxs-lookup"><span data-stu-id="db253-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="db253-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="db253-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="db253-117">**5**</span><span class="sxs-lookup"><span data-stu-id="db253-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="db253-118">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="db253-118">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db253-119">Требования</span><span class="sxs-lookup"><span data-stu-id="db253-119">Requirements</span></span>



| <span data-ttu-id="db253-120">Требование</span><span class="sxs-lookup"><span data-stu-id="db253-120">Requirement</span></span> | <span data-ttu-id="db253-121">Значение</span><span class="sxs-lookup"><span data-stu-id="db253-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db253-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db253-122">Minimum supported client</span></span><br/> | <span data-ttu-id="db253-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db253-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="db253-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db253-124">Minimum supported server</span></span><br/> | <span data-ttu-id="db253-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db253-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="db253-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db253-126">Namespace</span></span><br/>                | <span data-ttu-id="db253-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="db253-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="db253-128">MOF</span><span class="sxs-lookup"><span data-stu-id="db253-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db253-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db253-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="db253-130">DLL</span><span class="sxs-lookup"><span data-stu-id="db253-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db253-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db253-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="db253-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db253-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db253-133">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="db253-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="db253-134">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="db253-134">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="db253-135">**Метод Resume**</span><span class="sxs-lookup"><span data-stu-id="db253-135">**Resume method**</span></span>](resume-method-in-class-win32-printer.md)
</dt> </dl>

 

