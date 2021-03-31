---
title: Сообщение EM_GETFILELINECOUNT (Коммктрл. h)
description: Возвращает количество строк в многострочном элементе управления "поле ввода" независимо от того, как линии отображаются на экране.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Элементы управления Windows для EM_GETFILELINECOUNT сообщений
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136667"
---
# <a name="em_getfilelinecount-message-commctrlh"></a><span data-ttu-id="90063-104">Сообщение EM_GETFILELINECOUNT (Коммктрл. h)</span><span class="sxs-lookup"><span data-stu-id="90063-104">EM_GETFILELINECOUNT message (CommCtrl.h)</span></span>

<span data-ttu-id="90063-105">Возвращает количество строк в многострочном элементе управления "поле ввода" независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="90063-105">Gets the number of lines in a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="90063-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90063-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90063-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90063-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90063-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="90063-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="90063-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90063-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90063-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="90063-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90063-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90063-111">Return value</span></span>

<span data-ttu-id="90063-112">Возвращаемое значение — это целое число, указывающее общее количество текстовых строк в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="90063-112">The return value is an integer specifying the total number of text lines in the multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="90063-113">Если элемент управления не содержит текста, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="90063-113">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="90063-114">Возвращаемое значение никогда не будет меньше 1.</span><span class="sxs-lookup"><span data-stu-id="90063-114">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="90063-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90063-115">Remarks</span></span>

<span data-ttu-id="90063-116">Сообщение **EM \_ жетфилелинекаунт** извлекает общее количество текстовых строк независимо от того, как линии отображаются на экране, а не только на число видимых в данный момент строк.</span><span class="sxs-lookup"><span data-stu-id="90063-116">The **EM\_GETFILELINECOUNT** message retrieves the total number of text lines, independently of how lines are displayed on the screen, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="90063-117">Перенос по словам не изменяет число строк, возвращаемых этим сообщением, так как это сообщение работает независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="90063-117">Word-wrap does not change the number of lines this message returns, as this message works independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="90063-118">Требования</span><span class="sxs-lookup"><span data-stu-id="90063-118">Requirements</span></span>



| <span data-ttu-id="90063-119">Требование</span><span class="sxs-lookup"><span data-stu-id="90063-119">Requirement</span></span> | <span data-ttu-id="90063-120">Значение</span><span class="sxs-lookup"><span data-stu-id="90063-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90063-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90063-121">Minimum supported client</span></span><br/> | <span data-ttu-id="90063-122">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="90063-122">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="90063-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90063-123">Minimum supported server</span></span><br/> | <span data-ttu-id="90063-124">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="90063-124">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90063-125">Header</span><span class="sxs-lookup"><span data-stu-id="90063-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="90063-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="90063-126"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90063-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90063-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="90063-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="90063-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="90063-129">**EM \_ жетфилелине**</span><span class="sxs-lookup"><span data-stu-id="90063-129">**EM\_GETFILELINE**</span></span>](em-getfileline.md)
</dt> <dt>

[<span data-ttu-id="90063-130">**EM \_ филелинеленгс**</span><span class="sxs-lookup"><span data-stu-id="90063-130">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="90063-131">**Изменить \_ жетфилелинекаунт**</span><span class="sxs-lookup"><span data-stu-id="90063-131">**Edit\_GetFileLineCount**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





