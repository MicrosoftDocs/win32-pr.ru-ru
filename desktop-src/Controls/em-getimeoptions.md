---
title: Сообщение EM_GETIMEOPTIONS (RichEdit. h)
description: Извлекает текущие параметры редактора метода ввода (IME).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Элементы управления Windows для EM_GETIMEOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136659"
---
# <a name="em_getimeoptions-message"></a><span data-ttu-id="23793-104">\_Сообщение ЖЕТИМЕОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="23793-104">EM\_GETIMEOPTIONS message</span></span>

<span data-ttu-id="23793-105">Извлекает текущие параметры редактора метода ввода (IME).</span><span class="sxs-lookup"><span data-stu-id="23793-105">Retrieves the current Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="23793-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="23793-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="23793-107">Он не поддерживается в каких-либо более поздних версиях расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="23793-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="23793-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23793-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23793-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23793-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23793-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="23793-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="23793-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23793-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23793-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="23793-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23793-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23793-113">Return value</span></span>

<span data-ttu-id="23793-114">Это сообщение возвращает один или несколько значений флагов параметров IME, описанных в сообщении [**EM \_ сетимеоптионс**](em-setimeoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="23793-114">This message returns one or more of the IME option flag values described in the [**EM\_SETIMEOPTIONS**](em-setimeoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="23793-115">Требования</span><span class="sxs-lookup"><span data-stu-id="23793-115">Requirements</span></span>



| <span data-ttu-id="23793-116">Требование</span><span class="sxs-lookup"><span data-stu-id="23793-116">Requirement</span></span> | <span data-ttu-id="23793-117">Значение</span><span class="sxs-lookup"><span data-stu-id="23793-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23793-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23793-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23793-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23793-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23793-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23793-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23793-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23793-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23793-122">Header</span><span class="sxs-lookup"><span data-stu-id="23793-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="23793-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="23793-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23793-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23793-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23793-125">**EM \_ сетимеоптионс**</span><span class="sxs-lookup"><span data-stu-id="23793-125">**EM\_SETIMEOPTIONS**</span></span>](em-setimeoptions.md)
</dt> </dl>

 

 





