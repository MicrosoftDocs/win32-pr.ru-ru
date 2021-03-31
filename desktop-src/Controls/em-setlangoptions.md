---
title: Сообщение EM_SETLANGOPTIONS (RichEdit. h)
description: Задает параметры для редактора методов ввода (IME) и поддержки восточно-азиатских языков в элементе управления Rich Edit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- Элементы управления Windows для EM_SETLANGOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988553"
---
# <a name="em_setlangoptions-message"></a><span data-ttu-id="4cdf3-104">\_Сообщение СЕТЛАНГОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="4cdf3-104">EM\_SETLANGOPTIONS message</span></span>

<span data-ttu-id="4cdf3-105">Задает параметры для редактора методов ввода (IME) и поддержки восточно-азиатских языков в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-105">Sets options for Input Method Editor (IME) and Asian language support in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cdf3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cdf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cdf3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cdf3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cdf3-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4cdf3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cdf3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cdf3-110">Задает параметры языка.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-110">Specifies the language options.</span></span> <span data-ttu-id="4cdf3-111">Список возможных значений см. в разделе [**EM \_ жетлангоптионс**](em-getlangoptions.md).</span><span class="sxs-lookup"><span data-stu-id="4cdf3-111">For a list of possible values, see [**EM\_GETLANGOPTIONS**](em-getlangoptions.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cdf3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cdf3-112">Return value</span></span>

<span data-ttu-id="4cdf3-113">Это сообщение возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-113">This message returns a value of 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cdf3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cdf3-114">Remarks</span></span>

<span data-ttu-id="4cdf3-115">Сообщение **\_ сетлангоптионс EM** управляет следующими элементами:</span><span class="sxs-lookup"><span data-stu-id="4cdf3-115">The **EM\_SETLANGOPTIONS** message controls the following:</span></span>

-   <span data-ttu-id="4cdf3-116">Автоматическая привязка шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-116">Automatic font binding.</span></span>
-   <span data-ttu-id="4cdf3-117">Автоматическое переключение клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-117">Automatic keyboard switching.</span></span>
-   <span data-ttu-id="4cdf3-118">Автоматическая настройка размера шрифта.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-118">Automatic font size adjustment.</span></span>
-   <span data-ttu-id="4cdf3-119">Использование шрифтов по умолчанию пользовательского интерфейса вместо шрифтов по умолчанию для документов.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-119">Use of user-interface default fonts instead of document default fonts.</span></span>
-   <span data-ttu-id="4cdf3-120">Уведомления для клиента во время составления IME.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-120">Notifications to client during IME composition.</span></span>
-   <span data-ttu-id="4cdf3-121">Как редактор IME прерывает режим композиции.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-121">How IME aborts composition mode.</span></span>
-   <span data-ttu-id="4cdf3-122">Проверка орфографии, Автозамена и прогнозирование сенсорной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-122">Spell checking, autocorrect, and touch keyboard prediction.</span></span>

<span data-ttu-id="4cdf3-123">В этом сообщении задаются значения всех флагов параметров языка.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-123">This message sets the values of all language option flags.</span></span> <span data-ttu-id="4cdf3-124">Чтобы изменить подмножество флагов, отправьте сообщение [**\_ жетлангоптионс EM**](em-getlangoptions.md) для получения текущих флагов параметров, измените флаги, которые необходимо изменить, а затем отправьте сообщение **EM \_ сетлангоптионс** с результатом.</span><span class="sxs-lookup"><span data-stu-id="4cdf3-124">To change a subset of the flags, send the [**EM\_GETLANGOPTIONS**](em-getlangoptions.md) message to get the current option flags, change the flags that you need to change, and then send the **EM\_SETLANGOPTIONS** message with the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cdf3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4cdf3-125">Requirements</span></span>



| <span data-ttu-id="4cdf3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4cdf3-126">Requirement</span></span> | <span data-ttu-id="4cdf3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4cdf3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdf3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cdf3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4cdf3-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cdf3-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cdf3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cdf3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4cdf3-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4cdf3-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cdf3-132">Header</span><span class="sxs-lookup"><span data-stu-id="4cdf3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cdf3-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cdf3-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cdf3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cdf3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cdf3-135">**EM \_ жетлангоптионс**</span><span class="sxs-lookup"><span data-stu-id="4cdf3-135">**EM\_GETLANGOPTIONS**</span></span>](em-getlangoptions.md)
</dt> </dl>

 

 





