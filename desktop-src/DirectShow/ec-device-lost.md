---
description: Устройство самонастраивающийся было удалено или снова стало доступным.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679627"
---
# <a name="ec_device_lost"></a><span data-ttu-id="a0fec-103">\_устройство EC \_ потеряно</span><span class="sxs-lookup"><span data-stu-id="a0fec-103">EC\_DEVICE\_LOST</span></span>

<span data-ttu-id="a0fec-104">Устройство самонастраивающийся было удалено или снова стало доступным.</span><span class="sxs-lookup"><span data-stu-id="a0fec-104">A Plug and Play device was removed or became available again.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0fec-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0fec-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0fec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a0fec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a0fec-107">(**IUnknown** \* ) Указатель на интерфейс **IUnknown** фильтра, представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="a0fec-107">(**IUnknown**\*) Pointer to the **IUnknown** interface of the filter that represents the device.</span></span>

</dd> <dt>

<span data-ttu-id="a0fec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a0fec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a0fec-109">Нуль, если устройство было удалено, или значение 1, если устройство снова становится доступным.</span><span class="sxs-lookup"><span data-stu-id="a0fec-109">Zero if the device was removed, or 1 if the device is available again.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a0fec-110">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a0fec-110">Default Action</span></span>

<span data-ttu-id="a0fec-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="a0fec-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0fec-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="a0fec-112">Remarks</span></span>

<span data-ttu-id="a0fec-113">Когда устройство снова становится доступным, предыдущее состояние фильтра устройства больше не действует.</span><span class="sxs-lookup"><span data-stu-id="a0fec-113">When the device becomes available again, the previous state of the device filter is no longer valid.</span></span> <span data-ttu-id="a0fec-114">Приложение должно перестроить граф, чтобы использовать устройство.</span><span class="sxs-lookup"><span data-stu-id="a0fec-114">The application must rebuild the graph in order to use the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0fec-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a0fec-115">Requirements</span></span>



| <span data-ttu-id="a0fec-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a0fec-116">Requirement</span></span> | <span data-ttu-id="a0fec-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a0fec-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fec-118">Header</span><span class="sxs-lookup"><span data-stu-id="a0fec-118">Header</span></span><br/> | <dl> <span data-ttu-id="a0fec-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0fec-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0fec-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0fec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fec-121">Уведомление об удалении устройства</span><span class="sxs-lookup"><span data-stu-id="a0fec-121">Device Removal Notification</span></span>](device-removal-notification.md)
</dt> <dt>

[<span data-ttu-id="a0fec-122">Коды уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="a0fec-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a0fec-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0fec-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




