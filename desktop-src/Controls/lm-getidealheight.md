---
title: Сообщение LM_GETIDEALHEIGHT (Коммктрл. h)
description: Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.
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
ms.openlocfilehash: 5a92f24d63cc8f58e260d79dafd0555429d65d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891454"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="6ce87-104">\_Сообщение ЖЕТИДЕАЛХЕИГХТ LM</span><span class="sxs-lookup"><span data-stu-id="6ce87-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="6ce87-105">Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6ce87-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ce87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ce87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ce87-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6ce87-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6ce87-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6ce87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ce87-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6ce87-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6ce87-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ce87-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ce87-111">Return value</span></span>

<span data-ttu-id="6ce87-112">Целое число, представляющее предпочтительную высоту текста ссылки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6ce87-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ce87-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ce87-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6ce87-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="6ce87-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6ce87-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6ce87-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ce87-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6ce87-116">Requirements</span></span>



| <span data-ttu-id="6ce87-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6ce87-117">Requirement</span></span> | <span data-ttu-id="6ce87-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6ce87-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce87-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ce87-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ce87-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ce87-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ce87-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ce87-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ce87-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ce87-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ce87-123">Header</span><span class="sxs-lookup"><span data-stu-id="6ce87-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ce87-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ce87-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





