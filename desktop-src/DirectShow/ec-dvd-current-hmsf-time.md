---
description: Сигнализирует о текущем времени в формате хмсф времени (DVD-диск \_ \_ ) относительно начала заголовка. Это событие активируется в начале каждого ВОБУ, что происходит каждые 0,4 – 1,0 секунд.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685199"
---
# <a name="ec_dvd_current_hmsf_time"></a><span data-ttu-id="b4e08-104">\_ \_ текущее \_ хмсф \_ время в формате EC DVD</span><span class="sxs-lookup"><span data-stu-id="b4e08-104">EC\_DVD\_CURRENT\_HMSF\_TIME</span></span>

<span data-ttu-id="b4e08-105">Сигнализирует о текущем времени в формате [**\_ хмсф времени \_ (DVD-диск**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) ) относительно начала заголовка.</span><span class="sxs-lookup"><span data-stu-id="b4e08-105">Signals the current time, in [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) format, relative to the start of the title.</span></span> <span data-ttu-id="b4e08-106">Это событие активируется в начале каждого ВОБУ, что происходит каждые 0,4 – 1,0 секунд.</span><span class="sxs-lookup"><span data-stu-id="b4e08-106">This event is triggered at the beginning of every VOBU, which occurs every 0.4 to 1.0 seconds.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4e08-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4e08-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4e08-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b4e08-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b4e08-109">Значение типа ULONG, содержащее структуру времени \_ ХМСФ DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e08-109">A ULONG value that contains the DVD\_HMSF\_TIMECODE structure.</span></span> <span data-ttu-id="b4e08-110">Назначьте lParam1 переменной ULONG, а затем приведите эту переменную к DVD-хмсф времени, \_ \_ чтобы получить доступ к его значениям.</span><span class="sxs-lookup"><span data-stu-id="b4e08-110">Assign lParam1 to a ULONG variable and then cast that variable to a DVD\_HMSF\_TIMECODE to access its values.</span></span>

</dd> <dt>

<span data-ttu-id="b4e08-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b4e08-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b4e08-112">Значение типа ULONG, содержащее объединение [**\_ \_ флагов**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)времени в формате DVD.</span><span class="sxs-lookup"><span data-stu-id="b4e08-112">A ULONG value containing a union of [**DVD\_TIMECODE\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4e08-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4e08-113">Remarks</span></span>

<span data-ttu-id="b4e08-114">Формат времени выполнения \_ ХМСФ DVD \_ предназначен для замены старого формата BCD, возвращаемого в \_ \_ событиях текущего времени в формате "DVD" в формате EC \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e08-114">The DVD\_HMSF\_TIMECODE format is intended to replace the old BCD format that is returned in EC\_DVD\_CURRENT\_TIME events.</span></span> <span data-ttu-id="b4e08-115">Коды времени ХМСФ проще работать с.</span><span class="sxs-lookup"><span data-stu-id="b4e08-115">The HMSF timecodes are easier to work with.</span></span> <span data-ttu-id="b4e08-116">Чтобы в навигаторе отправлялись \_ \_ текущие \_ события хмсф времени EC для DVD \_ , а не для \_ \_ \_ событий текущего времени в формате DVD, приложение должно вызвать `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` .</span><span class="sxs-lookup"><span data-stu-id="b4e08-116">To have the Navigator send EC\_DVD\_CURRENT\_HMSF\_TIME events instead of EC\_DVD\_CURRENT\_TIME events, an application must call `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)`.</span></span> <span data-ttu-id="b4e08-117">Если этот флаг установлен, навигатор также будет предполагать, что все параметры времени в методах [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) и [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) передаются как коды времени DVD \_ хмсф \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e08-117">When this flag is set, the Navigator will also expect all time parameters in the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods to be passed as DVD\_HMSF\_TIMECODEs.</span></span>

<span data-ttu-id="b4e08-118">Это событие возникает в доменах заголовков.</span><span class="sxs-lookup"><span data-stu-id="b4e08-118">This event is raised in the title domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e08-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b4e08-119">Requirements</span></span>



| <span data-ttu-id="b4e08-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b4e08-120">Requirement</span></span> | <span data-ttu-id="b4e08-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e08-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e08-122">Header</span><span class="sxs-lookup"><span data-stu-id="b4e08-122">Header</span></span><br/> | <dl> <span data-ttu-id="b4e08-123"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4e08-123"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4e08-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4e08-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e08-125">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="b4e08-125">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b4e08-126">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="b4e08-126">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b4e08-127">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="b4e08-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




