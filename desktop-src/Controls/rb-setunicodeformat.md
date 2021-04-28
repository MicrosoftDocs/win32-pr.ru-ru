---
title: Сообщение RB_SETUNICODEFORMAT (Коммктрл. h)
description: RB_SETUNICODEFORMAT сообщение — задает флаг формата символов Юникода для элемента управления. Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.
ms.assetid: 769b74e0-c1f0-4068-80c4-075f1db2058a
keywords:
- Элементы управления Windows для RB_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- RB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9c168ee298d28d59010491031f7d94ebcaa650
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090972"
---
# <a name="rb_setunicodeformat-message"></a><span data-ttu-id="ccc42-105">\_Сообщение СЕТУНИКОДЕФОРМАТ RB</span><span class="sxs-lookup"><span data-stu-id="ccc42-105">RB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="ccc42-106">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ccc42-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="ccc42-107">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ccc42-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccc42-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccc42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc42-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ccc42-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc42-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="ccc42-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="ccc42-111">Если это значение не равно нулю, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="ccc42-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="ccc42-112">Если это значение равно нулю, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="ccc42-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="ccc42-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccc42-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ccc42-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ccc42-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc42-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccc42-115">Return value</span></span>

<span data-ttu-id="ccc42-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ccc42-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc42-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="ccc42-117">Remarks</span></span>

<span data-ttu-id="ccc42-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc42-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc42-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ccc42-119">Requirements</span></span>



| <span data-ttu-id="ccc42-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ccc42-120">Requirement</span></span> | <span data-ttu-id="ccc42-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ccc42-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc42-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccc42-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc42-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccc42-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ccc42-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccc42-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc42-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ccc42-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccc42-126">Header</span><span class="sxs-lookup"><span data-stu-id="ccc42-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc42-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc42-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc42-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ccc42-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc42-129">**\_ЖЕТУНИКОДЕФОРМАТ RB**</span><span class="sxs-lookup"><span data-stu-id="ccc42-129">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
</dt> </dl>

 

 





