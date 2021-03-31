---
title: Сообщение CB_GETCOUNT (Winuser. h)
description: Возвращает количество элементов списка в поле со списком.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- Элементы управления Windows для CB_GETCOUNT сообщений
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804163"
---
# <a name="cb_getcount-message"></a><span data-ttu-id="71f9c-104">\_Сообщение о ВЫЧИСЛЕ CB</span><span class="sxs-lookup"><span data-stu-id="71f9c-104">CB\_GETCOUNT message</span></span>

<span data-ttu-id="71f9c-105">Возвращает количество элементов списка в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="71f9c-105">Gets the number of items in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="71f9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71f9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71f9c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71f9c-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="71f9c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="71f9c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71f9c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71f9c-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="71f9c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f9c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71f9c-111">Return value</span></span>

<span data-ttu-id="71f9c-112">Возвращаемое значение — это число элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="71f9c-112">The return value is the number of items in the list box.</span></span> <span data-ttu-id="71f9c-113">Если возникает ошибка, это может быть значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="71f9c-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="71f9c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71f9c-114">Remarks</span></span>

<span data-ttu-id="71f9c-115">Индекс отсчитывается от нуля, поэтому возвращаемое значение Count больше значения индекса последнего элемента.</span><span class="sxs-lookup"><span data-stu-id="71f9c-115">The index is zero-based, so the returned count is one greater than the index value of the last item.</span></span>

## <a name="requirements"></a><span data-ttu-id="71f9c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="71f9c-116">Requirements</span></span>



| <span data-ttu-id="71f9c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="71f9c-117">Requirement</span></span> | <span data-ttu-id="71f9c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="71f9c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f9c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71f9c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71f9c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71f9c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71f9c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71f9c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71f9c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71f9c-123">Header</span><span class="sxs-lookup"><span data-stu-id="71f9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="71f9c-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71f9c-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





