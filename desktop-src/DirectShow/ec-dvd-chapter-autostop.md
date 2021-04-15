---
description: Указывает, что воспроизведение DVD остановлено в результате вызова метода IDvdControl2::P Лайчаптерсаутостоп.
ms.assetid: ccafaf76-ec8c-4d67-9b29-565f3ed6593b
title: EC_DVD_CHAPTER_AUTOSTOP (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 43e1414c0f9cee7e8daf37b87d5f0c3d0599a017
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689170"
---
# <a name="ec_dvd_chapter_autostop"></a><span data-ttu-id="b613c-103">\_автозавершение \_ глав DVD в EC \_</span><span class="sxs-lookup"><span data-stu-id="b613c-103">EC\_DVD\_CHAPTER\_AUTOSTOP</span></span>

<span data-ttu-id="b613c-104">Указывает, что воспроизведение DVD остановлено в результате вызова метода [**IDvdControl2::P лайчаптерсаутостоп**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) .</span><span class="sxs-lookup"><span data-stu-id="b613c-104">Indicates that DVD playback stopped as the result of a call to the [**IDvdControl2::PlayChaptersAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="b613c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b613c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b613c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b613c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b613c-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="b613c-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="b613c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b613c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b613c-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="b613c-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b613c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b613c-110">Remarks</span></span>

<span data-ttu-id="b613c-111">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="b613c-111">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="b613c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b613c-112">Requirements</span></span>



| <span data-ttu-id="b613c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b613c-113">Requirement</span></span> | <span data-ttu-id="b613c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b613c-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b613c-115">Header</span><span class="sxs-lookup"><span data-stu-id="b613c-115">Header</span></span><br/> | <dl> <span data-ttu-id="b613c-116"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b613c-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b613c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b613c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b613c-118">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="b613c-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b613c-119">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="b613c-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b613c-120">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="b613c-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




