---
title: Сообщение EM_GETELLIPSISSTATE (RichEdit. h)
description: Извлекает текущее состояние многоточия.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Элементы управления Windows для EM_GETELLIPSISSTATE сообщений
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490725"
---
# <a name="em_getellipsisstate-message"></a><span data-ttu-id="1529f-104">\_Сообщение ЖЕТЕЛЛИПСИССТАТЕ EM</span><span class="sxs-lookup"><span data-stu-id="1529f-104">EM\_GETELLIPSISSTATE message</span></span>

<span data-ttu-id="1529f-105">Извлекает текущее состояние многоточия.</span><span class="sxs-lookup"><span data-stu-id="1529f-105">Retrieves the current ellipsis state.</span></span>


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a><span data-ttu-id="1529f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1529f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1529f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1529f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1529f-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1529f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1529f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1529f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1529f-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1529f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1529f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1529f-111">Return value</span></span>

<span data-ttu-id="1529f-112">Возвращаемое значение равно TRUE, если отображается многоточие, и FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1529f-112">The return value is TRUE if an ellipsis is being displayed and FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1529f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1529f-113">Requirements</span></span>



| <span data-ttu-id="1529f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1529f-114">Requirement</span></span> | <span data-ttu-id="1529f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1529f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1529f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1529f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1529f-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1529f-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1529f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1529f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1529f-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1529f-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1529f-120">Header</span><span class="sxs-lookup"><span data-stu-id="1529f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1529f-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1529f-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1529f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1529f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1529f-123">**EM \_ жетеллипсисмоде**</span><span class="sxs-lookup"><span data-stu-id="1529f-123">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="1529f-124">**EM \_ сетеллипсисмоде**</span><span class="sxs-lookup"><span data-stu-id="1529f-124">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> </dl>

 

 





