---
description: '\_Константы битового флага линекаллкомплмоде описывают различные способы выполнения вызова.'
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Константы LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685422"
---
# <a name="linecallcomplmode_-constants"></a><span data-ttu-id="712b2-103">\_Константы линекаллкомплмоде</span><span class="sxs-lookup"><span data-stu-id="712b2-103">LINECALLCOMPLMODE\_ Constants</span></span>

<span data-ttu-id="712b2-104">Константы битового флага **линекаллкомплмоде \_** описывают различные способы выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="712b2-104">The **LINECALLCOMPLMODE\_** bit-flag constants describe different ways in which a call can be completed.</span></span>

<dl> <dt>

<span data-ttu-id="712b2-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_обратный вызов линекаллкомплмоде**</span><span class="sxs-lookup"><span data-stu-id="712b2-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="712b2-106">Запрашивает вызываемую станцию для возврата вызова, когда она возвращается в режим простоя.</span><span class="sxs-lookup"><span data-stu-id="712b2-106">Requests the called station to return the call when it returns to idle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="712b2-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**ЛИНЕКАЛЛКОМПЛМОДЕ \_ кампон**</span><span class="sxs-lookup"><span data-stu-id="712b2-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE\_CAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="712b2-108">Ставит в очередь вызов до завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="712b2-108">Queues the call until the call can be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="712b2-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**ЛИНЕКАЛЛКОМПЛМОДЕ \_ атака**</span><span class="sxs-lookup"><span data-stu-id="712b2-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="712b2-110">Добавляет приложение к существующему вызову на вызываемой станции (барже в).</span><span class="sxs-lookup"><span data-stu-id="712b2-110">Adds the application to the existing call at the called station (barge in).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="712b2-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_сообщение линекаллкомплмоде**</span><span class="sxs-lookup"><span data-stu-id="712b2-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="712b2-112">Оставляет короткое предопределенное сообщение для вызываемой станции (оставьте слово вызов).</span><span class="sxs-lookup"><span data-stu-id="712b2-112">Leaves a short predefined message for the called station (Leave Word Calling).</span></span> <span data-ttu-id="712b2-113">Отправляемое сообщение указывается отдельно.</span><span class="sxs-lookup"><span data-stu-id="712b2-113">The message to be sent is specified separately.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="712b2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="712b2-114">Remarks</span></span>

<span data-ttu-id="712b2-115">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="712b2-115">No extensibility.</span></span> <span data-ttu-id="712b2-116">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="712b2-116">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="712b2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="712b2-117">Requirements</span></span>



| <span data-ttu-id="712b2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="712b2-118">Requirement</span></span> | <span data-ttu-id="712b2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="712b2-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="712b2-120">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="712b2-120">TAPI version</span></span><br/> | <span data-ttu-id="712b2-121">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="712b2-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="712b2-122">Header</span><span class="sxs-lookup"><span data-stu-id="712b2-122">Header</span></span><br/>       | <dl> <span data-ttu-id="712b2-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="712b2-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




