---
description: '\_Константы побитового флага линеспеЦиалинфо описывают специальные информационные сигналы, которые сеть может использовать для сообщения различных операций создания отчетов и наблюдения за сетями.'
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Константы LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675311"
---
# <a name="linespecialinfo_-constants"></a><span data-ttu-id="a2648-103">\_Константы линеспеЦиалинфо</span><span class="sxs-lookup"><span data-stu-id="a2648-103">LINESPECIALINFO\_ Constants</span></span>

<span data-ttu-id="a2648-104">Константы побитового флага **линеспеЦиалинфо \_** описывают специальные информационные сигналы, которые сеть может использовать для сообщения различных операций создания отчетов и наблюдения за сетями.</span><span class="sxs-lookup"><span data-stu-id="a2648-104">The **LINESPECIALINFO\_** bit-flag constants describes special information signals that the network can use to report various reporting and network observation operations.</span></span> <span data-ttu-id="a2648-105">Они являются специальными закодированными последовательностями, передаваемыми в начале сетевых рекомендаций, зарегистрированных извещений.</span><span class="sxs-lookup"><span data-stu-id="a2648-105">They are special coded tone sequences transmitted at the beginning of network advisory recorded announcements.</span></span>

<dl> <dt>

<span data-ttu-id="a2648-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**ЛИНЕСПЕЦИАЛИНФО \_ кустиррег**</span><span class="sxs-lookup"><span data-stu-id="a2648-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO\_CUSTIRREG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2648-107">Этот Специальный звуковой сигнал предшествует вакантному номеру, AIS, Центрекс номеру и нерабочему исполнителю, коду доступа не набран или не набран в результате ошибки или к сообщению оператора перехвата вручную (категория неравномерности клиентов).</span><span class="sxs-lookup"><span data-stu-id="a2648-107">This special information tone precedes a vacant number, AIS, Centrex number change and nonworking station, access code not dialed or dialed in error, or manual intercept operator message (customer irregularity category).</span></span> <span data-ttu-id="a2648-108">ЛИНЕСПЕЦИАЛИНФО \_ кустиррег также сообщает о том, что сведения о выставлении счетов отклонены, и когда набранный адрес заблокирован на коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="a2648-108">LINESPECIALINFO\_CUSTIRREG is also reported when billing information is rejected and when the dialed address is blocked at the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2648-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**ЛИНЕСПЕЦИАЛИНФО \_**</span><span class="sxs-lookup"><span data-stu-id="a2648-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO\_NOCIRCUIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2648-110">Этот Специальный звуковой сигнал предшествует отсутствию цепи или аварийному объявлению (категории блокировки магистрали).</span><span class="sxs-lookup"><span data-stu-id="a2648-110">This special information tone precedes a no circuit or an emergency announcement (trunk blockage category).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2648-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**переупорядочить ЛИНЕСПЕЦИАЛИНФО \_**</span><span class="sxs-lookup"><span data-stu-id="a2648-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO\_REORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2648-112">Этот Специальный звуковой сигнал предшествует объявлению о переупорядочении (категория неравномерности оборудования).</span><span class="sxs-lookup"><span data-stu-id="a2648-112">This special information tone precedes a reorder announcement (equipment irregularity category).</span></span> <span data-ttu-id="a2648-113">\_ПЕРЕупорядочение линеспеЦиалинфо также сообщается, когда телефон оффхук слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="a2648-113">LINESPECIALINFO\_REORDER is also reported when the telephone is kept offhook too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2648-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**ЛИНЕСПЕЦИАЛИНФО \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="a2648-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2648-115">Особенности Специального звукового сигнала недоступны и не будут известны.</span><span class="sxs-lookup"><span data-stu-id="a2648-115">Specifics about the special information tone are unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2648-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**ЛИНЕСПЕЦИАЛИНФО \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="a2648-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a2648-117">Особенности особого звукового сигнала в настоящее время неизвестны, но могут быть известны позже.</span><span class="sxs-lookup"><span data-stu-id="a2648-117">Specifics about the special information tone are currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2648-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2648-118">Remarks</span></span>

<span data-ttu-id="a2648-119">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="a2648-119">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="a2648-120">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="a2648-120">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="a2648-121">Специальные информационные тона определяются для вспомогательных сообщений и обычно не используются для выставления счетов или для руководителей.</span><span class="sxs-lookup"><span data-stu-id="a2648-121">Special information tones are defined for advisory messages and are not normally used for billing or supervisory purpose.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2648-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a2648-122">Requirements</span></span>



| <span data-ttu-id="a2648-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a2648-123">Requirement</span></span> | <span data-ttu-id="a2648-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a2648-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a2648-125">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a2648-125">TAPI version</span></span><br/> | <span data-ttu-id="a2648-126">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a2648-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a2648-127">Header</span><span class="sxs-lookup"><span data-stu-id="a2648-127">Header</span></span><br/>       | <dl> <span data-ttu-id="a2648-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2648-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




