---
title: Сообщение RB_GETTOOLTIPS (Коммктрл. h)
description: Извлекает маркер любого элемента управления ToolTip, связанного с элементом управления "Главная панель".
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- Элементы управления Windows для RB_GETTOOLTIPS сообщений
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136403"
---
# <a name="rb_gettooltips-message"></a><span data-ttu-id="d4bae-104">\_Сообщение о ВЫсказке RB</span><span class="sxs-lookup"><span data-stu-id="d4bae-104">RB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="d4bae-105">Извлекает маркер любого элемента управления ToolTip, связанного с элементом управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="d4bae-105">Retrieves the handle to any tooltip control associated with the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4bae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4bae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4bae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4bae-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d4bae-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d4bae-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d4bae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4bae-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d4bae-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d4bae-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4bae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4bae-111">Return value</span></span>

<span data-ttu-id="d4bae-112">Возвращает значение **HWND** , которое является дескриптором элемента управления ToolTip, связанного с элементом управления главной панели, или нулем, если элемент управления ToolTip не связан с элементом управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="d4bae-112">Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4bae-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d4bae-113">Requirements</span></span>



| <span data-ttu-id="d4bae-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d4bae-114">Requirement</span></span> | <span data-ttu-id="d4bae-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d4bae-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bae-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4bae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d4bae-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4bae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4bae-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4bae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d4bae-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4bae-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4bae-120">Header</span><span class="sxs-lookup"><span data-stu-id="d4bae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4bae-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4bae-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





