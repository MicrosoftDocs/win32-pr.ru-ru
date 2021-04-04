---
title: Сообщение EM_GETIMECOLOR (RichEdit. h)
description: Извлекает цвет композиции редактора метода ввода (IME).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- Элементы управления Windows для EM_GETIMECOLOR сообщений
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989013"
---
# <a name="em_getimecolor-message"></a><span data-ttu-id="50c72-104">\_Сообщение ЖЕТИМЕКОЛОР EM</span><span class="sxs-lookup"><span data-stu-id="50c72-104">EM\_GETIMECOLOR message</span></span>

<span data-ttu-id="50c72-105">Извлекает цвет композиции редактора метода ввода (IME).</span><span class="sxs-lookup"><span data-stu-id="50c72-105">Retrieves the Input Method Editor (IME) composition color.</span></span>

> [!Note]  
> <span data-ttu-id="50c72-106">Это сообщение поддерживается только в версиях Microsoft Rich Edit 1,0, поддерживающих азиатские языки.</span><span class="sxs-lookup"><span data-stu-id="50c72-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="50c72-107">Он не поддерживается в каких-либо более поздних версиях расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="50c72-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="50c72-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50c72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50c72-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50c72-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50c72-110">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="50c72-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="50c72-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50c72-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50c72-112">Массив из четырех элементов структур [**компколор**](/windows/desktop/api/Richedit/ns-richedit-compcolor) , который получает цвет композиции.</span><span class="sxs-lookup"><span data-stu-id="50c72-112">A four-element array of [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structures that receives the composition color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50c72-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50c72-113">Return value</span></span>

<span data-ttu-id="50c72-114">Если операция завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="50c72-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="50c72-115">Если операция завершается ошибкой, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="50c72-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c72-116">Требования</span><span class="sxs-lookup"><span data-stu-id="50c72-116">Requirements</span></span>



| <span data-ttu-id="50c72-117">Требование</span><span class="sxs-lookup"><span data-stu-id="50c72-117">Requirement</span></span> | <span data-ttu-id="50c72-118">Значение</span><span class="sxs-lookup"><span data-stu-id="50c72-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50c72-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50c72-119">Minimum supported client</span></span><br/> | <span data-ttu-id="50c72-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50c72-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50c72-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50c72-121">Minimum supported server</span></span><br/> | <span data-ttu-id="50c72-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50c72-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50c72-123">Header</span><span class="sxs-lookup"><span data-stu-id="50c72-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="50c72-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="50c72-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50c72-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50c72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c72-126">**компколор**</span><span class="sxs-lookup"><span data-stu-id="50c72-126">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





