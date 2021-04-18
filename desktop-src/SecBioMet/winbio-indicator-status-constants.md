---
title: Константы WINBIO_INDICATOR_STATUS (Винбио \_ types. h)
description: Установите индикатор индикатора.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682152"
---
# <a name="winbio_indicator_status-constants"></a><span data-ttu-id="e3472-103">\_ \_ Константы состояния индикатора винбио</span><span class="sxs-lookup"><span data-stu-id="e3472-103">WINBIO\_INDICATOR\_STATUS Constants</span></span>

<span data-ttu-id="e3472-104">Чтобы задать индикатор индикатора, можно использовать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e3472-104">The following values can be used to set an indicator light.</span></span> <span data-ttu-id="e3472-105">По умолчанию датчики не имеют источника света, но приложения могут использовать эти значения для включения или отключения индикаторов индикатора.</span><span class="sxs-lookup"><span data-stu-id="e3472-105">By default, sensors will not have a light on, but applications can use these values to enable or disable indicator lights.</span></span> <span data-ttu-id="e3472-106">Значение **\_ \_ состояния датчика винбио** содержит более подробные сведения о состоянии индикатора индикаторов на.</span><span class="sxs-lookup"><span data-stu-id="e3472-106">The **WINBIO\_SENSOR\_STATUS** value provides more detail about the status of an indicator light that is on.</span></span> <span data-ttu-id="e3472-107">Дополнительные сведения см. в следующих функциях:</span><span class="sxs-lookup"><span data-stu-id="e3472-107">For more information, see the following functions:</span></span>

-   [<span data-ttu-id="e3472-108">**сенсорадаптерсетиндикаторстатус**</span><span class="sxs-lookup"><span data-stu-id="e3472-108">**SensorAdapterSetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [<span data-ttu-id="e3472-109">**сенсорадаптержетиндикаторстатус**</span><span class="sxs-lookup"><span data-stu-id="e3472-109">**SensorAdapterGetIndicatorStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [<span data-ttu-id="e3472-110">**сенсорадаптеркуеристатус**</span><span class="sxs-lookup"><span data-stu-id="e3472-110">**SensorAdapterQueryStatus**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| <span data-ttu-id="e3472-111">Константа</span><span class="sxs-lookup"><span data-stu-id="e3472-111">Constant</span></span>                                                                                                                                                                            | <span data-ttu-id="e3472-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e3472-112">Description</span></span>                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <span data-ttu-id="e3472-113"><dt>**\_индикатор винбио \_ на**</dt></span><span class="sxs-lookup"><span data-stu-id="e3472-113"><dt>**WINBIO\_INDICATOR\_ON**</dt></span></span> </dl>    | <span data-ttu-id="e3472-114">Индикатор датчика горит.</span><span class="sxs-lookup"><span data-stu-id="e3472-114">The sensor indicator light is on.</span></span><br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <span data-ttu-id="e3472-115"><dt>**\_индикатор винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3472-115"><dt>**WINBIO\_INDICATOR\_OFF**</dt></span></span> </dl> | <span data-ttu-id="e3472-116">Индикатор датчика горит.</span><span class="sxs-lookup"><span data-stu-id="e3472-116">The sensor indicator light is off.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e3472-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e3472-117">Requirements</span></span>



| <span data-ttu-id="e3472-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e3472-118">Requirement</span></span> | <span data-ttu-id="e3472-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e3472-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3472-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3472-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3472-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e3472-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e3472-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3472-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3472-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3472-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e3472-124">Header</span><span class="sxs-lookup"><span data-stu-id="e3472-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3472-125"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3472-125"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3472-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3472-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3472-127">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="e3472-127">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





