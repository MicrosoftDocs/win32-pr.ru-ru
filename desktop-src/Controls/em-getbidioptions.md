---
title: Сообщение EM_GETBIDIOPTIONS (RichEdit. h)
description: Указывает текущее состояние двунаправленных параметров в элементе управления Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- Элементы управления Windows для EM_GETBIDIOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136143"
---
# <a name="em_getbidioptions-message"></a><span data-ttu-id="8eb11-104">\_Сообщение ЖЕТБИДИОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="8eb11-104">EM\_GETBIDIOPTIONS message</span></span>

<span data-ttu-id="8eb11-105">Указывает текущее состояние двунаправленных параметров в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8eb11-105">Indicates the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8eb11-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8eb11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb11-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8eb11-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8eb11-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8eb11-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8eb11-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8eb11-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8eb11-110">Структура [**бидиоптионс**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) , которая получает текущее состояние двунаправленных параметров в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8eb11-110">A [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that receives the current state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb11-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8eb11-111">Return value</span></span>

<span data-ttu-id="8eb11-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8eb11-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb11-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8eb11-113">Remarks</span></span>

<span data-ttu-id="8eb11-114">Это сообщение устанавливает для элементов **вмаск** и **веффектс** значения текущего состояния двунаправленных параметров в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8eb11-114">This message sets the values of the **wMask** and **wEffects** members to the value of the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb11-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8eb11-115">Requirements</span></span>



| <span data-ttu-id="8eb11-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8eb11-116">Requirement</span></span> | <span data-ttu-id="8eb11-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8eb11-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb11-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8eb11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb11-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8eb11-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8eb11-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8eb11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb11-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8eb11-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8eb11-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8eb11-122">Redistributable</span></span><br/>          | <span data-ttu-id="8eb11-123">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="8eb11-123">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="8eb11-124">Header</span><span class="sxs-lookup"><span data-stu-id="8eb11-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eb11-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eb11-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eb11-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8eb11-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8eb11-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8eb11-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8eb11-128">**бидиоптионс**</span><span class="sxs-lookup"><span data-stu-id="8eb11-128">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="8eb11-129">**EM \_ сетбидиоптионс**</span><span class="sxs-lookup"><span data-stu-id="8eb11-129">**EM\_SETBIDIOPTIONS**</span></span>](em-setbidioptions.md)
</dt> </dl>

 

 





