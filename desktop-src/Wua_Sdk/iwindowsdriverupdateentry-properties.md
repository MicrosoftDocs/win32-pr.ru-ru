---
description: Интерфейс Ивиндовсдриверупдатинтри определяет следующие свойства.
ms.assetid: a0ff6ec2-13fe-4c0c-b375-9df55e1c1bb4
title: Свойства Ивиндовсдриверупдатинтри
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae63775bd7b13c67b4ec96c70107069730f828d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145688"
---
# <a name="iwindowsdriverupdateentry-properties"></a><span data-ttu-id="8aa1d-103">Свойства Ивиндовсдриверупдатинтри</span><span class="sxs-lookup"><span data-stu-id="8aa1d-103">IWindowsDriverUpdateEntry Properties</span></span>

<span data-ttu-id="8aa1d-104">Интерфейс [**ивиндовсдриверупдатинтри**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-104">The [**IWindowsDriverUpdateEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry) interface defines the following properties.</span></span>



| <span data-ttu-id="8aa1d-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="8aa1d-105">Property</span></span>                                                                     | <span data-ttu-id="8aa1d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8aa1d-106">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8aa1d-107">**девицепроблемнумбер**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-107">**DeviceProblemNumber**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_deviceproblemnumber) | <span data-ttu-id="8aa1d-108">Возвращает номер проблемы устройства, которое соответствует обновлению драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                                    |
| [<span data-ttu-id="8aa1d-109">**девицестатус**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_devicestatus)               | <span data-ttu-id="8aa1d-110">Возвращает состояние устройства, которое соответствует обновлению драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-110">Gets the status of the device that matches for the Windows driver update.</span></span>                                            |
| [<span data-ttu-id="8aa1d-111">**дриверкласс**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverclass)                 | <span data-ttu-id="8aa1d-112">Возвращает класс обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-112">Gets the class of the Windows driver update.</span></span>                                                                         |
| [<span data-ttu-id="8aa1d-113">**дриверхардвареид**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverhardwareid)       | <span data-ttu-id="8aa1d-114">Возвращает оборудование или совместимый идентификатор, который должен совпадать с обновлением драйвера Windows для установки.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-114">Gets the hardware or the compatible identifier that the Windows driver update must match in order to be installable.</span></span> |
| [<span data-ttu-id="8aa1d-115">**дривермануфактурер**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermanufacturer)   | <span data-ttu-id="8aa1d-116">Получает инвариантное от языка имя производителя обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                                   |
| [<span data-ttu-id="8aa1d-117">**дривермодел**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermodel)                 | <span data-ttu-id="8aa1d-118">Возвращает неизменяемое имя модели языка устройства, для которого предназначено обновление драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span>                |
| [<span data-ttu-id="8aa1d-119">**дриверпровидер**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverprovider)           | <span data-ttu-id="8aa1d-120">Возвращает инвариантное от языка имя поставщика обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                                       |
| [<span data-ttu-id="8aa1d-121">**дривервердате**</span><span class="sxs-lookup"><span data-stu-id="8aa1d-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driververdate)             | <span data-ttu-id="8aa1d-122">Возвращает дату версии драйвера для обновления драйвера Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa1d-122">Gets the driver version date of the Windows driver update.</span></span>                                                           |



 

 

 



