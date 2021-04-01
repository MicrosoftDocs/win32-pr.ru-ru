---
title: Сообщение MCM_GETMAXSELCOUNT (Коммктрл. h)
description: Возвращает максимальный диапазон дат, который можно выбрать в элементе управления ' календарь на месяц '. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жетмаксселкаунт.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Элементы управления Windows для MCM_GETMAXSELCOUNT сообщений
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071778"
---
# <a name="mcm_getmaxselcount-message"></a><span data-ttu-id="8d6a6-105">\_Сообщение MCM жетмаксселкаунт</span><span class="sxs-lookup"><span data-stu-id="8d6a6-105">MCM\_GETMAXSELCOUNT message</span></span>

<span data-ttu-id="8d6a6-106">Возвращает максимальный диапазон дат, который можно выбрать в элементе управления ' календарь на месяц '.</span><span class="sxs-lookup"><span data-stu-id="8d6a6-106">Retrieves the maximum date range that can be selected in a month calendar control.</span></span> <span data-ttu-id="8d6a6-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жетмаксселкаунт**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="8d6a6-107">You can send this message explicitly or by using the [**MonthCal\_GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d6a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d6a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d6a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d6a6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d6a6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8d6a6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d6a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d6a6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8d6a6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8d6a6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d6a6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d6a6-113">Return value</span></span>

<span data-ttu-id="8d6a6-114">Возвращает значение типа INT, представляющее общее количество дней, которое может быть выбрано для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8d6a6-114">Returns an INT value that represents the total number of days that can be selected for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d6a6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d6a6-115">Remarks</span></span>

<span data-ttu-id="8d6a6-116">Можно изменить максимальный диапазон дат, который можно выбрать, с помощью сообщения [**MCM \_ сетмаксселкаунт**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="8d6a6-116">You can change the maximum date range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d6a6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8d6a6-117">Requirements</span></span>



| <span data-ttu-id="8d6a6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8d6a6-118">Requirement</span></span> | <span data-ttu-id="8d6a6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8d6a6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d6a6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d6a6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d6a6-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d6a6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d6a6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d6a6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d6a6-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d6a6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d6a6-124">Header</span><span class="sxs-lookup"><span data-stu-id="8d6a6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d6a6-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d6a6-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





