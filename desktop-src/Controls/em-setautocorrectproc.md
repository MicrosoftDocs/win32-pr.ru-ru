---
title: Сообщение EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Определяет текущую процедуру обратного вызова для автозамены.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- Элементы управления Windows для EM_SETAUTOCORRECTPROC сообщений
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492483"
---
# <a name="em_setautocorrectproc-message"></a><span data-ttu-id="2282c-104">\_Сообщение СЕТАУТОКОРРЕКТПРОК EM</span><span class="sxs-lookup"><span data-stu-id="2282c-104">EM\_SETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="2282c-105">Определяет текущую процедуру обратного вызова для автозамены.</span><span class="sxs-lookup"><span data-stu-id="2282c-105">Defines the current autocorrect callback procedure.</span></span>


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a><span data-ttu-id="2282c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2282c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2282c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2282c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2282c-108">Функция обратного вызова [*аутокорректпрок*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .</span><span class="sxs-lookup"><span data-stu-id="2282c-108">The [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) callback function.</span></span>

</dd> <dt>

<span data-ttu-id="2282c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2282c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2282c-110">Не используется; должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="2282c-110">Not used; must be zero</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2282c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2282c-111">Return value</span></span>

<span data-ttu-id="2282c-112">Если операция выполнена удачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2282c-112">If the operation succeeds, the return value is zero.</span></span> <span data-ttu-id="2282c-113">Если операция завершается неудачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="2282c-113">If the operation fails, the return value is a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2282c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2282c-114">Requirements</span></span>



| <span data-ttu-id="2282c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2282c-115">Requirement</span></span> | <span data-ttu-id="2282c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2282c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2282c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2282c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2282c-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2282c-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2282c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2282c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2282c-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2282c-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2282c-121">Header</span><span class="sxs-lookup"><span data-stu-id="2282c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2282c-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2282c-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2282c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2282c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2282c-124">*аутокорректпрок*</span><span class="sxs-lookup"><span data-stu-id="2282c-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="2282c-125">**EM \_ каллаутокорректпрок**</span><span class="sxs-lookup"><span data-stu-id="2282c-125">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="2282c-126">**EM \_ жетаутокорректпрок**</span><span class="sxs-lookup"><span data-stu-id="2282c-126">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> </dl>

 

 





