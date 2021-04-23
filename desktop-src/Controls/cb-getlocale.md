---
title: Сообщение CB_GETLOCALE (Winuser. h)
description: Возвращает текущий языковой стандарт поля со списком. Языковой стандарт используется для определения правильного порядка сортировки отображаемого текста для полей со списком, имеющих \_ стиль сортировки CBS и текст, добавленный с помощью \_ сообщения ADDSTRING CB.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Элементы управления Windows для CB_GETLOCALE сообщений
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071615"
---
# <a name="cb_getlocale-message"></a><span data-ttu-id="90100-105">\_Сообщение о локализации CB</span><span class="sxs-lookup"><span data-stu-id="90100-105">CB\_GETLOCALE message</span></span>

<span data-ttu-id="90100-106">Возвращает текущий языковой стандарт поля со списком.</span><span class="sxs-lookup"><span data-stu-id="90100-106">Gets the current locale of the combo box.</span></span> <span data-ttu-id="90100-107">Языковой стандарт используется для определения правильного порядка сортировки отображаемого текста для полей со списком, имеющих [**стиль \_ сортировки CBS**](combo-box-styles.md) и текст, добавленный с помощью сообщения [**\_ ADDSTRING CB**](cb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="90100-107">The locale is used to determine the correct sorting order of displayed text for combo boxes with the [**CBS\_SORT**](combo-box-styles.md) style and text added by using the [**CB\_ADDSTRING**](cb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="90100-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90100-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90100-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90100-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90100-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="90100-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="90100-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90100-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90100-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="90100-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90100-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90100-113">Return value</span></span>

<span data-ttu-id="90100-114">Возвращаемое значение задает текущий языковой стандарт для поля со списком.</span><span class="sxs-lookup"><span data-stu-id="90100-114">The return value specifies the current locale of the combo box.</span></span> <span data-ttu-id="90100-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит код страны или региона, а [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="90100-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="90100-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90100-116">Remarks</span></span>

<span data-ttu-id="90100-117">Идентификатор языка состоит из идентификатора подязыка и основного идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="90100-117">The language identifier is made up of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="90100-118">Макрос [**примарилангид**](/windows/desktop/api/winnt/nf-winnt-primarylangid) получает основной идентификатор языка, а макрос [**сублангид**](/windows/desktop/api/winnt/nf-winnt-sublangid) получает идентификатор этого языка.</span><span class="sxs-lookup"><span data-stu-id="90100-118">The [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro obtains the primary language identifier and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro obtains the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="90100-119">Требования</span><span class="sxs-lookup"><span data-stu-id="90100-119">Requirements</span></span>



| <span data-ttu-id="90100-120">Требование</span><span class="sxs-lookup"><span data-stu-id="90100-120">Requirement</span></span> | <span data-ttu-id="90100-121">Значение</span><span class="sxs-lookup"><span data-stu-id="90100-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90100-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90100-122">Minimum supported client</span></span><br/> | <span data-ttu-id="90100-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90100-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="90100-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90100-124">Minimum supported server</span></span><br/> | <span data-ttu-id="90100-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90100-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90100-126">Header</span><span class="sxs-lookup"><span data-stu-id="90100-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="90100-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90100-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90100-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90100-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="90100-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="90100-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="90100-130">**\_ADDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="90100-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="90100-131">**CB \_ SETLOCALE**</span><span class="sxs-lookup"><span data-stu-id="90100-131">**CB\_SETLOCALE**</span></span>](cb-setlocale.md)
</dt> <dt>

<span data-ttu-id="90100-132">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="90100-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="90100-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90100-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="90100-134">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90100-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="90100-135">**примарилангид**</span><span class="sxs-lookup"><span data-stu-id="90100-135">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="90100-136">**сублангид**</span><span class="sxs-lookup"><span data-stu-id="90100-136">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

