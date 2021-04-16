---
description: Указывает, выполняется ли воспроизведение блока угла и могут быть выполнены изменения угла.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679623"
---
# <a name="ec_dvd_angles_available"></a><span data-ttu-id="f1d38-103">\_Доступные углы для DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1d38-103">EC\_DVD\_ANGLES\_AVAILABLE</span></span>

<span data-ttu-id="f1d38-104">Указывает, выполняется ли воспроизведение блока угла и могут быть выполнены изменения угла.</span><span class="sxs-lookup"><span data-stu-id="f1d38-104">Indicates whether an angle block is being played and angle changes can be performed.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1d38-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1d38-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1d38-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f1d38-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f1d38-107">Логическое значение (**bool**), указывающее, выполняется ли воспроизведение блока угла.</span><span class="sxs-lookup"><span data-stu-id="f1d38-107">Boolean (**BOOL**) value that indicates if an angle block is being played back.</span></span> <span data-ttu-id="f1d38-108">Ноль (0) означает, что воспроизведение не находится в блоке угла, а углы недоступны, один (1) указывает, что выполняется воспроизведение блока угла и можно выполнить изменения угла.</span><span class="sxs-lookup"><span data-stu-id="f1d38-108">Zero (0) indicates that playback is not in an angle block and angles are not available, One (1) indicates that an angle block is being played back and angle changes can be performed.</span></span>

</dd> <dt>

<span data-ttu-id="f1d38-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f1d38-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f1d38-110">Ноль.</span><span class="sxs-lookup"><span data-stu-id="f1d38-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1d38-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1d38-111">Remarks</span></span>

<span data-ttu-id="f1d38-112">Изменения угла не ограничиваются блоками углов, а возможность изменения угла может быть видна только в блоке угла.</span><span class="sxs-lookup"><span data-stu-id="f1d38-112">Angle changes are not restricted to angle blocks and the manifestation of the angle change can be seen only in an angle block.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d38-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f1d38-113">Requirements</span></span>



| <span data-ttu-id="f1d38-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f1d38-114">Requirement</span></span> | <span data-ttu-id="f1d38-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f1d38-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d38-116">Header</span><span class="sxs-lookup"><span data-stu-id="f1d38-116">Header</span></span><br/> | <dl> <span data-ttu-id="f1d38-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d38-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d38-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1d38-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d38-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="f1d38-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f1d38-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="f1d38-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f1d38-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="f1d38-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




