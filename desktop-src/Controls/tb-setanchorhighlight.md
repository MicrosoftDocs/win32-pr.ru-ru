---
title: Сообщение TB_SETANCHORHIGHLIGHT (Коммктрл. h)
description: Задает параметр выделения закреплений для панели инструментов.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- Элементы управления Windows для TB_SETANCHORHIGHLIGHT сообщений
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654419"
---
# <a name="tb_setanchorhighlight-message"></a><span data-ttu-id="32ca4-104">\_Сообщение СЕТАНЧОРХИГХЛИГХТ ТБ</span><span class="sxs-lookup"><span data-stu-id="32ca4-104">TB\_SETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="32ca4-105">Задает параметр выделения закреплений для панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="32ca4-105">Sets the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="32ca4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32ca4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ca4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32ca4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32ca4-108">**Логическое** значение, указывающее, включено или отключено выделение закреплений.</span><span class="sxs-lookup"><span data-stu-id="32ca4-108">**BOOL** value that specifies if anchor highlighting is enabled or disabled.</span></span> <span data-ttu-id="32ca4-109">Если это значение не равно нулю, выделение привязки будет включено.</span><span class="sxs-lookup"><span data-stu-id="32ca4-109">If this value is nonzero, anchor highlighting will be enabled.</span></span> <span data-ttu-id="32ca4-110">Если это значение равно нулю, выделение закреплений будет отключено.</span><span class="sxs-lookup"><span data-stu-id="32ca4-110">If this value is zero, anchor highlighting will be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="32ca4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32ca4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32ca4-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="32ca4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ca4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32ca4-113">Return value</span></span>

<span data-ttu-id="32ca4-114">Возвращает предыдущий параметр выделения привязки.</span><span class="sxs-lookup"><span data-stu-id="32ca4-114">Returns the previous anchor highlight setting.</span></span> <span data-ttu-id="32ca4-115">Если это значение не равно нулю, выделение закреплений включено.</span><span class="sxs-lookup"><span data-stu-id="32ca4-115">If this value is nonzero, anchor highlighting was enabled.</span></span> <span data-ttu-id="32ca4-116">Если это значение равно нулю, выделение закреплений отключено.</span><span class="sxs-lookup"><span data-stu-id="32ca4-116">If this value is zero, anchor highlighting was disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ca4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32ca4-117">Remarks</span></span>

<span data-ttu-id="32ca4-118">Выделение привязок на панели инструментов означает, что последний выделенный элемент останется выделенным, пока не будет выделен другой элемент.</span><span class="sxs-lookup"><span data-stu-id="32ca4-118">Anchor highlighting in a toolbar means that the last highlighted item will remain highlighted until another item is highlighted.</span></span> <span data-ttu-id="32ca4-119">Это происходит, даже если курсор покидает элемент управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="32ca4-119">This occurs even if the cursor leaves the toolbar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ca4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="32ca4-120">Requirements</span></span>



| <span data-ttu-id="32ca4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="32ca4-121">Requirement</span></span> | <span data-ttu-id="32ca4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="32ca4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32ca4-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32ca4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="32ca4-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32ca4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32ca4-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32ca4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="32ca4-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32ca4-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32ca4-127">Header</span><span class="sxs-lookup"><span data-stu-id="32ca4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ca4-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ca4-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





