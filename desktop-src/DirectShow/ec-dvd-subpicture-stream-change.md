---
description: Сообщает, что текущий номер потока субтитров изменен для основного заголовка.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675250"
---
# <a name="ec_dvd_subpicture_stream_change"></a><span data-ttu-id="f7986-103">\_ \_ изменение потока подизображений EC DVD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7986-103">EC\_DVD\_SUBPICTURE\_STREAM\_CHANGE</span></span>

<span data-ttu-id="f7986-104">Сообщает, что текущий номер потока субтитров изменен для основного заголовка.</span><span class="sxs-lookup"><span data-stu-id="f7986-104">Signals that the current subpicture stream number changed for the main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7986-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7986-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7986-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f7986-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f7986-107">Значение **типа DWORD** , указывающее на новый номер потока субтитров пользователей.</span><span class="sxs-lookup"><span data-stu-id="f7986-107">**DWORD** value indicating the new user subpicture stream number.</span></span> <span data-ttu-id="f7986-108">Число потоков субтитров в диапазоне от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="f7986-108">Subpicture stream numbers range from 0 to 31.</span></span> <span data-ttu-id="f7986-109">Поток 0xFFFFFFFF указывает, что поток не выбран.</span><span class="sxs-lookup"><span data-stu-id="f7986-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="f7986-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f7986-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f7986-111">Логическое значение, указывающее состояние включения или отключения подизображения.</span><span class="sxs-lookup"><span data-stu-id="f7986-111">Boolean value that indicates the subpicture's on/off state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7986-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7986-112">Remarks</span></span>

<span data-ttu-id="f7986-113">Подизображение может автоматически изменяться при помощи команды навигации, созданной на диске, а также через Управление приложениями с помощью [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span><span class="sxs-lookup"><span data-stu-id="f7986-113">The subpicture can change automatically with a navigation command authored on disc as well as through application control using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span>

<span data-ttu-id="f7986-114">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="f7986-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7986-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f7986-115">Requirements</span></span>



| <span data-ttu-id="f7986-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f7986-116">Requirement</span></span> | <span data-ttu-id="f7986-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f7986-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7986-118">Header</span><span class="sxs-lookup"><span data-stu-id="f7986-118">Header</span></span><br/> | <dl> <span data-ttu-id="f7986-119"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7986-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7986-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7986-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7986-121">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="f7986-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f7986-122">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="f7986-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f7986-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="f7986-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




