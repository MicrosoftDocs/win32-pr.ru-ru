---
title: Сообщение EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Задает расширенную процедуру разбиения по словам для элемента управления расширенного редактирования.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Элементы управления Windows для EM_SETWORDBREAKPROCEX сообщений
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988485"
---
# <a name="em_setwordbreakprocex-message"></a><span data-ttu-id="021d9-104">\_Сообщение СЕТВОРДБРЕАКПРОЦЕКС EM</span><span class="sxs-lookup"><span data-stu-id="021d9-104">EM\_SETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="021d9-105">Задает расширенную процедуру разбиения по словам для элемента управления расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="021d9-105">Sets the extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="021d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="021d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="021d9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="021d9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="021d9-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="021d9-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="021d9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="021d9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="021d9-110">Указатель на функцию [*едитвордбреакпроцекс*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) или **значение NULL** для использования процедуры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="021d9-110">Pointer to an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function, or **NULL** to use the default procedure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="021d9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="021d9-111">Return value</span></span>

<span data-ttu-id="021d9-112">Это сообщение возвращает адрес предыдущей расширенной процедуры разбиения по словам.</span><span class="sxs-lookup"><span data-stu-id="021d9-112">This message returns the address of the previous extended word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="021d9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="021d9-113">Requirements</span></span>



| <span data-ttu-id="021d9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="021d9-114">Requirement</span></span> | <span data-ttu-id="021d9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="021d9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="021d9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="021d9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="021d9-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="021d9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="021d9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="021d9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="021d9-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="021d9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="021d9-120">Header</span><span class="sxs-lookup"><span data-stu-id="021d9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="021d9-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="021d9-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="021d9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="021d9-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="021d9-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="021d9-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="021d9-124">**едитвордбреакпроцекс**</span><span class="sxs-lookup"><span data-stu-id="021d9-124">**EditWordBreakProcEx**</span></span>](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[<span data-ttu-id="021d9-125">**EM \_ жетвордбреакпроцекс**</span><span class="sxs-lookup"><span data-stu-id="021d9-125">**EM\_GETWORDBREAKPROCEX**</span></span>](em-getwordbreakprocex.md)
</dt> </dl>

 

 





