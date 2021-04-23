---
title: Константы WINBIO_SENSOR_MODE (Винбио \_ types. h)
description: Задайте режим адаптера датчика.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803904"
---
# <a name="winbio_sensor_mode-constants"></a><span data-ttu-id="5b490-103">\_ \_ Константы режима датчика винбио</span><span class="sxs-lookup"><span data-stu-id="5b490-103">WINBIO\_SENSOR\_MODE Constants</span></span>

<span data-ttu-id="5b490-104">Следующие значения используются в функции [**сенсорадаптерсетмоде**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) для установки режима адаптера датчика.</span><span class="sxs-lookup"><span data-stu-id="5b490-104">The following values are used in the [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) function to set the sensor adapter mode.</span></span>



| <span data-ttu-id="5b490-105">Константа</span><span class="sxs-lookup"><span data-stu-id="5b490-105">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="5b490-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5b490-106">Description</span></span>                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <span data-ttu-id="5b490-107"><dt>**\_неизвестный \_ \_ режим датчика винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="5b490-107"><dt>**WINBIO\_SENSOR\_UNKNOWN\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="5b490-108">Неизвестный режим работы.</span><span class="sxs-lookup"><span data-stu-id="5b490-108">The operating mode is not known.</span></span><br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <span data-ttu-id="5b490-109"><dt>**\_ \_ базовый режим датчика \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="5b490-109"><dt>**WINBIO\_SENSOR\_BASIC\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="5b490-110">Использовать датчик в базовом режиме.</span><span class="sxs-lookup"><span data-stu-id="5b490-110">Operate the sensor in basic mode.</span></span> <span data-ttu-id="5b490-111">Датчик действует только как устройство записи.</span><span class="sxs-lookup"><span data-stu-id="5b490-111">The sensor acts only as a capture device.</span></span> <span data-ttu-id="5b490-112">Любые существующие возможности обработки или хранения не используются.</span><span class="sxs-lookup"><span data-stu-id="5b490-112">Any onboard processing or storage capabilities that exist are not used.</span></span><br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <span data-ttu-id="5b490-113"><dt>**\_ \_ Расширенный режим датчика \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="5b490-113"><dt>**WINBIO\_SENSOR\_ADVANCED\_MODE**</dt></span></span> </dl>       | <span data-ttu-id="5b490-114">Использовать датчик в расширенном режиме.</span><span class="sxs-lookup"><span data-stu-id="5b490-114">Operate the sensor in advanced mode.</span></span> <span data-ttu-id="5b490-115">Датчик может собирать образцы и выполнять функции сопоставления и хранения.</span><span class="sxs-lookup"><span data-stu-id="5b490-115">The sensor can capture samples and perform matching and storage functions.</span></span><br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <span data-ttu-id="5b490-116"><dt>**\_ \_ режим навигации датчика \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="5b490-116"><dt>**WINBIO\_SENSOR\_NAVIGATION\_MODE**</dt></span></span> </dl> | <span data-ttu-id="5b490-117">Использовать датчик в качестве панели мыши.</span><span class="sxs-lookup"><span data-stu-id="5b490-117">Operate the sensor as a mouse pad.</span></span> <span data-ttu-id="5b490-118">Сейчас такая возможность не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5b490-118">This is not currently supported.</span></span><br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <span data-ttu-id="5b490-119"><dt>**\_ \_ режим сна датчика \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="5b490-119"><dt>**WINBIO\_SENSOR\_SLEEP\_MODE**</dt></span></span> </dl>                | <span data-ttu-id="5b490-120">Работа датчика в спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="5b490-120">Operate the sensor in sleep mode.</span></span><br/>                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="5b490-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5b490-121">Requirements</span></span>



| <span data-ttu-id="5b490-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5b490-122">Requirement</span></span> | <span data-ttu-id="5b490-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5b490-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b490-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b490-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5b490-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5b490-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="5b490-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b490-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5b490-127">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b490-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5b490-128">Header</span><span class="sxs-lookup"><span data-stu-id="5b490-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b490-129"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b490-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b490-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b490-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b490-131">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="5b490-131">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





