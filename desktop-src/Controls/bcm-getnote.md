---
title: Сообщение BCM_GETNOTE (Коммктрл. h)
description: Возвращает текст заметки, связанной с кнопкой ссылки на команду. Это сообщение можно отправить явным образом или воспользоваться макросом "Кнопка" \_ .
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- Элементы управления Windows для BCM_GETNOTE сообщений
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654528"
---
# <a name="bcm_getnote-message"></a><span data-ttu-id="11950-105">\_Сообщение о НЕзамете BCM</span><span class="sxs-lookup"><span data-stu-id="11950-105">BCM\_GETNOTE message</span></span>

<span data-ttu-id="11950-106">Возвращает текст заметки, связанной с кнопкой ссылки на команду.</span><span class="sxs-lookup"><span data-stu-id="11950-106">Gets the text of the note associated with a command link button.</span></span> <span data-ttu-id="11950-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**"Кнопка" \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .</span><span class="sxs-lookup"><span data-stu-id="11950-107">You can send this message explicitly or use the [**Button\_GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="11950-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11950-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11950-109">*wParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="11950-109">*wParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="11950-110">Значение **типа DWORD** , указывающее размер буфера, на который указывает *lParam*, в символах.</span><span class="sxs-lookup"><span data-stu-id="11950-110">A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="11950-111">*lParam* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="11950-111">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11950-112">Буфер строки для получения текста.</span><span class="sxs-lookup"><span data-stu-id="11950-112">The string buffer to receive the text.</span></span> <span data-ttu-id="11950-113">Размер буфера должен быть достаточным для размещения завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="11950-113">The buffer must be large enough to accommodate the terminating NULL character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11950-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11950-114">Return value</span></span>

<span data-ttu-id="11950-115">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="11950-115">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="11950-116">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="11950-116">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11950-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11950-117">Remarks</span></span>

<span data-ttu-id="11950-118">Сообщение **BCM/ \_ Note** работает только с кнопками, у которых есть стиль кнопки [**BS \_ коммандлинк**](button-styles.md) или [**BS \_ дефкоммандлинк**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="11950-118">The **BCM\_GETNOTE** message works only with buttons that have the [**BS\_COMMANDLINK**](button-styles.md) or [**BS\_DEFCOMMANDLINK**](button-styles.md) button style.</span></span>

<span data-ttu-id="11950-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) будет содержать:</span><span class="sxs-lookup"><span data-stu-id="11950-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will contain:</span></span>

-   <span data-ttu-id="11950-120">Ошибка \_ не \_ поддерживается, если у кнопки нет стиля " [**BS \_ Дефкоммандлинк**](button-styles.md) " или " [**BS \_ коммандлинк**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="11950-120">ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md) or [**BS\_COMMANDLINK**](button-styles.md) style.</span></span>
-   <span data-ttu-id="11950-121">Ошибка \_ \_ не хватает буфера, если буфер *lParam* слишком мал.</span><span class="sxs-lookup"><span data-stu-id="11950-121">ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small.</span></span> <span data-ttu-id="11950-122">Параметр *wParam* будет содержать требуемый размер буфера в символах.</span><span class="sxs-lookup"><span data-stu-id="11950-122">The *wParam* parameter will contain the required buffer size, in characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="11950-123">Требования</span><span class="sxs-lookup"><span data-stu-id="11950-123">Requirements</span></span>



| <span data-ttu-id="11950-124">Требование</span><span class="sxs-lookup"><span data-stu-id="11950-124">Requirement</span></span> | <span data-ttu-id="11950-125">Значение</span><span class="sxs-lookup"><span data-stu-id="11950-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11950-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11950-126">Minimum supported client</span></span><br/> | <span data-ttu-id="11950-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11950-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11950-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11950-128">Minimum supported server</span></span><br/> | <span data-ttu-id="11950-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11950-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11950-130">Header</span><span class="sxs-lookup"><span data-stu-id="11950-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="11950-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="11950-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11950-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11950-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="11950-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="11950-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="11950-134">Стили кнопок</span><span class="sxs-lookup"><span data-stu-id="11950-134">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="11950-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="11950-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="11950-136">Типы кнопок</span><span class="sxs-lookup"><span data-stu-id="11950-136">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

