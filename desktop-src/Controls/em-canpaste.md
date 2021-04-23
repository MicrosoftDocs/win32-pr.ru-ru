---
title: Сообщение EM_CANPASTE (RichEdit. h)
description: Определяет, может ли элемент управления Rich-Edit вставлять указанный формат буфера обмена.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- Элементы управления Windows для EM_CANPASTE сообщений
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071785"
---
# <a name="em_canpaste-message"></a><span data-ttu-id="5a52f-104">\_Сообщение КАНПАСТЕ EM</span><span class="sxs-lookup"><span data-stu-id="5a52f-104">EM\_CANPASTE message</span></span>

<span data-ttu-id="5a52f-105">Определяет, может ли элемент управления Rich-Edit вставлять указанный формат буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="5a52f-105">Determines whether a rich edit control can paste a specified clipboard format.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a52f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a52f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a52f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5a52f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a52f-108">Указывает [форматы буфера обмена](/windows/desktop/dataxchg/clipboard-formats) для попыток.</span><span class="sxs-lookup"><span data-stu-id="5a52f-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats) to try.</span></span> <span data-ttu-id="5a52f-109">Чтобы использовать любой формат в буфере обмена, присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="5a52f-109">To try any format currently on the clipboard, set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5a52f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5a52f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5a52f-111">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5a52f-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a52f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a52f-112">Return value</span></span>

<span data-ttu-id="5a52f-113">Если формат буфера обмена может быть вставлен, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="5a52f-113">If the clipboard format can be pasted, the return value is a nonzero value.</span></span>

<span data-ttu-id="5a52f-114">Если формат буфера обмена не может быть вставлен, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5a52f-114">If the clipboard format cannot be pasted, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a52f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5a52f-115">Requirements</span></span>



| <span data-ttu-id="5a52f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5a52f-116">Requirement</span></span> | <span data-ttu-id="5a52f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5a52f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a52f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a52f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a52f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a52f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a52f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a52f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a52f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a52f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a52f-122">Header</span><span class="sxs-lookup"><span data-stu-id="5a52f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a52f-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a52f-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a52f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a52f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a52f-125">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="5a52f-125">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

