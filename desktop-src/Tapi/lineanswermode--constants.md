---
description: '\_Константы побитового флага линеансвермоде описывают, как действует существующий активный вызов на устройстве линии, отвечая на вызов другого предложения в той же строке.'
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Константы LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679908"
---
# <a name="lineanswermode_-constants"></a><span data-ttu-id="f9661-103">\_Константы линеансвермоде</span><span class="sxs-lookup"><span data-stu-id="f9661-103">LINEANSWERMODE\_ Constants</span></span>

<span data-ttu-id="f9661-104">Константы побитового флага **линеансвермоде \_** описывают, как действует существующий активный вызов на устройстве линии, отвечая на вызов другого *предложения* в той же строке.</span><span class="sxs-lookup"><span data-stu-id="f9661-104">The **LINEANSWERMODE\_** bit-flag constants describe how an existing active call on a line device is affected by answering another *offering* call on the same line.</span></span>

<dl> <dt>

<span data-ttu-id="f9661-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**ЛИНЕАНСВЕРМОДЕ \_ DROP**</span><span class="sxs-lookup"><span data-stu-id="f9661-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f9661-106">Текущий активный вызов будет автоматически удален.</span><span class="sxs-lookup"><span data-stu-id="f9661-106">The currently active call will automatically be dropped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9661-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**ЛИНЕАНСВЕРМОДЕ \_ удержание**</span><span class="sxs-lookup"><span data-stu-id="f9661-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE\_HOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f9661-108">Текущий активный вызов будет автоматически помещен в удержание.</span><span class="sxs-lookup"><span data-stu-id="f9661-108">The currently active call will automatically be placed on hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9661-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**ЛИНЕАНСВЕРМОДЕ \_ None**</span><span class="sxs-lookup"><span data-stu-id="f9661-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f9661-110">Ответ на другой вызов в той же строке не влияет на существующий активный вызов в строке.</span><span class="sxs-lookup"><span data-stu-id="f9661-110">Answering another call on the same line has no effect on the existing active call on the line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9661-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9661-111">Remarks</span></span>

<span data-ttu-id="f9661-112">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="f9661-112">No extensibility.</span></span> <span data-ttu-id="f9661-113">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="f9661-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="f9661-114">Если вызов поступает в (предлагается) в момент, когда другой вызов уже активен, то новый вызов подключается с помощью вызова [**линеансвер**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="f9661-114">If a call comes in (is offered) at the time another call is already active, the new call is connected to by invoking [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="f9661-115">Воздействие на существующий активный вызов зависит от возможностей устройства линии.</span><span class="sxs-lookup"><span data-stu-id="f9661-115">The effect this has on the existing active call depends on the line's device capabilities.</span></span> <span data-ttu-id="f9661-116">Первый вызов может быть нетронут, он может быть автоматически удален или автоматически помещен в удержание.</span><span class="sxs-lookup"><span data-stu-id="f9661-116">The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9661-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f9661-117">Requirements</span></span>



| <span data-ttu-id="f9661-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f9661-118">Requirement</span></span> | <span data-ttu-id="f9661-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f9661-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f9661-120">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f9661-120">TAPI version</span></span><br/> | <span data-ttu-id="f9661-121">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f9661-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f9661-122">Header</span><span class="sxs-lookup"><span data-stu-id="f9661-122">Header</span></span><br/>       | <dl> <span data-ttu-id="f9661-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9661-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




