---
title: Сообщение MCM_SETCALENDARBORDER (Коммктрл. h)
description: Задает размер границы (в пикселях). Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткалендарбордер.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Элементы управления Windows для MCM_SETCALENDARBORDER сообщений
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490518"
---
# <a name="mcm_setcalendarborder-message"></a><span data-ttu-id="fe378-105">\_Сообщение MCM сеткалендарбордер</span><span class="sxs-lookup"><span data-stu-id="fe378-105">MCM\_SETCALENDARBORDER message</span></span>

<span data-ttu-id="fe378-106">Задает размер границы (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="fe378-106">Sets the size of the border, in pixels.</span></span> <span data-ttu-id="fe378-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеткалендарбордер**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .</span><span class="sxs-lookup"><span data-stu-id="fe378-107">You can send this message explicitly or by using the [**MonthCal\_SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe378-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe378-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe378-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe378-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe378-110">Если **значение равно true**, то размер границы устанавливается равным количеству пикселей, заданному параметром *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fe378-110">If **TRUE**, then the border size is set to the number of pixels that *lParam* specifies.</span></span> <span data-ttu-id="fe378-111">Если **значение равно false**, то размер границы сбрасывается до значения по умолчанию, указанного в теме, или нуль, если темы не используются.</span><span class="sxs-lookup"><span data-stu-id="fe378-111">If **FALSE**, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.</span></span>

</dd> <dt>

<span data-ttu-id="fe378-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe378-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe378-113">Число пикселей размера границы.</span><span class="sxs-lookup"><span data-stu-id="fe378-113">Number of pixels of the border size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe378-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe378-114">Return value</span></span>

<span data-ttu-id="fe378-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fe378-115">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe378-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fe378-116">Requirements</span></span>



| <span data-ttu-id="fe378-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fe378-117">Requirement</span></span> | <span data-ttu-id="fe378-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fe378-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe378-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe378-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe378-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe378-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe378-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe378-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe378-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe378-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe378-123">Header</span><span class="sxs-lookup"><span data-stu-id="fe378-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe378-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe378-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





