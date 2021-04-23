---
title: Сообщение MCM_SETCURRENTVIEW (Коммктрл. h)
description: Задает текущее представление календаря. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сеткуррентвиев.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- Элементы управления Windows для MCM_SETCURRENTVIEW сообщений
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989291"
---
# <a name="mcm_setcurrentview-message"></a><span data-ttu-id="a98ee-105">\_Сообщение MCM сеткуррентвиев</span><span class="sxs-lookup"><span data-stu-id="a98ee-105">MCM\_SETCURRENTVIEW message</span></span>

<span data-ttu-id="a98ee-106">Задает текущее представление календаря.</span><span class="sxs-lookup"><span data-stu-id="a98ee-106">Sets the current view of the calendar.</span></span> <span data-ttu-id="a98ee-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сеткуррентвиев**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="a98ee-107">You can send this message explicitly or by using the [**MonthCal\_SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a98ee-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a98ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a98ee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a98ee-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a98ee-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a98ee-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a98ee-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a98ee-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a98ee-112">Новое представление.</span><span class="sxs-lookup"><span data-stu-id="a98ee-112">New view.</span></span> <span data-ttu-id="a98ee-113">Одна из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="a98ee-113">One of the following constants.</span></span>



| <span data-ttu-id="a98ee-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a98ee-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="a98ee-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a98ee-115">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <span data-ttu-id="a98ee-116"><dt>**МКМВ \_ месяц**</dt></span><span class="sxs-lookup"><span data-stu-id="a98ee-116"><dt>**MCMV\_MONTH**</dt></span></span> </dl>       | <span data-ttu-id="a98ee-117">Представление за месяц.</span><span class="sxs-lookup"><span data-stu-id="a98ee-117">Monthly view.</span></span><br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <span data-ttu-id="a98ee-118"><dt>**МКМВ \_ год**</dt></span><span class="sxs-lookup"><span data-stu-id="a98ee-118"><dt>**MCMV\_YEAR**</dt></span></span> </dl>          | <span data-ttu-id="a98ee-119">Ежегодное представление.</span><span class="sxs-lookup"><span data-stu-id="a98ee-119">Annual view.</span></span><br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <span data-ttu-id="a98ee-120"><dt>**МКМВное \_ десятилетие**</dt></span><span class="sxs-lookup"><span data-stu-id="a98ee-120"><dt>**MCMV\_DECADE**</dt></span></span> </dl>    | <span data-ttu-id="a98ee-121">Представление десятилетия.</span><span class="sxs-lookup"><span data-stu-id="a98ee-121">Decade view.</span></span><br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <span data-ttu-id="a98ee-122"><dt>**МКМВ \_ век**</dt></span><span class="sxs-lookup"><span data-stu-id="a98ee-122"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="a98ee-123">Представление "век".</span><span class="sxs-lookup"><span data-stu-id="a98ee-123">Century view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a98ee-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a98ee-124">Return value</span></span>

<span data-ttu-id="a98ee-125">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a98ee-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a98ee-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a98ee-126">Requirements</span></span>



| <span data-ttu-id="a98ee-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a98ee-127">Requirement</span></span> | <span data-ttu-id="a98ee-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a98ee-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a98ee-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a98ee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a98ee-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a98ee-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a98ee-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a98ee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a98ee-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a98ee-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a98ee-133">Header</span><span class="sxs-lookup"><span data-stu-id="a98ee-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a98ee-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a98ee-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





