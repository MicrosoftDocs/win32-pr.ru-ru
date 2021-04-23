---
title: Сообщение EM_FMTLINES (Winuser. h)
description: Задает флаг, определяющий, содержит ли многострочный элемент управления Edit символ разрыва строки. Мягкий разрыв строки состоит из двух возвратов каретки и перевода строки и вставляется в конец строки, которая разорвана из-за вордвраппинг.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- Элементы управления Windows для EM_FMTLINES сообщений
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491010"
---
# <a name="em_fmtlines-message"></a><span data-ttu-id="fa5ba-105">\_Сообщение ФМТЛИНЕС EM</span><span class="sxs-lookup"><span data-stu-id="fa5ba-105">EM\_FMTLINES message</span></span>

<span data-ttu-id="fa5ba-106">Задает флаг, определяющий, содержит ли многострочный элемент управления Edit символ разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-106">Sets a flag that determines whether a multiline edit control includes soft line-break characters.</span></span> <span data-ttu-id="fa5ba-107">Мягкий разрыв строки состоит из двух возвратов каретки и перевода строки и вставляется в конец строки, которая разорвана из-за вордвраппинг.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-107">A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa5ba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa5ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa5ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa5ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa5ba-110">Указывает, следует ли вставлять символы мягкого разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-110">Specifies whether soft line-break characters are to be inserted.</span></span> <span data-ttu-id="fa5ba-111">Значение **true** вставляет символы; значение **false** удаляет их.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-111">A value of **TRUE** inserts the characters; a value of **FALSE** removes them.</span></span>

</dd> <dt>

<span data-ttu-id="fa5ba-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa5ba-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa5ba-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa5ba-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa5ba-114">Return value</span></span>

<span data-ttu-id="fa5ba-115">Возвращаемое значение идентично параметру *wParam* .</span><span class="sxs-lookup"><span data-stu-id="fa5ba-115">The return value is identical to the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa5ba-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa5ba-116">Remarks</span></span>

<span data-ttu-id="fa5ba-117">Это сообщение затрагивает только буфер, возвращенный сообщением [**EM \_**](em-gethandle.md) GetText, и текст, возвращаемый сообщением [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) .</span><span class="sxs-lookup"><span data-stu-id="fa5ba-117">This message affects only the buffer returned by the [**EM\_GETHANDLE**](em-gethandle.md) message and the text returned by the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message.</span></span> <span data-ttu-id="fa5ba-118">Он не влияет на отображение текста в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="fa5ba-118">It has no effect on the display of the text within the edit control.</span></span>

<span data-ttu-id="fa5ba-119">Сообщение **EM \_ фмтлинес** не влияет на линию, завершающуюся сплошным разрывом строки.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-119">The **EM\_FMTLINES** message does not affect a line that ends with a hard line break.</span></span> <span data-ttu-id="fa5ba-120">Фиксированный разрыв строки состоит из одного возврата каретки и перевода строки.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-120">A hard line break consists of one carriage return and a line feed.</span></span>

> [!Note]  
> <span data-ttu-id="fa5ba-121">Размер текста изменяется при обработке этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-121">The size of the text changes when this message is processed.</span></span>

 

<span data-ttu-id="fa5ba-122">**Расширенное редактирование:** Сообщение **EM \_ фмтлинес** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fa5ba-122">**Rich Edit:** The **EM\_FMTLINES** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5ba-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fa5ba-123">Requirements</span></span>



| <span data-ttu-id="fa5ba-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fa5ba-124">Requirement</span></span> | <span data-ttu-id="fa5ba-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fa5ba-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5ba-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa5ba-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa5ba-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa5ba-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa5ba-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa5ba-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa5ba-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa5ba-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa5ba-130">Header</span><span class="sxs-lookup"><span data-stu-id="fa5ba-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa5ba-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa5ba-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa5ba-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa5ba-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa5ba-133">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fa5ba-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa5ba-134">**EM \_**</span><span class="sxs-lookup"><span data-stu-id="fa5ba-134">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

<span data-ttu-id="fa5ba-135">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="fa5ba-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fa5ba-136">**WM \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="fa5ba-136">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

