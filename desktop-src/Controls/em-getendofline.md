---
title: Сообщение EM_GETENDOFLINE (Коммктрл. h)
description: Получает символ конца строки, используемый при вставке LineBreak. Отправьте это сообщение явным образом или с помощью \_ макроса Edit жетендофлине.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Элементы управления Windows для EM_GETENDOFLINE сообщений
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489465"
---
# <a name="em_getendofline-message"></a><span data-ttu-id="cf70c-105">\_Сообщение ЖЕТЕНДОФЛИНЕ EM</span><span class="sxs-lookup"><span data-stu-id="cf70c-105">EM\_GETENDOFLINE message</span></span>

<span data-ttu-id="cf70c-106">Извлекает символ конца строки для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="cf70c-106">Retrieves the end-of-line character for an edit control.</span></span> <span data-ttu-id="cf70c-107">Отправьте это сообщение явным образом или с помощью макроса [**Edit \_ жетендофлине**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .</span><span class="sxs-lookup"><span data-stu-id="cf70c-107">Send this message explicitly or by using the [**Edit\_GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf70c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf70c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf70c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf70c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cf70c-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cf70c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cf70c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf70c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cf70c-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cf70c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf70c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf70c-113">Return value</span></span>

<span data-ttu-id="cf70c-114">Возвращает символ конца строки, используемый элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="cf70c-114">Returns the end-of-line character used by the edit control.</span></span> <span data-ttu-id="cf70c-115">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cf70c-115">This can be one of the following values.</span></span>

| <span data-ttu-id="cf70c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cf70c-116">Value</span></span>                                                                                                                                                   | <span data-ttu-id="cf70c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cf70c-117">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="cf70c-118"><dt>**EC \_ ендофлине \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="cf70c-118"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl> | <span data-ttu-id="cf70c-119">Символ конца строки, используемый для New линебреакс, — возврат каретки, за которым следует перевод строки (CRLF).</span><span class="sxs-lookup"><span data-stu-id="cf70c-119">The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="cf70c-120"><dt>**EC \_ ендофлине \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="cf70c-120"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>       | <span data-ttu-id="cf70c-121">Символ конца строки, используемый для New линебреакс, — возврат каретки (CR).</span><span class="sxs-lookup"><span data-stu-id="cf70c-121">The end-of-line character used for new linebreaks is carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="cf70c-122"><dt>**EC \_ ендофлине \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="cf70c-122"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>       | <span data-ttu-id="cf70c-123">Символ конца строки, используемый для New линебреакс, — перевод строки (LF).</span><span class="sxs-lookup"><span data-stu-id="cf70c-123">The end-of-line character used for new linebreaks is linefeed (LF).</span></span><br/>                               |

## <a name="remarks"></a><span data-ttu-id="cf70c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf70c-124">Remarks</span></span>

<span data-ttu-id="cf70c-125">Если в качестве символа конца строки задано **EC \_ ендофлине \_ Детектфромконтент** с помощью [**Edit \_ сетендофлине**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), это сообщение вернет обнаруженный символ конца строки.</span><span class="sxs-lookup"><span data-stu-id="cf70c-125">When the end-of-line character used is set to **EC\_ENDOFLINE\_DETECTFROMCONTENT** using [**Edit\_SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), this message will return the detected end-of-line character.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf70c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cf70c-126">Requirements</span></span>



| <span data-ttu-id="cf70c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cf70c-127">Requirement</span></span> | <span data-ttu-id="cf70c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cf70c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf70c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf70c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf70c-130">\[Только для настольных приложений Windows 10 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="cf70c-130">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cf70c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf70c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf70c-132">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="cf70c-132">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf70c-133">Header</span><span class="sxs-lookup"><span data-stu-id="cf70c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf70c-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf70c-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf70c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf70c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf70c-136">\**EM \_ сетендофлине*</span><span class="sxs-lookup"><span data-stu-id="cf70c-136">\**EM\_SETENDOFLINE*</span></span>](em-setendofline.md)
</dt> </dl>
 

 





