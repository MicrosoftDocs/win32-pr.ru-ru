---
title: Сообщение EM_SETELLIPSISMODE (RichEdit. h)
description: Это сообщение задает текущий режим многоточия.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- Элементы управления Windows для EM_SETELLIPSISMODE сообщений
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071914"
---
# <a name="em_setellipsismode-message"></a><span data-ttu-id="0276a-104">\_Сообщение СЕТЕЛЛИПСИСМОДЕ EM</span><span class="sxs-lookup"><span data-stu-id="0276a-104">EM\_SETELLIPSISMODE message</span></span>

<span data-ttu-id="0276a-105">Это сообщение задает текущий режим многоточия.</span><span class="sxs-lookup"><span data-stu-id="0276a-105">This message sets the current ellipsis mode.</span></span> <span data-ttu-id="0276a-106">Если этот параметр включен, для текста, который не умещается в окне отображения, отображается многоточие ().</span><span class="sxs-lookup"><span data-stu-id="0276a-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="0276a-107">Многоточие используется только в том случае, если элемент управления неактивен.</span><span class="sxs-lookup"><span data-stu-id="0276a-107">The ellipsis is only used when the control isn t active.</span></span> <span data-ttu-id="0276a-108">При активном режиме полосы прокрутки используются для отображения текста, который не умещается в окне отображения.</span><span class="sxs-lookup"><span data-stu-id="0276a-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a><span data-ttu-id="0276a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0276a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0276a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0276a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0276a-111">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="0276a-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0276a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0276a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0276a-113">Значение типа DWORD, которое принимает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0276a-113">A DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="0276a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0276a-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="0276a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0276a-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="0276a-116"><dt>**МНОГОТОЧИе \_ нет**</dt></span><span class="sxs-lookup"><span data-stu-id="0276a-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="0276a-117">Многоточие не используется.</span><span class="sxs-lookup"><span data-stu-id="0276a-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="0276a-118"><dt>**конец МНОГОТОЧИя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0276a-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="0276a-119">Многоточие в конце (принудительное прерывание).</span><span class="sxs-lookup"><span data-stu-id="0276a-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="0276a-120"><dt>**слово МНОГОТОЧИя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0276a-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="0276a-121">Многоточие в конце (разрыв слова).</span><span class="sxs-lookup"><span data-stu-id="0276a-121">Ellipsis at the end (word break).</span></span><br/>   |



 

<span data-ttu-id="0276a-122">Биты для этих значений помещаются в **\_ маску многоточия**.</span><span class="sxs-lookup"><span data-stu-id="0276a-122">The bits for these values all fit in the **ELLIPSIS\_MASK**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0276a-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0276a-123">Return value</span></span>

<span data-ttu-id="0276a-124">Если параметр wParam равен 0, а параметр lParam является одним из значений в таблице выше, то возвращаемое значение равно TRUE; в противном случае возвращаемое значение равно FALSE.</span><span class="sxs-lookup"><span data-stu-id="0276a-124">If wparam is 0 and lparam is one of the values in the table above, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0276a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0276a-125">Requirements</span></span>



| <span data-ttu-id="0276a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0276a-126">Requirement</span></span> | <span data-ttu-id="0276a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0276a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0276a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0276a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0276a-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0276a-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0276a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0276a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0276a-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0276a-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0276a-132">Header</span><span class="sxs-lookup"><span data-stu-id="0276a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0276a-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0276a-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0276a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0276a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0276a-135">**EM \_ жетеллипсисмоде**</span><span class="sxs-lookup"><span data-stu-id="0276a-135">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="0276a-136">**EM \_ жетеллипсисстате**</span><span class="sxs-lookup"><span data-stu-id="0276a-136">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





