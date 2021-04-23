---
title: Сообщение CB_SETEXTENDEDUI (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТЕКСТЕНДЕДУИ CB, чтобы выбрать пользовательский интерфейс по умолчанию или расширенный пользовательский интерфейс для поля со списком, которое содержит \_ раскрывающийся список CBS или \_ стиль DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- Элементы управления Windows для CB_SETEXTENDEDUI сообщений
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490527"
---
# <a name="cb_setextendedui-message"></a><span data-ttu-id="41ddc-104">\_Сообщение СЕТЕКСТЕНДЕДУИ CB</span><span class="sxs-lookup"><span data-stu-id="41ddc-104">CB\_SETEXTENDEDUI message</span></span>

<span data-ttu-id="41ddc-105">Приложение отправляет сообщение **\_ сетекстендедуи CB** , чтобы выбрать пользовательский интерфейс по умолчанию или расширенный пользовательский интерфейс для поля со списком, которое содержит [**\_ раскрывающийся список CBS**](combo-box-styles.md) или стиль [**\_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="41ddc-105">An application sends a **CB\_SETEXTENDEDUI** message to select either the default UI or the extended UI for a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="41ddc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41ddc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41ddc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41ddc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41ddc-108">**Логическое** значение, указывающее, использует ли поле со списком расширенный пользовательский интерфейс (**true**) или пользовательский интерфейс по умолчанию (**false**).</span><span class="sxs-lookup"><span data-stu-id="41ddc-108">A **BOOL** that specifies whether the combo box uses the extended UI (**TRUE**) or the default UI (**FALSE**).</span></span>

</dd> <dt>

<span data-ttu-id="41ddc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41ddc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41ddc-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="41ddc-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41ddc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41ddc-111">Return value</span></span>

<span data-ttu-id="41ddc-112">Если операция выполнена успешно, возвращается значение CB \_ .</span><span class="sxs-lookup"><span data-stu-id="41ddc-112">If the operation succeeds, the return value is CB\_OKAY.</span></span> <span data-ttu-id="41ddc-113">Если возникает ошибка, это может быть значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="41ddc-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="41ddc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41ddc-114">Remarks</span></span>

<span data-ttu-id="41ddc-115">По умолчанию клавиша F4 открывает или закрывает список, а стрелка вниз изменяет текущее выделение.</span><span class="sxs-lookup"><span data-stu-id="41ddc-115">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="41ddc-116">В расширенном пользовательском интерфейсе клавиша F4 отключена, а клавиша со стрелкой вниз открывает раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="41ddc-116">In the extended UI, the F4 key is disabled and the DOWN ARROW key opens the drop-down list.</span></span> <span data-ttu-id="41ddc-117">Колесико мыши, которое обычно прокручивается по элементам списка, не действует при установке расширенного пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="41ddc-117">The mouse wheel, which normally scrolls through the items in the list, has no effect when the extended UI is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="41ddc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="41ddc-118">Requirements</span></span>



| <span data-ttu-id="41ddc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="41ddc-119">Requirement</span></span> | <span data-ttu-id="41ddc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="41ddc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41ddc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41ddc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41ddc-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41ddc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41ddc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41ddc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41ddc-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41ddc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41ddc-125">Header</span><span class="sxs-lookup"><span data-stu-id="41ddc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="41ddc-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41ddc-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41ddc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41ddc-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="41ddc-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="41ddc-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="41ddc-129">**\_ЖЕТЕКСТЕНДЕДУИ CB**</span><span class="sxs-lookup"><span data-stu-id="41ddc-129">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
</dt> <dt>

<span data-ttu-id="41ddc-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="41ddc-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="41ddc-131">Возможности поля со списком</span><span class="sxs-lookup"><span data-stu-id="41ddc-131">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





