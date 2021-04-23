---
title: Сообщение PSM_SETHEADERTITLE (Пршт. h)
description: Задает текст заголовка для заголовка внутренней страницы мастера. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ сесеадертитле.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Элементы управления Windows для PSM_SETHEADERTITLE сообщений
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654424"
---
# <a name="psm_setheadertitle-message"></a><span data-ttu-id="226b3-105">\_Сообщение ПСМ сесеадертитле</span><span class="sxs-lookup"><span data-stu-id="226b3-105">PSM\_SETHEADERTITLE message</span></span>

<span data-ttu-id="226b3-106">Задает текст заголовка для заголовка внутренней страницы мастера.</span><span class="sxs-lookup"><span data-stu-id="226b3-106">Sets the title text for the header of a wizard's interior page.</span></span> <span data-ttu-id="226b3-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ сесеадертитле**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .</span><span class="sxs-lookup"><span data-stu-id="226b3-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="226b3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="226b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="226b3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="226b3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="226b3-110">Отсчитываемый от нуля индекс страницы мастера.</span><span class="sxs-lookup"><span data-stu-id="226b3-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="226b3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="226b3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="226b3-112">Подзаголовок нового заголовка.</span><span class="sxs-lookup"><span data-stu-id="226b3-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="226b3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="226b3-113">Return value</span></span>

<span data-ttu-id="226b3-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="226b3-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="226b3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="226b3-115">Remarks</span></span>

<span data-ttu-id="226b3-116">Если указать текущую страницу, она будет немедленно перерисована для вывода нового заголовка.</span><span class="sxs-lookup"><span data-stu-id="226b3-116">If you specify the current page, it will immediately be repainted to display the new title.</span></span>

## <a name="requirements"></a><span data-ttu-id="226b3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="226b3-117">Requirements</span></span>



| <span data-ttu-id="226b3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="226b3-118">Requirement</span></span> | <span data-ttu-id="226b3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="226b3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="226b3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="226b3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="226b3-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="226b3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="226b3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="226b3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="226b3-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="226b3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="226b3-124">Header</span><span class="sxs-lookup"><span data-stu-id="226b3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="226b3-125"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="226b3-125"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="226b3-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="226b3-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="226b3-127">**ПСМ \_ СЕСЕАДЕРТИТЛЕВ** (Юникод) и **ПСМ \_ сесеадертитлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="226b3-127">**PSM\_SETHEADERTITLEW** (Unicode) and **PSM\_SETHEADERTITLEA** (ANSI)</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="226b3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="226b3-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="226b3-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="226b3-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="226b3-130">**ПСМ \_ хвндтоиндекс**</span><span class="sxs-lookup"><span data-stu-id="226b3-130">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="226b3-131">**ПСМ \_ идтоиндекс**</span><span class="sxs-lookup"><span data-stu-id="226b3-131">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="226b3-132">**ПСМ \_ пажетоиндекс**</span><span class="sxs-lookup"><span data-stu-id="226b3-132">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





