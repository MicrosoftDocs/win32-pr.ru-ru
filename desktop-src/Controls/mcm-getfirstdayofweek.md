---
title: Сообщение MCM_GETFIRSTDAYOFWEEK (Коммктрл. h)
description: Извлекает первый день недели для элемента управления "месячный календарь". Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетфирстдайофвик.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- Элементы управления Windows для MCM_GETFIRSTDAYOFWEEK сообщений
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654551"
---
# <a name="mcm_getfirstdayofweek-message"></a><span data-ttu-id="6259f-105">\_Сообщение MCM жетфирстдайофвик</span><span class="sxs-lookup"><span data-stu-id="6259f-105">MCM\_GETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="6259f-106">Извлекает первый день недели для элемента управления "месячный календарь".</span><span class="sxs-lookup"><span data-stu-id="6259f-106">Retrieves the first day of the week for a month calendar control.</span></span> <span data-ttu-id="6259f-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетфирстдайофвик**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="6259f-107">You can send this message explicitly or by using the [**MonthCal\_GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6259f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6259f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6259f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6259f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6259f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6259f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6259f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6259f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6259f-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6259f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6259f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6259f-113">Return value</span></span>

<span data-ttu-id="6259f-114">Возвращает значение **типа DWORD** , содержащее два значения.</span><span class="sxs-lookup"><span data-stu-id="6259f-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="6259f-115">Верхнее слово является **логическим** значением, которое не равно нулю, если первый день недели имеет значение, отличное от locale \_ ифирстдайофвик, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6259f-115">The high word is a **BOOL** value that is nonzero if the first day of the week is set to something other than LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="6259f-116">Младшее слово — это значение типа INT, представляющее первый день недели, где 0 — понедельник, 1 — вторник и т. д.</span><span class="sxs-lookup"><span data-stu-id="6259f-116">The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="6259f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6259f-117">Requirements</span></span>



| <span data-ttu-id="6259f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6259f-118">Requirement</span></span> | <span data-ttu-id="6259f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6259f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6259f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6259f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6259f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6259f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6259f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6259f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6259f-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6259f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6259f-124">Header</span><span class="sxs-lookup"><span data-stu-id="6259f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6259f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6259f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





