---
title: Сообщение EM_GETCTFOPENSTATUS (RichEdit. h)
description: Определяет, открыта или закрыта клавиатура платформы текстовых служб (TSF).
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- Элементы управления Windows для EM_GETCTFOPENSTATUS сообщений
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988768"
---
# <a name="em_getctfopenstatus-message"></a><span data-ttu-id="f7d35-104">\_Сообщение ЖЕТКТФОПЕНСТАТУС EM</span><span class="sxs-lookup"><span data-stu-id="f7d35-104">EM\_GETCTFOPENSTATUS message</span></span>

<span data-ttu-id="f7d35-105">Определяет, открыта или закрыта клавиатура платформы текстовых служб (TSF).</span><span class="sxs-lookup"><span data-stu-id="f7d35-105">Determines if the Text Services Framework (TSF) keyboard is open or closed.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7d35-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7d35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d35-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7d35-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d35-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f7d35-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f7d35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7d35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d35-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f7d35-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d35-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7d35-111">Return value</span></span>

<span data-ttu-id="f7d35-112">Если клавиатура TSF открыта, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="f7d35-112">If the TSF keyboard is open, the return value is **TRUE**.</span></span> <span data-ttu-id="f7d35-113">В противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="f7d35-113">Otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d35-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f7d35-114">Requirements</span></span>



| <span data-ttu-id="f7d35-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f7d35-115">Requirement</span></span> | <span data-ttu-id="f7d35-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f7d35-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d35-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7d35-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d35-118">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7d35-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7d35-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7d35-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d35-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7d35-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7d35-121">Header</span><span class="sxs-lookup"><span data-stu-id="f7d35-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d35-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d35-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d35-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7d35-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d35-124">**EM \_ сетктфопенстатус**</span><span class="sxs-lookup"><span data-stu-id="f7d35-124">**EM\_SETCTFOPENSTATUS**</span></span>](em-setctfopenstatus.md)
</dt> </dl>

 

 





