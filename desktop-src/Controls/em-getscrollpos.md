---
title: Сообщение EM_GETSCROLLPOS (RichEdit. h)
description: Получает текущую точку прокрутки элемента управления "поле ввода".
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- Элементы управления Windows для EM_GETSCROLLPOS сообщений
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490377"
---
# <a name="em_getscrollpos-message"></a><span data-ttu-id="a0f44-104">\_Сообщение ЖЕТСКРОЛЛПОС EM</span><span class="sxs-lookup"><span data-stu-id="a0f44-104">EM\_GETSCROLLPOS message</span></span>

<span data-ttu-id="a0f44-105">Получает текущую точку прокрутки элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="a0f44-105">Obtains the current scroll position of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0f44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0f44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0f44-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f44-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="a0f44-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0f44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0f44-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f44-110">Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a0f44-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="a0f44-111">После вызова **EM \_ жетскроллпос** эти параметры содержат точку в виртуальном текстовом пространстве документа, выраженную в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a0f44-111">After calling **EM\_GETSCROLLPOS**, this parameters contains a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="a0f44-112">Это будет точка, которая в данный момент находится в левом верхнем углу окна редактирования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a0f44-112">This point will be the point that is currently located in the upper-left corner of the edit control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f44-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0f44-113">Return value</span></span>

<span data-ttu-id="a0f44-114">Это сообщение всегда возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="a0f44-114">This message always returns 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f44-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0f44-115">Remarks</span></span>

<span data-ttu-id="a0f44-116">Значения, возвращаемые в структуре [**Point**](/previous-versions//dd162805(v=vs.85)) , представляют собой 16-разрядные значения (даже в 32-разрядных полях).</span><span class="sxs-lookup"><span data-stu-id="a0f44-116">The values returned in the [**POINT**](/previous-versions//dd162805(v=vs.85)) structure are 16-bit values (even in the 32-bit wide fields).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f44-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a0f44-117">Requirements</span></span>



| <span data-ttu-id="a0f44-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a0f44-118">Requirement</span></span> | <span data-ttu-id="a0f44-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a0f44-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f44-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0f44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f44-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0f44-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0f44-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0f44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f44-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0f44-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0f44-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a0f44-124">Redistributable</span></span><br/>          | <span data-ttu-id="a0f44-125">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="a0f44-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="a0f44-126">Header</span><span class="sxs-lookup"><span data-stu-id="a0f44-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f44-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f44-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f44-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0f44-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f44-129">**EM \_ сетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="a0f44-129">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

