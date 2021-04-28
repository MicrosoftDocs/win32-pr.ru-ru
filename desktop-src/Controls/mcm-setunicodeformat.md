---
title: Сообщение MCM_SETUNICODEFORMAT (Коммктрл. h)
description: MCM_SETUNICODEFORMAT сообщение — задает флаг формата символов Юникода для элемента управления.
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- Элементы управления Windows для MCM_SETUNICODEFORMAT сообщений
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa922b0dde8702f447690f9626938364174cbff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112373"
---
# <a name="mcm_setunicodeformat-message"></a><span data-ttu-id="c6dcf-104">\_Сообщение MCM сетуникодеформат</span><span class="sxs-lookup"><span data-stu-id="c6dcf-104">MCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="c6dcf-105">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="c6dcf-106">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="c6dcf-107">Это сообщение можно отправить явным образом или использовать макрос [**монскал \_ сетуникодеформат**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="c6dcf-107">You can send this message explicitly or use the [**MonthCal\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6dcf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6dcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6dcf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6dcf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6dcf-110">Определяет кодировку, используемую элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="c6dcf-111">Если это значение не равно нулю, элемент управления будет использовать символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="c6dcf-112">Если это значение равно нулю, элемент управления будет использовать символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="c6dcf-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6dcf-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c6dcf-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6dcf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6dcf-115">Return value</span></span>

<span data-ttu-id="c6dcf-116">Возвращает предыдущий флаг формата Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c6dcf-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6dcf-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="c6dcf-117">Remarks</span></span>

<span data-ttu-id="c6dcf-118">Обсуждение этого сообщения см. в примечаниях по [**CCM \_ сетуникодеформат**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="c6dcf-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6dcf-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c6dcf-119">Requirements</span></span>



| <span data-ttu-id="c6dcf-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c6dcf-120">Requirement</span></span> | <span data-ttu-id="c6dcf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c6dcf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dcf-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6dcf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c6dcf-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6dcf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6dcf-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6dcf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c6dcf-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c6dcf-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6dcf-126">Header</span><span class="sxs-lookup"><span data-stu-id="c6dcf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6dcf-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6dcf-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6dcf-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c6dcf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6dcf-129">**MCM \_ жетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="c6dcf-129">**MCM\_GETUNICODEFORMAT**</span></span>](mcm-getunicodeformat.md)
</dt> </dl>

 

 





