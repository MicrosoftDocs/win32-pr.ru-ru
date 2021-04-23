---
title: Сообщение EM_HIDESELECTION (RichEdit. h)
description: Сообщение EM \_ хидеселектион скрывает или отображает выделенный фрагмент в элементе управления Rich Edit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Элементы управления Windows для EM_HIDESELECTION сообщений
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988267"
---
# <a name="em_hideselection-message"></a><span data-ttu-id="3496b-104">\_Сообщение ХИДЕСЕЛЕКТИОН EM</span><span class="sxs-lookup"><span data-stu-id="3496b-104">EM\_HIDESELECTION message</span></span>

<span data-ttu-id="3496b-105">Сообщение **EM \_ хидеселектион** скрывает или отображает выделенный фрагмент в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3496b-105">The **EM\_HIDESELECTION** message hides or shows the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3496b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3496b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3496b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3496b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3496b-108">Значение, указывающее, следует ли скрывать или отображать выделенный фрагмент.</span><span class="sxs-lookup"><span data-stu-id="3496b-108">Value specifying whether to hide or show the selection.</span></span> <span data-ttu-id="3496b-109">Если этот параметр равен нулю, выводится выбранный фрагмент.</span><span class="sxs-lookup"><span data-stu-id="3496b-109">If this parameter is zero, the selection is shown.</span></span> <span data-ttu-id="3496b-110">В противном случае выделение будет скрыто.</span><span class="sxs-lookup"><span data-stu-id="3496b-110">Otherwise, the selection is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="3496b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3496b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3496b-112">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3496b-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3496b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3496b-113">Return value</span></span>

<span data-ttu-id="3496b-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3496b-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3496b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3496b-115">Requirements</span></span>



| <span data-ttu-id="3496b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3496b-116">Requirement</span></span> | <span data-ttu-id="3496b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3496b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3496b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3496b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3496b-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3496b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3496b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3496b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3496b-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3496b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3496b-122">Header</span><span class="sxs-lookup"><span data-stu-id="3496b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3496b-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3496b-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





