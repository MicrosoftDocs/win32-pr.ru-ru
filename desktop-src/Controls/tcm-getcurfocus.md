---
title: Сообщение TCM_GETCURFOCUS (Коммктрл. h)
description: Возвращает индекс элемента, который находится в фокусе ввода в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл жеткурфокус.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- Элементы управления Windows для TCM_GETCURFOCUS сообщений
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989227"
---
# <a name="tcm_getcurfocus-message"></a><span data-ttu-id="e231e-105">\_Сообщение ЖЕТКУРФОКУС TCM</span><span class="sxs-lookup"><span data-stu-id="e231e-105">TCM\_GETCURFOCUS message</span></span>

<span data-ttu-id="e231e-106">Возвращает индекс элемента, который находится в фокусе ввода в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="e231e-106">Returns the index of the item that has the focus in a tab control.</span></span> <span data-ttu-id="e231e-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ жеткурфокус**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="e231e-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e231e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e231e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e231e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e231e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e231e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e231e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e231e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e231e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e231e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e231e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e231e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e231e-113">Return value</span></span>

<span data-ttu-id="e231e-114">Возвращает индекс элемента вкладки, который находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="e231e-114">Returns the index of the tab item that has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="e231e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e231e-115">Remarks</span></span>

<span data-ttu-id="e231e-116">Элемент, имеющий фокус, может отличаться от выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="e231e-116">The item that has the focus may be different than the selected item.</span></span>

## <a name="requirements"></a><span data-ttu-id="e231e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e231e-117">Requirements</span></span>



| <span data-ttu-id="e231e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e231e-118">Requirement</span></span> | <span data-ttu-id="e231e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e231e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e231e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e231e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e231e-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e231e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e231e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e231e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e231e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e231e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e231e-124">Header</span><span class="sxs-lookup"><span data-stu-id="e231e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e231e-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e231e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





