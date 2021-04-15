---
title: Сообщение PBM_SETSTEP (Коммктрл. h)
description: Задает шаг приращения для индикатора выполнения. Шаг приращения — это величина, на которую индикатор выполнения увеличивает текущее местоположение при получении \_ сообщения СТЕПИТ PBM. По умолчанию шаг с шагом равен 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- Элементы управления Windows для PBM_SETSTEP сообщений
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654577"
---
# <a name="pbm_setstep-message"></a><span data-ttu-id="c5c68-106">\_Сообщение СЕТСТЕП PBM</span><span class="sxs-lookup"><span data-stu-id="c5c68-106">PBM\_SETSTEP message</span></span>

<span data-ttu-id="c5c68-107">Задает шаг приращения для индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="c5c68-107">Specifies the step increment for a progress bar.</span></span> <span data-ttu-id="c5c68-108">Шаг приращения — это величина, на которую индикатор выполнения увеличивает текущее местоположение при получении сообщения [**\_ степит PBM**](pbm-stepit.md) .</span><span class="sxs-lookup"><span data-stu-id="c5c68-108">The step increment is the amount by which the progress bar increases its current position whenever it receives a [**PBM\_STEPIT**](pbm-stepit.md) message.</span></span> <span data-ttu-id="c5c68-109">По умолчанию шаг с шагом равен 10.</span><span class="sxs-lookup"><span data-stu-id="c5c68-109">By default, the step increment is set to 10.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5c68-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5c68-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c68-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5c68-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5c68-112">Шаг приращения нового шага.</span><span class="sxs-lookup"><span data-stu-id="c5c68-112">New step increment.</span></span>

</dd> <dt>

<span data-ttu-id="c5c68-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5c68-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c5c68-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c5c68-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c68-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5c68-115">Return value</span></span>

<span data-ttu-id="c5c68-116">Возвращает шаг предыдущего шага.</span><span class="sxs-lookup"><span data-stu-id="c5c68-116">Returns the previous step increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c68-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c5c68-117">Requirements</span></span>



| <span data-ttu-id="c5c68-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c5c68-118">Requirement</span></span> | <span data-ttu-id="c5c68-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c5c68-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c68-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5c68-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c68-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5c68-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5c68-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5c68-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c68-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c5c68-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5c68-124">Header</span><span class="sxs-lookup"><span data-stu-id="c5c68-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c68-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c68-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





