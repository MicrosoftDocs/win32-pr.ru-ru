---
title: Сообщение PBM_GETBKCOLOR (Коммктрл. h)
description: Возвращает цвет фона индикатора выполнения.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Элементы управления Windows для PBM_GETBKCOLOR сообщений
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892285"
---
# <a name="pbm_getbkcolor-message"></a><span data-ttu-id="bf266-104">\_Сообщение ЖЕТБККОЛОР PBM</span><span class="sxs-lookup"><span data-stu-id="bf266-104">PBM\_GETBKCOLOR message</span></span>

<span data-ttu-id="bf266-105">Возвращает цвет фона индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="bf266-105">Gets the background color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf266-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf266-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf266-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf266-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bf266-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bf266-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bf266-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf266-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bf266-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bf266-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf266-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf266-111">Return value</span></span>

<span data-ttu-id="bf266-112">Возвращает цвет фона индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="bf266-112">Returns the background color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf266-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf266-113">Remarks</span></span>

<span data-ttu-id="bf266-114">Это цвет, заданный в сообщении [**\_ сетбкколор PBM**](pbm-setbkcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="bf266-114">This is the color set by the [**PBM\_SETBKCOLOR**](pbm-setbkcolor.md) message.</span></span> <span data-ttu-id="bf266-115">Значение по умолчанию — CLR \_ по умолчанию, которое определено в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="bf266-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="bf266-116">Эта функция влияет только на классический режим, а не на визуальный стиль.</span><span class="sxs-lookup"><span data-stu-id="bf266-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf266-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf266-117">Requirements</span></span>



| <span data-ttu-id="bf266-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bf266-118">Requirement</span></span> | <span data-ttu-id="bf266-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bf266-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf266-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf266-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf266-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf266-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf266-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf266-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf266-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf266-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf266-124">Header</span><span class="sxs-lookup"><span data-stu-id="bf266-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf266-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf266-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





