---
description: '\_Константы побитового флага линекаллхубтраккинг описывают тип предоставляемого отслеживания концентратора вызовов.'
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Константы LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675455"
---
# <a name="linecallhubtracking_-constants"></a><span data-ttu-id="587da-103">\_Константы линекаллхубтраккинг</span><span class="sxs-lookup"><span data-stu-id="587da-103">LINECALLHUBTRACKING\_ Constants</span></span>

<span data-ttu-id="587da-104">Константы побитового флага **линекаллхубтраккинг \_** описывают тип предоставляемого отслеживания концентратора вызовов.</span><span class="sxs-lookup"><span data-stu-id="587da-104">The **LINECALLHUBTRACKING\_** bit-flag constants describe the type of call hub tracking provided.</span></span>

<dl> <dt>

<span data-ttu-id="587da-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**ЛИНЕКАЛЛХУБТРАККИНГ \_ аллкаллс**</span><span class="sxs-lookup"><span data-stu-id="587da-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING\_ALLCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="587da-106">Отслеживание концентратора вызовов предоставляется на уровне вызовов.</span><span class="sxs-lookup"><span data-stu-id="587da-106">Call hub tracking is provided at the call level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="587da-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**ЛИНЕКАЛЛХУБТРАККИНГ \_ None**</span><span class="sxs-lookup"><span data-stu-id="587da-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="587da-108">Отслеживание концентратора вызовов не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="587da-108">No call hub tracking is provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="587da-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**ЛИНЕКАЛЛХУБТРАККИНГ \_ провидерлевел**</span><span class="sxs-lookup"><span data-stu-id="587da-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING\_PROVIDERLEVEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="587da-110">Концентраторы вызовов отправляются на уровне поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="587da-110">Call hubs are tracked at the service provider level.</span></span> <span data-ttu-id="587da-111">Не передаются сведения о вызове с помощью изменений вызова.</span><span class="sxs-lookup"><span data-stu-id="587da-111">Call by call changes are not reported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="587da-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="587da-112">Remarks</span></span>

<span data-ttu-id="587da-113">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="587da-113">No extensibility.</span></span> <span data-ttu-id="587da-114">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="587da-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="587da-115">Когда в этой структуре данных происходят изменения, в приложение отправляется сообщение [**Line \_ каллинфо**](line-callinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="587da-115">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="587da-116">Параметры этого сообщения являются маркером вызова и указанием измененного информационного элемента.</span><span class="sxs-lookup"><span data-stu-id="587da-116">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="587da-117">Структура данных [**линекаллхубтраккингинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) указывает, какой тип отслеживания предоставляется.</span><span class="sxs-lookup"><span data-stu-id="587da-117">The [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) data structure indicates which tracking type is provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="587da-118">Требования</span><span class="sxs-lookup"><span data-stu-id="587da-118">Requirements</span></span>



| <span data-ttu-id="587da-119">Требование</span><span class="sxs-lookup"><span data-stu-id="587da-119">Requirement</span></span> | <span data-ttu-id="587da-120">Значение</span><span class="sxs-lookup"><span data-stu-id="587da-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="587da-121">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="587da-121">TAPI version</span></span><br/> | <span data-ttu-id="587da-122">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="587da-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="587da-123">Header</span><span class="sxs-lookup"><span data-stu-id="587da-123">Header</span></span><br/>       | <dl> <span data-ttu-id="587da-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="587da-124"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="587da-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="587da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587da-126">**Строка \_ каллинфо**</span><span class="sxs-lookup"><span data-stu-id="587da-126">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="587da-127">**линекаллхубтраккингинфо**</span><span class="sxs-lookup"><span data-stu-id="587da-127">**LINECALLHUBTRACKINGINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[<span data-ttu-id="587da-128">**линекаллинфо**</span><span class="sxs-lookup"><span data-stu-id="587da-128">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




