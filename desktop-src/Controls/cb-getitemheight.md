---
title: Сообщение CB_GETITEMHEIGHT (Winuser. h)
description: Определяет высоту элементов списка или поля выбора в поле со списком.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- Элементы управления Windows для CB_GETITEMHEIGHT сообщений
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891925"
---
# <a name="cb_getitemheight-message"></a><span data-ttu-id="3b882-104">\_Сообщение GETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="3b882-104">CB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="3b882-105">Определяет высоту элементов списка или поля выбора в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="3b882-105">Determines the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b882-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b882-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b882-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b882-108">Компонент поля со списком, высота которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="3b882-108">The combo box component whose height is to be retrieved.</span></span> <span data-ttu-id="3b882-109">Этот параметр должен иметь значение-1, чтобы получить высоту поля выбора.</span><span class="sxs-lookup"><span data-stu-id="3b882-109">This parameter must be -1 to retrieve the height of the selection field.</span></span> <span data-ttu-id="3b882-110">Чтобы получить высоту элементов списка, значение должно быть равно нулю, если только поле со списком не имеет стиль [**CBS \_ овнердраввариабле**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3b882-110">It must be zero to retrieve the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="3b882-111">В этом случае параметр *wParam* — это Отсчитываемый от нуля индекс определенного элемента списка.</span><span class="sxs-lookup"><span data-stu-id="3b882-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="3b882-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b882-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b882-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="3b882-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b882-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b882-114">Return value</span></span>

<span data-ttu-id="3b882-115">Возвращаемое значение — это высота (в пикселях) элементов списка в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="3b882-115">The return value is the height, in pixels, of the list items in a combo box.</span></span> <span data-ttu-id="3b882-116">Если поле со списком имеет стиль [**CBS \_ овнердраввариабле**](combo-box-styles.md) , это высота элемента, заданного параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="3b882-116">If the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, it is the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="3b882-117">Если параметр *wParam* равен-1, то возвращаемое значение является высотой элемента управления редактирования (или статического текста) в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="3b882-117">If *wParam* is -1, the return value is the height of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="3b882-118">Если возникает ошибка, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3b882-118">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b882-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3b882-119">Requirements</span></span>



| <span data-ttu-id="3b882-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3b882-120">Requirement</span></span> | <span data-ttu-id="3b882-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3b882-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b882-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b882-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b882-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b882-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3b882-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b882-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b882-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b882-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3b882-126">Header</span><span class="sxs-lookup"><span data-stu-id="3b882-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b882-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b882-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b882-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b882-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b882-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3b882-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3b882-130">**\_СЕТИТЕМХЕИГХТ CB**</span><span class="sxs-lookup"><span data-stu-id="3b882-130">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
</dt> <dt>

[<span data-ttu-id="3b882-131">**WM \_ меасуреитем**</span><span class="sxs-lookup"><span data-stu-id="3b882-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





