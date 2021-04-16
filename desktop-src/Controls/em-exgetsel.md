---
title: Сообщение EM_EXGETSEL (RichEdit. h)
description: Получает позиции начального и конечного символов выделения в элементе управления Rich Edit.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- Элементы управления Windows для EM_EXGETSEL сообщений
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491487"
---
# <a name="em_exgetsel-message"></a><span data-ttu-id="71a6f-104">\_Сообщение ЕКСЖЕТСЕЛ EM</span><span class="sxs-lookup"><span data-stu-id="71a6f-104">EM\_EXGETSEL message</span></span>

<span data-ttu-id="71a6f-105">Получает позиции начального и конечного символов выделения в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="71a6f-105">Retrieves the starting and ending character positions of the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="71a6f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71a6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71a6f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71a6f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71a6f-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="71a6f-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="71a6f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71a6f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71a6f-110">Структура [**чарранже**](/windows/desktop/api/Richedit/ns-richedit-charrange) , которая получает диапазон выбора.</span><span class="sxs-lookup"><span data-stu-id="71a6f-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that receives the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71a6f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71a6f-111">Return value</span></span>

<span data-ttu-id="71a6f-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="71a6f-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="71a6f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="71a6f-113">Requirements</span></span>



| <span data-ttu-id="71a6f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="71a6f-114">Requirement</span></span> | <span data-ttu-id="71a6f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="71a6f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71a6f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71a6f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="71a6f-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71a6f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71a6f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71a6f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="71a6f-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71a6f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71a6f-120">Header</span><span class="sxs-lookup"><span data-stu-id="71a6f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="71a6f-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="71a6f-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a6f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71a6f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a6f-123">**чарранже**</span><span class="sxs-lookup"><span data-stu-id="71a6f-123">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





