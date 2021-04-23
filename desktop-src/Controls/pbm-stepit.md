---
title: Сообщение PBM_STEPIT (Коммктрл. h)
description: Изменяет текущую позицию индикатора выполнения на шаг с шагом и перерисовывает линию, чтобы отразить новую позицию. Приложение задает шаг шага, отправляя \_ сообщение PBM сетстеп.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- Элементы управления Windows для PBM_STEPIT сообщений
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988995"
---
# <a name="pbm_stepit-message"></a><span data-ttu-id="f278e-105">\_Сообщение СТЕПИТ PBM</span><span class="sxs-lookup"><span data-stu-id="f278e-105">PBM\_STEPIT message</span></span>

<span data-ttu-id="f278e-106">Изменяет текущую позицию индикатора выполнения на шаг с шагом и перерисовывает линию, чтобы отразить новую позицию.</span><span class="sxs-lookup"><span data-stu-id="f278e-106">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="f278e-107">Приложение задает шаг шага, отправляя сообщение [**PBM \_ сетстеп**](pbm-setstep.md) .</span><span class="sxs-lookup"><span data-stu-id="f278e-107">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="f278e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f278e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f278e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f278e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f278e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f278e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f278e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f278e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f278e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f278e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f278e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f278e-113">Return value</span></span>

<span data-ttu-id="f278e-114">Возвращает предыдущее расположение.</span><span class="sxs-lookup"><span data-stu-id="f278e-114">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="f278e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f278e-115">Remarks</span></span>

<span data-ttu-id="f278e-116">Если эта величина превышает максимальное значение диапазона, это сообщение сбрасывает текущее расположение, чтобы индикатор выполнения снова начинался с самого начала.</span><span class="sxs-lookup"><span data-stu-id="f278e-116">When the position exceeds the maximum range value, this message resets the current position so that the progress indicator starts over again from the beginning.</span></span>

## <a name="requirements"></a><span data-ttu-id="f278e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f278e-117">Requirements</span></span>



| <span data-ttu-id="f278e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f278e-118">Requirement</span></span> | <span data-ttu-id="f278e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f278e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f278e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f278e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f278e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f278e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f278e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f278e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f278e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f278e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f278e-124">Header</span><span class="sxs-lookup"><span data-stu-id="f278e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f278e-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f278e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





