---
title: Сообщение EM_SETCTFOPENSTATUS (RichEdit. h)
description: Открывает или закрывает клавиатуру платформы текстовых служб (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Элементы управления Windows для EM_SETCTFOPENSTATUS сообщений
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071915"
---
# <a name="em_setctfopenstatus-message"></a><span data-ttu-id="eb4d1-104">\_Сообщение СЕТКТФОПЕНСТАТУС EM</span><span class="sxs-lookup"><span data-stu-id="eb4d1-104">EM\_SETCTFOPENSTATUS message</span></span>

<span data-ttu-id="eb4d1-105">Открывает или закрывает клавиатуру платформы текстовых служб (TSF).</span><span class="sxs-lookup"><span data-stu-id="eb4d1-105">Opens or closes the Text Services Framework (TSF) keyboard.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb4d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb4d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb4d1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb4d1-108">Чтобы включить клавиатуру TSF, используйте **значение true**.</span><span class="sxs-lookup"><span data-stu-id="eb4d1-108">To turn on the TSF keyboard, use **TRUE**.</span></span> <span data-ttu-id="eb4d1-109">Чтобы отключить клавиатуру TSF, используйте **значение false**.</span><span class="sxs-lookup"><span data-stu-id="eb4d1-109">To turn off the TSF keyboard, use **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb4d1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb4d1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb4d1-111">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="eb4d1-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4d1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb4d1-112">Return value</span></span>

<span data-ttu-id="eb4d1-113">В случае успеха это сообщение возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="eb4d1-113">If successful, this message returns **TRUE**.</span></span> <span data-ttu-id="eb4d1-114">В случае неудачи это сообщение возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="eb4d1-114">If unsuccessful, this message returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4d1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="eb4d1-115">Requirements</span></span>



| <span data-ttu-id="eb4d1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="eb4d1-116">Requirement</span></span> | <span data-ttu-id="eb4d1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eb4d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4d1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb4d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eb4d1-119">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb4d1-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb4d1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb4d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eb4d1-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb4d1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb4d1-122">Header</span><span class="sxs-lookup"><span data-stu-id="eb4d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb4d1-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4d1-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb4d1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb4d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4d1-125">**EM \_ жетктфопенстатус**</span><span class="sxs-lookup"><span data-stu-id="eb4d1-125">**EM\_GETCTFOPENSTATUS**</span></span>](em-getctfopenstatus.md)
</dt> </dl>

 

 





