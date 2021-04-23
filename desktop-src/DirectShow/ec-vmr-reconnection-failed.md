---
description: Посылается VMR-7 и VMR-9, когда ему не удалось принять динамический запрос на изменение формата из восходящего декодера.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675546"
---
# <a name="ec_vmr_reconnection_failed"></a><span data-ttu-id="8f829-103">\_сбой при повторном подключении EC VMR \_ \_</span><span class="sxs-lookup"><span data-stu-id="8f829-103">EC\_VMR\_RECONNECTION\_FAILED</span></span>

<span data-ttu-id="8f829-104">Посылается VMR-7 и VMR-9, когда ему не удалось принять динамический запрос на изменение формата из восходящего декодера.</span><span class="sxs-lookup"><span data-stu-id="8f829-104">Sent by the VMR-7 and the VMR-9 when it was unable to accept a dynamic format change request from the upstream decoder.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f829-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f829-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f829-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8f829-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8f829-107">(**HRESULT**) Код состояния, возвращенный из [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) для входного ПИН-кода VMR, который не смог выполнить повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="8f829-107">(**HRESULT**) Status code returned from [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the VMR's input pin that failed the reconnection.</span></span>

</dd> <dt>

<span data-ttu-id="8f829-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8f829-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8f829-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8f829-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f829-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f829-110">Remarks</span></span>

<span data-ttu-id="8f829-111">Это событие перенаправляется в приложения.</span><span class="sxs-lookup"><span data-stu-id="8f829-111">This event is forwarded to applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f829-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8f829-112">Requirements</span></span>



| <span data-ttu-id="8f829-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8f829-113">Requirement</span></span> | <span data-ttu-id="8f829-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8f829-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f829-115">Header</span><span class="sxs-lookup"><span data-stu-id="8f829-115">Header</span></span><br/> | <dl> <span data-ttu-id="8f829-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f829-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f829-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f829-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f829-118">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="8f829-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8f829-119">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f829-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




