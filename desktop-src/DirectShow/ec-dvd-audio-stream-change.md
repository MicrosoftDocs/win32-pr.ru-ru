---
description: Сообщает, что номер текущего аудиопотока изменился для главного заголовка DVD-диска.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679671"
---
# <a name="ec_dvd_audio_stream_change"></a><span data-ttu-id="a243f-103">\_ \_ \_ изменение потокового воспроизведения на DVD-диске EC \_</span><span class="sxs-lookup"><span data-stu-id="a243f-103">EC\_DVD\_AUDIO\_STREAM\_CHANGE</span></span>

<span data-ttu-id="a243f-104">Сообщает, что номер текущего аудиопотока изменился для главного заголовка DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="a243f-104">Signals that the current audio stream number changed for the DVD main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="a243f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a243f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a243f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a243f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a243f-107">Значение **типа DWORD** , указывающее номер нового потока звука пользователя.</span><span class="sxs-lookup"><span data-stu-id="a243f-107">**DWORD** value indicating the new user audio stream number.</span></span> <span data-ttu-id="a243f-108">Номера звуковых потоков находятся в диапазоне от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="a243f-108">Audio stream numbers range from 0 to 7.</span></span> <span data-ttu-id="a243f-109">Поток 0xFFFFFFFF указывает, что поток не выбран.</span><span class="sxs-lookup"><span data-stu-id="a243f-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="a243f-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a243f-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a243f-111">Ноль.</span><span class="sxs-lookup"><span data-stu-id="a243f-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a243f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a243f-112">Remarks</span></span>

<span data-ttu-id="a243f-113">Текущий звуковой поток может автоматически измениться с помощью команды навигации, созданной на диске, а также через Управление приложениями с использованием интерфейса [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="a243f-113">The current audio stream can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="a243f-114">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="a243f-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="a243f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a243f-115">Requirements</span></span>



| <span data-ttu-id="a243f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a243f-116">Requirement</span></span> | <span data-ttu-id="a243f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a243f-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a243f-118">Header</span><span class="sxs-lookup"><span data-stu-id="a243f-118">Header</span></span><br/> | <dl> <span data-ttu-id="a243f-119"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a243f-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a243f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a243f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a243f-121">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="a243f-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a243f-122">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="a243f-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a243f-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="a243f-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




