---
title: Сообщение SB_SETUNICODEFORMAT (Коммктрл. h)
description: Задает флаг формата символов Юникода для элемента управления. Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- Элементы управления Windows для SB_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c5223f1e707747356c8869ad047a69f6e8d94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654607"
---
# <a name="sb_setunicodeformat-message"></a><span data-ttu-id="4996a-105">\_Сообщение SB сетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="4996a-105">SB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="4996a-106">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4996a-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="4996a-107">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="4996a-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4996a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4996a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4996a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4996a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4996a-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="4996a-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="4996a-111">Если это значение равно **true**, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="4996a-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="4996a-112">Если это значение равно **false**, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="4996a-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="4996a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4996a-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4996a-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4996a-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4996a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4996a-115">Return value</span></span>

<span data-ttu-id="4996a-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4996a-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4996a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4996a-117">Remarks</span></span>

<span data-ttu-id="4996a-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="4996a-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4996a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4996a-119">Requirements</span></span>



| <span data-ttu-id="4996a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4996a-120">Requirement</span></span> | <span data-ttu-id="4996a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4996a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4996a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4996a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4996a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4996a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4996a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4996a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4996a-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4996a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4996a-126">Header</span><span class="sxs-lookup"><span data-stu-id="4996a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4996a-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4996a-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4996a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4996a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4996a-129">**SB \_ жетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="4996a-129">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md)
</dt> </dl>

 

 





