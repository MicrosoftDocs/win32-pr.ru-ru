---
title: Сообщение CB_GETEXTENDEDUI (Winuser. h)
description: Определяет, имеет ли поле со списком пользовательский интерфейс по умолчанию или расширенный пользовательский интерфейс.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- Элементы управления Windows для CB_GETEXTENDEDUI сообщений
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490548"
---
# <a name="cb_getextendedui-message"></a><span data-ttu-id="63713-104">\_Сообщение ЖЕТЕКСТЕНДЕДУИ CB</span><span class="sxs-lookup"><span data-stu-id="63713-104">CB\_GETEXTENDEDUI message</span></span>

<span data-ttu-id="63713-105">Определяет, имеет ли поле со списком пользовательский интерфейс по умолчанию или расширенный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="63713-105">Determines whether a combo box has the default user interface or the extended user interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="63713-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63713-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63713-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63713-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63713-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="63713-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="63713-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63713-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63713-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="63713-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63713-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63713-111">Return value</span></span>

<span data-ttu-id="63713-112">Если поле со списком содержит расширенный пользовательский интерфейс, возвращаемое значение равно **true**; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="63713-112">If the combo box has the extended user interface, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="63713-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63713-113">Remarks</span></span>

<span data-ttu-id="63713-114">По умолчанию клавиша F4 открывает или закрывает список, а стрелка вниз изменяет текущее выделение.</span><span class="sxs-lookup"><span data-stu-id="63713-114">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="63713-115">В поле со списком с расширенным пользовательским интерфейсом клавиша F4 отключена, а нажатие клавиши со стрелкой вниз открывает раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="63713-115">In a combo box with the extended user interface, the F4 key is disabled and pressing the DOWN ARROW key opens the drop-down list.</span></span>

## <a name="requirements"></a><span data-ttu-id="63713-116">Требования</span><span class="sxs-lookup"><span data-stu-id="63713-116">Requirements</span></span>



| <span data-ttu-id="63713-117">Требование</span><span class="sxs-lookup"><span data-stu-id="63713-117">Requirement</span></span> | <span data-ttu-id="63713-118">Значение</span><span class="sxs-lookup"><span data-stu-id="63713-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63713-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63713-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63713-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63713-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63713-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63713-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63713-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63713-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63713-123">Header</span><span class="sxs-lookup"><span data-stu-id="63713-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="63713-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63713-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63713-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63713-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="63713-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="63713-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="63713-127">**\_СЕТЕКСТЕНДЕДУИ CB**</span><span class="sxs-lookup"><span data-stu-id="63713-127">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
</dt> <dt>

<span data-ttu-id="63713-128">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="63713-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="63713-129">Возможности поля со списком</span><span class="sxs-lookup"><span data-stu-id="63713-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





