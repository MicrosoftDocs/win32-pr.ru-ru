---
title: Сообщение MCM_GETCALID (Коммктрл. h)
description: Возвращает идентификатор календаря для данного элемента управления "Календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткалид.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Элементы управления Windows для MCM_GETCALID сообщений
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136138"
---
# <a name="mcm_getcalid-message"></a><span data-ttu-id="7364a-105">\_Сообщение MCM жеткалид</span><span class="sxs-lookup"><span data-stu-id="7364a-105">MCM\_GETCALID message</span></span>

<span data-ttu-id="7364a-106">Возвращает идентификатор календаря для данного элемента управления "Календарь".</span><span class="sxs-lookup"><span data-stu-id="7364a-106">Gets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="7364a-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жеткалид**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .</span><span class="sxs-lookup"><span data-stu-id="7364a-107">You can send this message explicitly or by using the [**MonthCal\_GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7364a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7364a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7364a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7364a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7364a-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7364a-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7364a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7364a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7364a-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7364a-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7364a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7364a-113">Return value</span></span>

<span data-ttu-id="7364a-114">Идентификатор текущего календаря.</span><span class="sxs-lookup"><span data-stu-id="7364a-114">ID of the current calendar.</span></span> <span data-ttu-id="7364a-115">Одна из констант [идентификаторов календаря](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="7364a-115">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="7364a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7364a-116">Requirements</span></span>



| <span data-ttu-id="7364a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7364a-117">Requirement</span></span> | <span data-ttu-id="7364a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7364a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7364a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7364a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7364a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7364a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7364a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7364a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7364a-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7364a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7364a-123">Header</span><span class="sxs-lookup"><span data-stu-id="7364a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7364a-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7364a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

