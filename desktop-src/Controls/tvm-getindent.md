---
title: Сообщение TVM_GETINDENT (Коммктрл. h)
description: Извлекает величину отступа (в пикселях) дочерних элементов относительно их родительских элементов. Это сообщение можно отправить явным образом или с помощью \_ макроса TreeView.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- Элементы управления Windows для TVM_GETINDENT сообщений
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892602"
---
# <a name="tvm_getindent-message"></a><span data-ttu-id="50a06-105">TVM. \_ сообщение с отступом</span><span class="sxs-lookup"><span data-stu-id="50a06-105">TVM\_GETINDENT message</span></span>

<span data-ttu-id="50a06-106">Извлекает величину отступа (в пикселях) дочерних элементов относительно их родительских элементов.</span><span class="sxs-lookup"><span data-stu-id="50a06-106">Retrieves the amount, in pixels, that child items are indented relative to their parent items.</span></span> <span data-ttu-id="50a06-107">Это сообщение можно отправить явным образом или с помощью макроса [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .</span><span class="sxs-lookup"><span data-stu-id="50a06-107">You can send this message explicitly or by using the [**TreeView\_GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="50a06-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50a06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50a06-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50a06-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="50a06-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="50a06-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="50a06-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50a06-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="50a06-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="50a06-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50a06-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50a06-113">Return value</span></span>

<span data-ttu-id="50a06-114">Возвращает величину отступа.</span><span class="sxs-lookup"><span data-stu-id="50a06-114">Returns the amount of indentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="50a06-115">Требования</span><span class="sxs-lookup"><span data-stu-id="50a06-115">Requirements</span></span>



| <span data-ttu-id="50a06-116">Требование</span><span class="sxs-lookup"><span data-stu-id="50a06-116">Requirement</span></span> | <span data-ttu-id="50a06-117">Значение</span><span class="sxs-lookup"><span data-stu-id="50a06-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50a06-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50a06-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50a06-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50a06-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50a06-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50a06-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50a06-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50a06-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50a06-122">Header</span><span class="sxs-lookup"><span data-stu-id="50a06-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a06-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a06-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





