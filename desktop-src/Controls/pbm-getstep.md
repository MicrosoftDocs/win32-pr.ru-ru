---
title: Сообщение PBM_GETSTEP (Коммктрл. h)
description: Извлекает шаг шага из индикатора выполнения. Шаг приращения — это величина, на которую индикатор выполнения увеличивает текущее местоположение при получении \_ сообщения СТЕПИТ PBM. По умолчанию шаг с шагом равен 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- Элементы управления Windows для PBM_GETSTEP сообщений
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988999"
---
# <a name="pbm_getstep-message"></a><span data-ttu-id="5b342-106">\_ПОшаговое сообщение PBM</span><span class="sxs-lookup"><span data-stu-id="5b342-106">PBM\_GETSTEP message</span></span>

<span data-ttu-id="5b342-107">Извлекает шаг шага из индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="5b342-107">Retrieves the step increment from a progress bar.</span></span> <span data-ttu-id="5b342-108">Шаг приращения — это величина, на которую индикатор выполнения увеличивает текущее местоположение при получении сообщения [**\_ степит PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="5b342-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="5b342-109">По умолчанию шаг с шагом равен 10.</span><span class="sxs-lookup"><span data-stu-id="5b342-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b342-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b342-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b342-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b342-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5b342-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5b342-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5b342-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b342-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5b342-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5b342-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b342-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b342-115">Return value</span></span>

<span data-ttu-id="5b342-116">Возвращает текущий шаг шага.</span><span class="sxs-lookup"><span data-stu-id="5b342-116">Returns the current step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b342-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5b342-117">Requirements</span></span>



| <span data-ttu-id="5b342-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5b342-118">Requirement</span></span> | <span data-ttu-id="5b342-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5b342-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b342-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b342-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b342-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b342-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b342-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b342-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b342-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b342-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b342-124">Header</span><span class="sxs-lookup"><span data-stu-id="5b342-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b342-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b342-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





