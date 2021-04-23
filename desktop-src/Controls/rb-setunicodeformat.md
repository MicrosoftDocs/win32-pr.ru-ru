---
title: Сообщение RB_SETUNICODEFORMAT (Коммктрл. h)
description: Задает флаг формата символов Юникода для элемента управления. Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.
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
ms.openlocfilehash: cfc9d0ce256af0de740c487fd6514848db79c2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803040"
---
# <a name="rb_setunicodeformat-message"></a><span data-ttu-id="177d4-105">\_Сообщение СЕТУНИКОДЕФОРМАТ RB</span><span class="sxs-lookup"><span data-stu-id="177d4-105">RB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="177d4-106">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="177d4-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="177d4-107">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="177d4-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="177d4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="177d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="177d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="177d4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="177d4-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="177d4-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="177d4-111">Если это значение не равно нулю, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="177d4-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="177d4-112">Если это значение равно нулю, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="177d4-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="177d4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="177d4-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="177d4-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="177d4-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="177d4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="177d4-115">Return value</span></span>

<span data-ttu-id="177d4-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="177d4-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="177d4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="177d4-117">Remarks</span></span>

<span data-ttu-id="177d4-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="177d4-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="177d4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="177d4-119">Requirements</span></span>



| <span data-ttu-id="177d4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="177d4-120">Requirement</span></span> | <span data-ttu-id="177d4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="177d4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="177d4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="177d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="177d4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="177d4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="177d4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="177d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="177d4-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="177d4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="177d4-126">Header</span><span class="sxs-lookup"><span data-stu-id="177d4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="177d4-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="177d4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177d4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="177d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177d4-129">**\_ЖЕТУНИКОДЕФОРМАТ RB**</span><span class="sxs-lookup"><span data-stu-id="177d4-129">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
</dt> </dl>

 

 





