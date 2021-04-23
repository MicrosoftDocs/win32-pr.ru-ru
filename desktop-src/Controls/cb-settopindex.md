---
title: Сообщение CB_SETTOPINDEX (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТТОПИНДЕКС CB, чтобы убедиться, что конкретный элемент отображается в списке поля со списком.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Элементы управления Windows для CB_SETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801240"
---
# <a name="cb_settopindex-message"></a><span data-ttu-id="2477e-104">\_Сообщение СЕТТОПИНДЕКС CB</span><span class="sxs-lookup"><span data-stu-id="2477e-104">CB\_SETTOPINDEX message</span></span>

<span data-ttu-id="2477e-105">Приложение отправляет сообщение **\_ сеттопиндекс CB** , чтобы убедиться, что конкретный элемент отображается в списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="2477e-105">An application sends the **CB\_SETTOPINDEX** message to ensure that a particular item is visible in the list box of a combo box.</span></span> <span data-ttu-id="2477e-106">Система прокручивает содержимое списка таким образом, чтобы указанный элемент появился в верхней части окна списка или был достигнут максимальный диапазон прокрутки.</span><span class="sxs-lookup"><span data-stu-id="2477e-106">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="2477e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2477e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2477e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2477e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2477e-109">Указывает отсчитываемый от нуля индекс элемента списка.</span><span class="sxs-lookup"><span data-stu-id="2477e-109">Specifies the zero-based index of the list item.</span></span>

</dd> <dt>

<span data-ttu-id="2477e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2477e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2477e-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="2477e-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2477e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2477e-112">Return value</span></span>

<span data-ttu-id="2477e-113">Если сообщение прошло успешно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2477e-113">If the message is successful, the return value is zero.</span></span>

<span data-ttu-id="2477e-114">Если сообщение не выполняется, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="2477e-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="2477e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2477e-115">Requirements</span></span>



| <span data-ttu-id="2477e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2477e-116">Requirement</span></span> | <span data-ttu-id="2477e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2477e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2477e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2477e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2477e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2477e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2477e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2477e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2477e-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2477e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2477e-122">Header</span><span class="sxs-lookup"><span data-stu-id="2477e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2477e-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2477e-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2477e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2477e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2477e-125">**\_ЖЕТТОПИНДЕКС CB**</span><span class="sxs-lookup"><span data-stu-id="2477e-125">**CB\_GETTOPINDEX**</span></span>](cb-gettopindex.md)
</dt> </dl>

 

 





