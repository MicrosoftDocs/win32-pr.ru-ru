---
description: Категория датчика \_ \_ ALL представляет набор всех категорий датчиков, определенных платформой.
ms.assetid: e2d9fe6d-450a-446b-968b-0924116af6fe
title: SENSOR_CATEGORY_ALL (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2e5641e51dde130cc51d9b2fc35fcc1e158ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809263"
---
# <a name="sensor_category_all"></a><span data-ttu-id="bd2a1-103">\_Категория датчика \_ все</span><span class="sxs-lookup"><span data-stu-id="bd2a1-103">SENSOR\_CATEGORY\_ALL</span></span>

<span data-ttu-id="bd2a1-104">Категория датчика \_ \_ ALL представляет набор всех категорий датчиков, определенных платформой.</span><span class="sxs-lookup"><span data-stu-id="bd2a1-104">The SENSOR\_CATEGORY\_ALL category represents the set of all platform-defined sensor categories.</span></span>

<span data-ttu-id="bd2a1-105">**Ключи свойств, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="bd2a1-105">**Platform-Defined Property Keys**</span></span>

<span data-ttu-id="bd2a1-106">Ключи свойств, определяемые платформой для этой категории, основаны на \_ типе данных датчика \_ \_ общего \_ идентификатора GUID:</span><span class="sxs-lookup"><span data-stu-id="bd2a1-106">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_COMMON\_GUID:</span></span>

<span data-ttu-id="bd2a1-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span><span class="sxs-lookup"><span data-stu-id="bd2a1-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span></span>

<span data-ttu-id="bd2a1-108">В следующей таблице описаны определенные платформой поля данных.</span><span class="sxs-lookup"><span data-stu-id="bd2a1-108">The following table describes platform-defined data fields.</span></span>



| <span data-ttu-id="bd2a1-109">Имя поля данных и идентификатор процесса</span><span class="sxs-lookup"><span data-stu-id="bd2a1-109">Data field name and PID</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="bd2a1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bd2a1-110">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_TIMESTAMP"></span><span id="sensor_data_type_timestamp"></span><dl> <span data-ttu-id="bd2a1-111"><dt>**Датчик \_ \_Тип данных \_ timestamp**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="bd2a1-111"><dt>**SENSOR\_DATA\_TYPE\_TIMESTAMP**</dt> <dt>(PID = 2 ) </dt></span></span> </dl> | <span data-ttu-id="bd2a1-112">**VT \_ fileTime**</span><span class="sxs-lookup"><span data-stu-id="bd2a1-112">**VT\_FILETIME**</span></span><br/> <span data-ttu-id="bd2a1-113">Требуется для всех отчетов данных.</span><span class="sxs-lookup"><span data-stu-id="bd2a1-113">Required for all data reports.</span></span> <span data-ttu-id="bd2a1-114">Помечает каждый отчет данных с учетом времени создания отчета данных в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="bd2a1-114">Marks each data report with the time the data report was created in Coordinated Universal Time (UTC) format.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bd2a1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bd2a1-115">Requirements</span></span>



| <span data-ttu-id="bd2a1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bd2a1-116">Requirement</span></span> | <span data-ttu-id="bd2a1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bd2a1-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2a1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd2a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2a1-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bd2a1-119">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bd2a1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd2a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2a1-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bd2a1-121">None supported</span></span><br/>                                                            |
| <span data-ttu-id="bd2a1-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd2a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd2a1-123"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd2a1-123"><dt>Sensors.h</dt></span></span> </dl> |



 

 




