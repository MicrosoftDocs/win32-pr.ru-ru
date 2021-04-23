---
description: Сигнализирует, что доступный набор методов интерфейса IDvdControl2 изменился.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651765"
---
# <a name="ec_dvd_valid_uops_change"></a><span data-ttu-id="67c00-103">\_ \_ изменение УОПС допустимого DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="67c00-103">EC\_DVD\_VALID\_UOPS\_CHANGE</span></span>

<span data-ttu-id="67c00-104">Сигнализирует, что доступный набор методов интерфейса [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) изменился.</span><span class="sxs-lookup"><span data-stu-id="67c00-104">Signals that the available set of [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface methods has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="67c00-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="67c00-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="67c00-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="67c00-107">Значение **типа DWORD** , содержащее сочетание одного или нескольких флагов из [**допустимого \_ перечисления \_ флагов УОП**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) .</span><span class="sxs-lookup"><span data-stu-id="67c00-107">**DWORD** value that contains a combination of zero or more flags from the [**VALID\_UOP\_FLAG**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enumeration.</span></span> <span data-ttu-id="67c00-108">Биты указывают, какие команды [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) были явно отключены DVD-диском.</span><span class="sxs-lookup"><span data-stu-id="67c00-108">The bits indicate which [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) commands were explicitly disabled by the DVD disc.</span></span>

</dd> <dt>

<span data-ttu-id="67c00-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="67c00-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="67c00-110">Ноль.</span><span class="sxs-lookup"><span data-stu-id="67c00-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67c00-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67c00-111">Remarks</span></span>

<span data-ttu-id="67c00-112">Это событие указывает только, какие операции явно отключены содержимым на DVD-диске. Он не гарантирует, что он может вызывать методы, которые не были отключены.</span><span class="sxs-lookup"><span data-stu-id="67c00-112">This event indicates only which operations are explicitly disabled by the content on the DVD disc. It does not guarantee that it is valid to call methods that are not disabled.</span></span> <span data-ttu-id="67c00-113">Например, если нет кнопок, метод [**IDvdControl2:: активатебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) не будет работать, даже если метод явно не отключен.</span><span class="sxs-lookup"><span data-stu-id="67c00-113">For example, if no buttons are present, the [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) method won't work, even though the method is not explicitly disabled.</span></span>

<span data-ttu-id="67c00-114">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="67c00-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c00-115">Требования</span><span class="sxs-lookup"><span data-stu-id="67c00-115">Requirements</span></span>



| <span data-ttu-id="67c00-116">Требование</span><span class="sxs-lookup"><span data-stu-id="67c00-116">Requirement</span></span> | <span data-ttu-id="67c00-117">Значение</span><span class="sxs-lookup"><span data-stu-id="67c00-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c00-118">Header</span><span class="sxs-lookup"><span data-stu-id="67c00-118">Header</span></span><br/> | <dl> <span data-ttu-id="67c00-119"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67c00-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c00-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67c00-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c00-121">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="67c00-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="67c00-122">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="67c00-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="67c00-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="67c00-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




