---
title: Сообщение CB_GETITEMDATA (Winuser. h)
description: Приложение отправляет \_ сообщение ЖЕТИТЕМДАТА CB в поле со списком для получения указанного приложением значения, связанного с указанным элементом в поле со списком.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- Элементы управления Windows для CB_GETITEMDATA сообщений
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802242"
---
# <a name="cb_getitemdata-message"></a><span data-ttu-id="6096a-104">\_Сообщение ЖЕТИТЕМДАТА CB</span><span class="sxs-lookup"><span data-stu-id="6096a-104">CB\_GETITEMDATA message</span></span>

<span data-ttu-id="6096a-105">Приложение отправляет сообщение **\_ жетитемдата CB** в поле со списком для получения указанного приложением значения, связанного с указанным элементом в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="6096a-105">An application sends a **CB\_GETITEMDATA** message to a combo box to retrieve the application-supplied value associated with the specified item in the combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6096a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6096a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6096a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6096a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6096a-108">Основанный на нуле индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="6096a-108">The zero-based index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="6096a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6096a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6096a-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="6096a-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6096a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6096a-111">Return value</span></span>

<span data-ttu-id="6096a-112">Возвращаемое значение — это значение, связанное с элементом.</span><span class="sxs-lookup"><span data-stu-id="6096a-112">The return value is the value associated with the item.</span></span> <span data-ttu-id="6096a-113">Если возникает ошибка, это может быть значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6096a-113">If an error occurs, it is CB\_ERR.</span></span>

<span data-ttu-id="6096a-114">Если элемент находится в поле со списком, созданном владельцем, без стиля [**\_ хасстрингс CBS**](combo-box-styles.md) , возвращаемое значение является значением, содержащимся в параметре *lParam* сообщения [**CB \_ ADDSTRING**](cb-addstring.md) или [**CB \_ инсертстринг**](cb-insertstring.md) , которое добавляет элемент в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="6096a-114">If the item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the return value is the value contained in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message, that added the item to the combo box.</span></span> <span data-ttu-id="6096a-115">Если стиль **\_ хасстрингс CBS** не использовался, возвращаемое значение является параметром *lParam* , содержащимся в [**сообщении \_ сетитемдата CB**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6096a-115">If the **CBS\_HASSTRINGS** style was not used, the return value is the *lParam* parameter contained in a [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6096a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6096a-116">Requirements</span></span>



| <span data-ttu-id="6096a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6096a-117">Requirement</span></span> | <span data-ttu-id="6096a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6096a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6096a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6096a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6096a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6096a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6096a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6096a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6096a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6096a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6096a-123">Header</span><span class="sxs-lookup"><span data-stu-id="6096a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6096a-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6096a-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6096a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6096a-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6096a-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6096a-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6096a-127">**\_ADDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="6096a-127">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="6096a-128">**\_ИНСЕРТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="6096a-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="6096a-129">**\_СЕТИТЕМДАТА CB**</span><span class="sxs-lookup"><span data-stu-id="6096a-129">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
</dt> </dl>

 

 





