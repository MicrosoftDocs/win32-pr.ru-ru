---
title: Сообщение EM_GETTEXTRANGE (RichEdit. h)
description: Извлекает указанный диапазон символов из элемента управления Rich Edit.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- Элементы управления Windows для EM_GETTEXTRANGE сообщений
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989088"
---
# <a name="em_gettextrange-message"></a><span data-ttu-id="92402-104">\_Сообщение ЖЕТТЕКСТРАНЖЕ EM</span><span class="sxs-lookup"><span data-stu-id="92402-104">EM\_GETTEXTRANGE message</span></span>

<span data-ttu-id="92402-105">Извлекает указанный диапазон символов из элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="92402-105">Retrieves a specified range of characters from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="92402-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92402-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92402-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92402-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92402-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="92402-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="92402-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92402-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92402-110">Указатель на структуру [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) , указывающую диапазон извлекаемых символов, и буфер для копирования символов.</span><span class="sxs-lookup"><span data-stu-id="92402-110">Pointer to a [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure that specifies the range of characters to retrieve and a buffer to copy the characters to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92402-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92402-111">Return value</span></span>

<span data-ttu-id="92402-112">Сообщение возвращает число скопированных символов, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="92402-112">The message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="92402-113">Требования</span><span class="sxs-lookup"><span data-stu-id="92402-113">Requirements</span></span>



| <span data-ttu-id="92402-114">Требование</span><span class="sxs-lookup"><span data-stu-id="92402-114">Requirement</span></span> | <span data-ttu-id="92402-115">Значение</span><span class="sxs-lookup"><span data-stu-id="92402-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92402-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92402-116">Minimum supported client</span></span><br/> | <span data-ttu-id="92402-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92402-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92402-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92402-118">Minimum supported server</span></span><br/> | <span data-ttu-id="92402-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92402-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92402-120">Header</span><span class="sxs-lookup"><span data-stu-id="92402-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="92402-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="92402-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92402-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92402-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92402-123">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="92402-123">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





