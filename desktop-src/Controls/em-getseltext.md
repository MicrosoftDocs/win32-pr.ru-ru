---
title: Сообщение EM_GETSELTEXT (RichEdit. h)
description: Извлекает текущий выделенный текст в элементе управления Rich Edit.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Элементы управления Windows для EM_GETSELTEXT сообщений
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891838"
---
# <a name="em_getseltext-message"></a><span data-ttu-id="89ea0-104">\_Сообщение ЖЕТСЕЛТЕКСТ EM</span><span class="sxs-lookup"><span data-stu-id="89ea0-104">EM\_GETSELTEXT message</span></span>

<span data-ttu-id="89ea0-105">Извлекает текущий выделенный текст в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="89ea0-105">Retrieves the currently selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="89ea0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89ea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89ea0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89ea0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89ea0-108">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="89ea0-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="89ea0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89ea0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89ea0-110">Указатель на буфер, который получает выделенный текст.</span><span class="sxs-lookup"><span data-stu-id="89ea0-110">Pointer to a buffer that receives the selected text.</span></span> <span data-ttu-id="89ea0-111">Вызывающее приложение должно гарантировать, что буфер достаточно велик, чтобы вместить выделенный текст.</span><span class="sxs-lookup"><span data-stu-id="89ea0-111">The calling application must ensure that the buffer is large enough to hold the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89ea0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89ea0-112">Return value</span></span>

<span data-ttu-id="89ea0-113">Это сообщение возвращает число скопированных символов, не включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="89ea0-113">This message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ea0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="89ea0-114">Requirements</span></span>



| <span data-ttu-id="89ea0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="89ea0-115">Requirement</span></span> | <span data-ttu-id="89ea0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="89ea0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89ea0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89ea0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="89ea0-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89ea0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89ea0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89ea0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="89ea0-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89ea0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89ea0-121">Header</span><span class="sxs-lookup"><span data-stu-id="89ea0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="89ea0-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="89ea0-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





