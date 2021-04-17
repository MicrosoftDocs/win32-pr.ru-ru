---
description: '\_Константы побитового флага линекаллпривилеже описывают типы прав доступа или привилегий, которыми может обладать приложение с маркером вызова для соответствующего вызова.'
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: Константы LINECALLPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679905"
---
# <a name="linecallprivilege_-constants"></a><span data-ttu-id="be7f8-103">\_Константы линекаллпривилеже</span><span class="sxs-lookup"><span data-stu-id="be7f8-103">LINECALLPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="be7f8-104">Константы побитового флага **линекаллпривилеже \_** описывают типы прав доступа или привилегий, которыми может обладать приложение с маркером вызова для соответствующего вызова.</span><span class="sxs-lookup"><span data-stu-id="be7f8-104">The **LINECALLPRIVILEGE\_** bit-flag constants describe the kinds of access rights or privileges an application with a call handle may have to the corresponding call.</span></span>

<dl> <dt>

<span data-ttu-id="be7f8-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**\_монитор линекаллпривилеже**</span><span class="sxs-lookup"><span data-stu-id="be7f8-105"><span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**LINECALLPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be7f8-106">Приложение имеет права монитора для вызова.</span><span class="sxs-lookup"><span data-stu-id="be7f8-106">The application has monitor privileges to the call.</span></span> <span data-ttu-id="be7f8-107">Эти привилегии позволяют приложению отслеживать изменения состояния, сведения о запросе и состояние вызова.</span><span class="sxs-lookup"><span data-stu-id="be7f8-107">These privileges allow the application to monitor state changes and query information and status about the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be7f8-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**ЛИНЕКАЛЛПРИВИЛЕЖЕ \_ None**</span><span class="sxs-lookup"><span data-stu-id="be7f8-108"><span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be7f8-109">Приложение не имеет прав доступа к вызову.</span><span class="sxs-lookup"><span data-stu-id="be7f8-109">The application has no privileges to the call.</span></span> <span data-ttu-id="be7f8-110">Маркер приложения является пустым и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="be7f8-110">The application's handle is void and should not be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be7f8-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**\_владелец линекаллпривилеже**</span><span class="sxs-lookup"><span data-stu-id="be7f8-111"><span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="be7f8-112">Приложение имеет права владельца для вызова.</span><span class="sxs-lookup"><span data-stu-id="be7f8-112">The application has owner privileges to the call.</span></span> <span data-ttu-id="be7f8-113">Эти привилегии позволяют приложению манипулировать вызовом способами, влияющими на состояние вызова.</span><span class="sxs-lookup"><span data-stu-id="be7f8-113">These privileges allow the application to manipulate the call in ways that affect the state of the call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be7f8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be7f8-114">Remarks</span></span>

<span data-ttu-id="be7f8-115">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="be7f8-115">No extensibility.</span></span> <span data-ttu-id="be7f8-116">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="be7f8-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="be7f8-117">При первом запуске обработчика вызова для приложения или при каждом изменении привилегий вызова этого приложения в приложение отправляется сообщение [**Line \_ каллстате**](line-callstate.md) .</span><span class="sxs-lookup"><span data-stu-id="be7f8-117">When a call handle is first provided to an application or whenever call privileges of that application are modified, the [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="be7f8-118">Когда приложение передает вызов, и если у принимающего приложения еще нет маркера с правами владельца, это сообщение информирует приложение о новых привилегиях на вызов.</span><span class="sxs-lookup"><span data-stu-id="be7f8-118">When an application hands off a call, and if the receiving application does not already have a handle with owner privileges, then this message informs the application about its new privileges to the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7f8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="be7f8-119">Requirements</span></span>



| <span data-ttu-id="be7f8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="be7f8-120">Requirement</span></span> | <span data-ttu-id="be7f8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="be7f8-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="be7f8-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="be7f8-122">TAPI version</span></span><br/> | <span data-ttu-id="be7f8-123">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="be7f8-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="be7f8-124">Header</span><span class="sxs-lookup"><span data-stu-id="be7f8-124">Header</span></span><br/>       | <dl> <span data-ttu-id="be7f8-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7f8-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




