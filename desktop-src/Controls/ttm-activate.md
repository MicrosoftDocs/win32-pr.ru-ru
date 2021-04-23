---
title: Сообщение TTM_ACTIVATE (Коммктрл. h)
description: Активирует или деактивирует элемент управления ToolTip.
ms.assetid: f37da001-748c-4c51-bb32-dc49031ff2fb
keywords:
- Элементы управления Windows для TTM_ACTIVATE сообщений
topic_type:
- apiref
api_name:
- TTM_ACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e200b769cd3d9e07cb63a5a540960bcc707f862d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071644"
---
# <a name="ttm_activate-message"></a><span data-ttu-id="53141-104">\_Сообщение о активации ТТМ</span><span class="sxs-lookup"><span data-stu-id="53141-104">TTM\_ACTIVATE message</span></span>

<span data-ttu-id="53141-105">Активирует или деактивирует элемент управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="53141-105">Activates or deactivates a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53141-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53141-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53141-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53141-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53141-108">Флаг активации.</span><span class="sxs-lookup"><span data-stu-id="53141-108">Activation flag.</span></span> <span data-ttu-id="53141-109">Если этот параметр имеет **значение true**, элемент управления ToolTip активируется.</span><span class="sxs-lookup"><span data-stu-id="53141-109">If this parameter is **TRUE**, the tooltip control is activated.</span></span> <span data-ttu-id="53141-110">Если значение равно **false**, элемент управления ToolTip деактивируется.</span><span class="sxs-lookup"><span data-stu-id="53141-110">If it is **FALSE**, the tooltip control is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="53141-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53141-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="53141-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="53141-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53141-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53141-113">Return value</span></span>

<span data-ttu-id="53141-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="53141-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53141-115">Требования</span><span class="sxs-lookup"><span data-stu-id="53141-115">Requirements</span></span>



| <span data-ttu-id="53141-116">Требование</span><span class="sxs-lookup"><span data-stu-id="53141-116">Requirement</span></span> | <span data-ttu-id="53141-117">Значение</span><span class="sxs-lookup"><span data-stu-id="53141-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53141-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53141-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53141-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53141-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53141-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53141-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53141-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53141-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53141-122">Header</span><span class="sxs-lookup"><span data-stu-id="53141-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53141-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="53141-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





