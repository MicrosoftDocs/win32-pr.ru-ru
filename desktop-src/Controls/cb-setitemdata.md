---
title: Сообщение CB_SETITEMDATA (Winuser. h)
description: Приложение отправляет \_ сообщение СЕТИТЕМДАТА CB, чтобы задать значение, связанное с указанным элементом в поле со списком.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Элементы управления Windows для CB_SETITEMDATA сообщений
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892253"
---
# <a name="cb_setitemdata-message"></a><span data-ttu-id="c9ed2-104">\_Сообщение СЕТИТЕМДАТА CB</span><span class="sxs-lookup"><span data-stu-id="c9ed2-104">CB\_SETITEMDATA message</span></span>

<span data-ttu-id="c9ed2-105">Приложение отправляет сообщение **\_ сетитемдата CB** , чтобы задать значение, связанное с указанным элементом в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="c9ed2-105">An application sends a **CB\_SETITEMDATA** message to set the value associated with the specified item in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9ed2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9ed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ed2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9ed2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ed2-108">Указывает индекс (Отсчитываемый от нуля) элемента.</span><span class="sxs-lookup"><span data-stu-id="c9ed2-108">Specifies the item's zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="c9ed2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9ed2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ed2-110">Указывает новое значение, которое должно быть связано с элементом.</span><span class="sxs-lookup"><span data-stu-id="c9ed2-110">Specifies the new value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ed2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9ed2-111">Return value</span></span>

<span data-ttu-id="c9ed2-112">Если возникает ошибка, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="c9ed2-112">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9ed2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9ed2-113">Remarks</span></span>

<span data-ttu-id="c9ed2-114">Если указанный элемент находится в поле со списком, рисуемом владельцем, созданным без стиля [**\_ хасстрингс CBS**](combo-box-styles.md) , это сообщение заменяет значение параметра *lParam* сообщения [**CB \_ ADDSTRING**](cb-addstring.md) или [**CB \_ инсертстринг**](cb-insertstring.md) , которое добавляет элемент в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="c9ed2-114">If the specified item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, this message replaces the value in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message that added the item to the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ed2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c9ed2-115">Requirements</span></span>



| <span data-ttu-id="c9ed2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c9ed2-116">Requirement</span></span> | <span data-ttu-id="c9ed2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c9ed2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ed2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9ed2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9ed2-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9ed2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9ed2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9ed2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9ed2-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9ed2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c9ed2-122">Header</span><span class="sxs-lookup"><span data-stu-id="c9ed2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9ed2-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9ed2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ed2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9ed2-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9ed2-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c9ed2-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c9ed2-126">**\_ADDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="c9ed2-126">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="c9ed2-127">**\_ЖЕТИТЕМДАТА CB**</span><span class="sxs-lookup"><span data-stu-id="c9ed2-127">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="c9ed2-128">**\_ИНСЕРТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="c9ed2-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





