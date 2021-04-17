---
description: API расположения определяет следующие типы перечислений.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Структуры и типы перечислений (API Location)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674055"
---
# <a name="structures-and-enumeration-types-location-api"></a><span data-ttu-id="593e1-103">Структуры и типы перечислений (API Location)</span><span class="sxs-lookup"><span data-stu-id="593e1-103">Structures and Enumeration Types (Location API)</span></span>

<span data-ttu-id="593e1-104">\[API расположения Win32 доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="593e1-104">\[The Win32 Location API is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="593e1-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="593e1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="593e1-106">Вместо этого используйте API [**Windows. Devices. географического расположения**](/uwp/api/Windows.Devices.Geolocation) .</span><span class="sxs-lookup"><span data-stu-id="593e1-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="593e1-107">\]</span><span class="sxs-lookup"><span data-stu-id="593e1-107">\]</span></span>

<span data-ttu-id="593e1-108">API расположения определяет следующие типы перечислений.</span><span class="sxs-lookup"><span data-stu-id="593e1-108">The Location API defines the following enumeration types.</span></span>



| <span data-ttu-id="593e1-109">Перечисление</span><span class="sxs-lookup"><span data-stu-id="593e1-109">Enumeration</span></span>                                                                       | <span data-ttu-id="593e1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="593e1-110">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="593e1-111">[**\_Требуемая \_ точность расположения**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="593e1-111">[**LOCATION\_DESIRED\_ACCURACY**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span></span>                  | <span data-ttu-id="593e1-112">Определяет возможные типы точности.</span><span class="sxs-lookup"><span data-stu-id="593e1-112">Defines the possible desired accuracy types.</span></span>                         |
| [<span data-ttu-id="593e1-113">**\_состояние отчета о расположении \_**</span><span class="sxs-lookup"><span data-stu-id="593e1-113">**LOCATION\_REPORT\_STATUS**</span></span>](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | <span data-ttu-id="593e1-114">Определяет возможное состояние для новых отчетов определенного типа отчета.</span><span class="sxs-lookup"><span data-stu-id="593e1-114">Defines possible status for new reports of a particular report type.</span></span> |



 

## <a name="location-constants-from-the-sensor-api"></a><span data-ttu-id="593e1-115">Константы расположения из API датчика</span><span class="sxs-lookup"><span data-stu-id="593e1-115">Location Constants from the Sensor API</span></span>

<span data-ttu-id="593e1-116">API датчика также определяет связанные с расположением ключи и константы свойств.</span><span class="sxs-lookup"><span data-stu-id="593e1-116">The Sensor API also defines location-related property keys and constants.</span></span> <span data-ttu-id="593e1-117">Ключи свойств, определенные в sensors. h, можно использовать для получения данных о местоположении из отчета путем вызова [**илокатионрепорт:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span><span class="sxs-lookup"><span data-stu-id="593e1-117">The property keys defined in sensors.h can be used to retrieve location data from a report by calling [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span></span>

 

 
