---
title: Сообщение EM_SETBKGNDCOLOR (RichEdit. h)
description: В \_ сообщении EM сетбкгндколор задается цвет фона для элемента управления Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Элементы управления Windows для EM_SETBKGNDCOLOR сообщений
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892485"
---
# <a name="em_setbkgndcolor-message"></a><span data-ttu-id="edb4c-104">\_Сообщение СЕТБКГНДКОЛОР EM</span><span class="sxs-lookup"><span data-stu-id="edb4c-104">EM\_SETBKGNDCOLOR message</span></span>

<span data-ttu-id="edb4c-105">В сообщении **EM \_ сетбкгндколор** задается цвет фона для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="edb4c-105">The **EM\_SETBKGNDCOLOR** message sets the background color for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="edb4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="edb4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb4c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edb4c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edb4c-108">Указывает, следует ли использовать системный цвет.</span><span class="sxs-lookup"><span data-stu-id="edb4c-108">Specifies whether to use the system color.</span></span> <span data-ttu-id="edb4c-109">Если этот параметр имеет ненулевое значение, для фона задается цвет системы фона окна.</span><span class="sxs-lookup"><span data-stu-id="edb4c-109">If this parameter is a nonzero value, the background is set to the window background system color.</span></span> <span data-ttu-id="edb4c-110">В противном случае для фона задается указанный цвет.</span><span class="sxs-lookup"><span data-stu-id="edb4c-110">Otherwise, the background is set to the specified color.</span></span>

</dd> <dt>

<span data-ttu-id="edb4c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edb4c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edb4c-112">Структура [**COLORREF**](/windows/desktop/gdi/colorref) , указывающая цвет, если параметр *wParam* равен нулю.</span><span class="sxs-lookup"><span data-stu-id="edb4c-112">A [**COLORREF**](/windows/desktop/gdi/colorref) structure specifying the color if *wParam* is zero.</span></span> <span data-ttu-id="edb4c-113">Чтобы создать **COLORREF**, используйте макрос [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="edb4c-113">To generate a **COLORREF**, use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb4c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edb4c-114">Return value</span></span>

<span data-ttu-id="edb4c-115">Это сообщение возвращает исходный цвет фона.</span><span class="sxs-lookup"><span data-stu-id="edb4c-115">This message returns the original background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb4c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="edb4c-116">Requirements</span></span>



| <span data-ttu-id="edb4c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="edb4c-117">Requirement</span></span> | <span data-ttu-id="edb4c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="edb4c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edb4c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edb4c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="edb4c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edb4c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edb4c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edb4c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="edb4c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="edb4c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edb4c-123">Header</span><span class="sxs-lookup"><span data-stu-id="edb4c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="edb4c-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb4c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb4c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edb4c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="edb4c-126">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="edb4c-126">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="edb4c-127">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="edb4c-127">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> <dt>

[<span data-ttu-id="edb4c-128">**RGB**</span><span class="sxs-lookup"><span data-stu-id="edb4c-128">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

