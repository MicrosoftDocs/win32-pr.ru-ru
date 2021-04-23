---
description: Метод Вмиреверттополицибригхтнесс используется для возврата яркости к параметру политики. Этот метод не влияет на настройки яркости Кроме.
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: Метод Вмиреверттополицибригхтнесс класса Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264999"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="3d474-104">Метод Вмиреверттополицибригхтнесс класса Вмимониторбригхтнессмесодс</span><span class="sxs-lookup"><span data-stu-id="3d474-104">WmiRevertToPolicyBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="3d474-105">Метод **вмиреверттополицибригхтнесс** используется для возврата яркости к параметру политики.</span><span class="sxs-lookup"><span data-stu-id="3d474-105">The **WmiRevertToPolicyBrightness** method is used to revert the brightness to the policy setting.</span></span> <span data-ttu-id="3d474-106">Этот метод не влияет на настройки яркости Кроме.</span><span class="sxs-lookup"><span data-stu-id="3d474-106">This method has no effect on the ALS brightness settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d474-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d474-107">Syntax</span></span>


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a><span data-ttu-id="3d474-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d474-108">Parameters</span></span>

<span data-ttu-id="3d474-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3d474-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d474-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d474-110">Return value</span></span>

<span data-ttu-id="3d474-111">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="3d474-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="3d474-112">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="3d474-112">Any other number indicates an error.</span></span> <span data-ttu-id="3d474-113">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3d474-113">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d474-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3d474-114">Requirements</span></span>



| <span data-ttu-id="3d474-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3d474-115">Requirement</span></span> | <span data-ttu-id="3d474-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3d474-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d474-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d474-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3d474-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d474-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3d474-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d474-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3d474-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d474-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3d474-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d474-121">Namespace</span></span><br/>                | <span data-ttu-id="3d474-122">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="3d474-122">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="3d474-123">MOF</span><span class="sxs-lookup"><span data-stu-id="3d474-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d474-124"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d474-124"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d474-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3d474-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d474-126"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d474-126"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d474-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d474-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d474-128">**вмимониторбригхтнессмесодс**</span><span class="sxs-lookup"><span data-stu-id="3d474-128">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="3d474-129">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="3d474-129">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

