---
description: Не удалось выполнить асинхронную команду для выполнения графа.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674961"
---
# <a name="ec_error_stillplaying"></a><span data-ttu-id="bc3bd-103">EC \_ об ошибке \_ стиллплайинг</span><span class="sxs-lookup"><span data-stu-id="bc3bd-103">EC\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="bc3bd-104">Не удалось выполнить асинхронную команду для выполнения графа.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-104">An asynchronous command to run the graph has failed.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc3bd-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc3bd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc3bd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bc3bd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bc3bd-107">(**HRESULT**) Код ошибки операции, которая завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="bc3bd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bc3bd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bc3bd-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="bc3bd-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bc3bd-110">Default Action</span></span>

<span data-ttu-id="bc3bd-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc3bd-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="bc3bd-112">Remarks</span></span>

<span data-ttu-id="bc3bd-113">Если диспетчер графа фильтров выдает команду асинхронного выполнения, которая завершается ошибкой, она отправляет это событие в приложение.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-113">If the filter graph manager issues an asynchronous run command that fails, it sends this event to the application.</span></span> <span data-ttu-id="bc3bd-114">Граф остается в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-114">The graph remains in a running state.</span></span> <span data-ttu-id="bc3bd-115">Состояние базовых фильтров не определено.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-115">The state of the underlying filters is indeterminate.</span></span> <span data-ttu-id="bc3bd-116">Некоторые фильтры могут выполняться, другие могут не иметь.</span><span class="sxs-lookup"><span data-stu-id="bc3bd-116">Some filters might be running, others might not.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc3bd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bc3bd-117">Requirements</span></span>



| <span data-ttu-id="bc3bd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bc3bd-118">Requirement</span></span> | <span data-ttu-id="bc3bd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bc3bd-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3bd-120">Header</span><span class="sxs-lookup"><span data-stu-id="bc3bd-120">Header</span></span><br/> | <dl> <span data-ttu-id="bc3bd-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc3bd-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc3bd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc3bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3bd-123">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="bc3bd-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bc3bd-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc3bd-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




