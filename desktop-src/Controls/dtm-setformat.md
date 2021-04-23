---
title: Сообщение DTM_SETFORMAT (Коммктрл. h)
description: Задает отображение элемента управления "Выбор даты и времени" (DTP) на основе заданной строки формата. Это сообщение можно отправить явным образом или использовать \_ макрос Сетформат DateTime.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- Элементы управления Windows для DTM_SETFORMAT сообщений
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071825"
---
# <a name="dtm_setformat-message"></a><span data-ttu-id="b64ea-105">\_Сообщение DTM сетформат</span><span class="sxs-lookup"><span data-stu-id="b64ea-105">DTM\_SETFORMAT message</span></span>

<span data-ttu-id="b64ea-106">Задает отображение элемента управления "Выбор даты и времени" (DTP) на основе заданной строки формата.</span><span class="sxs-lookup"><span data-stu-id="b64ea-106">Sets the display of a date and time picker (DTP) control based on a given format string.</span></span> <span data-ttu-id="b64ea-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетформат DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .</span><span class="sxs-lookup"><span data-stu-id="b64ea-107">You can send this message explicitly or use the [**DateTime\_SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b64ea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b64ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b64ea-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b64ea-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b64ea-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b64ea-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b64ea-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b64ea-112">Указатель на [строку формата](date-and-time-picker-controls.md) с нулевым нулем, которая определяет требуемый вид.</span><span class="sxs-lookup"><span data-stu-id="b64ea-112">A pointer to a zero-terminated [format string](date-and-time-picker-controls.md) that defines the desired display.</span></span> <span data-ttu-id="b64ea-113">Если задать для этого параметра **значение NULL** , элемент управления будет сброшен в строку форматирования по умолчанию для текущего стиля.</span><span class="sxs-lookup"><span data-stu-id="b64ea-113">Setting this parameter to **NULL** will reset the control to the default format string for the current style.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64ea-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b64ea-114">Return value</span></span>

<span data-ttu-id="b64ea-115">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b64ea-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b64ea-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b64ea-116">Remarks</span></span>

<span data-ttu-id="b64ea-117">Можно включить в строку формата дополнительные символы, чтобы получить более широкие возможности просмотра.</span><span class="sxs-lookup"><span data-stu-id="b64ea-117">It is acceptable to include extra characters within the format string to produce a more rich display.</span></span> <span data-ttu-id="b64ea-118">Однако любые неформатированные символы должны быть заключены в одинарные кавычки.</span><span class="sxs-lookup"><span data-stu-id="b64ea-118">However, any nonformat characters must be enclosed within single quotes.</span></span> <span data-ttu-id="b64ea-119">Например, строка формата "" уже сегодня: "ЧЧ": "m": Ддддмммдд "," yyy "выдаст выходные данные, как" сегодня: 04:22:31 вторник марта 23, 1996 ".</span><span class="sxs-lookup"><span data-stu-id="b64ea-119">For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996".</span></span>

> [!Note]  
> <span data-ttu-id="b64ea-120">Элемент управления DTP отслеживает изменения языкового стандарта при использовании строки формата по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b64ea-120">A DTP control tracks locale changes when it is using the default format string.</span></span> <span data-ttu-id="b64ea-121">Если задать строку настраиваемого формата, она не будет обновляться в ответ на изменения языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="b64ea-121">If you set a custom format string, it will not be updated in response to locale changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b64ea-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b64ea-122">Requirements</span></span>



| <span data-ttu-id="b64ea-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b64ea-123">Requirement</span></span> | <span data-ttu-id="b64ea-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b64ea-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b64ea-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b64ea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b64ea-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b64ea-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b64ea-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b64ea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b64ea-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b64ea-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b64ea-129">Header</span><span class="sxs-lookup"><span data-stu-id="b64ea-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b64ea-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b64ea-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b64ea-131">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b64ea-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b64ea-132">**DTM \_ СЕТФОРМАТВ** (Юникод) и **DTM \_ сетформата** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b64ea-132">**DTM\_SETFORMATW** (Unicode) and **DTM\_SETFORMATA** (ANSI)</span></span><br/>               |



 

 





