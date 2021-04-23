---
title: Сообщение CB_SETITEMHEIGHT (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТИТЕМХЕИГХТ CB, чтобы задать высоту элементов списка или поле выбора в поле со списком.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- Элементы управления Windows для CB_SETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654676"
---
# <a name="cb_setitemheight-message"></a><span data-ttu-id="caaa6-104">\_Сообщение СЕТИТЕМХЕИГХТ CB</span><span class="sxs-lookup"><span data-stu-id="caaa6-104">CB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="caaa6-105">Приложение отправляет сообщение **\_ сетитемхеигхт CB** , чтобы задать высоту элементов списка или поле выбора в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="caaa6-105">An application sends a **CB\_SETITEMHEIGHT** message to set the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="caaa6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="caaa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caaa6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="caaa6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caaa6-108">Указывает компонент поля со списком, для которого задается высота.</span><span class="sxs-lookup"><span data-stu-id="caaa6-108">Specifies the component of the combo box for which to set the height.</span></span>

<span data-ttu-id="caaa6-109">Этот параметр должен иметь значение 1, чтобы задать высоту поля выбора.</span><span class="sxs-lookup"><span data-stu-id="caaa6-109">This parameter must be  1 to set the height of the selection field.</span></span> <span data-ttu-id="caaa6-110">Значение высоты элементов списка должно быть равно нулю, если только поле со списком не имеет стиль [**CBS \_ овнердраввариабле**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="caaa6-110">It must be zero to set the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="caaa6-111">В этом случае параметр *wParam* — это Отсчитываемый от нуля индекс определенного элемента списка.</span><span class="sxs-lookup"><span data-stu-id="caaa6-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="caaa6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="caaa6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caaa6-113">Задает высоту (в пикселях) компонента поля со списком, идентифицируемого параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="caaa6-113">Specifies the height, in pixels, of the combo box component identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caaa6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="caaa6-114">Return value</span></span>

<span data-ttu-id="caaa6-115">Если индекс или высота являются недопустимыми, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="caaa6-115">If the index or height is invalid, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="caaa6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="caaa6-116">Remarks</span></span>

<span data-ttu-id="caaa6-117">Высота поля выбора в поле со списком задается независимо от высоты элементов списка.</span><span class="sxs-lookup"><span data-stu-id="caaa6-117">The selection field height in a combo box is set independently of the height of the list items.</span></span> <span data-ttu-id="caaa6-118">Приложение должно гарантировать, что высота поля выбора не меньше высоты определенного элемента списка.</span><span class="sxs-lookup"><span data-stu-id="caaa6-118">An application must ensure that the height of the selection field is not smaller than the height of a particular list item.</span></span>

## <a name="requirements"></a><span data-ttu-id="caaa6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="caaa6-119">Requirements</span></span>



| <span data-ttu-id="caaa6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="caaa6-120">Requirement</span></span> | <span data-ttu-id="caaa6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="caaa6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caaa6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="caaa6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="caaa6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="caaa6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="caaa6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="caaa6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="caaa6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="caaa6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="caaa6-126">Header</span><span class="sxs-lookup"><span data-stu-id="caaa6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="caaa6-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="caaa6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caaa6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caaa6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="caaa6-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="caaa6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="caaa6-130">**\_GETITEMHEIGHT CB**</span><span class="sxs-lookup"><span data-stu-id="caaa6-130">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
</dt> <dt>

[<span data-ttu-id="caaa6-131">**WM \_ меасуреитем**</span><span class="sxs-lookup"><span data-stu-id="caaa6-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





