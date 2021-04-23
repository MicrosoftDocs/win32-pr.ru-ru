---
description: Выводит тестовую страницу.
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: Метод Принттестпаже класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656073"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a><span data-ttu-id="4eb4b-103">Метод Принттестпаже \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="4eb4b-103">PrintTestPage method of the Win32\_Printer class</span></span>

<span data-ttu-id="4eb4b-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) принттестпаже выводит тестовую страницу.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-104">The **PrintTestPage** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method prints a test page.</span></span>

<span data-ttu-id="4eb4b-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4eb4b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4eb4b-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4eb4b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb4b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eb4b-107">Syntax</span></span>


```mof
uint32 PrintTestPage();
```



## <a name="parameters"></a><span data-ttu-id="4eb4b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eb4b-108">Parameters</span></span>

<span data-ttu-id="4eb4b-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4eb4b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4eb4b-110">Return value</span></span>

<span data-ttu-id="4eb4b-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="4eb4b-112">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4eb4b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4eb4b-113">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4eb4b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4eb4b-114">**0**</span><span class="sxs-lookup"><span data-stu-id="4eb4b-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4eb4b-115">Успешно</span><span class="sxs-lookup"><span data-stu-id="4eb4b-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="4eb4b-116">**5**</span><span class="sxs-lookup"><span data-stu-id="4eb4b-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4eb4b-117">доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="4eb4b-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4eb4b-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="4eb4b-118">Examples</span></span>

<span data-ttu-id="4eb4b-119">В следующем примере кода PowerShell выводится тестовая страница.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-119">The following PowerShell code sample prints a test page.</span></span>


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
```



## <a name="requirements"></a><span data-ttu-id="4eb4b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4eb4b-120">Requirements</span></span>



| <span data-ttu-id="4eb4b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4eb4b-121">Requirement</span></span> | <span data-ttu-id="4eb4b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4eb4b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb4b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eb4b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb4b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4eb4b-124">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4eb4b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eb4b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb4b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4eb4b-126">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4eb4b-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4eb4b-127">Namespace</span></span><br/>                | <span data-ttu-id="4eb4b-128">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4eb4b-128">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="4eb4b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4eb4b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4eb4b-130"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4eb4b-130"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="4eb4b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4eb4b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4eb4b-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4eb4b-132"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4eb4b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eb4b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb4b-134">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="4eb4b-134">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4eb4b-135">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="4eb4b-135">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

