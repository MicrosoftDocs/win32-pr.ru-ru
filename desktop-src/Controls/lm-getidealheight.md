---
title: Сообщение LM_GETIDEALHEIGHT (Коммктрл. h)
description: LM_GETIDEALHEIGHT сообщение — получает предпочтительную высоту ссылки для текущей ширины элемента управления.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- Элементы управления Windows для LM_GETIDEALHEIGHT сообщений
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112402"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="87877-104">\_Сообщение ЖЕТИДЕАЛХЕИГХТ LM</span><span class="sxs-lookup"><span data-stu-id="87877-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="87877-105">Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.</span><span class="sxs-lookup"><span data-stu-id="87877-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="87877-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87877-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87877-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="87877-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="87877-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="87877-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87877-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87877-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="87877-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87877-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87877-111">Return value</span></span>

<span data-ttu-id="87877-112">Целое число, представляющее предпочтительную высоту текста ссылки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="87877-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="87877-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="87877-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87877-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="87877-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="87877-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="87877-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87877-116">Требования</span><span class="sxs-lookup"><span data-stu-id="87877-116">Requirements</span></span>



| <span data-ttu-id="87877-117">Требование</span><span class="sxs-lookup"><span data-stu-id="87877-117">Requirement</span></span> | <span data-ttu-id="87877-118">Значение</span><span class="sxs-lookup"><span data-stu-id="87877-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87877-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87877-119">Minimum supported client</span></span><br/> | <span data-ttu-id="87877-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87877-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87877-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87877-121">Minimum supported server</span></span><br/> | <span data-ttu-id="87877-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87877-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87877-123">Header</span><span class="sxs-lookup"><span data-stu-id="87877-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="87877-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="87877-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





