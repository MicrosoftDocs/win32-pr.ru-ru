---
description: '\_Константы битового флага линеофферингмоде (TAPI версии 1,4 и более поздние) описывают различные подсостояния вызова предложения.'
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Константы LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689176"
---
# <a name="lineofferingmode_-constants"></a><span data-ttu-id="ef675-103">\_Константы линеофферингмоде</span><span class="sxs-lookup"><span data-stu-id="ef675-103">LINEOFFERINGMODE\_ Constants</span></span>

<span data-ttu-id="ef675-104">Константы битового флага **линеофферингмоде \_** (TAPI версии 1,4 и более поздние) описывают различные подсостояния вызова предложения.</span><span class="sxs-lookup"><span data-stu-id="ef675-104">The **LINEOFFERINGMODE\_** bit-flag constants (TAPI versions 1.4 and later) describe different substates of an offering call.</span></span> <span data-ttu-id="ef675-105">Режим будет доступен в виде состояния вызова для приложения после трданситионс состояния вызова и в [**строке \_ каллстате**](line-callstate.md) , указывающей на вызов линекаллстате \_ .</span><span class="sxs-lookup"><span data-stu-id="ef675-105">A mode is available as call status to the application after the call state trdansitions to offering, and within the [**LINE\_CALLSTATE**](line-callstate.md) message indicating the call is in LINECALLSTATE\_OFFERING.</span></span> <span data-ttu-id="ef675-106">Эти значения используются, когда вызов осуществляется на адресе, который является общим (передается через мост) с другими станциями (см. [**\_ константы линеаддрессшаринг**](lineaddresssharing--constants.md)), в первую очередь на электронные ключевые системы.</span><span class="sxs-lookup"><span data-stu-id="ef675-106">These values are used when the call is on an address that is shared (bridged) with other stations (see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span>

<dl> <dt>

<span data-ttu-id="ef675-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**ЛИНЕОФФЕРИНГМОДЕ \_ Active**</span><span class="sxs-lookup"><span data-stu-id="ef675-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef675-108">Указывает, что вызов уведомляется на текущей станции (будет сопровождаться ЛИНЕДЕВСТАТЕными \_ сообщениями), и если какое-либо приложение настроено на автоматический ответ, это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="ef675-108">Indicates that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="ef675-109">Если режим вызова равен нулю, приложение должно предположить, что значение активно (это может быть ситуация на немостном адресе).</span><span class="sxs-lookup"><span data-stu-id="ef675-109">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="ef675-110">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="ef675-110">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef675-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**ЛИНЕОФФЕРИНГМОДЕ \_ неактивен**</span><span class="sxs-lookup"><span data-stu-id="ef675-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef675-112">Указывает, что вызов предлагается на нескольких станциях, но текущая станция не является оповещением (например, это может быть станция помощника, где состояние предложения — это Совет, например мигающий лампочку); программное обеспечение на станции, настроенном для автоматического ответа, предпочтительно не отвечать на вызов, так как это должно быть прерогативе на основной станции (оповещение), но для соединения вызова может использоваться [**линеансвер**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) .</span><span class="sxs-lookup"><span data-stu-id="ef675-112">Indicates that the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) may be used to connect the call.</span></span> <span data-ttu-id="ef675-113">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="ef675-113">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef675-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef675-114">Remarks</span></span>

<span data-ttu-id="ef675-115">Не расширяемый.</span><span class="sxs-lookup"><span data-stu-id="ef675-115">Not extensible.</span></span> <span data-ttu-id="ef675-116">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="ef675-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="ef675-117">Для обеспечения обратной совместимости поставщик услуг должен проверить согласованную версию API в строке и не использовать эти значения ЛИНЕОФФЕРИНГМОДЕ, \_ если они не поддерживаются в согласованной версии.</span><span class="sxs-lookup"><span data-stu-id="ef675-117">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEOFFERINGMODE\_ values if they are not supported on the negotiated version.</span></span> <span data-ttu-id="ef675-118">Приложения, которые не компания cognizant ЛИНЕОФФЕРИНГМОДЕ, \_ скорее всего, предполагают, что вызов, находящиеся в \_ ПРЕДЛОЖЕНии линекаллстате, находится в линеофферингмоде \_ Active.</span><span class="sxs-lookup"><span data-stu-id="ef675-118">Applications that are not cognizant of LINEOFFERINGMODE\_ will most likely assume that a call that is in LINECALLSTATE\_OFFERING is in LINEOFFERINGMODE\_ACTIVE.</span></span>

<span data-ttu-id="ef675-119">Неактивные \_ значения линеофферингмоде Active и линеофферингмоде \_ используются, когда вызов осуществляется на адресе, который используется совместно с другими станциями (с мостом; см. [ \_ константы линеаддрессшаринг](lineaddresssharing--constants.md)), в первую очередь на электронные ключевые системы.</span><span class="sxs-lookup"><span data-stu-id="ef675-119">The LINEOFFERINGMODE\_ACTIVE and LINEOFFERINGMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [LINEADDRESSSHARING\_ Constants](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="ef675-120">Если для параметра Состояние вызова предложения задано значение "активно", это означает, что вызов уведомляется на текущей станции (он будет сопровождаться ЛИНЕДЕВСТАТЕными \_ сообщениями), и если какое-либо приложение настроено на автоматический ответ, это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="ef675-120">If the offering call state mode is "active," it means that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="ef675-121">Если режим вызова имеет состояние "Неактивный", вызов предлагается на нескольких станциях, но текущая станция не является оповещением (например, это может быть станция помощника, где состояние предложения — это Совет, например мигающий источник); программное обеспечение на станции, настроенном для автоматического ответа, предпочтительно не отвечать на вызов, так как это должно быть прерогативе на основной станции (оповещение), но для соединения вызова можно использовать [**линеансвер**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) .</span><span class="sxs-lookup"><span data-stu-id="ef675-121">If the call state mode is "inactive," the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) can be used to connect the call.</span></span> <span data-ttu-id="ef675-122">Если режим вызова равен нулю, приложение должно предположить, что значение активно (это может быть ситуация на немостном адресе).</span><span class="sxs-lookup"><span data-stu-id="ef675-122">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef675-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ef675-123">Requirements</span></span>



| <span data-ttu-id="ef675-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ef675-124">Requirement</span></span> | <span data-ttu-id="ef675-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ef675-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ef675-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ef675-126">TAPI version</span></span><br/> | <span data-ttu-id="ef675-127">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ef675-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ef675-128">Header</span><span class="sxs-lookup"><span data-stu-id="ef675-128">Header</span></span><br/>       | <dl> <span data-ttu-id="ef675-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef675-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




