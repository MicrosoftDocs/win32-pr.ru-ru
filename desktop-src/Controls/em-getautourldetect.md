---
title: Сообщение EM_GETAUTOURLDETECT (RichEdit. h)
description: Указывает, включено ли автоматическое обнаружение URL-адресов в элементе управления Rich Edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- Элементы управления Windows для EM_GETAUTOURLDETECT сообщений
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071709"
---
# <a name="em_getautourldetect-message"></a><span data-ttu-id="99aa8-104">\_Сообщение ЖЕТАУТАУРЛДЕТЕКТ EM</span><span class="sxs-lookup"><span data-stu-id="99aa8-104">EM\_GETAUTOURLDETECT message</span></span>

<span data-ttu-id="99aa8-105">Указывает, включено ли автоматическое обнаружение URL-адресов в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="99aa8-105">Indicates whether the auto URL detection is turned on in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="99aa8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99aa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99aa8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99aa8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99aa8-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="99aa8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="99aa8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99aa8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99aa8-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="99aa8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99aa8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99aa8-111">Return value</span></span>

<span data-ttu-id="99aa8-112">Если автоматическое обнаружение URL-адресов активно, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="99aa8-112">If auto-URL detection is active, the return value is 1.</span></span>

<span data-ttu-id="99aa8-113">Если автоматическое обнаружение URL-адресов неактивно, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="99aa8-113">If auto-URL detection is inactive, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="99aa8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99aa8-114">Remarks</span></span>

<span data-ttu-id="99aa8-115">Если включено автоматическое обнаружение URL-адресов, Microsoft Rich Edit постоянно проверяет вводимый текст на наличие допустимого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="99aa8-115">When auto URL detection is on, Microsoft Rich Edit is constantly checking typed text for a valid URL.</span></span> <span data-ttu-id="99aa8-116">Расширенное редактирование распознает URL-адреса, которые начинаются с этих префиксов:</span><span class="sxs-lookup"><span data-stu-id="99aa8-116">Rich Edit recognizes URLs that start with these prefixes:</span></span>

-   <span data-ttu-id="99aa8-117">http:</span><span class="sxs-lookup"><span data-stu-id="99aa8-117">http:</span></span>
-   <span data-ttu-id="99aa8-118">file.</span><span class="sxs-lookup"><span data-stu-id="99aa8-118">file:</span></span>
-   <span data-ttu-id="99aa8-119">mailto:</span><span class="sxs-lookup"><span data-stu-id="99aa8-119">mailto:</span></span>
-   <span data-ttu-id="99aa8-120">адресов</span><span class="sxs-lookup"><span data-stu-id="99aa8-120">ftp:</span></span>
-   <span data-ttu-id="99aa8-121">https:</span><span class="sxs-lookup"><span data-stu-id="99aa8-121">https:</span></span>
-   <span data-ttu-id="99aa8-122">Протокол</span><span class="sxs-lookup"><span data-stu-id="99aa8-122">gopher:</span></span>
-   <span data-ttu-id="99aa8-123">Разверните</span><span class="sxs-lookup"><span data-stu-id="99aa8-123">nntp:</span></span>
-   <span data-ttu-id="99aa8-124">Просперо:</span><span class="sxs-lookup"><span data-stu-id="99aa8-124">prospero:</span></span>
-   <span data-ttu-id="99aa8-125">Telnet</span><span class="sxs-lookup"><span data-stu-id="99aa8-125">telnet:</span></span>
-   <span data-ttu-id="99aa8-126">Интернета</span><span class="sxs-lookup"><span data-stu-id="99aa8-126">news:</span></span>
-   <span data-ttu-id="99aa8-127">WAIS</span><span class="sxs-lookup"><span data-stu-id="99aa8-127">wais:</span></span>
-   <span data-ttu-id="99aa8-128">невозможно</span><span class="sxs-lookup"><span data-stu-id="99aa8-128">outlook:</span></span>

<span data-ttu-id="99aa8-129">Расширенное редактирование также распознает имена стандартных путей, начинающихся с \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="99aa8-129">Rich Edit also recognizes standard path names that start with \\\\.</span></span> <span data-ttu-id="99aa8-130">Когда форматируемый текст находит URL-адрес, он изменяет цвет текста URL-адреса, подчеркивает текст и уведомляет клиента по [ \_ ссылке EN](en-link.md).</span><span class="sxs-lookup"><span data-stu-id="99aa8-130">When Rich Edit locates a URL, it changes the URL text color, underlines the text, and notifies the client using [EN\_LINK](en-link.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99aa8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="99aa8-131">Requirements</span></span>



| <span data-ttu-id="99aa8-132">Требование</span><span class="sxs-lookup"><span data-stu-id="99aa8-132">Requirement</span></span> | <span data-ttu-id="99aa8-133">Значение</span><span class="sxs-lookup"><span data-stu-id="99aa8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99aa8-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99aa8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="99aa8-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99aa8-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99aa8-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99aa8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="99aa8-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99aa8-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99aa8-138">Header</span><span class="sxs-lookup"><span data-stu-id="99aa8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="99aa8-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="99aa8-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99aa8-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99aa8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99aa8-141">\_ссылка EN</span><span class="sxs-lookup"><span data-stu-id="99aa8-141">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

 





