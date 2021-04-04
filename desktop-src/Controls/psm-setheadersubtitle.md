---
title: Сообщение PSM_SETHEADERSUBTITLE (Пршт. h)
description: Задает текст подзаголовка для заголовка внутренней страницы мастера. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ сесеадерсубтитле.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- Элементы управления Windows для PSM_SETHEADERSUBTITLE сообщений
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988594"
---
# <a name="psm_setheadersubtitle-message"></a><span data-ttu-id="f2338-105">\_Сообщение ПСМ сесеадерсубтитле</span><span class="sxs-lookup"><span data-stu-id="f2338-105">PSM\_SETHEADERSUBTITLE message</span></span>

<span data-ttu-id="f2338-106">Задает текст подзаголовка для заголовка внутренней страницы мастера.</span><span class="sxs-lookup"><span data-stu-id="f2338-106">Sets the subtitle text for the header of a wizard's interior page.</span></span> <span data-ttu-id="f2338-107">Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ сесеадерсубтитле**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .</span><span class="sxs-lookup"><span data-stu-id="f2338-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2338-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2338-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2338-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2338-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2338-110">Отсчитываемый от нуля индекс страницы мастера.</span><span class="sxs-lookup"><span data-stu-id="f2338-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="f2338-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2338-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2338-112">Подзаголовок нового заголовка.</span><span class="sxs-lookup"><span data-stu-id="f2338-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2338-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2338-113">Return value</span></span>

<span data-ttu-id="f2338-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f2338-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2338-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2338-115">Remarks</span></span>

<span data-ttu-id="f2338-116">Если указать текущую страницу, она будет немедленно перерисована для вывода нового субтитра.</span><span class="sxs-lookup"><span data-stu-id="f2338-116">If you specify the current page, it will immediately be repainted to display the new subtitle.</span></span>

> [!Note]  
> <span data-ttu-id="f2338-117">Это сообщение не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="f2338-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2338-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f2338-118">Requirements</span></span>



| <span data-ttu-id="f2338-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f2338-119">Requirement</span></span> | <span data-ttu-id="f2338-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f2338-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2338-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2338-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2338-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2338-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f2338-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2338-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2338-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2338-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2338-125">Header</span><span class="sxs-lookup"><span data-stu-id="f2338-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2338-126"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2338-126"><dt>Prsht.h</dt></span></span> </dl>      |
| <span data-ttu-id="f2338-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f2338-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f2338-128">**ПСМ \_ СЕСЕАДЕРСУБТИТЛЕВ** (Юникод) и **ПСМ \_ сесеадерсубтитлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f2338-128">**PSM\_SETHEADERSUBTITLEW** (Unicode) and **PSM\_SETHEADERSUBTITLEA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2338-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2338-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2338-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f2338-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2338-131">**ПСМ \_ хвндтоиндекс**</span><span class="sxs-lookup"><span data-stu-id="f2338-131">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="f2338-132">**ПСМ \_ идтоиндекс**</span><span class="sxs-lookup"><span data-stu-id="f2338-132">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="f2338-133">**ПСМ \_ пажетоиндекс**</span><span class="sxs-lookup"><span data-stu-id="f2338-133">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 





