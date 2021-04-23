---
title: Константы WINBIO_ORIENTATION (Винбио \_ types. h)
description: Следующие константы указывают возможные ориентации камеры, которые компонент датчика указывает как обязательный.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892734"
---
# <a name="winbio_orientation-constants"></a><span data-ttu-id="1e399-103">\_Константы ориентации винбио</span><span class="sxs-lookup"><span data-stu-id="1e399-103">WINBIO\_ORIENTATION Constants</span></span>

<span data-ttu-id="1e399-104">Следующие константы указывают возможные ориентации камеры, которые компонент датчика указывает как обязательный.</span><span class="sxs-lookup"><span data-stu-id="1e399-104">The following constants specify the possible camera orientations that the sensor component specifies as mandatory.</span></span>



| <span data-ttu-id="1e399-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="1e399-105">Constant/value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="1e399-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1e399-106">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <span data-ttu-id="1e399-107"><dt>**Винбио \_ ОРИЕНТАЦИЯ не \_ указана**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e399-107"><dt>**WINBIO\_ORIENTATION\_UNSPECIFIED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="1e399-108">Не указана обязательная ориентация для камеры.</span><span class="sxs-lookup"><span data-stu-id="1e399-108">A mandatory orientation for the camera is not specified.</span></span><br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <span data-ttu-id="1e399-109"><dt>**Винбио \_ \_Альбомная ориентация**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1e399-109"><dt>**WINBIO\_ORIENTATION\_LANDSCAPE**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="1e399-110">Для камеры требуется альбомная ориентация.</span><span class="sxs-lookup"><span data-stu-id="1e399-110">The landscape orientation is required for the camera.</span></span><br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <span data-ttu-id="1e399-111"><dt>**Винбио \_ ОРИЕНТАЦИЯ \_ Книжная**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1e399-111"><dt>**WINBIO\_ORIENTATION\_PORTRAIT**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="1e399-112">Для камеры требуется книжная ориентация.</span><span class="sxs-lookup"><span data-stu-id="1e399-112">The portrait orientation is required for the camera.</span></span><br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <span data-ttu-id="1e399-113"><dt>**Винбио \_ ОРИЕНТАЦИЯ \_**</dt> — <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1e399-113"><dt>**WINBIO\_ORIENTATION\_ANY**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="1e399-114">Для камеры разрешена любая ориентация.</span><span class="sxs-lookup"><span data-stu-id="1e399-114">Any orientation is permitted for the camera.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="1e399-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1e399-115">Requirements</span></span>



| <span data-ttu-id="1e399-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1e399-116">Requirement</span></span> | <span data-ttu-id="1e399-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1e399-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e399-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e399-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e399-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1e399-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="1e399-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e399-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e399-121">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="1e399-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="1e399-122">Header</span><span class="sxs-lookup"><span data-stu-id="1e399-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e399-123"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="1e399-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e399-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e399-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e399-125">**\_ \_ сведения о расширенном ДАТЧИКе винбио \_**</span><span class="sxs-lookup"><span data-stu-id="1e399-125">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





