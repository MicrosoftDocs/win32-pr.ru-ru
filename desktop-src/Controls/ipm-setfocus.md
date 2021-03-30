---
title: Сообщение IPM_SETFOCUS (Коммктрл. h)
description: Устанавливает фокус клавиатуры на указанное поле в элементе управления IP-адреса. Будет выбран весь текст в этом поле.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- Элементы управления Windows для IPM_SETFOCUS сообщений
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136419"
---
# <a name="ipm_setfocus-message"></a><span data-ttu-id="fa4b5-105">\_Сообщение IPM SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="fa4b5-105">IPM\_SETFOCUS message</span></span>

<span data-ttu-id="fa4b5-106">Устанавливает фокус клавиатуры на указанное поле в элементе управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="fa4b5-106">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="fa4b5-107">Будет выбран весь текст в этом поле.</span><span class="sxs-lookup"><span data-stu-id="fa4b5-107">All of the text in that field will be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa4b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa4b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa4b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa4b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa4b5-110">Отсчитываемый от нуля индекс поля, к которому должен быть установлен фокус.</span><span class="sxs-lookup"><span data-stu-id="fa4b5-110">A zero-based field index to which the focus should be set.</span></span> <span data-ttu-id="fa4b5-111">Если это значение больше числа полей, фокус устанавливается на первое пустое поле.</span><span class="sxs-lookup"><span data-stu-id="fa4b5-111">If this value is greater than the number of fields, focus is set to the first blank field.</span></span> <span data-ttu-id="fa4b5-112">Если все поля не пусты, фокус устанавливается на первое поле.</span><span class="sxs-lookup"><span data-stu-id="fa4b5-112">If all fields are nonblank, focus is set to the first field.</span></span>

</dd> <dt>

<span data-ttu-id="fa4b5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa4b5-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fa4b5-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fa4b5-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa4b5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa4b5-115">Return value</span></span>

<span data-ttu-id="fa4b5-116">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="fa4b5-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa4b5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="fa4b5-117">Requirements</span></span>



| <span data-ttu-id="fa4b5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="fa4b5-118">Requirement</span></span> | <span data-ttu-id="fa4b5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="fa4b5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4b5-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa4b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa4b5-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa4b5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa4b5-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa4b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa4b5-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa4b5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa4b5-124">Header</span><span class="sxs-lookup"><span data-stu-id="fa4b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa4b5-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa4b5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





