---
title: Сообщение CB_SETLOCALE (Winuser. h)
description: Приложение отправляет \_ сообщение CB SETLOCALE для установки текущего языкового стандарта поля со списком. Если поле со списком имеет \_ стиль сортировки CBS и строки добавляются с помощью CB \_ ADDSTRING, языковой стандарт поля со списком влияет на порядок сортировки элементов списка.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- Элементы управления Windows для CB_SETLOCALE сообщений
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491541"
---
# <a name="cb_setlocale-message"></a><span data-ttu-id="e56f8-105">\_Сообщение CB SETLOCALE</span><span class="sxs-lookup"><span data-stu-id="e56f8-105">CB\_SETLOCALE message</span></span>

<span data-ttu-id="e56f8-106">Приложение отправляет сообщение **CB \_ SETLOCALE** для установки текущего языкового стандарта поля со списком.</span><span class="sxs-lookup"><span data-stu-id="e56f8-106">An application sends a **CB\_SETLOCALE** message to set the current locale of the combo box.</span></span> <span data-ttu-id="e56f8-107">Если поле со списком имеет стиль [**\_ сортировки CBS**](combo-box-styles.md) и строки добавляются с помощью [**CB \_ ADDSTRING**](cb-addstring.md), языковой стандарт поля со списком влияет на порядок сортировки элементов списка.</span><span class="sxs-lookup"><span data-stu-id="e56f8-107">If the combo box has the [**CBS\_SORT**](combo-box-styles.md) style and strings are added using [**CB\_ADDSTRING**](cb-addstring.md), the locale of a combo box affects how list items are sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="e56f8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e56f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e56f8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e56f8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e56f8-110">Задает код локали для поля со списком, используемого для сортировки при добавлении текста.</span><span class="sxs-lookup"><span data-stu-id="e56f8-110">Specifies the locale identifier for the combo box to use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="e56f8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e56f8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e56f8-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="e56f8-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e56f8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e56f8-113">Return value</span></span>

<span data-ttu-id="e56f8-114">Возвращаемое значение — это предыдущий идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="e56f8-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="e56f8-115">Если параметр *wParam* задает языковой стандарт, не установленный в системе, возвращается значение CB \_ Err, а текущий языковой стандарт поля со списком не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e56f8-115">If *wParam* specifies a locale not installed on the system, the return value is CB\_ERR and the current combo box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e56f8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e56f8-116">Remarks</span></span>

<span data-ttu-id="e56f8-117">Используйте макрос [**макелЦид**](/windows/desktop/api/winnt/nf-winnt-makelcid) для создания идентификатора языкового стандарта и макроса [**макелангид**](/windows/desktop/api/winnt/nf-winnt-makelangid) для создания идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="e56f8-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier and the [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) macro to construct a language identifier.</span></span> <span data-ttu-id="e56f8-118">Идентификатор языка состоит из основного идентификатора языка и идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="e56f8-118">The language identifier is made up of a primary language identifier and a sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="e56f8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e56f8-119">Requirements</span></span>



| <span data-ttu-id="e56f8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e56f8-120">Requirement</span></span> | <span data-ttu-id="e56f8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e56f8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e56f8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e56f8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e56f8-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e56f8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e56f8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e56f8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e56f8-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e56f8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e56f8-126">Header</span><span class="sxs-lookup"><span data-stu-id="e56f8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e56f8-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e56f8-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56f8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e56f8-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="e56f8-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e56f8-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e56f8-130">**\_ADDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="e56f8-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e56f8-131">**CB \_ ЦБ**</span><span class="sxs-lookup"><span data-stu-id="e56f8-131">**CB\_GETLOCALE**</span></span>](cb-getlocale.md)
</dt> <dt>

<span data-ttu-id="e56f8-132">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e56f8-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e56f8-133">**макелангид**</span><span class="sxs-lookup"><span data-stu-id="e56f8-133">**MAKELANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[<span data-ttu-id="e56f8-134">**макелЦид**</span><span class="sxs-lookup"><span data-stu-id="e56f8-134">**MAKELCID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

