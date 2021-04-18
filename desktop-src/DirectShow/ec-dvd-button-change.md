---
description: Сигнализирует, что изменилось число кнопок в меню DVD, или что кнопка была изменена.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652128"
---
# <a name="ec_dvd_button_change"></a><span data-ttu-id="bf0cd-103">\_ \_ изменение кнопки DVD \_ EC</span><span class="sxs-lookup"><span data-stu-id="bf0cd-103">EC\_DVD\_BUTTON\_CHANGE</span></span>

<span data-ttu-id="bf0cd-104">Сигнализирует, что изменилось число кнопок в меню DVD, или что кнопка была изменена.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-104">Signals that the number of DVD menu buttons has changed, or that the button selection has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf0cd-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf0cd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bf0cd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bf0cd-107">Значение **типа DWORD** , указывающее количество доступных кнопок.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-107">**DWORD** value indicating the number of available buttons.</span></span>

</dd> <dt>

<span data-ttu-id="bf0cd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bf0cd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bf0cd-109">Значение **типа DWORD** , указывающее номер выбранного в данный момент кнопки.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-109">**DWORD** value indicating the currently selected button number.</span></span> <span data-ttu-id="bf0cd-110">Номер выбранной кнопки ноль означает, что кнопка не выбрана.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-110">Selected button number zero implies that no button is selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf0cd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf0cd-111">Remarks</span></span>

<span data-ttu-id="bf0cd-112">Номера кнопок находятся в диапазоне от 1 до 36.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-112">Button numbers range from 1 to 36.</span></span>

<span data-ttu-id="bf0cd-113">Выбранная в данный момент кнопка может изменяться автоматически при помощи команды навигации, созданной на диске, а также через Управление приложениями с помощью интерфейса [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="bf0cd-113">The currently selected button can change automatically with a navigation command authored on the disc as well as through application control by using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="bf0cd-114">Это событие может подать сигнал любому из доступных номеров кнопок.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-114">This event can signal any of the available button numbers.</span></span> <span data-ttu-id="bf0cd-115">Эти числа не всегда соответствуют номерам кнопок, используемых для [**IDvdControl2:: селектандактиватебуттон**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) , так как этот метод может активировать только подмножество кнопок.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-115">These numbers do not always correspond to button numbers used for [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) because that method can activate only a subset of buttons.</span></span>

<span data-ttu-id="bf0cd-116">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="bf0cd-116">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0cd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf0cd-117">Requirements</span></span>



| <span data-ttu-id="bf0cd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bf0cd-118">Requirement</span></span> | <span data-ttu-id="bf0cd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bf0cd-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0cd-120">Header</span><span class="sxs-lookup"><span data-stu-id="bf0cd-120">Header</span></span><br/> | <dl> <span data-ttu-id="bf0cd-121"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf0cd-121"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf0cd-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf0cd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0cd-123">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="bf0cd-123">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="bf0cd-124">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="bf0cd-124">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bf0cd-125">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf0cd-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




