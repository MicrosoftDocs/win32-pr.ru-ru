---
description: Задает яркость экрана монитора компьютера.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Метод Вмисетбригхтнесс класса Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081005"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="2451a-103">Метод Вмисетбригхтнесс класса Вмимониторбригхтнессмесодс</span><span class="sxs-lookup"><span data-stu-id="2451a-103">WmiSetBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="2451a-104">Метод **вмисетбригхтнесс** задает яркость экрана монитора компьютера.</span><span class="sxs-lookup"><span data-stu-id="2451a-104">The **WmiSetBrightness** method sets the display brightness of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="2451a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2451a-105">Syntax</span></span>


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="2451a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2451a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2451a-107">*Timeout*</span><span class="sxs-lookup"><span data-stu-id="2451a-107">*Timeout*</span></span> 
</dt> <dd>

<span data-ttu-id="2451a-108">Время ожидания в секундах.</span><span class="sxs-lookup"><span data-stu-id="2451a-108">Timeout, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="2451a-109">*Brightness*</span><span class="sxs-lookup"><span data-stu-id="2451a-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="2451a-110">Яркость в процентах.</span><span class="sxs-lookup"><span data-stu-id="2451a-110">Brightness, in percent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2451a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2451a-111">Return value</span></span>

<span data-ttu-id="2451a-112">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="2451a-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="2451a-113">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="2451a-113">Any other number indicates an error.</span></span> <span data-ttu-id="2451a-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2451a-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="2451a-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="2451a-115">Examples</span></span>

<span data-ttu-id="2451a-116">Дополнительные сведения о получении и настройке яркости монитора см. в блоге, посвященном [использованию PowerShell для создания отчетов и настройки яркости](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) монитора.</span><span class="sxs-lookup"><span data-stu-id="2451a-116">For an extended discussion of retrieving and setting monitor brightness, see the Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) blog topic.</span></span>

<span data-ttu-id="2451a-117">В следующем примере PowerShell яркость монитора устанавливается равным 50%.</span><span class="sxs-lookup"><span data-stu-id="2451a-117">The following PowerShell sample sets the brightness of the monitor to 50%.</span></span>


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a><span data-ttu-id="2451a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2451a-118">Requirements</span></span>



| <span data-ttu-id="2451a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2451a-119">Requirement</span></span> | <span data-ttu-id="2451a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2451a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2451a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2451a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2451a-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2451a-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2451a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2451a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2451a-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2451a-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2451a-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2451a-125">Namespace</span></span><br/>                | <span data-ttu-id="2451a-126">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="2451a-126">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2451a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="2451a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2451a-128"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2451a-128"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2451a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2451a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2451a-130"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2451a-130"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2451a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2451a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2451a-132">**вмимониторбригхтнессмесодс**</span><span class="sxs-lookup"><span data-stu-id="2451a-132">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="2451a-133">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="2451a-133">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

