---
title: Сообщение LB_GETLOCALE (Winuser. h)
description: Возвращает текущий языковой стандарт для списка. Языковой стандарт можно использовать для определения правильного порядка сортировки отображаемого текста (для списков с \_ стилем сортировки фунтов) и текста, добавленного \_ сообщением ADDSTRING балансировки нагрузки.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Элементы управления Windows для LB_GETLOCALE сообщений
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491181"
---
# <a name="lb_getlocale-message"></a><span data-ttu-id="9ee0a-105">\_Сообщение о НЕстандартной балансировке нагрузки</span><span class="sxs-lookup"><span data-stu-id="9ee0a-105">LB\_GETLOCALE message</span></span>

<span data-ttu-id="9ee0a-106">Возвращает текущий языковой стандарт для списка.</span><span class="sxs-lookup"><span data-stu-id="9ee0a-106">Gets the current locale of the list box.</span></span> <span data-ttu-id="9ee0a-107">Языковой стандарт можно использовать для определения правильного порядка сортировки отображаемого текста (для списков с стилем [**\_ сортировки фунтов**](list-box-styles.md) ) и текста, добавленного сообщением [**\_ ADDSTRING балансировки нагрузки**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="9ee0a-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ee0a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ee0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ee0a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ee0a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee0a-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9ee0a-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9ee0a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ee0a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee0a-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9ee0a-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ee0a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ee0a-113">Return value</span></span>

<span data-ttu-id="9ee0a-114">Возвращаемое значение указывает текущий языковой стандарт для списка.</span><span class="sxs-lookup"><span data-stu-id="9ee0a-114">The return value specifies the current locale of the list box.</span></span> <span data-ttu-id="9ee0a-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит код страны или региона, а [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="9ee0a-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ee0a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ee0a-116">Remarks</span></span>

<span data-ttu-id="9ee0a-117">Идентификатор языка состоит из идентификатора подязыка и основного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="9ee0a-117">The language identifier consists of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="9ee0a-118">Используйте макрос [**примарилангид**](/windows/desktop/api/winnt/nf-winnt-primarylangid) для извлечения идентификатора основного языка из [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) возвращаемого значения и макроса [**сублангид**](/windows/desktop/api/winnt/nf-winnt-sublangid) для извлечения идентификатора этого языка.</span><span class="sxs-lookup"><span data-stu-id="9ee0a-118">Use the [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro to extract the primary language identifier from the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro to extract the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ee0a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9ee0a-119">Requirements</span></span>



| <span data-ttu-id="9ee0a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9ee0a-120">Requirement</span></span> | <span data-ttu-id="9ee0a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9ee0a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee0a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ee0a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9ee0a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ee0a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9ee0a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ee0a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9ee0a-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ee0a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ee0a-126">Header</span><span class="sxs-lookup"><span data-stu-id="9ee0a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ee0a-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ee0a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee0a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ee0a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ee0a-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9ee0a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ee0a-130">**ADDSTRING балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="9ee0a-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="9ee0a-131">**ФУНТОВая \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="9ee0a-131">**LB\_SETLOCALE**</span></span>](lb-setlocale.md)
</dt> <dt>

<span data-ttu-id="9ee0a-132">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="9ee0a-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9ee0a-133">**примарилангид**</span><span class="sxs-lookup"><span data-stu-id="9ee0a-133">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="9ee0a-134">**сублангид**</span><span class="sxs-lookup"><span data-stu-id="9ee0a-134">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

