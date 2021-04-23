---
description: Сообщает о том, что изменяется родительский уровень авторского содержимого DVD.
ms.assetid: c6817e1a-f860-4ba2-9e0f-e195624230c5
title: EC_DVD_PARENTAL_LEVEL_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PARENTAL_LEVEL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f6e1dbcbcb285f33b6ea2b99c59c5c82dae0ae03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651768"
---
# <a name="ec_dvd_parental_level_change"></a><span data-ttu-id="868cb-103">\_изменение на \_ уровне родительского DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="868cb-103">EC\_DVD\_PARENTAL\_LEVEL\_CHANGE</span></span>

<span data-ttu-id="868cb-104">Сообщает о том, что изменяется родительский уровень авторского содержимого DVD.</span><span class="sxs-lookup"><span data-stu-id="868cb-104">Signals that the parental level of the authored DVD content is about to change.</span></span>

## <a name="parameters"></a><span data-ttu-id="868cb-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="868cb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="868cb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="868cb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="868cb-107">Значение типа LONG, представляющее новый набор родительских уровней в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="868cb-107">LONG value representing the new parental level set in the player.</span></span>

</dd> <dt>

<span data-ttu-id="868cb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="868cb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="868cb-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="868cb-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="868cb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="868cb-110">Remarks</span></span>

<span data-ttu-id="868cb-111">Фильтр " [Навигатор DVD](dvd-navigator-filter.md) " не поддерживает изменения родительского уровня во время потоковой передачи в ответ на команды сеттмппмл на DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="868cb-111">The [DVD Navigator](dvd-navigator-filter.md) filter does not support parental level changes during streaming in response to SetTmpPML commands on a DVD disc.</span></span>

## <a name="requirements"></a><span data-ttu-id="868cb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="868cb-112">Requirements</span></span>



| <span data-ttu-id="868cb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="868cb-113">Requirement</span></span> | <span data-ttu-id="868cb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="868cb-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="868cb-115">Header</span><span class="sxs-lookup"><span data-stu-id="868cb-115">Header</span></span><br/> | <dl> <span data-ttu-id="868cb-116"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="868cb-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="868cb-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="868cb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868cb-118">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="868cb-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="868cb-119">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="868cb-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="868cb-120">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="868cb-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




