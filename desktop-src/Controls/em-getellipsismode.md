---
title: Сообщение EM_GETELLIPSISMODE (RichEdit. h)
description: Извлекает текущий режим с многоточием.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- Элементы управления Windows для EM_GETELLIPSISMODE сообщений
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135970"
---
# <a name="em_getellipsismode-message"></a><span data-ttu-id="373ae-104">\_Сообщение ЖЕТЕЛЛИПСИСМОДЕ EM</span><span class="sxs-lookup"><span data-stu-id="373ae-104">EM\_GETELLIPSISMODE message</span></span>

<span data-ttu-id="373ae-105">Извлекает текущий режим с многоточием.</span><span class="sxs-lookup"><span data-stu-id="373ae-105">Retrieves the current ellipsis mode.</span></span> <span data-ttu-id="373ae-106">Если этот параметр включен, для текста, который не умещается в окне отображения, отображается многоточие ().</span><span class="sxs-lookup"><span data-stu-id="373ae-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="373ae-107">Многоточие используется только в том случае, если элемент управления неактивен.</span><span class="sxs-lookup"><span data-stu-id="373ae-107">The ellipsis is only used when the control is not active.</span></span> <span data-ttu-id="373ae-108">При активном режиме полосы прокрутки используются для отображения текста, который не умещается в окне отображения.</span><span class="sxs-lookup"><span data-stu-id="373ae-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a><span data-ttu-id="373ae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="373ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="373ae-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="373ae-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="373ae-111">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="373ae-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="373ae-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="373ae-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="373ae-113">Указатель на DWORD, который получает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="373ae-113">Pointer to a DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="373ae-114">Значение</span><span class="sxs-lookup"><span data-stu-id="373ae-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="373ae-115">Значение</span><span class="sxs-lookup"><span data-stu-id="373ae-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="373ae-116"><dt>**МНОГОТОЧИе \_ нет**</dt></span><span class="sxs-lookup"><span data-stu-id="373ae-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="373ae-117">Многоточие не используется.</span><span class="sxs-lookup"><span data-stu-id="373ae-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="373ae-118"><dt>**конец МНОГОТОЧИя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="373ae-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="373ae-119">Многоточие в конце (принудительное прерывание).</span><span class="sxs-lookup"><span data-stu-id="373ae-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="373ae-120"><dt>**слово МНОГОТОЧИя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="373ae-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="373ae-121">Многоточие в конце (разрыв слова).</span><span class="sxs-lookup"><span data-stu-id="373ae-121">Ellipsis at the end (word break).</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="373ae-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="373ae-122">Return value</span></span>

<span data-ttu-id="373ae-123">Если параметр wParam равен 0, а параметр lParam не равен NULL, то возвращаемое значение равно TRUE; в противном случае возвращаемое значение равно FALSE.</span><span class="sxs-lookup"><span data-stu-id="373ae-123">If wparam is 0 and lparam is not NULL, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="373ae-124">Требования</span><span class="sxs-lookup"><span data-stu-id="373ae-124">Requirements</span></span>



| <span data-ttu-id="373ae-125">Требование</span><span class="sxs-lookup"><span data-stu-id="373ae-125">Requirement</span></span> | <span data-ttu-id="373ae-126">Значение</span><span class="sxs-lookup"><span data-stu-id="373ae-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="373ae-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="373ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="373ae-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="373ae-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="373ae-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="373ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="373ae-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="373ae-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="373ae-131">Header</span><span class="sxs-lookup"><span data-stu-id="373ae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="373ae-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="373ae-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="373ae-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="373ae-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="373ae-134">**EM \_ сетеллипсисмоде**</span><span class="sxs-lookup"><span data-stu-id="373ae-134">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> <dt>

[<span data-ttu-id="373ae-135">**EM \_ жетеллипсисстате**</span><span class="sxs-lookup"><span data-stu-id="373ae-135">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





