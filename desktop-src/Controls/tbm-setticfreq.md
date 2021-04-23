---
title: Сообщение TBM_SETTICFREQ (Коммктрл. h)
description: Задает частоту интервала для делений в TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Элементы управления Windows для TBM_SETTICFREQ сообщений
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071374"
---
# <a name="tbm_setticfreq-message"></a><span data-ttu-id="9a3a5-104">\_Сообщение ТБМ сеттикфрек</span><span class="sxs-lookup"><span data-stu-id="9a3a5-104">TBM\_SETTICFREQ message</span></span>

<span data-ttu-id="9a3a5-105">Задает частоту интервала для делений в TrackBar.</span><span class="sxs-lookup"><span data-stu-id="9a3a5-105">Sets the interval frequency for tick marks in a trackbar.</span></span> <span data-ttu-id="9a3a5-106">Например, если задана частота 2, то для каждого второго приращения в диапазоне TrackBar отображается деление.</span><span class="sxs-lookup"><span data-stu-id="9a3a5-106">For example, if the frequency is set to two, a tick mark is displayed for every other increment in the trackbar's range.</span></span> <span data-ttu-id="9a3a5-107">Значение по умолчанию для периодичности — единица; то есть каждый шаг приращения в диапазоне связан с делением.</span><span class="sxs-lookup"><span data-stu-id="9a3a5-107">The default setting for the frequency is one; that is, every increment in the range is associated with a tick mark.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a3a5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a3a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a3a5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a3a5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a3a5-110">Частота делений.</span><span class="sxs-lookup"><span data-stu-id="9a3a5-110">Frequency of the tick marks.</span></span>

</dd> <dt>

<span data-ttu-id="9a3a5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a3a5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9a3a5-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9a3a5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a3a5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a3a5-113">Return value</span></span>

<span data-ttu-id="9a3a5-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9a3a5-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a3a5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a3a5-115">Remarks</span></span>

<span data-ttu-id="9a3a5-116">Для использования этого сообщения параметр TrackBar должен иметь стиль [**TBS \_**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9a3a5-116">The trackbar must have the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) style to use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a3a5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9a3a5-117">Requirements</span></span>



| <span data-ttu-id="9a3a5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9a3a5-118">Requirement</span></span> | <span data-ttu-id="9a3a5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9a3a5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3a5-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a3a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9a3a5-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a3a5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a3a5-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a3a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9a3a5-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a3a5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a3a5-124">Header</span><span class="sxs-lookup"><span data-stu-id="9a3a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a3a5-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a3a5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





