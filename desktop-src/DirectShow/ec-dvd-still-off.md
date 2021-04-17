---
description: Сигнализирует об окончании всех по-прежнему (PGC, Cell или ВОБУ).
ms.assetid: 459464b1-3085-4ad7-8eb3-960cee89d395
title: EC_DVD_STILL_OFF (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_OFF
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 811bc85deafb40676041280daa0a1cdd8f8b3dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675252"
---
# <a name="ec_dvd_still_off"></a><span data-ttu-id="ce507-103">\_неподвижный DVD-диск EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="ce507-103">EC\_DVD\_STILL\_OFF</span></span>

<span data-ttu-id="ce507-104">Сигнализирует об окончании всех по-прежнему (PGC, Cell или ВОБУ).</span><span class="sxs-lookup"><span data-stu-id="ce507-104">Signals the end of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="ce507-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce507-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce507-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ce507-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ce507-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="ce507-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce507-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ce507-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ce507-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="ce507-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce507-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce507-110">Remarks</span></span>

<span data-ttu-id="ce507-111">Это событие указывает, что все активные в настоящее время события по-прежнему освобождены.</span><span class="sxs-lookup"><span data-stu-id="ce507-111">This event indicates that any currently active still has been released.</span></span>

<span data-ttu-id="ce507-112">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="ce507-112">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce507-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ce507-113">Requirements</span></span>



| <span data-ttu-id="ce507-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ce507-114">Requirement</span></span> | <span data-ttu-id="ce507-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ce507-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce507-116">Header</span><span class="sxs-lookup"><span data-stu-id="ce507-116">Header</span></span><br/> | <dl> <span data-ttu-id="ce507-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce507-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce507-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce507-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce507-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="ce507-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ce507-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="ce507-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ce507-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ce507-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




