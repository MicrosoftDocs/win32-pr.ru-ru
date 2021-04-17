---
description: '\_Константы побитового флага линероаммоде описывают состояние роуминга для линейного устройства.'
ms.assetid: af0eb263-8deb-44ab-8acb-00e4ff7930ab
title: Константы LINEROAMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e40c40291567e7800b53070f882bf1e0bdac93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685376"
---
# <a name="lineroammode_-constants"></a><span data-ttu-id="8639b-103">\_Константы линероаммоде</span><span class="sxs-lookup"><span data-stu-id="8639b-103">LINEROAMMODE\_ Constants</span></span>

<span data-ttu-id="8639b-104">Константы побитового флага **линероаммоде \_** описывают состояние роуминга для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="8639b-104">The **LINEROAMMODE\_** bit-flag constants describe the roaming status of a line device.</span></span>

<dl> <dt>

<span data-ttu-id="8639b-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**\_Домашняя страница линероаммоде**</span><span class="sxs-lookup"><span data-stu-id="8639b-105"><span id="LINEROAMMODE_HOME"></span><span id="lineroammode_home"></span>**LINEROAMMODE\_HOME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8639b-106">Линия подключена к узлу домашней сети.</span><span class="sxs-lookup"><span data-stu-id="8639b-106">The line is connected to the home network node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8639b-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**ЛИНЕРОАММОДЕ \_ перемещаемый**</span><span class="sxs-lookup"><span data-stu-id="8639b-107"><span id="LINEROAMMODE_ROAMA"></span><span id="lineroammode_roama"></span>**LINEROAMMODE\_ROAMA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8639b-108">Линия подключается к роумингу, и звонки начисляются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8639b-108">The line is connected to the Roam-A carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8639b-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**ЛИНЕРОАММОДЕ \_ роамб**</span><span class="sxs-lookup"><span data-stu-id="8639b-109"><span id="LINEROAMMODE_ROAMB"></span><span id="lineroammode_roamb"></span>**LINEROAMMODE\_ROAMB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8639b-110">Линия подключена к перевозчику роуминга, а звонки начисляются соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8639b-110">The line is connected to the Roam-B carrier and calls are charged accordingly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8639b-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**ЛИНЕРОАММОДЕ \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="8639b-111"><span id="LINEROAMMODE_UNAVAIL"></span><span id="lineroammode_unavail"></span>**LINEROAMMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8639b-112">Режим перемещения недоступен и не будет известен.</span><span class="sxs-lookup"><span data-stu-id="8639b-112">The roam mode is unavailable and will not be known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8639b-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**ЛИНЕРОАММОДЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="8639b-113"><span id="LINEROAMMODE_UNKNOWN"></span><span id="lineroammode_unknown"></span>**LINEROAMMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8639b-114">Режим перемещения в настоящее время неизвестен, но может быть известен позже.</span><span class="sxs-lookup"><span data-stu-id="8639b-114">The roam mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8639b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8639b-115">Remarks</span></span>

<span data-ttu-id="8639b-116">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="8639b-116">No extensibility.</span></span> <span data-ttu-id="8639b-117">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="8639b-117">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="8639b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8639b-118">Requirements</span></span>



| <span data-ttu-id="8639b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8639b-119">Requirement</span></span> | <span data-ttu-id="8639b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8639b-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8639b-121">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8639b-121">TAPI version</span></span><br/> | <span data-ttu-id="8639b-122">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8639b-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8639b-123">Header</span><span class="sxs-lookup"><span data-stu-id="8639b-123">Header</span></span><br/>       | <dl> <span data-ttu-id="8639b-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8639b-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




