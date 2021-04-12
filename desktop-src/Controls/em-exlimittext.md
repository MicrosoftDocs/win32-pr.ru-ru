---
title: Сообщение EM_EXLIMITTEXT (RichEdit. h)
description: Задает верхний предел для объема текста, который пользователь может ввести или вставить в элемент управления Rich Edit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- Элементы управления Windows для EM_EXLIMITTEXT сообщений
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491490"
---
# <a name="em_exlimittext-message"></a><span data-ttu-id="bbf7d-104">\_Сообщение ЕКСЛИМИТТЕКСТ EM</span><span class="sxs-lookup"><span data-stu-id="bbf7d-104">EM\_EXLIMITTEXT message</span></span>

<span data-ttu-id="bbf7d-105">Задает верхний предел для объема текста, который пользователь может ввести или вставить в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-105">Sets an upper limit to the amount of text the user can type or paste into a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbf7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbf7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf7d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbf7d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf7d-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bbf7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbf7d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf7d-110">Указывает максимальный объем текста, который можно указать.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-110">Specifies the maximum amount of text that can be entered.</span></span> <span data-ttu-id="bbf7d-111">Если этот параметр равен нулю, используется максимальное значение по умолчанию (64 000 символов).</span><span class="sxs-lookup"><span data-stu-id="bbf7d-111">If this parameter is zero, the default maximum is used, which is 64K characters.</span></span> <span data-ttu-id="bbf7d-112">COM-объект считается одиночным символом.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-112">A COM object counts as a single character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf7d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbf7d-113">Return value</span></span>

<span data-ttu-id="bbf7d-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf7d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbf7d-115">Remarks</span></span>

<span data-ttu-id="bbf7d-116">Ограничение текста, заданное в сообщении **EM \_ екслимиттекст** , не ограничивает объем текста, который можно передать в элемент управления Rich Edit с помощью сообщения [**EM \_ Streaming**](em-streamin.md) с параметром *lParam* , имеющим значение SF \_ .</span><span class="sxs-lookup"><span data-stu-id="bbf7d-116">The text limit set by the **EM\_EXLIMITTEXT** message does not limit the amount of text that you can stream into a rich edit control using the [**EM\_STREAMIN**](em-streamin.md) message with *lParam* set to SF\_TEXT.</span></span> <span data-ttu-id="bbf7d-117">Однако он ограничивает объем текста, который можно передать в элемент управления Rich Edit с помощью сообщения **EM \_ Streaming** с параметром *lParam* , имеющим значение SF \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-117">However, it does limit the amount of text that you can stream into a rich edit control using the **EM\_STREAMIN** message with *lParam* set to SF\_RTF.</span></span>

<span data-ttu-id="bbf7d-118">Перед вызовом **EM \_ екслимиттекст** ограничение по умолчанию для объема текста, который может ввести пользователь, — 32 767 символов.</span><span class="sxs-lookup"><span data-stu-id="bbf7d-118">Before **EM\_EXLIMITTEXT** is called, the default limit to the amount of text a user can enter is 32,767 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf7d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bbf7d-119">Requirements</span></span>



| <span data-ttu-id="bbf7d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bbf7d-120">Requirement</span></span> | <span data-ttu-id="bbf7d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bbf7d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf7d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbf7d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf7d-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbf7d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbf7d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbf7d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf7d-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bbf7d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbf7d-126">Header</span><span class="sxs-lookup"><span data-stu-id="bbf7d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf7d-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf7d-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf7d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbf7d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf7d-129">**\_поток EM**</span><span class="sxs-lookup"><span data-stu-id="bbf7d-129">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





