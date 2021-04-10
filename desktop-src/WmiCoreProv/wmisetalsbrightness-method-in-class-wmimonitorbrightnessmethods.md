---
description: Используется для установки значения яркости датчика внешнего освещения.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Метод Вмисеталсбригхтнесс класса Вмимониторбригхтнессмесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272923"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="b86a3-103">Метод Вмисеталсбригхтнесс класса Вмимониторбригхтнессмесодс</span><span class="sxs-lookup"><span data-stu-id="b86a3-103">WmiSetALSBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="b86a3-104">Метод **вмисеталсбригхтнесс** используется для установки значения яркости датчика внешнего освещения.</span><span class="sxs-lookup"><span data-stu-id="b86a3-104">The **WmiSetALSBrightness** method is used to set the ambient light sensor brightness value.</span></span> <span data-ttu-id="b86a3-105">Если при использовании метода [**вмисетбригхтнесс**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) было установлено переопределение яркости, то это переопределение будет иметь приоритет над заданной для Кроме яркости, используя этот метод.</span><span class="sxs-lookup"><span data-stu-id="b86a3-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="b86a3-106">Чтобы переопределение КРОМЕной яркости вступило в силу, необходимо отменить политику яркости, используя метод [**вмиреверттополицибригхтнесс**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="b86a3-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b86a3-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="b86a3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b86a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86a3-109">*Brightness*</span><span class="sxs-lookup"><span data-stu-id="b86a3-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="b86a3-110">Яркость Кроме в процентах.</span><span class="sxs-lookup"><span data-stu-id="b86a3-110">The ALS brightness as a percentage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b86a3-111">Return value</span></span>

<span data-ttu-id="b86a3-112">Возвращает ноль (0), чтобы указать на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="b86a3-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="b86a3-113">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="b86a3-113">Any other number indicates an error.</span></span> <span data-ttu-id="b86a3-114">Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b86a3-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="b86a3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b86a3-115">Requirements</span></span>



| <span data-ttu-id="b86a3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b86a3-116">Requirement</span></span> | <span data-ttu-id="b86a3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b86a3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b86a3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b86a3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b86a3-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b86a3-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b86a3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b86a3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b86a3-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b86a3-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b86a3-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b86a3-122">Namespace</span></span><br/>                | <span data-ttu-id="b86a3-123">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="b86a3-123">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b86a3-124">MOF</span><span class="sxs-lookup"><span data-stu-id="b86a3-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b86a3-125"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b86a3-125"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b86a3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b86a3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b86a3-127"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86a3-127"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86a3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b86a3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86a3-129">**вмимониторбригхтнессмесодс**</span><span class="sxs-lookup"><span data-stu-id="b86a3-129">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="b86a3-130">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="b86a3-130">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

