---
title: Сообщение MCM_GETCURRENTVIEW (Коммктрл. h)
description: Возвращает текущее представление календаря. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал жеткуррентвиев.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- Элементы управления Windows для MCM_GETCURRENTVIEW сообщений
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492384"
---
# <a name="mcm_getcurrentview-message"></a><span data-ttu-id="838db-105">\_Сообщение MCM жеткуррентвиев</span><span class="sxs-lookup"><span data-stu-id="838db-105">MCM\_GETCURRENTVIEW message</span></span>

<span data-ttu-id="838db-106">Возвращает текущее представление календаря.</span><span class="sxs-lookup"><span data-stu-id="838db-106">Gets the current view of the calendar.</span></span> <span data-ttu-id="838db-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ жеткуррентвиев**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="838db-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="838db-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="838db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838db-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="838db-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="838db-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="838db-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="838db-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="838db-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="838db-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="838db-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838db-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="838db-113">Return value</span></span>

<span data-ttu-id="838db-114">Текущее представление.</span><span class="sxs-lookup"><span data-stu-id="838db-114">Current view.</span></span> <span data-ttu-id="838db-115">Одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="838db-115">One of the following values.</span></span>



| <span data-ttu-id="838db-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="838db-116">Return code</span></span>                                                                                  | <span data-ttu-id="838db-117">Описание</span><span class="sxs-lookup"><span data-stu-id="838db-117">Description</span></span>              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="838db-118"><dt>**МКМВ \_ месяц**</dt></span><span class="sxs-lookup"><span data-stu-id="838db-118"><dt>**MCMV\_MONTH**</dt></span></span> </dl>   | <span data-ttu-id="838db-119">Представление за месяц.</span><span class="sxs-lookup"><span data-stu-id="838db-119">Monthly view.</span></span><br/> |
| <dl> <span data-ttu-id="838db-120"><dt>**МКМВ \_ год**</dt></span><span class="sxs-lookup"><span data-stu-id="838db-120"><dt>**MCMV\_YEAR**</dt></span></span> </dl>    | <span data-ttu-id="838db-121">Ежегодное представление.</span><span class="sxs-lookup"><span data-stu-id="838db-121">Annual view.</span></span><br/>  |
| <dl> <span data-ttu-id="838db-122"><dt>**МКМВное \_ десятилетие**</dt></span><span class="sxs-lookup"><span data-stu-id="838db-122"><dt>**MCMV\_DECADE**</dt></span></span> </dl>  | <span data-ttu-id="838db-123">Представление десятилетия.</span><span class="sxs-lookup"><span data-stu-id="838db-123">Decade view.</span></span><br/>  |
| <dl> <span data-ttu-id="838db-124"><dt>**МКМВ \_ век**</dt></span><span class="sxs-lookup"><span data-stu-id="838db-124"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="838db-125">Представление "век".</span><span class="sxs-lookup"><span data-stu-id="838db-125">Century view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="838db-126">Требования</span><span class="sxs-lookup"><span data-stu-id="838db-126">Requirements</span></span>



| <span data-ttu-id="838db-127">Требование</span><span class="sxs-lookup"><span data-stu-id="838db-127">Requirement</span></span> | <span data-ttu-id="838db-128">Значение</span><span class="sxs-lookup"><span data-stu-id="838db-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="838db-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="838db-129">Minimum supported client</span></span><br/> | <span data-ttu-id="838db-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="838db-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="838db-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="838db-131">Minimum supported server</span></span><br/> | <span data-ttu-id="838db-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="838db-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="838db-133">Header</span><span class="sxs-lookup"><span data-stu-id="838db-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="838db-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="838db-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





