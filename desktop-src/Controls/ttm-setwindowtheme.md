---
title: Сообщение TTM_SETWINDOWTHEME (Коммктрл. h)
description: Задает визуальный стиль элемента управления ToolTip.
ms.assetid: eeddb91e-8eb8-4480-9ab2-5efa9e3ef48a
keywords:
- Элементы управления Windows для TTM_SETWINDOWTHEME сообщений
topic_type:
- apiref
api_name:
- TTM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c3f25b62bf0fe38a679234183cd5046f60784f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535249"
---
# <a name="ttm_setwindowtheme-message"></a><span data-ttu-id="bd7f5-104">\_Сообщение ТТМ SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="bd7f5-104">TTM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="bd7f5-105">Задает визуальный стиль элемента управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="bd7f5-105">Sets the visual style of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd7f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd7f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd7f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd7f5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd7f5-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bd7f5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd7f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd7f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd7f5-110">Указатель на строку в Юникоде, содержащую стиль визуального элемента ToolTip, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="bd7f5-110">Pointer to a Unicode string that contains the tooltip visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd7f5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd7f5-111">Return value</span></span>

<span data-ttu-id="bd7f5-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="bd7f5-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd7f5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd7f5-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bd7f5-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="bd7f5-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="bd7f5-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bd7f5-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd7f5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="bd7f5-116">Requirements</span></span>



| <span data-ttu-id="bd7f5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="bd7f5-117">Requirement</span></span> | <span data-ttu-id="bd7f5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bd7f5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd7f5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd7f5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bd7f5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd7f5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd7f5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd7f5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bd7f5-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd7f5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd7f5-123">Header</span><span class="sxs-lookup"><span data-stu-id="bd7f5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd7f5-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd7f5-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





