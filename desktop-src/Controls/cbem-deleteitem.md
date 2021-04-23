---
title: Сообщение CBEM_DELETEITEM (Коммктрл. h)
description: Удаляет элемент из элемента управления ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- Элементы управления Windows для CBEM_DELETEITEM сообщений
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654709"
---
# <a name="cbem_deleteitem-message"></a><span data-ttu-id="a9a8f-104">\_Сообщение кбем DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="a9a8f-104">CBEM\_DELETEITEM message</span></span>

<span data-ttu-id="a9a8f-105">Удаляет элемент из элемента управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="a9a8f-105">Removes an item from a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9a8f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9a8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a8f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9a8f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a8f-108">Отсчитываемый от нуля индекс удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a9a8f-108">The zero-based index of the item to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="a9a8f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9a8f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a9a8f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a9a8f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a8f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9a8f-111">Return value</span></span>

<span data-ttu-id="a9a8f-112">Возвращает значение типа INT, представляющее количество элементов, остающихся в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="a9a8f-112">Returns an INT value that represents the number of items remaining in the control.</span></span> <span data-ttu-id="a9a8f-113">Если *ииндекс* является недопустимым, сообщение ВОЗВРАЩАЕТ значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="a9a8f-113">If *iIndex* is invalid, the message returns CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a8f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9a8f-114">Remarks</span></span>

<span data-ttu-id="a9a8f-115">Это сообщение сопоставляется с полем со списком элемент управления "сообщение [**CB \_ делетестринг**](cb-deletestring.md)".</span><span class="sxs-lookup"><span data-stu-id="a9a8f-115">This message maps to the combo box control message [**CB\_DELETESTRING**](cb-deletestring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a8f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a9a8f-116">Requirements</span></span>



| <span data-ttu-id="a9a8f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a9a8f-117">Requirement</span></span> | <span data-ttu-id="a9a8f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a9a8f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a8f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9a8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a8f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9a8f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9a8f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9a8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a8f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9a8f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9a8f-123">Header</span><span class="sxs-lookup"><span data-stu-id="a9a8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9a8f-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9a8f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





