---
description: Сигнализирует, что количество доступных углов изменилось или изменилось текущее значение угла.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679624"
---
# <a name="ec_dvd_angle_change"></a><span data-ttu-id="ea85d-103">\_изменение угла для DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea85d-103">EC\_DVD\_ANGLE\_CHANGE</span></span>

<span data-ttu-id="ea85d-104">Сигнализирует, что количество доступных углов изменилось или изменилось текущее значение угла.</span><span class="sxs-lookup"><span data-stu-id="ea85d-104">Signals that either the number of available angles changed or that the current angle number changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea85d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea85d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea85d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ea85d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ea85d-107">Значение **типа DWORD** , указывающее количество доступных углов.</span><span class="sxs-lookup"><span data-stu-id="ea85d-107">**DWORD** value indicating the number of available angles.</span></span> <span data-ttu-id="ea85d-108">Если число доступных углов равно 1, текущее видео не является многоугловым.</span><span class="sxs-lookup"><span data-stu-id="ea85d-108">When the number of available angles is 1, the current video is not multiangle.</span></span>

</dd> <dt>

<span data-ttu-id="ea85d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ea85d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ea85d-110">Значение **типа DWORD** , указывающее текущий номер угла.</span><span class="sxs-lookup"><span data-stu-id="ea85d-110">**DWORD** value indicating the current angle number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea85d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea85d-111">Remarks</span></span>

<span data-ttu-id="ea85d-112">Значения угла в диапазоне от 1 до 9.</span><span class="sxs-lookup"><span data-stu-id="ea85d-112">Angle numbers range from 1 to 9.</span></span>

<span data-ttu-id="ea85d-113">Текущий номер угла может изменяться автоматически при помощи команды навигации, созданной на диске, а также через Управление приложениями с помощью интерфейса [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="ea85d-113">The current angle number can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="ea85d-114">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="ea85d-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea85d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ea85d-115">Requirements</span></span>



| <span data-ttu-id="ea85d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ea85d-116">Requirement</span></span> | <span data-ttu-id="ea85d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ea85d-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea85d-118">Header</span><span class="sxs-lookup"><span data-stu-id="ea85d-118">Header</span></span><br/> | <dl> <span data-ttu-id="ea85d-119"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea85d-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea85d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea85d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea85d-121">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="ea85d-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ea85d-122">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="ea85d-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ea85d-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ea85d-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




