---
title: Сообщение EM_GETWORDWRAPMODE (RichEdit. h)
description: Возвращает текущие параметры переноса по словам и разрыва слов для элемента управления Rich Edit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Элементы управления Windows для EM_GETWORDWRAPMODE сообщений
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489459"
---
# <a name="em_getwordwrapmode-message"></a><span data-ttu-id="51f55-104">\_Сообщение ЖЕТВОРДВРАПМОДЕ EM</span><span class="sxs-lookup"><span data-stu-id="51f55-104">EM\_GETWORDWRAPMODE message</span></span>

<span data-ttu-id="51f55-105">Возвращает текущие параметры переноса по словам и разрыва слов для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="51f55-105">Gets the current word wrap and word-break options for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="51f55-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="51f55-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="51f55-107">Он не поддерживается в каких-либо более поздних версиях расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="51f55-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="51f55-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="51f55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f55-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51f55-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51f55-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="51f55-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="51f55-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51f55-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51f55-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="51f55-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51f55-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51f55-113">Return value</span></span>

<span data-ttu-id="51f55-114">Сообщение возвращает текущие параметры переноса по словам и разрыва слов.</span><span class="sxs-lookup"><span data-stu-id="51f55-114">The message returns the current word wrap and word-break options.</span></span>

## <a name="remarks"></a><span data-ttu-id="51f55-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51f55-115">Remarks</span></span>

<span data-ttu-id="51f55-116">Это сообщение не должно отправляться с помощью определяемой приложением, процедурой разбиения по словам.</span><span class="sxs-lookup"><span data-stu-id="51f55-116">This message must not be sent by the application-defined, word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f55-117">Требования</span><span class="sxs-lookup"><span data-stu-id="51f55-117">Requirements</span></span>



| <span data-ttu-id="51f55-118">Требование</span><span class="sxs-lookup"><span data-stu-id="51f55-118">Requirement</span></span> | <span data-ttu-id="51f55-119">Значение</span><span class="sxs-lookup"><span data-stu-id="51f55-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51f55-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51f55-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51f55-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51f55-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51f55-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51f55-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51f55-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51f55-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51f55-124">Header</span><span class="sxs-lookup"><span data-stu-id="51f55-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="51f55-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f55-125"><dt>Richedit.h</dt></span></span> </dl> |



 

 





