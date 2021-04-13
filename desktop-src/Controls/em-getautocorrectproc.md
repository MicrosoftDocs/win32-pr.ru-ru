---
title: Сообщение EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Возвращает указатель на определяемую приложением функцию Аутокорректпрок.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Элементы управления Windows для EM_GETAUTOCORRECTPROC сообщений
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491007"
---
# <a name="em_getautocorrectproc-message"></a><span data-ttu-id="bb982-104">\_Сообщение ЖЕТАУТОКОРРЕКТПРОК EM</span><span class="sxs-lookup"><span data-stu-id="bb982-104">EM\_GETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="bb982-105">Возвращает указатель на определяемую приложением функцию [*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .</span><span class="sxs-lookup"><span data-stu-id="bb982-105">Gets a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb982-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb982-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb982-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb982-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb982-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bb982-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bb982-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb982-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb982-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bb982-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb982-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb982-111">Return value</span></span>

<span data-ttu-id="bb982-112">Возвращает указатель на определяемую приложением функцию [*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .</span><span class="sxs-lookup"><span data-stu-id="bb982-112">Returns a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb982-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bb982-113">Requirements</span></span>



| <span data-ttu-id="bb982-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bb982-114">Requirement</span></span> | <span data-ttu-id="bb982-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bb982-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb982-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb982-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb982-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bb982-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bb982-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb982-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb982-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bb982-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb982-120">Header</span><span class="sxs-lookup"><span data-stu-id="bb982-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb982-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb982-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb982-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb982-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb982-123">*аутокорректпрок*</span><span class="sxs-lookup"><span data-stu-id="bb982-123">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="bb982-124">**EM \_ каллаутокорректпрок**</span><span class="sxs-lookup"><span data-stu-id="bb982-124">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="bb982-125">**EM \_ сетаутокорректпрок**</span><span class="sxs-lookup"><span data-stu-id="bb982-125">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





