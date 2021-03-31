---
title: Сообщение MCM_SETCALID (Коммктрл. h)
description: Задает идентификатор календаря для данного элемента управления Calendar. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткалид.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Элементы управления Windows для MCM_SETCALID сообщений
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071257"
---
# <a name="mcm_setcalid-message"></a><span data-ttu-id="95c03-105">\_Сообщение MCM сеткалид</span><span class="sxs-lookup"><span data-stu-id="95c03-105">MCM\_SETCALID message</span></span>

<span data-ttu-id="95c03-106">Задает идентификатор календаря для данного элемента управления Calendar.</span><span class="sxs-lookup"><span data-stu-id="95c03-106">Sets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="95c03-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеткалид**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .</span><span class="sxs-lookup"><span data-stu-id="95c03-107">You can send this message explicitly or by using the [**MonthCal\_SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="95c03-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95c03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c03-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95c03-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95c03-110">ИДЕНТИФИКАТОР календаря.</span><span class="sxs-lookup"><span data-stu-id="95c03-110">The calendar ID.</span></span> <span data-ttu-id="95c03-111">Одна из констант [идентификаторов календаря](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="95c03-111">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

</dd> <dt>

<span data-ttu-id="95c03-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95c03-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95c03-113">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="95c03-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c03-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95c03-114">Return value</span></span>

<span data-ttu-id="95c03-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="95c03-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c03-116">Требования</span><span class="sxs-lookup"><span data-stu-id="95c03-116">Requirements</span></span>



| <span data-ttu-id="95c03-117">Требование</span><span class="sxs-lookup"><span data-stu-id="95c03-117">Requirement</span></span> | <span data-ttu-id="95c03-118">Значение</span><span class="sxs-lookup"><span data-stu-id="95c03-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95c03-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95c03-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95c03-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95c03-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95c03-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95c03-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95c03-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95c03-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95c03-123">Header</span><span class="sxs-lookup"><span data-stu-id="95c03-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c03-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c03-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

