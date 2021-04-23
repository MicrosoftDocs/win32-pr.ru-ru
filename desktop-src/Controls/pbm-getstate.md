---
title: Сообщение PBM_GETSTATE (Коммктрл. h)
description: Возвращает состояние индикатора выполнения.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- Элементы управления Windows для PBM_GETSTATE сообщений
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989000"
---
# <a name="pbm_getstate-message"></a><span data-ttu-id="86683-104">\_Сообщение о состоянии PBM</span><span class="sxs-lookup"><span data-stu-id="86683-104">PBM\_GETSTATE message</span></span>

<span data-ttu-id="86683-105">Возвращает состояние индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="86683-105">Gets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="86683-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86683-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86683-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="86683-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="86683-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="86683-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86683-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86683-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="86683-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86683-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86683-111">Return value</span></span>

<span data-ttu-id="86683-112">Возвращает текущее состояние индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="86683-112">Returns the current state of the progress bar.</span></span> <span data-ttu-id="86683-113">Одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="86683-113">One of the following values.</span></span>



| <span data-ttu-id="86683-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="86683-114">Return code</span></span>                                                                                 | <span data-ttu-id="86683-115">Описание</span><span class="sxs-lookup"><span data-stu-id="86683-115">Description</span></span>             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="86683-116"><dt>**ПБСТ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="86683-116"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="86683-117">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="86683-117">In progress.</span></span><br/> |
| <dl> <span data-ttu-id="86683-118"><dt>**ПБСТ, \_ Ошибка**</dt></span><span class="sxs-lookup"><span data-stu-id="86683-118"><dt>**PBST\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="86683-119">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="86683-119">Error.</span></span><br/>       |
| <dl> <span data-ttu-id="86683-120"><dt>**ПБСТ \_ приостановлена**</dt></span><span class="sxs-lookup"><span data-stu-id="86683-120"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="86683-121">приостановлено</span><span class="sxs-lookup"><span data-stu-id="86683-121">Paused.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="86683-122">Требования</span><span class="sxs-lookup"><span data-stu-id="86683-122">Requirements</span></span>



| <span data-ttu-id="86683-123">Требование</span><span class="sxs-lookup"><span data-stu-id="86683-123">Requirement</span></span> | <span data-ttu-id="86683-124">Значение</span><span class="sxs-lookup"><span data-stu-id="86683-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86683-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86683-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86683-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86683-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86683-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86683-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86683-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86683-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86683-129">Header</span><span class="sxs-lookup"><span data-stu-id="86683-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="86683-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="86683-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





