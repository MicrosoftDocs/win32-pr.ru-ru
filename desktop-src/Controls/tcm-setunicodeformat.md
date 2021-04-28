---
title: Сообщение TCM_SETUNICODEFORMAT (Коммктрл. h)
description: TCM_SETUNICODEFORMAT сообщение — задает флаг формата символов Юникода для элемента управления.
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- Элементы управления Windows для TCM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- TCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b84f944be9bd20897d25e4b111f55ced558a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085852"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="90ad6-104">\_Сообщение СЕТУНИКОДЕФОРМАТ TCM</span><span class="sxs-lookup"><span data-stu-id="90ad6-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="90ad6-105">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="90ad6-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="90ad6-106">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="90ad6-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="90ad6-107">Это сообщение можно отправить явным образом или использовать макрос [**табктрл \_ сетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="90ad6-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="90ad6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90ad6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ad6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90ad6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90ad6-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="90ad6-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="90ad6-111">Если это значение не равно нулю, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="90ad6-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="90ad6-112">Если это значение равно нулю, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="90ad6-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="90ad6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90ad6-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="90ad6-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="90ad6-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ad6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90ad6-115">Return value</span></span>

<span data-ttu-id="90ad6-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="90ad6-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ad6-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="90ad6-117">Remarks</span></span>

<span data-ttu-id="90ad6-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="90ad6-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ad6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="90ad6-119">Requirements</span></span>



| <span data-ttu-id="90ad6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="90ad6-120">Requirement</span></span> | <span data-ttu-id="90ad6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="90ad6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90ad6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90ad6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90ad6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90ad6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90ad6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90ad6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90ad6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90ad6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90ad6-126">Header</span><span class="sxs-lookup"><span data-stu-id="90ad6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ad6-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ad6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ad6-128">См. также</span><span class="sxs-lookup"><span data-stu-id="90ad6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ad6-129">**\_ЖЕТУНИКОДЕФОРМАТ TCM**</span><span class="sxs-lookup"><span data-stu-id="90ad6-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





