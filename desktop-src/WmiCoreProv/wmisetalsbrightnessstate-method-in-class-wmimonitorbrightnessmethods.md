---
description: Используется для управления состоянием яркости датчика внешнего освещения.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Метод Вмисеталсбригхтнессстате класса Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693758"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="1d320-103">Метод Вмисеталсбригхтнессстате класса Вмимониторбригхтнессмесодс</span><span class="sxs-lookup"><span data-stu-id="1d320-103">WmiSetALSBrightnessState method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="1d320-104">Метод **вмисеталсбригхтнессстате** используется для управления состоянием яркости датчика внешнего освещения.</span><span class="sxs-lookup"><span data-stu-id="1d320-104">The **WmiSetALSBrightnessState** method is used to control the ambient light sensor brightness state.</span></span> <span data-ttu-id="1d320-105">Если при использовании метода [**вмисетбригхтнесс**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) было установлено переопределение яркости, то это переопределение будет иметь приоритет над заданной для Кроме яркости, используя этот метод.</span><span class="sxs-lookup"><span data-stu-id="1d320-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="1d320-106">Чтобы переопределение КРОМЕной яркости вступило в силу, необходимо отменить политику яркости, используя метод [**вмиреверттополицибригхтнесс**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="1d320-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d320-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d320-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a><span data-ttu-id="1d320-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d320-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d320-109">*Состояние*</span><span class="sxs-lookup"><span data-stu-id="1d320-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="1d320-110">Состояние яркости Кроме.</span><span class="sxs-lookup"><span data-stu-id="1d320-110">ALS brightness state.</span></span> <span data-ttu-id="1d320-111">Значение false отключает переопределение яркости Кроме, а значение true включает его.</span><span class="sxs-lookup"><span data-stu-id="1d320-111">False disables the ALS brightness override and true enables it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d320-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d320-112">Return value</span></span>

<span data-ttu-id="1d320-113">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="1d320-113">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="1d320-114">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="1d320-114">Any other number indicates an error.</span></span> <span data-ttu-id="1d320-115">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1d320-115">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d320-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1d320-116">Requirements</span></span>



| <span data-ttu-id="1d320-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1d320-117">Requirement</span></span> | <span data-ttu-id="1d320-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1d320-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d320-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d320-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d320-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d320-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1d320-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d320-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d320-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d320-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1d320-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d320-123">Namespace</span></span><br/>                | <span data-ttu-id="1d320-124">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="1d320-124">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1d320-125">MOF</span><span class="sxs-lookup"><span data-stu-id="1d320-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d320-126"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d320-126"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d320-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1d320-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d320-128"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d320-128"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d320-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d320-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d320-130">**вмимониторбригхтнессмесодс**</span><span class="sxs-lookup"><span data-stu-id="1d320-130">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="1d320-131">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="1d320-131">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

