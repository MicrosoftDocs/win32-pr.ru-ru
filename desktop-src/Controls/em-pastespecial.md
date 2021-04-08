---
title: Сообщение EM_PASTESPECIAL (RichEdit. h)
description: Замещает конкретный формат буфера обмена в элементе управления Rich Edit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- Элементы управления Windows для EM_PASTESPECIAL сообщений
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892169"
---
# <a name="em_pastespecial-message"></a><span data-ttu-id="96462-104">\_Сообщение PASTESPECIAL EM</span><span class="sxs-lookup"><span data-stu-id="96462-104">EM\_PASTESPECIAL message</span></span>

<span data-ttu-id="96462-105">Замещает конкретный формат буфера обмена в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="96462-105">Pastes a specific clipboard format in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="96462-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96462-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96462-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96462-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96462-108">Указывает [форматы буфера обмена](/windows/desktop/dataxchg/clipboard-formats).</span><span class="sxs-lookup"><span data-stu-id="96462-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats).</span></span>

</dd> <dt>

<span data-ttu-id="96462-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96462-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96462-110">Указатель на структуру [**репастеспеЦиал**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="96462-110">Pointer to a [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) structure or **NULL**.</span></span> <span data-ttu-id="96462-111">Если объект вставляется, структура **репастеспеЦиал** заполняется требуемым аспектом дисплея.</span><span class="sxs-lookup"><span data-stu-id="96462-111">If an object is being pasted, the **REPASTESPECIAL** structure is filled in with the desired display aspect.</span></span> <span data-ttu-id="96462-112">Если параметр *lParam* имеет **значение NULL** или элемент **дваспект** равен нулю, то используемый аспект изображения будет содержимым дескриптора объекта.</span><span class="sxs-lookup"><span data-stu-id="96462-112">If *lParam* is **NULL** or the **dwAspect** member is zero, the display aspect used will be the contents of the object descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96462-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96462-113">Return value</span></span>

<span data-ttu-id="96462-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="96462-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="96462-115">Требования</span><span class="sxs-lookup"><span data-stu-id="96462-115">Requirements</span></span>



| <span data-ttu-id="96462-116">Требование</span><span class="sxs-lookup"><span data-stu-id="96462-116">Requirement</span></span> | <span data-ttu-id="96462-117">Значение</span><span class="sxs-lookup"><span data-stu-id="96462-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96462-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96462-118">Minimum supported client</span></span><br/> | <span data-ttu-id="96462-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96462-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96462-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96462-120">Minimum supported server</span></span><br/> | <span data-ttu-id="96462-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96462-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96462-122">Header</span><span class="sxs-lookup"><span data-stu-id="96462-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="96462-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="96462-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96462-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96462-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96462-125">**репастеспеЦиал**</span><span class="sxs-lookup"><span data-stu-id="96462-125">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

