---
description: Интерфейс Ивиндовсдриверупдате определяет следующие свойства.
ms.assetid: 2177c5e0-47db-44ae-a0ce-2544ff2d0855
title: Свойства Ивиндовсдриверупдате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291d7933cf3e73dee6f47edab3240c4ebd14f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682756"
---
# <a name="iwindowsdriverupdate-properties"></a><span data-ttu-id="89ab6-103">Свойства Ивиндовсдриверупдате</span><span class="sxs-lookup"><span data-stu-id="89ab6-103">IWindowsDriverUpdate Properties</span></span>

<span data-ttu-id="89ab6-104">Интерфейс [**ивиндовсдриверупдате**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="89ab6-104">The [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="89ab6-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="89ab6-105">Property</span></span>                                                                                                    | <span data-ttu-id="89ab6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="89ab6-106">Description</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89ab6-107">[**Девицепроблемнумбер**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**адрес**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span><span class="sxs-lookup"><span data-stu-id="89ab6-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Address**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span></span> | <span data-ttu-id="89ab6-108">Возвращает номер проблемы устройства, которое соответствует обновлению драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="89ab6-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                     |
| [<span data-ttu-id="89ab6-109">**девицестатус**</span><span class="sxs-lookup"><span data-stu-id="89ab6-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_devicestatus)                                                   | <span data-ttu-id="89ab6-110">Возвращает состояние устройства, которое соответствует обновлению драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="89ab6-110">Gets the status of the device that matches for the Windows driver update.</span></span>                             |
| [<span data-ttu-id="89ab6-111">**дриверкласс**</span><span class="sxs-lookup"><span data-stu-id="89ab6-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverclass)                                                     | <span data-ttu-id="89ab6-112">Возвращает класс обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="89ab6-112">Gets the class of the Windows driver update.</span></span>                                                          |
| [<span data-ttu-id="89ab6-113">**дриверхардвареид**</span><span class="sxs-lookup"><span data-stu-id="89ab6-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverhardwareid)                                           | <span data-ttu-id="89ab6-114">Возвращает идентификатор оборудования или совместимый идентификатор, которому должен соответствовать обновление драйвера Windows для установки.</span><span class="sxs-lookup"><span data-stu-id="89ab6-114">Gets the hardware ID or compatible ID that the Windows driver update must match to be installable.</span></span>    |
| [<span data-ttu-id="89ab6-115">**дривермануфактурер**</span><span class="sxs-lookup"><span data-stu-id="89ab6-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermanufacturer)                                       | <span data-ttu-id="89ab6-116">Получает инвариантное от языка имя производителя обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="89ab6-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                    |
| [<span data-ttu-id="89ab6-117">**дривермодел**</span><span class="sxs-lookup"><span data-stu-id="89ab6-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermodel)                                                     | <span data-ttu-id="89ab6-118">Возвращает неизменяемое имя модели языка устройства, для которого предназначено обновление драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="89ab6-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span> |
| [<span data-ttu-id="89ab6-119">**дриверпровидер**</span><span class="sxs-lookup"><span data-stu-id="89ab6-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverprovider)                                               | <span data-ttu-id="89ab6-120">Возвращает инвариантное от языка имя поставщика обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="89ab6-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                        |
| [<span data-ttu-id="89ab6-121">**дривервердате**</span><span class="sxs-lookup"><span data-stu-id="89ab6-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driververdate)                                                 | <span data-ttu-id="89ab6-122">Возвращает дату версии драйвера для обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="89ab6-122">Gets the driver version date of the Windows driver update.</span></span>                                            |



 

 

 



