---
title: Сообщение LVM_SETUNICODEFORMAT (Коммктрл. h)
description: LVM_SETUNICODEFORMAT сообщение — задает флаг формата символов Юникода для элемента управления.
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- Элементы управления Windows для LVM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0f700cd057bc77eddc699404f37b19a6cc9c39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120152"
---
# <a name="lvm_setunicodeformat-message"></a><span data-ttu-id="7fcb7-104">\_Сообщение LVM сетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="7fcb7-104">LVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="7fcb7-105">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="7fcb7-106">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="7fcb7-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетуникодеформат ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="7fcb7-107">You can send this message explicitly or use the [**ListView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fcb7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fcb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fcb7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fcb7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fcb7-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="7fcb7-111">Если это значение не равно нулю, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="7fcb7-112">Если это значение равно нулю, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="7fcb7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fcb7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7fcb7-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fcb7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fcb7-115">Return value</span></span>

<span data-ttu-id="7fcb7-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="7fcb7-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fcb7-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="7fcb7-117">Remarks</span></span>

<span data-ttu-id="7fcb7-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="7fcb7-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcb7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7fcb7-119">Requirements</span></span>



| <span data-ttu-id="7fcb7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7fcb7-120">Requirement</span></span> | <span data-ttu-id="7fcb7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7fcb7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcb7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fcb7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcb7-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fcb7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fcb7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fcb7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcb7-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fcb7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fcb7-126">Header</span><span class="sxs-lookup"><span data-stu-id="7fcb7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcb7-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcb7-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcb7-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7fcb7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcb7-129">**LVM \_ жетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="7fcb7-129">**LVM\_GETUNICODEFORMAT**</span></span>](lvm-getunicodeformat.md)
</dt> </dl>

 

 





