---
title: Сообщение MCM_GETMAXTODAYWIDTH (Коммктрл. h)
description: Получает максимальную ширину \ 0034; сегодня \ 0034; строка в элементе управления "месячный календарь". Сюда входит текст метки и текст даты. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетмакстодайвидс.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- Элементы управления Windows для MCM_GETMAXTODAYWIDTH сообщений
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802513"
---
# <a name="mcm_getmaxtodaywidth-message"></a><span data-ttu-id="6c392-106">\_Сообщение MCM жетмакстодайвидс</span><span class="sxs-lookup"><span data-stu-id="6c392-106">MCM\_GETMAXTODAYWIDTH message</span></span>

<span data-ttu-id="6c392-107">Получает максимальную ширину строки "Today" в элементе управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="6c392-107">Retrieves the maximum width of the "today" string in a month calendar control.</span></span> <span data-ttu-id="6c392-108">Сюда входит текст метки и текст даты.</span><span class="sxs-lookup"><span data-stu-id="6c392-108">This includes the label text and the date text.</span></span> <span data-ttu-id="6c392-109">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетмакстодайвидс**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .</span><span class="sxs-lookup"><span data-stu-id="6c392-109">You can send this message explicitly or by using the [**MonthCal\_GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c392-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c392-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c392-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c392-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6c392-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6c392-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6c392-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c392-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6c392-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6c392-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c392-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c392-115">Return value</span></span>

<span data-ttu-id="6c392-116">Возвращает ширину строки "Today" в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6c392-116">Returns the width of the "today" string, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c392-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6c392-117">Requirements</span></span>



| <span data-ttu-id="6c392-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6c392-118">Requirement</span></span> | <span data-ttu-id="6c392-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6c392-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c392-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c392-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c392-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c392-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c392-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c392-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c392-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c392-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c392-124">Header</span><span class="sxs-lookup"><span data-stu-id="6c392-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c392-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c392-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





