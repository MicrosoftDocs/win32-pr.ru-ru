---
title: Сообщение PBM_SETSTATE (Коммктрл. h)
description: Задает состояние индикатора выполнения.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- Элементы управления Windows для PBM_SETSTATE сообщений
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491799"
---
# <a name="pbm_setstate-message"></a><span data-ttu-id="1545b-104">\_Сообщение SETSTATE PBM</span><span class="sxs-lookup"><span data-stu-id="1545b-104">PBM\_SETSTATE message</span></span>

<span data-ttu-id="1545b-105">Задает состояние индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="1545b-105">Sets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1545b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1545b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1545b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1545b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1545b-108">Состояние установленного индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="1545b-108">State of the progress bar that is being set.</span></span> <span data-ttu-id="1545b-109">Одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1545b-109">One of the following values.</span></span>



| <span data-ttu-id="1545b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1545b-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="1545b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1545b-111">Meaning</span></span>                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="1545b-112"><dt>**ПБСТ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="1545b-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="1545b-113">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="1545b-113">In progress.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="1545b-114"><dt>**ПБСТ, \_ Ошибка**</dt></span><span class="sxs-lookup"><span data-stu-id="1545b-114"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="1545b-115">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="1545b-115">Error.</span></span><br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="1545b-116"><dt>**ПБСТ \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="1545b-116"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="1545b-117">приостановлено</span><span class="sxs-lookup"><span data-stu-id="1545b-117">Paused.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="1545b-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1545b-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1545b-119">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1545b-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1545b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1545b-120">Return value</span></span>

<span data-ttu-id="1545b-121">Возвращает предыдущее состояние.</span><span class="sxs-lookup"><span data-stu-id="1545b-121">Returns the previous state.</span></span>

## <a name="requirements"></a><span data-ttu-id="1545b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1545b-122">Requirements</span></span>



| <span data-ttu-id="1545b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1545b-123">Requirement</span></span> | <span data-ttu-id="1545b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1545b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1545b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1545b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1545b-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1545b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1545b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1545b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1545b-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1545b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1545b-129">Header</span><span class="sxs-lookup"><span data-stu-id="1545b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1545b-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1545b-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





