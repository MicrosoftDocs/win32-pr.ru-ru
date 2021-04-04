---
title: Сообщение CB_GETTOPINDEX (Winuser. h)
description: Приложение отправляет \_ сообщение ЖЕТТОПИНДЕКС CB, чтобы получить Отсчитываемый от нуля индекс первого видимого элемента в списке в поле со списком.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Элементы управления Windows для CB_GETTOPINDEX сообщений
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988639"
---
# <a name="cb_gettopindex-message"></a><span data-ttu-id="3ca4d-104">\_Сообщение ЖЕТТОПИНДЕКС CB</span><span class="sxs-lookup"><span data-stu-id="3ca4d-104">CB\_GETTOPINDEX message</span></span>

<span data-ttu-id="3ca4d-105">Приложение отправляет сообщение **\_ жеттопиндекс CB** , чтобы получить Отсчитываемый от нуля индекс первого видимого элемента в списке в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="3ca4d-105">An application sends the **CB\_GETTOPINDEX** message to retrieve the zero-based index of the first visible item in the list box portion of a combo box.</span></span> <span data-ttu-id="3ca4d-106">Изначально элемент с индексом 0 находится в верхней части окна списка, но если содержимое списка было прокручено, то в верхней части может находиться другой элемент.</span><span class="sxs-lookup"><span data-stu-id="3ca4d-106">Initially, the item with index 0 is at the top of the list box, but if the list box contents have been scrolled, another item may be at the top.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ca4d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ca4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca4d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ca4d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ca4d-109">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3ca4d-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3ca4d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ca4d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ca4d-111">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3ca4d-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca4d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ca4d-112">Return value</span></span>

<span data-ttu-id="3ca4d-113">Если сообщение прошло успешно, возвращается значение индекса первого видимого элемента в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="3ca4d-113">If the message is successful, the return value is the index of the first visible item in the list box of the combo box.</span></span>

<span data-ttu-id="3ca4d-114">Если сообщение не выполняется, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3ca4d-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca4d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3ca4d-115">Requirements</span></span>



| <span data-ttu-id="3ca4d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3ca4d-116">Requirement</span></span> | <span data-ttu-id="3ca4d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3ca4d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca4d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ca4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca4d-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ca4d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ca4d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ca4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca4d-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ca4d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ca4d-122">Header</span><span class="sxs-lookup"><span data-stu-id="3ca4d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca4d-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ca4d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ca4d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ca4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca4d-125">**\_СЕТТОПИНДЕКС CB**</span><span class="sxs-lookup"><span data-stu-id="3ca4d-125">**CB\_SETTOPINDEX**</span></span>](cb-settopindex.md)
</dt> </dl>

 

 





