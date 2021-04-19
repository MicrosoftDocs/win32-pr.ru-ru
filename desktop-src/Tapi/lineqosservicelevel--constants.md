---
description: Эти константы используются TSP для выяснения типа требуемого уровня качества обслуживания (Quality Service).
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Константы LINEQOSSERVICELEVEL_ (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689172"
---
# <a name="lineqosservicelevel_-constants"></a><span data-ttu-id="de24f-103">\_Константы линекоссервицелевел</span><span class="sxs-lookup"><span data-stu-id="de24f-103">LINEQOSSERVICELEVEL\_ Constants</span></span>

<span data-ttu-id="de24f-104">Эти константы используются TSP для выяснения типа требуемого уровня качества обслуживания (Quality Service).</span><span class="sxs-lookup"><span data-stu-id="de24f-104">These constants are used by a TSP to identify the type of a QoS (Quality of Service) level required.</span></span>

<dl> <dt>

<span data-ttu-id="de24f-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**\_требуется линекоссервицелевел**</span><span class="sxs-lookup"><span data-stu-id="de24f-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="de24f-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="de24f-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="de24f-107">Запрошенный уровень качества обслуживания является обязательным.</span><span class="sxs-lookup"><span data-stu-id="de24f-107">The quality of service level requested is a requirement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de24f-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**ЛИНЕКОССЕРВИЦЕЛЕВЕЛ \_ ифаваилабле**</span><span class="sxs-lookup"><span data-stu-id="de24f-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL\_IFAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="de24f-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="de24f-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="de24f-110">Требуемый уровень качества обслуживания, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="de24f-110">The quality of service level required, if available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="de24f-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**ЛИНЕКОССЕРВИЦЕЛЕВЕЛ \_ бестеффорт**</span><span class="sxs-lookup"><span data-stu-id="de24f-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL\_BESTEFFORT**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="de24f-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="de24f-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="de24f-113">Требуемый уровень качества обслуживания — «лучшие усилия».</span><span class="sxs-lookup"><span data-stu-id="de24f-113">The quality of service level required is "best effort."</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de24f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="de24f-114">Requirements</span></span>



| <span data-ttu-id="de24f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="de24f-115">Requirement</span></span> | <span data-ttu-id="de24f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="de24f-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="de24f-117">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="de24f-117">TAPI version</span></span><br/> | <span data-ttu-id="de24f-118">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="de24f-118">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="de24f-119">Header</span><span class="sxs-lookup"><span data-stu-id="de24f-119">Header</span></span><br/>       | <dl> <span data-ttu-id="de24f-120"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="de24f-120"><dt>Tspi.h</dt></span></span> </dl> |



 

 




