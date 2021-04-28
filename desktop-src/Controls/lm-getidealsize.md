---
title: Сообщение LM_GETIDEALSIZE (Коммктрл. h)
description: LM_GETIDEALSIZE сообщение — получает предпочтительную высоту ссылки для текущей ширины элемента управления.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- Элементы управления Windows для LM_GETIDEALSIZE сообщений
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112392"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="edbd3-104">\_Сообщение ЖЕТИДЕАЛСИЗЕ LM</span><span class="sxs-lookup"><span data-stu-id="edbd3-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="edbd3-105">Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.</span><span class="sxs-lookup"><span data-stu-id="edbd3-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="edbd3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="edbd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edbd3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edbd3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="edbd3-108">Максимальная ширина ссылки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="edbd3-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="edbd3-109">*lParam* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="edbd3-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="edbd3-110">При возвращении этого сообщения содержит указатель на структуру <a href="/previous-versions//dd145106(v=vs.85)">**размера**</a> .</span><span class="sxs-lookup"><span data-stu-id="edbd3-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="edbd3-111">Элемент **CY** этой структуры указывает идеальную высоту элемента управления для заданной ширины.</span><span class="sxs-lookup"><span data-stu-id="edbd3-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="edbd3-112">Он корректирует элемент **CX** на фактически необходимый объем пространства.</span><span class="sxs-lookup"><span data-stu-id="edbd3-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edbd3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edbd3-113">Return value</span></span>

<span data-ttu-id="edbd3-114">Целое число, представляющее предпочтительную высоту текста ссылки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="edbd3-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbd3-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="edbd3-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="edbd3-116">Чтобы использовать этот API, необходимо предоставить манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="edbd3-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="edbd3-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="edbd3-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="edbd3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="edbd3-118">Requirements</span></span>



| <span data-ttu-id="edbd3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="edbd3-119">Requirement</span></span> | <span data-ttu-id="edbd3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="edbd3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edbd3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edbd3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="edbd3-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edbd3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edbd3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edbd3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="edbd3-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="edbd3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edbd3-125">Header</span><span class="sxs-lookup"><span data-stu-id="edbd3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="edbd3-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="edbd3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

