---
description: '\_Константы линетонемоде описывают различные варианты выбора, используемые при создании тонов линий.'
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Константы LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685206"
---
# <a name="linetonemode_-constants"></a><span data-ttu-id="70a0e-103">\_Константы линетонемоде</span><span class="sxs-lookup"><span data-stu-id="70a0e-103">LINETONEMODE\_ Constants</span></span>

<span data-ttu-id="70a0e-104">**\_ Константы линетонемоде** описывают различные варианты выбора, используемые при создании тонов линий.</span><span class="sxs-lookup"><span data-stu-id="70a0e-104">The **LINETONEMODE\_ constants** describe different selections that are used when generating line tones.</span></span>

<dl> <dt>

<span data-ttu-id="70a0e-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**\_звуковой сигнал линетонемоде**</span><span class="sxs-lookup"><span data-stu-id="70a0e-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE\_BEEP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="70a0e-106">Гудок — это звуковой сигнал, который используется для объявления начала записи.</span><span class="sxs-lookup"><span data-stu-id="70a0e-106">The tone is a beep, such as that used to announce the beginning of a recording.</span></span> <span data-ttu-id="70a0e-107">Точное определение определяется поставщиком службы.</span><span class="sxs-lookup"><span data-stu-id="70a0e-107">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70a0e-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**\_выставление счетов линетонемоде**</span><span class="sxs-lookup"><span data-stu-id="70a0e-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE\_BILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="70a0e-109">Гудок — это гудок информации о выставлении счетов, например сигнал запроса кредитной карты.</span><span class="sxs-lookup"><span data-stu-id="70a0e-109">The tone is a billing information tone such as a credit card prompt tone.</span></span> <span data-ttu-id="70a0e-110">Точное определение определяется поставщиком службы.</span><span class="sxs-lookup"><span data-stu-id="70a0e-110">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70a0e-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**ЛИНЕТОНЕМОДЕ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="70a0e-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="70a0e-112">Гудок — это занятый тон.</span><span class="sxs-lookup"><span data-stu-id="70a0e-112">The tone is a busy tone.</span></span> <span data-ttu-id="70a0e-113">Точное определение определяется поставщиком службы.</span><span class="sxs-lookup"><span data-stu-id="70a0e-113">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70a0e-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**ЛИНЕТОНЕМОДЕ \_ настраиваемый**</span><span class="sxs-lookup"><span data-stu-id="70a0e-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="70a0e-115">Тон — это пользовательский тон, определяемый по частоте его компонентов, типа [**линеженератетоне**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span><span class="sxs-lookup"><span data-stu-id="70a0e-115">The tone is a custom tone defined by its component frequencies, of type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70a0e-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**ЛИНЕТОНЕМОДЕ \_ звонка**</span><span class="sxs-lookup"><span data-stu-id="70a0e-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="70a0e-117">Тон — звонка тон.</span><span class="sxs-lookup"><span data-stu-id="70a0e-117">The tone is ringback tone.</span></span> <span data-ttu-id="70a0e-118">Точное определение определяется поставщиком службы.</span><span class="sxs-lookup"><span data-stu-id="70a0e-118">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70a0e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70a0e-119">Remarks</span></span>

<span data-ttu-id="70a0e-120">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="70a0e-120">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="70a0e-121">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="70a0e-121">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="70a0e-122">Эти константы используются для определения тонов, которые будут создаваться в нестандартном виде при вызове удаленной стороны.</span><span class="sxs-lookup"><span data-stu-id="70a0e-122">These constants are used to define tones to be generated inband over a call to the remote party.</span></span> <span data-ttu-id="70a0e-123">Обратите внимание, что при обнаружении тона нестандартных тонов эти константы не используются.</span><span class="sxs-lookup"><span data-stu-id="70a0e-123">Note that tone detection of non-custom tones does not use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a0e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="70a0e-124">Requirements</span></span>



| <span data-ttu-id="70a0e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="70a0e-125">Requirement</span></span> | <span data-ttu-id="70a0e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="70a0e-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="70a0e-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="70a0e-127">TAPI version</span></span><br/> | <span data-ttu-id="70a0e-128">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="70a0e-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="70a0e-129">Header</span><span class="sxs-lookup"><span data-stu-id="70a0e-129">Header</span></span><br/>       | <dl> <span data-ttu-id="70a0e-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a0e-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




